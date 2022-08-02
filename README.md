### Interactive-Grid-Reports-Using-JavaScript | Oracle APEX
#### I am GitHub Readme Generator's creator
![I am GitHub Readme Generator's creator](https://i9.ytimg.com/vi_webp/HTaFS1IxgxE/mqdefault.webp?v=628f9c82&sqp=CMTVoZYG&rs=AOn4CLAC7omjc1ehZm8mTyQWv5yEmAZDQA)

Live tutorial on YouTube [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/youtube.svg' alt='youtube' height='40'>](https://www.youtube.com/watch?v=HTaFS1IxgxE&t)  

CSS

--------------

.ig-windows-style .a-GV-table .a-GV-cell,

.ig-windows-style .a-GV-table .a-GV-controlBreakHeader {

    border-color: transparent;

}

.ig-windows-style .a-GV-w-frozen .a-GV-table {

    border-right: none;

}

.ig-windows-style .a-GV-table tr.is-hover .a-GV-cell,

.ig-windows-style .a-GV-table tr.is-hover.is-selected .a-GV-cell {

    background-color: #f2f6ff;

}

.ig-windows-style .a-GV-table tr.is-selected .a-GV-cell,

.ig-windows-style .a-GV-table tr.is-hover.is-selected .a-GV-cell {

    background-color: #dbe8ff;

}

.ig-windows-style .a-GV-hdr {

    background-color: #fcfcfc;

}

.a-IG-contentContainer {

    margin-top: 0;

}



.ig-windows-style .u-selector {

    box-shadow: none;

    border: 1px transparent;

}



.ig-windows-style .a-GV-hdr tr .u-selector,

.ig-windows-style tr.is-selected .u-selector,

.ig-windows-style tr.is-hover .u-selector {

    box-shadow: 0 1px 1px rgba(0,0,0,.05) inset;

    border: 1px solid #404040;

}



JavaScript Initialization Code

--------------

function(config) {

    config.defaultGridViewOptions = {

        // this was mentioned in my blog: http://hardlikesoftware.com/weblog/2017/01/24/how-to-hack-apex-interactive-grid-part-2/#more-537

        // relies on internal detail of menu id generation but no other way to get this

        contextMenuId: "emp_ig_selection_actions_menu",

    };

    // Logically want to do this: config.views.grid.features.stretchColumns = false;

    // But the server may not generate the views, grid, or features objects depending on what declrative options are selected.

    // So must check for and add if needed each one. Seems like there should be an easier way :-(

    var o = config;

    "views.grid.features".split(".").forEach(function(p) { 

        if ( !o[p] ) {

            o[p] = {};

        }

        o = o[p];

    });

    o.stretchColumns = false;

/* or you could do it this way

    if (!config.views) {

        config.views = {};

    }

    if (!config.views.grid) {

        config.views.grid = {};

    }

    if (!config.views.grid.features) {

        config.views.grid.features = {};

    }

    config.views.grid.features.stretchColumns = false;

*/

    return config;

}


Static ID
--------------
emp


<b>Related article:</b> Edit Grid [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/youtube.svg' alt='youtube' height='20'>](https://www.youtube.com/watch?v=kd667U7Mvvc&t) Grid with JavaScript [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/youtube.svg' alt='youtube' height='20'>](https://www.youtube.com/watch?v=hoYLDXgO-mY)

Subscribe on My Channel [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/youtubestudio.svg' alt='youtubestudio' height='40'>](https://www.youtube.com/oracleapexbd) 
 

