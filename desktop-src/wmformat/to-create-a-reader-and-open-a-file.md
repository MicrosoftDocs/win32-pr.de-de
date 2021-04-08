---
title: So erstellen Sie einen Reader und öffnen eine Datei
description: So erstellen Sie einen Reader und öffnen eine Datei
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Advanced Systems Format (ASF), Erstellen von Lesern
- ASF (Advanced Systems Format), Erstellen von Lesern
- Advanced Systems Format (ASF), Öffnen von Dateien
- ASF (Advanced Systems Format), Öffnen von Dateien
- asynchrone Leser, erstellen
- asynchrone Leser, Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724091"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="b0dd5-109">So erstellen Sie einen Reader und öffnen eine Datei</span><span class="sxs-lookup"><span data-stu-id="b0dd5-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="b0dd5-110">Bevor Sie mit dem Reader arbeiten können, müssen Sie ein Reader-Objekt erstellen und eine Datei zum Lesen laden.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="b0dd5-111">Führen Sie die folgenden Schritte aus, um den Reader zu initialisieren und eine Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="b0dd5-112">Erstellen Sie ein Reader-Objekt, indem Sie die [**wmcreatereader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="b0dd5-113">Sie müssen die gewünschte Ebene der Rechteverwaltung für das neue Reader-Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="b0dd5-114">Die verfügbaren Modi sind im Enumerationstyp [**WMT- \_ Rechte**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="b0dd5-115">Geben Sie eine zu lesende Datei an, indem Sie [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="b0dd5-116">Sie müssen eine Reader-Rückruf Schnittstelle angeben, die der Reader verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="b0dd5-117">Weitere Informationen zum readerrückruf finden [Sie unter So implementieren Sie Reader-Meldungen im OnStatus-Rückruf](to-implement-reader-messages-in-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="b0dd5-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="b0dd5-118">Warten Sie, bis der Reader die Datei öffnet.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="b0dd5-119">Wenn Sie **Öffnen** zum Laden einer Datei aufzurufen, wird fast sofort zurückgegeben und die Verarbeitung in einem anderen Thread fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="b0dd5-120">Sie sollten auf den Abschluss von Vorgängen warten, indem Sie ein Ereignis signalisieren, wenn der **OnStatus** -Rückruf die geöffnete WMT- \_ Statusmeldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="b0dd5-121">Der Reader unterstützt auch die Verwendung der **IStream** -com-Schnittstelle zum Öffnen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="b0dd5-122">Sie können die **IStream** -Schnittstelle beliebig implementieren.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="b0dd5-123">Nachdem die gewünschte Datei in **IStream** geöffnet wurde, können Sie die oben aufgeführten Schritte ausführen, mit dem Unterschied, dass Sie [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) anstelle von **iwmreader:: Open** in Schritt 2 aufgerufen haben müssen.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0dd5-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0dd5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0dd5-125">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b0dd5-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="b0dd5-126">**IWMReaderAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b0dd5-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="b0dd5-127">**Iwmstatus Callback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b0dd5-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="b0dd5-128">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="b0dd5-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b0dd5-129">**Verwenden der Rückruf Methoden**</span><span class="sxs-lookup"><span data-stu-id="b0dd5-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




