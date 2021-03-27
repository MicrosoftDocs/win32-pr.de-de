---
description: Die folgenden Funktionen werden mit Koordinaten Räumen und Transformationen verwendet.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Koordinatenraum und Transformations Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e561f5cc9784439f5bef4f696e98d5919cb052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215209"
---
# <a name="coordinate-space-and-transformation-functions"></a>Koordinatenraum und Transformations Funktionen

Die folgenden Funktionen werden mit Koordinaten Räumen und Transformationen verwendet.



| Funktion                                                                       | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Client Anwendungsbildschirm**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Konvertiert die Client Bereichs Koordinaten eines angegebenen Punkts in Bildschirm Koordinaten.                                                 |
| [**Combinetransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Verkettet zwei Flächen-und Seiten Raum Transformationen.                                                                      |
| [**Dptolp**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Konvertiert Geräte Koordinaten in logische Koordinaten.                                                                            |
| [**Getcurrentpositionex**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Ruft die aktuelle Position in logischen Koordinaten ab.                                                                           |
| [**Getdisplayautorotationpreferences**](/previous-versions//dn376360(v=vs.85)) | Ruft die Ausrichtungs Einstellungen der Anzeige ab.                                                                                 |
| [**Getgraphicsmode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Ruft den aktuellen Grafikmodus für den angegebenen Gerätekontext ab.                                                            |
| [**Getmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Ruft den aktuellen Mapping-Modus ab.                                                                                              |
| [**Getviewportextex**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Ruft den x-und y-Wert des aktuellen Viewports für den angegebenen Gerätekontext ab.                                    |
| [**Getviewportor Gex**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Ruft die x-Koordinaten und y-Koordinaten des viewportursprungs für den angegebenen Gerätekontext ab.                           |
| [**Getwindowextex**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Ruft den x-und y-Block des Fensters für den angegebenen Gerätekontext ab.                                              |
| [**Getwindoworgex**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Ruft die x-Koordinaten und y-Koordinaten des Fenster Ursprungs für den angegebenen Gerätekontext ab.                             |
| [**Getworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Ruft die aktuelle Transformation für Welt Raum zu Seiten Raum ab.                                                                  |
| [**Lptodp**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Konvertiert logische Koordinaten in Geräte Koordinaten.                                                                            |
| [**Mapwindowpoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Konvertiert (ordnet) einen Satz von Punkten aus einem Koordinatenraum relativ zu einem Fenster in einen Koordinatenraum relativ zu einem anderen Fenster. |
| [**Modifyworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Ändert die globale Transformation für einen Gerätekontext unter Verwendung des angegebenen Modus.                                                  |
| [**Offsetviewportor Gex**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Ändert den Viewportursprung für einen Gerätekontext unter Verwendung der angegebenen horizontalen und vertikalen Offsets.                           |
| [**Offsetwindoworgex**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Ändert den Fenster Ursprung für einen Gerätekontext unter Verwendung der angegebenen horizontalen und vertikalen Offsets.                             |
| [**Scaleviewportextex**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Ändert den Viewport für einen Gerätekontext unter Verwendung der von den angegebenen multiplizierungen und Divisoren formatierten Verhältnisse.                  |
| [**Scalewindowextex**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Ändert das Fenster für einen Gerätekontext unter Verwendung der von den angegebenen multiplizierungen und Divisoren formatierten Verhältnisse.                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Konvertiert die Bildschirm Koordinaten eines angegebenen Punkts auf dem Bildschirm in Client Koordinaten.                                        |
| [**Setdisplayautorotationpreferences**](/previous-versions//dn376361(v=vs.85)) | Legt die Orientierungs Einstellungen der Anzeige fest.                                                                                 |
| [**Setgraphicsmode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Legt den Grafikmodus für den angegebenen Gerätekontext fest.                                                                         |
| [**Setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Legt den Kartenmodus für den angegebenen Gerätekontext fest.                                                                           |
| [**Setviewportextex**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Legt die horizontalen und vertikalen Blöcke des Viewports für einen Gerätekontext mithilfe der angegebenen Werte fest.                     |
| [**Setviewportor Gex**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Gibt an, welcher Geräte Punkt dem Fenster Ursprung (0, 0) zugeordnet wird.                                                                    |
| [**Setwindowextex**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Legt die horizontalen und vertikalen Blöcke des Fensters für einen Gerätekontext mithilfe der angegebenen Werte fest.                       |
| [**Setwindoworgex**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Gibt an, welcher Fenster Punkt dem Viewportursprung (0, 0) zugeordnet wird.                                                                  |
| [**Setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Legt eine zweidimensionale lineare Transformation zwischen dem Welt Raum und dem Seiten Raum für den angegebenen Gerätekontext fest.                |



 

 

 
