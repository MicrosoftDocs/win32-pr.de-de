---
title: Geräteunabhängige Farbräume
description: In Der Erkenntnis, dass standardmäßige, geräteunabhängige Farbmessungen erforderlich sind, hat die International de l'Eassoage (International Commission onLuminage) oder CIE einen Farbraum basierend auf \ 0034;imaginär \ 0034; erstellt. Primärfarben.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Color System (WCS), geräteunabhängige Farbräume
- WCS (Windows Color System), geräteunabhängige Farbräume
- Bildfarbverwaltung, geräteunabhängige Farbräume
- Farbverwaltung, geräteunabhängige Farbräume
- Farben, geräteunabhängige Farbräume
- Farbräume, geräteunabhängig
- Geräteunabhängige Farbräume
- Commission International de l'Eassoage (CIE)
- International Commission onLumin (CIE)
- CIE (Commission International de l'Eassoage)
- CIE (International Commission onLumin)
- CIEXYZ-Farbraum
- XYZ-Farbraum
- sRGB-Farbraum
- Farbräume, CIEXYZ
- Farbräume, sRGB
- Farbräume, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c350ca4aa4b046d35926cd7568c4fbdfe030b7d7c13b085b9f3837c5dd8418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028788"
---
# <a name="device-independent-color-spaces"></a>Geräteunabhängige Farbräume

In Der Erkenntnis, dass standardmäßige, geräteunabhängige Farbmessungen erforderlich sind, hat die International de l'Eassoage (International Commission on Devices, CIE) einen [Farbraum](c.md) basierend auf "imaginären" [Primärfarben](p.md)erstellt. Es wird nicht erwartet, dass ein gerät Farben in diesem Farbraum erzeugt. Es wird verwendet, um Farben von einem Farbraum in einen anderen zu konvertieren. Die Hauptfarben in diesem Farbraum sind die abstrakten Farben X, Y und Z.

Der CIEXYZ-Farbraum aus dem Jahr 1931 wird häufig als Grundlage für die Farbraumkonvertierung verwendet. Mit dem Anstieg des Internets haben Jedoch Bandbreitenüberlegungen den XYZ-Farbraum unhandlich gemacht. Der Austausch von Bildern über die begrenzte Bandbreite des Internets erfordert ein kompakteres [Farbmodell.](c.md)

Daher haben Hewlett-Packard und Microsoft die Einführung eines vordefinierten RGB-Standardfarbraums namens sRGB vorgeschlagen, um eine präzise Farbverwaltung mit sehr geringem Datenaufwand zu ermöglichen. Dieser Standard wurde vom Internationale Elektrotechnische Kommission (IEC) als formaler internationaler Standard gemäß IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Equipment ManagementDefault RGB Color Space genehmigt. Sie ist direkt über die IEC unter <https://www.iec.ch/> verfügbar. Informationen zu den technischen Problemen im Zusammenhang mit sRGB finden Sie im Internet unter:

[Standardfarbraum für das Internet – sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

Eine Hilfedateiversion eines Whitepapers, in dem die technischen Probleme im Zusammenhang mit sRGB, sRGB.HLP, erörtert werden, finden Sie im \\ Ordner Hilfe der WCS 1.0-Programmierreferenz im Plattform-SDK.

Verschiedene Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Bild im sRGB-Farbraum befindet. Im Windows geräteunabhängigen Bitmapformat (DEVICE-Independent Bitmap, DIB) gibt das Festlegen des **bV5CSType-Elements** der [BITMAPV5HEADER-Struktur](using-structures-in-wcs-1-0.md) auf LCS \_ sRGB an, dass sich die DIB-Farben im sRGB-Farbraum befinden.

 

 




