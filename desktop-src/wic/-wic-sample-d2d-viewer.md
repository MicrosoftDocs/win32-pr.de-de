---
description: Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren einer Bilddatei und Direct2D, um das Bild auf dem Bildschirm zu Rendering.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: WIC-Image-Viewer mit Direct2D-Beispiel
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106364023"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="61dc3-103">WIC-Image-Viewer mit Direct2D-Beispiel</span><span class="sxs-lookup"><span data-stu-id="61dc3-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="61dc3-104">Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren einer Bilddatei und Direct2D, um das Bild auf dem Bildschirm zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="61dc3-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="61dc3-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61dc3-105">Requirements</span></span>

<span data-ttu-id="61dc3-106">Für dieses Beispiel gelten die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="61dc3-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="61dc3-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61dc3-107">Requirement</span></span> | <span data-ttu-id="61dc3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="61dc3-108">Value</span></span> |
|-|-|
| <span data-ttu-id="61dc3-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61dc3-109">Minimum supported client</span></span> | <span data-ttu-id="61dc3-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61dc3-110">Windows Vista</span></span> |
| <span data-ttu-id="61dc3-111">Minimale Windows SDK</span><span class="sxs-lookup"><span data-stu-id="61dc3-111">Minimum Windows SDK</span></span> | <span data-ttu-id="61dc3-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7</span><span class="sxs-lookup"><span data-stu-id="61dc3-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="61dc3-113">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61dc3-113">Downloading the sample</span></span>

<span data-ttu-id="61dc3-114">Dieses Beispiel ist im [WIC-Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61dc3-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="61dc3-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61dc3-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="61dc3-116">Verwenden von Visual Studio (bevorzugte Methode)</span><span class="sxs-lookup"><span data-stu-id="61dc3-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="61dc3-117">Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="61dc3-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="61dc3-118">Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um die Datei in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="61dc3-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="61dc3-119">Wählen Sie im Menü **Erstellen** die Option **Projektmappe erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="61dc3-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="61dc3-120">Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="61dc3-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="61dc3-121">Verwenden der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="61dc3-121">Using the command prompt</span></span>

<span data-ttu-id="61dc3-122">So erstellen Sie das Beispiel mithilfe einer Eingabeaufforderung:</span><span class="sxs-lookup"><span data-stu-id="61dc3-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="61dc3-123">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zum Beispiel Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="61dc3-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="61dc3-124">Geben Sie `msbuild WICViewerD2D.sln` ein</span><span class="sxs-lookup"><span data-stu-id="61dc3-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="61dc3-125">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61dc3-125">Running the sample</span></span>

<span data-ttu-id="61dc3-126">Nachdem Sie die Anwendung gestartet haben, laden Sie eine Bilddatei mit dem Befehl **Öffnen** im Menü **Datei** .</span><span class="sxs-lookup"><span data-stu-id="61dc3-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="61dc3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61dc3-127">See also</span></span>

[<span data-ttu-id="61dc3-128">Microsoft Windows Imaging-Codec</span><span class="sxs-lookup"><span data-stu-id="61dc3-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="61dc3-129">Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="61dc3-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="61dc3-130">Verweis</span><span class="sxs-lookup"><span data-stu-id="61dc3-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="61dc3-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="61dc3-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="61dc3-132">Beispiele und Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="61dc3-132">Samples and code examples</span></span>](-wic-samples.md)
