---
title: sRGB Standardfarbraum
description: Aufgrund von Überlegungen zur Internet Bandbreite hat Hewlett-Packard und Microsoft die Annahme eines standardmäßigen vordefinierten Farbraum vorgeschlagen, der als sRGB (IEC 61966-2-1) bezeichnet wird, damit eine exakte Farbzuordnung mit sehr geringem Daten Aufwand ermöglicht wird.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), sRGB-Farbraum
- WCS (Windows Color System), sRGB-Farbraum
- Bild Farbverwaltung, sRGB-Farbraum
- Farbverwaltung, sRGB-Farbraum
- Farben, sRGB-Farbraum
- sRGB-Farbraum
- Farbbereiche, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "106349749"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: ein Standard Farbraum

Aufgrund von Überlegungen zur Internet Bandbreite hat Hewlett-Packard und Microsoft die Annahme eines standardmäßigen vordefinierten [Farbraum](c.md) vorgeschlagen, der als *sRGB* (IEC 61966-2-1) bezeichnet wird, damit eine exakte [Farbzuordnung](c.md) mit sehr geringem Daten Aufwand ermöglicht wird.

Eine Hilfedatei Version eines Whitepaper, in dem die technischen Details von sRGB (sRGB. hlp) erörtert werden, finden Sie im \\ Hilfe Ordner der WCS 1,0-Programmier Referenz.

Unterschiedliche Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Image im sRGB-Farbraum befindet. Im Windows-DIB-Format (geräteunabhängige Bitmap) wird durch Festlegen des **bV5CSType** -Members der [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) -Struktur auf **LCS \_ sRGB** festgelegt, dass die DIB-Farben den sRGB-Farbraum aufweisen.

WCS 1,0 bietet native Unterstützung für sRGB. Es gibt zwei Möglichkeiten, WCS 1,0 zum Rendern eines Bilds zu verwenden, das im sRGB-Farbraum definiert ist:

**So Rendering Sie ein Bild innerhalb des Geräte Kontexts**

1.  Erstellen Sie einen Gerätekontext (DC) auf dem Anzeigegerät.
2.  Legen Sie die Farbverwaltung mithilfe der [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) -Funktion fest.
3.  Verwenden Sie die Funktion [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) , um das DIB in den DC zu übertragen. Solange der **bV5CSMType** -Member der Disb [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) -Struktur auf **LCS \_ sRGB** festgelegt ist, führt das System die entsprechende Farbverwaltung aus.

**So Rendering Sie ein Bild außerhalb des Geräte Kontexts**

1.  Erstellen Sie eine Transformation mithilfe von " [**kreatecolortransformw**](/windows/win32/api/icm/nf-icm-createcolortransformw)". Der **lcscstype** -Member der [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) -Struktur, auf die der *plogcolorspace* -Parameter verweist, sollte auf **LCS \_ sRGB** festgelegt werden. Der *hdestprofile* -Parameter gibt den Farbraum des Anzeige Geräts an.
2.  Verwenden Sie die erstellte Farb Transformation, um die Farbe der Abbildung zuzuordnen, bevor Sie auf dem Gerät angezeigt wird.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>WCS 1,0-Standardwerte für Eingabe Farbraum und Ausgabeprofil

Wenn kein Eingabe Farbraum angegeben ist, verwendet WCS 1,0 standardmäßig den sRGB-Farbraum als Eingabe Farbraum für die [Farbzuordnung](c.md).

Wenn kein Ausgabeprofil angegeben wird, aber ein Standardgerät angegeben ist, wählt WCS 1,0 ein Standardausgabe Profil aus. Wenn dem Standardgerät kein Profil zugeordnet ist, verwendet WCS 1,0 den sRGB-Farbraum als Ausgabeprofil.

Die folgende Tabelle zeigt die resultierenden Farb Transformationen, wenn ein Standardgerät nicht verfügbar ist.



|                                 | Ausgabeprofil angegeben                              | Das Ausgabeprofil ist nicht angegeben.                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Eingegebener Eingabe Farbraum     | Die Transformation verwendet die angegebenen Profile.                | Transform konvertiert von einem bekannten Eingabe Farbraum in sRGB. |
| Der Eingabe Farbraum ist nicht angegeben. | Transformation konvertiert von sRGB in ein bekanntes Ausgabeprofil. | Es wird davon ausgegangen, dass die Transformation von sRGB in sRGB erfolgt Es erfolgt nichts. |



 

## <a name="srgb-and-embedded-profiles"></a>sRGB und eingebettete Profile

Ab ICM, Version 2,0, können Anwendungen, die WCS verwenden, Profile in Bilder einbetten. Eingebettete Profile unterstützen Benutzer Anwendungen bei der Beibehaltung einer konsistenten Farbdarstellung, auch wenn Bilder über das Internet übertragen werden.

Für Images, die den sRGB-Farbraum verwenden, ist kein eingebettetes Farbprofil erforderlich. Da Sie kein eingebettetes Profil aufweisen, sind sRGB-basierte Images kleiner und leichter über Datenkanäle mit eingeschränkter Bandbreite hinweg übertragbar.

Anwendungen sollten das **LCS \_ sRGB** -Flag im Bitmap-Header des Bilds festlegen, um anzugeben, dass das Bild den sRGB-Farbraum verwendet. Weitere Informationen finden Sie unter [Windows-Bitmap-Header Strukturen](using-structures-in-wcs-1-0.md) und [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 