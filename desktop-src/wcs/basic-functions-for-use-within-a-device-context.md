---
title: Grundlegende Funktionen zur Verwendung innerhalb eines Gerätekontexts
description: Die folgenden WCS-Funktionen bieten grundlegende Farbzuordnungsfunktionen innerhalb von Gerätekontexten. Sie sind nützlich für alle Anwendungen, die die Farbverwaltung mit geringem Mehraufwand und minimalem Benutzereingriff implementieren müssen.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Farbsystem (WCS), Funktionen
- WCS (Windows Color System), Functions
- Bildfarbverwaltung,Funktionen
- Farbverwaltung,Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCS, Functions
- Windows Farbsystem (WCS), Gerätekontexte
- WCS (Windows Color System), Gerätekontexte
- Bildfarbverwaltung, Gerätekontexte
- Farbverwaltung,Gerätekontexte
- Farben,Gerätekontexte
- WCS-Referenz, Gerätekontexte
- Referenz für WCS, Gerätekontexte
- Gerätekontexte
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a934c1737a7eea8b32a9589325e73300db82334a40ee47b411922b89cb61f568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118210979"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Grundlegende Funktionen zur Verwendung innerhalb eines Gerätekontexts

Die folgenden WCS-Funktionen bieten grundlegende [Farbzuordnungsfunktionen](c.md) innerhalb von Gerätekontexten. Sie sind nützlich für alle Anwendungen, die die Farbverwaltung mit geringem Mehraufwand und minimalem Benutzereingriff implementieren müssen.



| Funktion                                                           | Beschreibung                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Überprüft, ob die angegebenen Farben in der Gamut eines Geräts angegeben sind.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Korrigiert die Einträge in einer Palette für einen Gerätekontext.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Führt eine Farbzuordnung für Vorschauzwecke aus.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Erstellt einen Farbraum.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Löscht einen Farbraum.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Aufzählen von Ausgabefarbprofilen, die für einen bestimmten Gerätekontext verfügbar sind.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Anwendungsdefinierte Rückruffunktion für [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). Der Name dieser Funktion wird auch von der Anwendung definiert. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ruft den aktuellen Eingabefarbraum in einem Gerätekontext ab. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Ruft das aktuelle Ausgabefarbprofil eines Gerätekontexts ab.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Ruft die [**LOGCOLORSPACE-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) eines Gerätekontexts ab.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Legt den Eingabefarbraum eines Gerätekontexts fest.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Aktiviert oder deaktiviert die Farbverwaltung in einem Gerätekontext.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Legt das Ausgabefarbprofil für einen bestimmten Gerätekontext fest.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Enumeriert alle Farbprofile, die die Enumerationskriterien im angegebenen Profilverwaltungsbereich erfüllen.                                      |



 

 

 




