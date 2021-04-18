---
title: IPaper speichern
description: Der wichtigste Schwerpunkt in diesem Beispielcode ist, wie copaper seine Papier Daten in Verbund Dateien laden und speichern kann. Die iPaper-, Load-und Save-Methoden Implementierungen werden ausführlich erläutert.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340233"
---
# <a name="ipapersave"></a><span data-ttu-id="d74cd-104">IPaper:: Save</span><span class="sxs-lookup"><span data-stu-id="d74cd-104">IPaper::Save</span></span>

<span data-ttu-id="d74cd-105">Der wichtigste Schwerpunkt in diesem Beispielcode ist, wie copaper seine Papier Daten in Verbund Dateien laden und speichern kann.</span><span class="sxs-lookup"><span data-stu-id="d74cd-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="d74cd-106">Die [**iPaper**](ipaper-methods.md)-, [**Load**](ipaper--load.md)-und **Save** -Methoden Implementierungen werden ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="d74cd-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="d74cd-107">Im folgenden finden Sie die **iPaper:: Save** -Methode von Paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="d74cd-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



<span data-ttu-id="d74cd-108">In dieser Client-und Server Beziehung erstellt copaper nicht die Verbund Datei, mit der Papier Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d74cd-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="d74cd-109">Sowohl für die **Save** -als auch die [**Load**](ipaper--load.md) -Methode übergibt der Client einen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstellen Zeiger für eine vorhandene Verbund Datei.</span><span class="sxs-lookup"><span data-stu-id="d74cd-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="d74cd-110">Anschließend wird der **IStorage** zum Schreiben und Lesen von Daten in dieser Verbund Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="d74cd-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="d74cd-111">In **iPaper:: Save** oberhalb werden mehrere Datentypen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d74cd-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="d74cd-112">Die CLSID für dllpaper, CLSID \_ dllpaper, wird serialisiert und in einem speziellen com-gesteuerten Stream im Speicher Objekt mit dem Namen " \\ 001compobj" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d74cd-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="d74cd-113">Die Funktion " [**Write Service classstg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) " führt diesen Speicher aus.</span><span class="sxs-lookup"><span data-stu-id="d74cd-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="d74cd-114">Diese gespeicherten CLSID-Daten können verwendet werden, um die Speicherinhalte der dllpaper-Komponente zuzuordnen, die Sie erstellt hat und interpretieren kann.</span><span class="sxs-lookup"><span data-stu-id="d74cd-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="d74cd-115">In diesem Beispiel wird der Stamm Speicher von **stoclien** übergeben, und daher ist die gesamte Verbund Datei der Komponente dllpaper zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d74cd-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="d74cd-116">Diese CLSID-Daten können später mit einem Rückruf der Dienstfunktion " [**leserclassg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d74cd-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="d74cd-117">Da in dllpaper bearbeitbare Daten behandelt werden, ist es auch sinnvoll, ein Zwischenablage Format im Speicher aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d74cd-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="d74cd-118">Die Funktion " [**schreitefmtusertypestg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) " wird aufgerufen, um sowohl eine Format Bezeichnung für die Zwischenablage als auch einen Benutzer lesbaren Namen für das Format zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d74cd-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="d74cd-119">Der für den Benutzer lesbare Name ist für die GUI-Anzeige in Auswahllisten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d74cd-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="d74cd-120">Der oben weiter gegebene Name verwendet das-Makro clipbdfmt \_ Str, das in Paper. h als "dllpaper 1,0" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d74cd-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="d74cd-121">Diese gespeicherten Zwischenablage Daten können später mit einem Aufrufen der Dienstfunktion " [**leserfmtusertypestg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d74cd-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="d74cd-122">Diese Funktion gibt einen Zeichen folgen Wert zurück, der mithilfe der Arbeitsspeicher Zuweisung zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="d74cd-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="d74cd-123">Der Aufrufer ist für das Freigeben der Zeichenfolge verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d74cd-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="d74cd-124">Beim nächsten **Speichern** wird ein Stream im Speicher für die copaper-Papier Daten erstellt.</span><span class="sxs-lookup"><span data-stu-id="d74cd-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="d74cd-125">Der Stream wird als "Taschen Daten" bezeichnet und mithilfe des Stream \_ Taschen \_ datentops "USTR" übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d74cd-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="d74cd-126">Die [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) -Methode erfordert, dass diese Zeichenfolge in Unicode enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d74cd-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="d74cd-127">Da die Zeichenfolge zur Kompilierzeit festgelegt ist, wird das Makro in Paper. h als Unicode definiert.</span><span class="sxs-lookup"><span data-stu-id="d74cd-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="d74cd-128">Das "L" vor der Zeichenfolge, das Long angibt, erreicht dies.</span><span class="sxs-lookup"><span data-stu-id="d74cd-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="d74cd-129">Die Methode " [**kreatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) " erstellt und öffnet einen Stream innerhalb des angegebenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="d74cd-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="d74cd-130">Ein [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen Zeiger für den neuen Stream wird in der Zeiger Variablen der aufrufenden Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="d74cd-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="d74cd-131">Die adressf wird für diesen Schnittstellen Zeiger innerhalb von " **kreatestream**" aufgerufen, und der Aufrufer muss diesen Zeiger nach der Verwendung freigeben.</span><span class="sxs-lookup"><span data-stu-id="d74cd-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="d74cd-132">Der Methode " **kreatestream** " werden wie folgt zahlreiche zugriffsmodusflags übergeben.</span><span class="sxs-lookup"><span data-stu-id="d74cd-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="d74cd-133">STGM \_ Create \| STGM \_ Write \| STGM \_ Direct \| STGM \_ share \_ exklusiv</span><span class="sxs-lookup"><span data-stu-id="d74cd-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="d74cd-134">[**STGM \_ Create**](stgm-constants.md) erstellt einen neuen Stream oder überschreibt einen vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="d74cd-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="d74cd-135">[**STGM \_ Write**](stgm-constants.md) öffnet den Stream mit Schreib Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="d74cd-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="d74cd-136">[**STGM \_ Direkt**](stgm-constants.md) öffnet den Stream für den direkten Zugriff im Gegensatz zum transaktiven Zugriff.</span><span class="sxs-lookup"><span data-stu-id="d74cd-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="d74cd-137">[**STGM \_ Freigabe \_ exklusiv**](stgm-constants.md) öffnet die Datei für den exklusiven, nicht freigegebenen Gebrauch durch den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="d74cd-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="d74cd-138">Nachdem der Taschen Datenstrom erfolgreich erstellt wurde, wird die [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstelle verwendet, um in den Stream zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d74cd-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="d74cd-139">Die **IStream:: Write** -Methode wird verwendet, um zuerst den Inhalt der Papier \_ Eigenschafts Struktur zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d74cd-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="d74cd-140">Dabei handelt es sich im Wesentlichen um einen Eigenschaften Header am Anfang des Streams.</span><span class="sxs-lookup"><span data-stu-id="d74cd-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="d74cd-141">Da die Versionsnummer das erste Ergebnis in der Datei ist, kann Sie unabhängig voneinander gelesen werden, um zu bestimmen, wie die folgenden Daten behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d74cd-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="d74cd-142">Wenn die tatsächlich geschriebene Datenmenge nicht mit der angeforderten Menge übereinstimmt, wird die Save-Methode abgebrochen und gibt STG \_ E \_ kansave zurück.</span><span class="sxs-lookup"><span data-stu-id="d74cd-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="d74cd-143">Es ist einfach, das gesamte Array von frei Hand Daten in den Stream zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d74cd-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="d74cd-144">Da die [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) -Methode mit einem Bytearray arbeitet, wird die Anzahl der Bytes gespeicherter frei Hand Daten im Array berechnet, und der Schreibvorgang beginnt am Anfang des Arrays.</span><span class="sxs-lookup"><span data-stu-id="d74cd-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="d74cd-145">Wenn die tatsächlich geschriebene Datenmenge nicht mit der angeforderten Menge übereinstimmt, gibt die **Save** -Methode STG \_ E \_ kansave zurück.</span><span class="sxs-lookup"><span data-stu-id="d74cd-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="d74cd-146">Nachdem der Stream geschrieben wurde, gibt die **iPaper:: Save** -Methode den verwendeten [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="d74cd-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="d74cd-147">Die **Save** -Methode ruft auch den Client [**itaschen Sink**](ipapersink-methods.md) (in der internen Methode "copaper-notifysinks") auf, um den Client zu benachrichtigen, dass der Speichervorgang beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d74cd-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="d74cd-148">An diesem Punkt wird die **Save** -Methode an den aufrufenden Client zurückgegeben, der in der Regel den [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger freigibt.</span><span class="sxs-lookup"><span data-stu-id="d74cd-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 




