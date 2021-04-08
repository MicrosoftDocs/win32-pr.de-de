---
title: Auflisten von senken
description: Auflisten von senken
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF), Aufzählen von senken
- ASF (Advanced Systems Format), Enumerieren von senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, auflisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724030"
---
# <a name="enumerating-sinks"></a><span data-ttu-id="3f870-108">Auflisten von senken</span><span class="sxs-lookup"><span data-stu-id="3f870-108">Enumerating Sinks</span></span>

<span data-ttu-id="3f870-109">Dem Writer können viele senken zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3f870-109">The writer can have many sinks associated with it.</span></span> <span data-ttu-id="3f870-110">Sie können die senken, die dem Writer hinzugefügt wurden, mithilfe von [**iwmschreiteradvanced:: getsink count**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) und [**iwmschreiteradvanced:: getsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink)auflisten.</span><span class="sxs-lookup"><span data-stu-id="3f870-110">You can enumerate the sinks that have been added to the writer by using [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) and [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span></span>

<span data-ttu-id="3f870-111">Der Beispielcode in den [Fehlermeldungen aus einer Senke](getting-error-messages-from-a-sink.md) veranschaulicht die Senke-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="3f870-111">The example code in the [Getting Error Messages from a Sink](getting-error-messages-from-a-sink.md) demonstrates sink enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="3f870-112">Beim Auflisten von senken wird die standardmäßige Datei Senke, die als Reaktion auf einen [**callmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) erstellt wurde, zusammen mit allen anderen senken aufgelistet, die Sie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="3f870-112">When enumerating sinks, the default file sink created in response to a call to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) will be enumerated along with any other sinks you have added.</span></span> <span data-ttu-id="3f870-113">Wenn Sie nur die standardmäßige Datei Senke verwenden, können Sie darauf zugreifen, indem Sie **getsink** für Senke-Index 0 aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3f870-113">If you are using only the default file sink, you can access it by calling **GetSink** for sink index 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3f870-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f870-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f870-115">**Iwmschreiteradvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3f870-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="3f870-116">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="3f870-116">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




