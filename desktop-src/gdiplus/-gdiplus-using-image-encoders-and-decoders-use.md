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
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="4ee3f-103">Verwenden von Bild Encodern und-Decodern</span><span class="sxs-lookup"><span data-stu-id="4ee3f-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="4ee3f-104">Windows GDI+ bietet die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse und die [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse zum Speichern von Bildern im Speicher und zum Bearbeiten von Bildern im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4ee3f-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="4ee3f-105">GDI+ schreibt Bilder mithilfe von Bild Encodern in Datenträger Dateien und lädt Bilder aus Datenträger Dateien mithilfe von Image-Decodern.</span><span class="sxs-lookup"><span data-stu-id="4ee3f-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="4ee3f-106">Ein Encoder übersetzt die Daten in einem **Image** -oder **Bitmap** -Objekt in ein festgelegte Datenträger Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="4ee3f-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="4ee3f-107">Ein Decoder übersetzt die Daten in einer Datenträger Datei in das Format, das für die **Image** -und **Bitmap** -Objekte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4ee3f-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="4ee3f-108">GDI+ verfügt über integrierte Encoder und decoderer, die die folgenden Dateitypen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="4ee3f-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="4ee3f-109">BMP</span><span class="sxs-lookup"><span data-stu-id="4ee3f-109">BMP</span></span>
-   <span data-ttu-id="4ee3f-110">GIF</span><span class="sxs-lookup"><span data-stu-id="4ee3f-110">GIF</span></span>
-   <span data-ttu-id="4ee3f-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="4ee3f-111">JPEG</span></span>
-   <span data-ttu-id="4ee3f-112">PNG</span><span class="sxs-lookup"><span data-stu-id="4ee3f-112">PNG</span></span>
-   <span data-ttu-id="4ee3f-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="4ee3f-113">TIFF</span></span>

<span data-ttu-id="4ee3f-114">GDI+ verfügt auch über integrierte decoderer, die die folgenden Dateitypen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="4ee3f-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="4ee3f-115">WMF</span><span class="sxs-lookup"><span data-stu-id="4ee3f-115">WMF</span></span>
-   <span data-ttu-id="4ee3f-116">EMF</span><span class="sxs-lookup"><span data-stu-id="4ee3f-116">EMF</span></span>
-   <span data-ttu-id="4ee3f-117">ICON</span><span class="sxs-lookup"><span data-stu-id="4ee3f-117">ICON</span></span>

<span data-ttu-id="4ee3f-118">In den folgenden Themen werden Encoder und Decoder ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="4ee3f-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="4ee3f-119">Auflisten installierter Encoder</span><span class="sxs-lookup"><span data-stu-id="4ee3f-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="4ee3f-120">Auflisten installierter decoderer</span><span class="sxs-lookup"><span data-stu-id="4ee3f-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="4ee3f-121">Abrufen des Klassen Bezeichners für einen Encoder</span><span class="sxs-lookup"><span data-stu-id="4ee3f-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="4ee3f-122">Bestimmen der von einem Encoder unterstützten Parameter</span><span class="sxs-lookup"><span data-stu-id="4ee3f-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="4ee3f-123">Wandeln eines BMP-Bilds in ein PNG-Bild</span><span class="sxs-lookup"><span data-stu-id="4ee3f-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="4ee3f-124">Festlegen der JPEG-Komprimierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="4ee3f-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="4ee3f-125">Transformieren eines JPEG-Bilds ohne Informationsverlust</span><span class="sxs-lookup"><span data-stu-id="4ee3f-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="4ee3f-126">Erstellen und Speichern eines Bilds mit mehreren Frames</span><span class="sxs-lookup"><span data-stu-id="4ee3f-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="4ee3f-127">Kopieren einzelner Frames aus einem Multiple-Frame Bild</span><span class="sxs-lookup"><span data-stu-id="4ee3f-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



