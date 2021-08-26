---
description: Die folgenden Funktionen werden mit Farbe verwendet.
ms.assetid: 9dd32d4a-30bd-406f-a934-bb71ad4ca2cb
title: Farbfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef9e233e5376718ac983982fd3f06e9fcd6c6fc5843d4a32d685fe64bbc1af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966310"
---
# <a name="color-functions"></a>Farbfunktionen

Die folgenden Funktionen werden mit Farbe verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette)                   | Ersetzt Einträge in der angegebenen logischen Palette.                                                                                                    |
| [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette)     | Erstellt eine Halbtonpalette für den angegebenen Gerätekontext (DC).                                                                                     |
| [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                     | Erstellt eine logische Palette.                                                                                                                            |
| [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment)           | Ruft die Farbanpassungswerte für den angegebenen DC ab.                                                                                           |
| [**GetGrammrestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor)                 | Ruft einen Farbwert ab, der eine Farbe aus der Systempalette identifiziert, die angezeigt wird, wenn der angegebene Farbwert verwendet wird.                    |
| [**GetGrammrestPaletteIndex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex)   | Ruft den Index für den Eintrag in der angegebenen logischen Palette ab, der am besten zu einem angegebenen Farbwertpasst.                                     |
| [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries)             | Ruft einen angegebenen Bereich von Paletteneinträgen aus der angegebenen logischen Palette ab.                                                                        |
| [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) | Ruft einen Bereich von Paletteneinträgen aus der Systempalette ab, die dem angegebenen DC zugeordnet ist.                                                |
| [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse)         | Ruft den aktuellen Zustand der (physischen) Systempalette für den angegebenen DC ab.                                                                    |
| [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette)                   | Karten Paletteneinträge aus der aktuellen logischen Palette in die Systempalette.                                                                          |
| [**ResizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette)                     | Vergrößert oder verkleinert einer logischen Palette auf der Grundlage des angegebenen Werts.                                                                    |
| [**Wählen SiePalette aus.**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette)                     | Wählt die angegebene logische Palette in einem Gerätekontext aus.                                                                                          |
| [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment)           | Legt die Farbanpassungswerte für einen Domänencontroller mithilfe der angegebenen Werte fest.                                                                                 |
| [**SetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries)             | Legt RGB-Farbwerte (Rot, Grün, Blau) und Flags in einem Bereich von Einträgen in einer logischen Palette fest.                                                        |
| [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse)         | Ermöglicht einer Anwendung anzugeben, ob die Systempalette 2 oder 20 statische Farben enthält.                                                           |
| [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)                 | Setzt den Ursprung eines Pinsels zurück oder setzt eine logische Palette zurück.                                                                                             |
| [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors)                       | Aktualisiert den Clientbereich des angegebenen Gerätekontexts, indem die aktuellen Farben im Clientbereich der aktuell realisierten logischen Palette neu zuweise. |



 

 

 



