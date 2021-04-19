---
title: Grundlegende Funktionen zur Verwendung innerhalb eines Gerätekontexts
description: Die folgenden WCS-Funktionen bieten grundlegende Funktionen zur Farbzuordnung innerhalb von Geräte Kontexten. Sie sind für alle Anwendungen nützlich, die die Farbverwaltung mit geringem mehr Aufwand und minimalem Benutzereingriff implementieren müssen.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), Geräte Kontexte
- WCS (Windows Color System), Geräte Kontexte
- Bild Farbverwaltung, Geräte Kontexte
- Farbverwaltung, Geräte Kontexte
- Farben, Geräte Kontexte
- WCS-Referenz, Geräte Kontexte
- Referenz für WCs, Geräte Kontexte
- Gerätekontexte
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106357135"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Grundlegende Funktionen zur Verwendung innerhalb eines Gerätekontexts

Die folgenden WCS-Funktionen bieten grundlegende Funktionen zur [Farbzuordnung](c.md) innerhalb von Geräte Kontexten. Sie sind für alle Anwendungen nützlich, die die Farbverwaltung mit geringem mehr Aufwand und minimalem Benutzereingriff implementieren müssen.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Checkcolorsingamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Überprüft, ob die angegebenen Farben sich im Gamut eines Geräts befinden.                                                                                                     |
| [**Colorcorrectpalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Korrigiert die Einträge in einer Palette für einen Gerätekontext.                                                                                             |
| [**Colormatchdetarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Führt eine Farbzuordnung für Vorschau Zwecke aus.                                                                                                        |
| [**"Kreatecolorspace"**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Erstellt einen Farbraum.                                                                                                                              |
| [**Deletecolorspace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Löscht einen Farbraum.                                                                                                                              |
| [**"Umumicmprofiles"**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Listet Ausgabe Farbprofile auf, die für einen bestimmten Gerätekontext verfügbar sind.                                                                              |
| [**"Umumicmprofilesproccallback"**](/windows/desktop/api/Wingdi/) | Anwendungs definierte Rückruffunktion für [**enumicmprofiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). Der Name dieser Funktion wird auch von der Anwendung definiert. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ruft den aktuellen Eingabe Farbraum in einem Gerätekontext ab. |
| [**Geticmprofile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Ruft das aktuelle Ausgabe Farbprofil eines Geräte Kontexts ab.                                                                                          |
| [**Getlogcolorspace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Ruft die [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) -Struktur eines Geräte Kontexts ab.                                                                      |
| [**Setcolorspace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Legt den Eingabe Farbraum eines Geräte Kontexts fest.                                                                                                          |
| [**-Modus**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Schaltet die Farbverwaltung in einem Gerätekontext ein bzw. aus.                                                                                               |
| [**"Abbild profile"**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Legt das Ausgabe Farbprofil für einen angegebenen Gerätekontext fest.                                                                                           |
| [**Wcsenaufcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Listet alle Farbprofile auf, die die enumerationskriterien im angegebenen Profil Verwaltungsbereich erfüllen.                                      |



 

 

 




