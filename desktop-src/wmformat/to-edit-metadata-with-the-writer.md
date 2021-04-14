---
title: So bearbeiten Sie Metadaten mit dem Writer
description: So bearbeiten Sie Metadaten mit dem Writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media-Format-SDK, Bearbeiten von Metadaten mit dem Writer
- Windows Media-Format-SDK, Metadatenbearbeitung
- Advanced Systems Format (ASF), Bearbeiten von Metadaten mit dem Writer
- ASF (Advanced Systems Format), Bearbeiten von Metadaten mit dem Writer
- Advanced Systems Format (ASF), Metadatenbearbeitung
- ASF (Advanced Systems Format), Metadatenbearbeitung
- Metadaten, bearbeiten mit dem Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390060"
---
# <a name="to-edit-metadata-with-the-writer"></a><span data-ttu-id="a73dd-110">So bearbeiten Sie Metadaten mit dem Writer</span><span class="sxs-lookup"><span data-stu-id="a73dd-110">To Edit Metadata with the Writer</span></span>

<span data-ttu-id="a73dd-111">Sie können direkt vom Writer aus auf die Metadaten, die in den Header der Datei gelangen, zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a73dd-111">You can access, directly from the writer, the metadata that will go into the header of the file.</span></span> <span data-ttu-id="a73dd-112">Rufen Sie die **QueryInterface** -Methode einer beliebigen Schnittstelle im Writer-Objekt auf, um einen Zeiger auf die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -oder [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a73dd-112">Call the **QueryInterface** method of any interface in the writer object to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interface.</span></span> <span data-ttu-id="a73dd-113">Nachdem Sie über einen Zeiger auf die entsprechende Schnittstelle verfügen, können Sie die Metadaten genauso bearbeiten, wie Sie dies tun würden, wenn Sie die Datei im Metadateneditor-Objekt geladen hätten.</span><span class="sxs-lookup"><span data-stu-id="a73dd-113">After you have a pointer to the appropriate interface, you can manipulate the metadata just as you would if you had loaded the file in the metadata editor object.</span></span> <span data-ttu-id="a73dd-114">Weitere Informationen zum Bearbeiten von Metadaten finden Sie unter [Arbeiten mit Metadaten](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="a73dd-114">For more information about editing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

<span data-ttu-id="a73dd-115">Sie müssen vor dem Aufrufen von [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)alle Änderungen an den Metadaten vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a73dd-115">You must make all changes to the metadata before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

> [!Note]  
> <span data-ttu-id="a73dd-116">Wenn Sie Metadaten für eine Datei festlegen, die Datei schreiben und dann vorbereiten, eine neue Datei zu schreiben, ohne den Writer freizugeben, bleiben einige Metadaten, die für die erste Datei festgelegt wurden, festgelegt und werden in nachfolgende Dateien eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a73dd-116">If you set metadata for a file, write the file, and then prepare to write a new file without releasing the writer, some metadata that was set for the first file will remain set and will be included with subsequent files.</span></span> <span data-ttu-id="a73dd-117">Wenn Sie mehrere Dateien mit derselben Instanz des Writer-Objekts schreiben, haben Sie zwei Möglichkeiten: Überprüfen Sie alle Metadaten, bevor Sie jede Datei schreiben, oder schreiben Sie nur in die Writer-Metadaten, die für alle Dateien gelten, die Sie schreiben.</span><span class="sxs-lookup"><span data-stu-id="a73dd-117">When writing several files with the same instance of the writer object, you have two options: check all the metadata before writing each file, or only write in the writer metadata that applies to all of the files you are writing.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a73dd-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a73dd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a73dd-119">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="a73dd-119">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




