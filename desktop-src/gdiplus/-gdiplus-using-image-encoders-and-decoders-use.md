---
description: Windows GDI+ bietet die Image-Klasse und die Bitmap-Klasse zum Speichern von Bildern im Speicher und zum Bearbeiten von Bildern im Arbeitsspeicher.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Verwenden von Bild Encodern und-Decodern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129052"
---
# <a name="using-image-encoders-and-decoders"></a>Verwenden von Bild Encodern und-Decodern

Windows GDI+ bietet die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse und die [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse zum Speichern von Bildern im Speicher und zum Bearbeiten von Bildern im Arbeitsspeicher. GDI+ schreibt Bilder mithilfe von Bild Encodern in Datenträger Dateien und lädt Bilder aus Datenträger Dateien mithilfe von Image-Decodern. Ein Encoder übersetzt die Daten in einem **Image** -oder **Bitmap** -Objekt in ein festgelegte Datenträger Dateiformat. Ein Decoder übersetzt die Daten in einer Datenträger Datei in das Format, das für die **Image** -und **Bitmap** -Objekte erforderlich ist. GDI+ verfügt über integrierte Encoder und decoderer, die die folgenden Dateitypen unterstützen:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ verfügt auch über integrierte decoderer, die die folgenden Dateitypen unterstützen:

-   WMF
-   EMF
-   ICON

In den folgenden Themen werden Encoder und Decoder ausführlicher erläutert:

-   [Auflisten installierter Encoder](-gdiplus-listing-installed-encoders-use.md)
-   [Auflisten installierter decoderer](-gdiplus-listing-installed-decoders-use.md)
-   [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Bestimmen der von einem Encoder unterstützten Parameter](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Wandeln eines BMP-Bilds in ein PNG-Bild](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Festlegen der JPEG-Komprimierungs Ebene](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Transformieren eines JPEG-Bilds ohne Informationsverlust](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Erstellen und Speichern eines Bilds mit mehreren Frames](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Kopieren einzelner Frames aus einem Multiple-Frame Bild](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



