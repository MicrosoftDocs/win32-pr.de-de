---
title: Makros für CMYK-Werte und -Farben
description: Die folgenden Makros sind beim Bearbeiten von CMYK-Werten nützlich.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS), CMYK-Makros
- WCS (Windows Color System), CMYK-Makros
- Bildfarbverwaltung, CMYK-Makros
- Farbverwaltung, CMYK-Makros
- Farben, CMYK-Makros
- WCS-Referenz, CMYK-Makros
- Referenz für WCS,CMYK-Makros
- CMYK-Makros
- cyan magenta yellow black (CMYK)
- CMYK (cyan magenta yellow black)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591c479686db45f1b0d6fc6097d5134de481307b144200604a15b360bcf2c146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593360"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Makros für CMYK-Werte und -Farben

Die folgenden Makros sind beim Bearbeiten von CMYK-Werten nützlich.



| Makro                          | Beschreibung                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**Cmyk**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Erstellt einen CMYK-Wert aus einzelnen Cyan-, Magenta-, Gelb- und Schwarzwerten. |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Ruft den Cyan-Farbwert aus einem CMYK-Farbwert ab.                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Ruft den Wert der schwarzen Farbe aus einem CMYK-Farbwert ab.                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Ruft den Magentawert aus einem CMYK-Farbwert ab.                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Ruft den gelben Farbwert aus einem CMYK-Farbwert ab.                    |



 

Die folgenden Makros werden mit Farbe verwendet.



| Makro                                | Beschreibung                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Ruft einen rgbblauen Wert ab.                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Ruft einen RGB-Grünwert ab.                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Ruft einen rgb-roten Wert ab.                                                                                                                                |
| [**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85)) | Akzeptiert einen Index für einen Eintrag in einer logischen Farbpalette und gibt einen Paletteneintragsspezifizierer zurück.                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Akzeptiert drei Werte, die die relativen Größen von Rot, Grün und Blau darstellen, und gibt einen RGB-Bezeichner (Paletten-relatives Rot, Grün, Blau) zurück. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Wählt basierend auf den angegebenen Argumenten und den Farbfunktionen des Ausgabegeräts eine farbe rot, grün, blau (RGB) aus.                               |



 

 

 