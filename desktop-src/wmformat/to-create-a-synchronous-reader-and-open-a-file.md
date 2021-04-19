---
title: So erstellen Sie einen synchronen Reader und öffnen eine Datei
description: So erstellen Sie einen synchronen Reader und öffnen eine Datei
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF), Erstellen von Lesern
- ASF (Advanced Systems Format), Erstellen von Lesern
- Advanced Systems Format (ASF), Öffnen von Dateien
- ASF (Advanced Systems Format), Öffnen von Dateien
- synchrone Leser, erstellen
- synchrone Leser, Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106341509"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="c4e25-109">So erstellen Sie einen synchronen Reader und öffnen eine Datei</span><span class="sxs-lookup"><span data-stu-id="c4e25-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="c4e25-110">Bevor Sie mit dem synchronen Reader arbeiten können, müssen Sie ein synchrones Reader-Objekt erstellen und eine Datei zum Lesen laden.</span><span class="sxs-lookup"><span data-stu-id="c4e25-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="c4e25-111">Führen Sie die folgenden Schritte aus, um den synchronen Reader zu initialisieren und eine Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c4e25-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="c4e25-112">Erstellen Sie ein synchrones Reader-Objekt, indem Sie die [**wmcreatesyncreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4e25-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="c4e25-113">Sie müssen die gewünschte Ebene der Rechteverwaltung für das neue Reader-Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="c4e25-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="c4e25-114">Die verfügbaren Modi sind im Enumerationstyp **WMT- \_ Rechte** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4e25-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="c4e25-115">Geben Sie eine Datei an, die Sie lesen möchten, indem Sie [**iwmsyncreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4e25-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="c4e25-116">Der synchrone Reader unterstützt auch die Verwendung der **IStream** -com-Schnittstelle zum Öffnen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="c4e25-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="c4e25-117">Sie können die **IStream** -Schnittstelle beliebig implementieren.</span><span class="sxs-lookup"><span data-stu-id="c4e25-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="c4e25-118">Nachdem die gewünschte Datei in **IStream** geöffnet wurde, können Sie die oben aufgeführten Schritte ausführen, mit dem Unterschied, dass Sie in Schritt 2 iwmsynkreader:: [**OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) anstelle von **iwmsynanader:: Open** aufrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="c4e25-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4e25-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4e25-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e25-120">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4e25-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="c4e25-121">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="c4e25-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




