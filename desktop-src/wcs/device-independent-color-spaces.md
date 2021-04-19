---
title: Geräteunabhängige Farbräume
description: Wenn Sie den Bedarf an standardmäßigen, geräteunabhängigen Farbmessungen, der International de d. d. d. d. d. d. d. d. d. d. 0034 d. Primärfarben.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Color System (WCS), geräteunabhängige Farbbereiche
- WCS (Windows Color System), geräteunabhängige Farbbereiche
- Bild Farbverwaltung, geräteunabhängige Farbbereiche
- Farbverwaltung, geräteunabhängige Farbbereiche
- Farben, geräteunabhängige Farbbereiche
- Farbbereiche, Geräte unabhängig
- geräteunabhängige Farbbereiche
- Commission International de/Eclairage (CIE)
- International Commission on Illumination (CIE)
- Cie (Commission International de l Eclairage)
- Cie (Internationale Kommission bei der Beleuchtung)
- CIEXYZ-Farbraum
- XYZ-Farbraum
- sRGB-Farbraum
- Farbbereiche, CIEXYZ
- Farbbereiche, sRGB
- Farbbereiche, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106357134"
---
# <a name="device-independent-color-spaces"></a>Geräteunabhängige Farbräume

Wenn Sie den Bedarf an standardmäßigen, geräteunabhängigen Farbmessungen, der International de [d. d](p.md). d. d. d. d. d. d. d [](c.md) . d. d. Es wird nicht erwartet, dass das Gerät in diesem Farbraum Farben erzeugt. Sie wird als Mittel zum Umrechnen von Farben von einem Farb Raum in einen anderen verwendet. Die Hauptfarben in diesem Farbraum sind die abstrakten Farben X, Y und Z.

Der 1931 CIEXYZ-Farbraum wird häufig als Grundlage für die Farb Raum Konvertierung verwendet. Mit dem Anstieg des Internets hat die Überlegungen zur Bandbreite jedoch den XYZ-Farbraum nicht schwerfällig. Der Austausch von Images über die begrenzte Bandbreite des Internets erfordert ein kompakteres [Farbmodell](c.md).

Daher haben Hewlett-Packard und Microsoft die Übernahme eines vordefinierten standardmäßigen RGB-Farbraum, der als sRGB bezeichnet wird, vorgeschlagen, um eine exakte Farbverwaltung mit sehr geringem Daten Aufwand zu ermöglichen. Dieser Standard wurde als formaler internationaler Standard vom Internationale Elektrotechnische Kommission (IEC) als IEC 61966-2-1: Multimedia Systems und equipmentcolor Messung und managementpart 2-1: Color managementdefault RGB-Farbraum genehmigt. Er ist direkt von der IEC unter verfügbar <https://www.iec.ch/> . Informationen über die technischen Probleme, die bei sRGB auftreten, sind im Internet verfügbar unter:

[Ein standardmäßiger Standard Farbraum für das Internet (sRGB)](https://www.w3.org/Graphics/Color/sRGB.html)

Eine Hilfedatei Version eines Whitepaper, in dem die technischen Probleme erläutert werden, die mit sRGB (sRGB. hlp) verbunden sind, finden Sie im \\ Hilfe Ordner der WCS 1,0-Programmier Referenz im Platform SDK.

Unterschiedliche Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Image im sRGB-Farbraum befindet. Im Windows-DIB-Format (geräteunabhängige Bitmap) wird durch Festlegen des **bV5CSType** -Members der [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) -Struktur auf LCS \_ sRGB festgelegt, dass die DIB-Farben den sRGB-Farbraum aufweisen.

 

 




