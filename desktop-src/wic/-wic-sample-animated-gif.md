---
description: Dieses Beispiel veranschaulicht das Decodieren verschiedener Frames in einer GIF-Datei, das Lesen entsprechender Metadaten für jeden Frame, das Verfassen von Frames und das Rendern der Animation mit Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: WIC animieren GIF-Beispiel
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106353412"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="dbbfd-103">WIC animieren GIF-Beispiel</span><span class="sxs-lookup"><span data-stu-id="dbbfd-103">WIC animated GIF sample</span></span>

<span data-ttu-id="dbbfd-104">Dieses Beispiel veranschaulicht das Decodieren verschiedener Frames in einer GIF-Datei, das Lesen entsprechender Metadaten für jeden Frame, das Verfassen von Frames und das Rendern der Animation mit Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbbfd-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbbfd-105">Requirements</span></span>

<span data-ttu-id="dbbfd-106">Für dieses Beispiel gelten die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="dbbfd-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="dbbfd-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbbfd-107">Requirement</span></span> | <span data-ttu-id="dbbfd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="dbbfd-108">Value</span></span> |
|-|-|
| <span data-ttu-id="dbbfd-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbbfd-109">Minimum supported client</span></span> | <span data-ttu-id="dbbfd-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbbfd-110">Windows 7</span></span> |
| <span data-ttu-id="dbbfd-111">Minimale Windows SDK</span><span class="sxs-lookup"><span data-stu-id="dbbfd-111">Minimum Windows SDK</span></span> | <span data-ttu-id="dbbfd-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbbfd-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="dbbfd-113">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dbbfd-113">Downloading the sample</span></span>

<span data-ttu-id="dbbfd-114">Dieses Beispiel finden Sie unter [WIC animierte GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span><span class="sxs-lookup"><span data-stu-id="dbbfd-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="dbbfd-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dbbfd-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="dbbfd-116">Verwenden von Visual Studio (bevorzugte Methode)</span><span class="sxs-lookup"><span data-stu-id="dbbfd-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="dbbfd-117">Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="dbbfd-118">Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um die Datei in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="dbbfd-119">Wählen Sie im Menü **Erstellen** die Option **Projektmappe erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="dbbfd-120">Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="dbbfd-121">Verwenden der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="dbbfd-121">Using the command prompt</span></span>

<span data-ttu-id="dbbfd-122">So erstellen Sie das Beispiel mithilfe einer Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="dbbfd-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="dbbfd-123">Öffnen Sie die Eingabeaufforderung, und navigieren Sie zum Beispiel Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="dbbfd-124">Geben Sie `msbuild WICAnimatedGif.sln` ein</span><span class="sxs-lookup"><span data-stu-id="dbbfd-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="dbbfd-125">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dbbfd-125">Running the sample</span></span>

<span data-ttu-id="dbbfd-126">Nachdem die Anwendung gestartet wurde, laden Sie eine Bilddatei mit dem Befehl **Öffnen** im Menü **Datei** .</span><span class="sxs-lookup"><span data-stu-id="dbbfd-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="dbbfd-127">Die Fenstergröße wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbbfd-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbbfd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbbfd-128">See also</span></span>

[<span data-ttu-id="dbbfd-129">Microsoft Windows Imaging-Codec</span><span class="sxs-lookup"><span data-stu-id="dbbfd-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="dbbfd-130">Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="dbbfd-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="dbbfd-131">Verweis</span><span class="sxs-lookup"><span data-stu-id="dbbfd-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="dbbfd-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="dbbfd-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="dbbfd-133">Beispiele und Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="dbbfd-133">Samples and code examples</span></span>](-wic-samples.md)
