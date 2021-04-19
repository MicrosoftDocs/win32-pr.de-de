---
title: Makros für CMYK-Werte und -Farben
description: Die folgenden Makros sind hilfreich beim Bearbeiten von CMYK-Werten.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS), CMYK-Makros
- WCS (Windows Color System), CMYK-Makros
- Bild Farbverwaltung, CMYK-Makros
- Farbverwaltung, CMYK-Makros
- Farben, CMYK-Makros
- WCS-Referenz, CMYK-Makros
- Referenz für WCs, CMYK-Makros
- CMYK-Makros
- Zyan Magenta Gelb Schwarz (CMYK)
- CMYK (Cyan Magenta gelb schwarz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106367256"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Makros für CMYK-Werte und -Farben

Die folgenden Makros sind hilfreich beim Bearbeiten von CMYK-Werten.



| Makro                          | Beschreibung                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**CMYK**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Erstellt einen CMYK-Wert aus den Werten einzelner Cyan, Magenta, gelb und schwarz. |
| [**Getcvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Ruft den Zyan-Farbwert aus einem CMYK-Farbwert ab.                      |
| [**Getkvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Ruft den schwarzen Farbwert aus einem CMYK-Farbwert ab.                     |
| [**Getmvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Ruft den Magenta-Wert aus einem CMYK-Farbwert ab.                         |
| [**Getyvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Ruft den gelben Farbwert aus einem CMYK-Farbwert ab.                    |



 

Die folgenden Makros werden mit Color verwendet.



| Makro                                | Beschreibung                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getbvalue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Ruft einen RGB-blauen Wert ab.                                                                                                                               |
| [**Getgvalue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Ruft einen grünen RGB-Wert ab.                                                                                                                              |
| [**Getrvalue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Ruft einen RGB-roten Wert ab.                                                                                                                                |
| [**Paletteingedex**](/previous-versions//dd162770(v=vs.85)) | Akzeptiert einen Index für einen Eintrag in der logischen Farbpalette und gibt einen paletteneintrags Bezeichner zurück.                                                              |
| [**Palettergb**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Akzeptiert drei Werte, die die relativen Intensitäten von rot, grün und blau darstellen, und gibt einen palettenrelativen roten, grünen, blauen (RGB) Spezifizierer zurück. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Wählt eine rote, grüne, blaue (RGB) Farbe basierend auf den angegebenen Argumenten und den Farbfunktionen des Ausgabegeräts aus.                               |



 

 

 