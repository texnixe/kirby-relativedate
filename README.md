# Kirby 2 - Relative Date Plugin
Plugin for Kirby 2 CMS that coverts date and time to a human-readable relative format:

Converts your absolute date (and time) in something relative and more readable, like e.g. 2 months 3 days ago.

# Installation & Usage
1. Add the ```relative-date.php``` and ```relative-date-lang.php``` to your ```site/plugins/`` folder. You can also move them to a subfolder (e.g. called ```relative-date```) within the ```plugins```directory.
2. Then use it on any date field, e.g.: ```$page->published()->relative()```

# Options
You can define how many date/time elements the phrase should entail. The default is 2 elements ('1 year 4 months' or '2 weeks 3 days' or '2 hours 34 minutes'). You can set your own phrase length in tow ways:

**globally in your ```sites/config/config.php```:**
```php
c::set('relativedate.length', 4);
```

**On a per case basis:**
```php
$page->published()->relative(4);
```

# Languages supported
So far this plugin supports:

- English
- German
- Spanish
- French

If you can help with other languages, please open up an issue. The following information is necessary:

- Words (singular & plural) for second, minute, hour, day, week, month and year
- Terms that express A) that date & time are still ahead of the current time (e.g. "left" as in "5 minutes left") and B) that date & time are passed the current time (e.g. "ago" as in "3 days ago")
- The information if these terms have to be added before or after the actual relative date phrase
