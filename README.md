# The Sun Rising

## Startup file in SC3
```
s.options.sampleRate = 48000;
s.options.memSize = 2**18;
FreqScope.new;
s.meter;

// TSR init
{ BALC.init }.defer(5);
User doAfterActivate: {
	{ BALC.globalizeBufs; }.defer(8);
	TsrStartup(\geodia);
};
User.enable("the_sun_rising2", 5, \iani, \geodia, \vasilis, \kosmas, \penny);
```
