---
description: Die folgenden Funktionen werden mit Koordinatenräumen und Transformationen verwendet.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Koordinatenraum und Transformationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe24e78002393d7a840e99d33840dfa4ba0d9e2ac89d941f998261955683e13f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718080"
---
# <a name="coordinate-space-and-transformation-functions"></a>Koordinatenraum und Transformationsfunktionen

Die folgenden Funktionen werden mit Koordinatenräumen und Transformationen verwendet.



| Funktion                                                                       | Beschreibung                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ClientToScreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Konvertiert die Clientbereichkoordinaten eines angegebenen Punkts in Bildschirmkoordinaten.                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Verkettet zwei Transformationen zwischen Welt- und Seitenbereich.                                                                      |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Konvertiert Gerätekoordinaten in logische Koordinaten.                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Ruft die aktuelle Position in logischen Koordinaten ab.                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | Ruft die Ausrichtungseinstellungen der Anzeige ab.                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Ruft den aktuellen Grafikmodus für den angegebenen Gerätekontext ab.                                                            |
| [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Ruft den aktuellen Zuordnungsmodus ab.                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Ruft den x-Extent und den y-Extent des aktuellen Viewports für den angegebenen Gerätekontext ab.                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Ruft die x-Koordinaten und y-Koordinaten des Viewport-Ursprungs für den angegebenen Gerätekontext ab.                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Ruft den x-Extent und den y-Extent des Fensters für den angegebenen Gerätekontext ab.                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Ruft die x-Koordinaten und y-Koordinaten des Fenster-Ursprungs für den angegebenen Gerätekontext ab.                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Ruft die aktuelle Transformation von Raum zu Seitenbereich ab.                                                                  |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Konvertiert logische Koordinaten in Gerätekoordinaten.                                                                            |
| [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Konvertiert (ordnet) einen Satz von Punkten aus einem Koordinatenraum relativ zu einem Fenster in einen Koordinatenraum relativ zu einem anderen Fenster zu. |
| [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Ändert die Welttransformation für einen Gerätekontext im angegebenen Modus.                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Ändert den Viewport-Ursprung für einen Gerätekontext unter Verwendung der angegebenen horizontalen und vertikalen Offsets.                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Ändert den Fensterstart für einen Gerätekontext unter Verwendung der angegebenen horizontalen und vertikalen Offsets.                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Ändert den Viewport für einen Gerätekontext unter Verwendung der Verhältnisse, die von den angegebenen Multipliknden und Divisoren gebildet werden.                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Ändert das Fenster für einen Gerätekontext unter Verwendung der Verhältnisse, die von den angegebenen Multipliknden und Divisoren gebildet werden.                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Konvertiert die Bildschirmkoordinaten eines angegebenen Punkts auf dem Bildschirm in Clientkoordinaten.                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | Legt die Ausrichtungseinstellungen der Anzeige fest.                                                                                 |
| [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Legt den Grafikmodus für den angegebenen Gerätekontext fest.                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Legt den Zuordnungsmodus des angegebenen Gerätekontexts fest.                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Legt die horizontalen und vertikalen Werte des Viewports für einen Gerätekontext mithilfe der angegebenen Werte fest.                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Gibt an, welcher Gerätepunkt dem Ursprung des Fensters (0,0) zugibt.                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Legt die horizontalen und vertikalen Werte des Fensters für einen Gerätekontext mithilfe der angegebenen Werte fest.                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Gibt an, welcher Fensterpunkt dem Viewport-Ursprung (0,0) zugibt.                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Legt eine zweidimensionale lineare Transformation zwischen Welt- und Seitenraum für den angegebenen Gerätekontext fest.                |



 

 

 
