---
title: sRGB Standardfarbraum
description: Aufgrund von Überlegungen zur Internetbandbreite haben Hewlett-Packard und Microsoft die Einführung eines vordefinierten Standardfarbraums namens sRGB (IEC 61966-2-1) vorgeschlagen, um eine genaue Farbzuordnung mit sehr geringem Datenaufwand zu ermöglichen.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), sRGB-Farbraum
- WCS (Windows-Farbsystem),sRGB-Farbraum
- Bildfarbverwaltung, sRGB-Farbraum
- Farbverwaltung,sRGB-Farbraum
- Farben, sRGB-Farbraum
- sRGB-Farbraum
- Farbräume, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443641"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: Ein Standardfarbraum

Aufgrund von Überlegungen zur Internetbandbreite haben Hewlett-Packard und Microsoft die Einführung eines vordefinierten [Standardfarbraums](c.md) namens *sRGB* (IEC 61966-2-1) vorgeschlagen, um eine genaue [Farbzuordnung](c.md) mit sehr geringem Datenaufwand zu ermöglichen.

Eine Hilfedateiversion eines Whitepapers, in dem die technischen Details von sRGB, sRGB.hlp, erörtert werden, finden Sie im \\ Hilfeordner der WCS 1.0-Programmierreferenz.

Verschiedene Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Bild im sRGB-Farbraum befindet. Im Windows-DIB-Format (Device-Independent Bitmap) gibt das Festlegen des **bV5CSType-Elements** der [**BITMAPV5HEADER-Struktur**](using-structures-in-wcs-1-0.md) auf **LCS \_ sRGB** an, dass sich die DIB-Farben im sRGB-Farbraum befinden.

WCS 1.0 bietet native Unterstützung für sRGB. Es gibt zwei Möglichkeiten, WCS 1.0 zum Rendern eines im sRGB-Farbraum definierten Bilds zu verwenden:

**So rendern Sie ein Bild im Gerätekontext**

1.  Erstellen Sie einen Gerätekontext (DC) auf dem Anzeigegerät.
2.  Legen Sie die Farbverwaltung mithilfe der [**SetICMMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) fest.
3.  Verwenden Sie die [**SetDIBitsToDevice-Funktion,**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) um das DIB auf den DC zu übertragen. Solange das **bV5CSMType-Element** der [**BITMAPV5HEADER-Struktur**](using-structures-in-wcs-1-0.md) des DIBs auf **LCS \_ sRGB** festgelegt ist, führt das System die entsprechende Farbverwaltung durch.

**So rendern Sie ein Bild außerhalb des Gerätekontexts**

1.  Erstellen Sie mit [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw)eine Transformation. Der **lcsCSType-Member** der [**LOGCOLORSPACE-Struktur,**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) auf den der *pLogColorSpace-Parameter* zeigt, sollte auf **LCS \_ sRGB** festgelegt werden. Der *Parameter hDestProfile* gibt den Farbraum des Anzeigegeräts an.
2.  Verwenden Sie die erstellte Farbtransformation, um die Farbe mit dem Bild abzugleichen, bevor Sie es auf dem Gerät anzeigen.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>WCS 1.0-Standardwerte für Eingabefarbraum und Ausgabeprofil

Wenn kein Eingabefarbraum angegeben ist, verwendet WCS 1.0 standardmäßig den sRGB-Farbraum als Eingabefarbraum für die [Farbzuordnung.](c.md)

Wenn kein Ausgabeprofil angegeben ist, aber ein Standardgerät angegeben ist, wählt WCS 1.0 ein Standardausgabeprofil aus. Wenn dem Standardgerät kein Profil zugeordnet ist, verwendet WCS 1.0 den sRGB-Farbraum als Ausgabeprofil.

Die folgende Tabelle zeigt die resultierenden Farbtransformationen, wenn kein Standardgerät verfügbar ist.



|  &nbsp;                               | Angegebenes Ausgabeprofil                              | Ausgabeprofil nicht angegeben                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Eingabefarbraum angegeben     | Die Transformation verwendet die angegebenen Profile.                | Transformiert Konvertierungen aus dem bekannten Eingabefarbraum in sRGB. |
| Eingabefarbraum nicht angegeben | Transformiert Konvertierungen von sRGB in ein bekanntes Ausgabeprofil. | Die Transformation von sRGB in sRGB wird angenommen. es wird nichts ausgeführt. |



 

## <a name="srgb-and-embedded-profiles"></a>sRGB und eingebettete Profile

Ab ICM Version 2.0 können Anwendungen, die WCS verwenden, Profile in Images einbetten. Eingebettete Profile unterstützen Die Anwendungen von Benutzern dabei, eine konsistente Farbdarstellung beizubehalten, auch wenn Bilder über das Internet übertragen werden.

Bilder, die den sRGB-Farbraum verwenden, benötigen kein eingebettetes Farbprofil. Da sie über kein eingebettetes Profil verfügen, sind sRGB-basierte Images kleiner und leichter über Datenkanäle mit begrenzter Bandbreite übertragbar.

Anwendungen sollten das **LCS \_ sRGB-Flag** im Bitmapheader des Bilds festlegen, um anzugeben, dass das Bild den sRGB-Farbraum verwendet. Weitere Informationen finden Sie unter [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) und [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 