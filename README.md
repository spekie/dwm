# patches applied
- attachaside
- hide vacant tags
- fix borders (in picom)
# patching
```sh
patch -F3 -i *.diff
```
# config.h changes
```diff
37c37
< static const int resizehints = 1;    /* 1 means respect size hints in tiled resizals */
---
> static const int resizehints = 0;    /* 1 means respect size hints in tiled resizals */
48c48
< #define MODKEY Mod1Mask
---
> #define MODKEY Mod4Mask
65,66c65,66
<       { MODKEY,                       XK_p,      spawn,          {.v = dmenucmd } },
<       { MODKEY|ShiftMask,             XK_Return, spawn,          {.v = termcmd } },
---
>       { MODKEY,                       XK_d,      spawn,          {.v = dmenucmd } },
>       { MODKEY,                       XK_Return, spawn,          {.v = termcmd } },
71c71
<       { MODKEY,                       XK_d,      incnmaster,     {.i = -1 } },
---
>       { MODKEY,                       XK_o,      incnmaster,     {.i = -1 } },
74c74
<       { MODKEY,                       XK_Return, zoom,           {0} },
---
>       { MODKEY|ShiftMask,             XK_Return, zoom,           {0} },
76c76
<       { MODKEY|ShiftMask,             XK_c,      killclient,     {0} },
---
>       { MODKEY,                       XK_q,      killclient,     {0} },
```
