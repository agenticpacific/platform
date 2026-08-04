# Modifications for AP (agenticpacific.com.fj/platform) Deployment

### Github Workflows Deployment

Disable all *.yml files under .github/workflows/ apart from pages.yml.

Change from site/demo to /site eg: `cp -R apps/geolibre-desktop/dist/. site/`

### Title Change

index.html @ apps/geolibre-desktop: `<title>Agentic Geospatial Platform - Agentic Pacific</title>`

### Remove Help Menu

TopToolbar.tsx @ apps/geolibre-desktop/src/components/layout

`
125:    // import { HelpMenu } from "./toolbar/HelpMenu";
`

`
1637:   {/* {isMenuVisible(uiProfile, "help") && (
        <HelpMenu
          chrome={chrome}
          diagnosticsErrorCount={diagnosticsErrorCount}
          onOpenCommandPalette={() => setCommandPaletteOpen(true)}
          onOpenShortcuts={() => setShortcutsOpen(true)}
          onOpenDiagnostics={onOpenDiagnostics}
          onCheckForUpdates={() => {
            setAboutOpen(true);
            setCheckForUpdatesRequest((value) => value + 1);
          }}
          onAbout={() => setAboutOpen(true)}
        />
    )} */}
`

### Center Fiji

project.ts @ packages/core/src

`
function createDefaultMapView():
center: [-100, 40],
zoom: 2,
`
