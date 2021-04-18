---
description: Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren eines Bilds, das mit progressiven Ebenen codiert ist.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Beispiel für eine progressive WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106365362"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="41fc7-103">Beispiel für eine progressive WIC</span><span class="sxs-lookup"><span data-stu-id="41fc7-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="41fc7-104">Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren eines Bilds, das mit progressiven Ebenen codiert ist.</span><span class="sxs-lookup"><span data-stu-id="41fc7-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="41fc7-105">In diesem Beispiel wird Direct2D verwendet, um die verschiedenen progressiven Ebenen auf dem Bildschirm zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="41fc7-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="41fc7-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41fc7-106">Requirements</span></span>

<span data-ttu-id="41fc7-107">Für dieses Beispiel gelten die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="41fc7-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="41fc7-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41fc7-108">Requirement</span></span> | <span data-ttu-id="41fc7-109">Wert</span><span class="sxs-lookup"><span data-stu-id="41fc7-109">Value</span></span> |
|-|
| <span data-ttu-id="41fc7-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41fc7-110">Minimum supported client</span></span> | <span data-ttu-id="41fc7-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="41fc7-111">Windows 7</span></span> |
| <span data-ttu-id="41fc7-112">Minimale Windows SDK</span><span class="sxs-lookup"><span data-stu-id="41fc7-112">Minimum Windows SDK</span></span> | <span data-ttu-id="41fc7-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7</span><span class="sxs-lookup"><span data-stu-id="41fc7-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="41fc7-114">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="41fc7-114">Downloading the sample</span></span>

<span data-ttu-id="41fc7-115">Dieses Beispiel ist für die [Progressive WIC-Codierung](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41fc7-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="41fc7-116">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="41fc7-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="41fc7-117">Verwenden von Visual Studio (bevorzugte Methode)</span><span class="sxs-lookup"><span data-stu-id="41fc7-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="41fc7-118">Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="41fc7-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="41fc7-119">Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um die Datei in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="41fc7-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="41fc7-120">Wählen Sie im Menü Erstellen die Option Projektmappe erstellen aus.</span><span class="sxs-lookup"><span data-stu-id="41fc7-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="41fc7-121">Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="41fc7-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="41fc7-122">Verwenden der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="41fc7-122">Using the command prompt</span></span>

<span data-ttu-id="41fc7-123">So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="41fc7-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="41fc7-124">Öffnen Sie die Eingabeaufforderung, und navigieren Sie zum Beispiel Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="41fc7-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="41fc7-125">Geben Sie `msbuild WICProgressiveDecoding.sln` ein</span><span class="sxs-lookup"><span data-stu-id="41fc7-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="41fc7-126">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="41fc7-126">Running the sample</span></span>

<span data-ttu-id="41fc7-127">Nachdem die Anwendung gestartet wurde, laden Sie eine Bilddatei über das Menü Datei öffnen.</span><span class="sxs-lookup"><span data-stu-id="41fc7-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="41fc7-128">Beim Laden wird die standardmäßige Progressive Ebene auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41fc7-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="41fc7-129">Sie können entweder über das Menü oder die nach-unten-Taste zu verschiedenen progressiven Ebenen navigieren.</span><span class="sxs-lookup"><span data-stu-id="41fc7-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="41fc7-130">Der aktuelle Text der progressiven Ebene wird in der Statusleiste des Hauptfensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41fc7-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="41fc7-131">Die Fenstergröße wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41fc7-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="41fc7-132">Die Progressive Decodierung ist nur für Images verfügbar, die progressiv codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="41fc7-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="41fc7-133">Das in diesem Beispiel bereitgestellte Image wurde progressiv codiert.</span><span class="sxs-lookup"><span data-stu-id="41fc7-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="41fc7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41fc7-134">See also</span></span>

[<span data-ttu-id="41fc7-135">Microsoft Windows Imaging-Codec</span><span class="sxs-lookup"><span data-stu-id="41fc7-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="41fc7-136">Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="41fc7-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="41fc7-137">Verweis</span><span class="sxs-lookup"><span data-stu-id="41fc7-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="41fc7-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="41fc7-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="41fc7-139">Beispiele und Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="41fc7-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="41fc7-140">Übersicht über Progressive Decodierung</span><span class="sxs-lookup"><span data-stu-id="41fc7-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
