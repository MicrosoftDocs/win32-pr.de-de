---
title: So identifizieren Sie Ausgabe Nummern
description: So identifizieren Sie Ausgabe Nummern
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media-Format-SDK, Identifizieren von Ausgabe Nummern
- Advanced Systems Format (ASF), identifizierende Ausgabe Nummern
- ASF (Advanced Systems Format), Identifizieren von Ausgabe Nummern
- Advanced Systems Format (ASF), Ausgabe Nummern und Formate
- ASF (Advanced Systems Format), Ausgabe Nummern und Formate
- ausgabezahlen und Formate, identifizieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341504"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="126b4-109">So identifizieren Sie Ausgabe Nummern</span><span class="sxs-lookup"><span data-stu-id="126b4-109">To Identify Output Numbers</span></span>

<span data-ttu-id="126b4-110">Führen Sie die folgenden Schritte aus, um die Ausgabe Nummern für eine geladene Datei zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="126b4-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="126b4-111">Diese Prozeduren sind sowohl für den asynchronen Reader als auch für den synchronen Reader identisch.</span><span class="sxs-lookup"><span data-stu-id="126b4-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="126b4-112">Wenn Schnittstellennamen unterschiedlich sind, werden die synchronen Reader-Methoden nach den Methoden des asynchronen Readers in Klammern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="126b4-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="126b4-113">Erstellen Sie ein Reader-Objekt, und laden Sie eine Datei zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="126b4-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="126b4-114">Weitere Informationen finden Sie unter so [Erstellen Sie einen Reader und öffnen eine Datei](to-create-a-reader-and-open-a-file.md) (oder [zum Erstellen eines synchronen Readers und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="126b4-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="126b4-115">Rufen Sie die Gesamtanzahl der Ausgaben für die Datei ab, indem Sie [**iwmreader:: getoutputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (oder [**iwmsyncreader:: getoutputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="126b4-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="126b4-116">Führen Sie nacheinander die Ausgaben aus, und führen Sie jeweils die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="126b4-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="126b4-117">Rufen Sie die [**iwmoutputmediadie**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) -Schnittstelle für die aktuelle Ausgabe mit einem Befehl von [**iwmreader:: getoutputrequi(**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) oder [**iwmsynkreader:: GetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)Eigenschaften) ab.</span><span class="sxs-lookup"><span data-stu-id="126b4-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="126b4-118">Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für die Ausgabe ab, indem Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)durchführen.</span><span class="sxs-lookup"><span data-stu-id="126b4-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="126b4-119">Führen Sie den ersten-Befehl aus, um die Größe der Struktur abzurufen, und weisen Sie dann Arbeitsspeicher zu, und übergeben Sie einen Zeiger auf den zugeordneten Speicher im zweiten-Befehl.</span><span class="sxs-lookup"><span data-stu-id="126b4-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="126b4-120">Alternativ können Sie [**iwmmedia-Eigenschaften:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)aufrufen, das den Haupttyp übermittelt, ohne dass Sie Arbeitsspeicher für die **WM- \_ \_ Medientyp** Struktur zuweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="126b4-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="126b4-121">Sie können Ausgaben des falschen Haupt Typs überspringen.</span><span class="sxs-lookup"><span data-stu-id="126b4-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="126b4-122">Rufen Sie den Haupt Medientyp und den Medien Untertyp aus der **WM- \_ \_ Medientyp** Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="126b4-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="126b4-123">Diese Werte werden in den Datenmembern **majortype** und **Untertyp** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="126b4-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="126b4-124">Überprüfen Sie den Wert von **WM \_ Media \_ Type. formatType**.</span><span class="sxs-lookup"><span data-stu-id="126b4-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="126b4-125">Gibt den Typ der Struktur an, die im Puffer bei **WM \_ Media \_ Type. pbformat** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="126b4-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="126b4-126">Weitere Informationen zu Format Typen finden Sie unter [Medientypen](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="126b4-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="126b4-127">Weisen Sie Arbeitsspeicher zu, um die Struktur des Typs zu speichern, der im vorherigen Schritt identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="126b4-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="126b4-128">Kopieren Sie die Struktur in den zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="126b4-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="126b4-129">Für Audiodaten und Videos bietet diese Struktur wichtige Informationen darüber, wie die Daten gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="126b4-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="126b4-130">Der synchrone Reader bietet auch Methoden zum Abrufen von Zuordnungen zwischen Ausgabe Nummern und streamnummern.</span><span class="sxs-lookup"><span data-stu-id="126b4-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="126b4-131">Weitere Informationen [finden Sie unter so finden Sie streamnummern und Ausgabe Nummern](to-find-stream-numbers-and-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="126b4-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="126b4-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="126b4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="126b4-133">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="126b4-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="126b4-134">**Iwmmedia-Eigenschaften Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="126b4-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="126b4-135">**Iwmoutputmediadie-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="126b4-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="126b4-136">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="126b4-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="126b4-137">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="126b4-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="126b4-138">**Arbeiten mit Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="126b4-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




