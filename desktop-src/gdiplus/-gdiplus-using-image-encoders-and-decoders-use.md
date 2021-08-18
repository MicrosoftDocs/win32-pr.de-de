---
description: Windows GDI+ stellt die Image-Klasse und die Bitmap-Klasse zum Speichern von Bildern im Arbeitsspeicher und Bearbeiten von Bildern im Arbeitsspeicher zur Verfügung.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Verwenden von Bildencodern und Decodern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3509b8fc48ff8c9ef2c52093a6fd06a4349602c6e904df24cf7e528e9f8e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977280"
---
# <a name="using-image-encoders-and-decoders"></a>Verwenden von Bildencodern und Decodern

Windows GDI+ stellt die [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) und die [**Bitmap-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) zum Speichern von Bildern im Arbeitsspeicher und Bearbeiten von Bildern im Arbeitsspeicher zur Verfügung. GDI+ schreibt Bilder mithilfe von Bildencodern in Datenträgerdateien und lädt Bilder mithilfe von Imagedecodern aus Datenträgerdateien. Ein Encoder übersetzt die Daten in einem **Bild-** oder **Bitmapobjekt** in ein bestimmtes Datenträgerdateiformat. Ein Decoder übersetzt die Daten in einer Datenträgerdatei in das für die **Bild-** und **Bitmapobjekte erforderliche** Format. GDI+ verfügt über integrierte Encoder und Decoder, die die folgenden Dateitypen unterstützen:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ verfügt auch über integrierte Decoder, die die folgenden Dateitypen unterstützen:

-   WMF
-   EMF
-   ICON

In den folgenden Themen werden Encoder und Decoder ausführlicher behandelt:

-   [Auflisten installierter Encoder](-gdiplus-listing-installed-encoders-use.md)
-   [Auflisten installierter Decoder](-gdiplus-listing-installed-decoders-use.md)
-   [Abrufen des Klassenbezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Bestimmen der von einem Encoder unterstützten Parameter](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Konvertieren eines BMP-Bilds in ein PNG-Bild](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Festlegen der JPEG-Komprimierungsstufe](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Transformieren eines JPEG-Bilds ohne Informationsverlust](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Erstellen und Speichern eines Bilds mit mehreren Frames](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Kopieren einzelner Frames aus einem Multiple-Frame Bild](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



