---
title: So identifizieren Sie Eingaben nach Zahl
description: So identifizieren Sie Eingaben nach Zahl
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF), Identifizieren von Eingaben nach Zahl
- ASF (Advanced Systems Format), Identifizieren von Eingaben nach Zahl
- Profile, Identifizieren von Eingaben nach Zahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038545"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="60593-106">So identifizieren Sie Eingaben nach Zahl</span><span class="sxs-lookup"><span data-stu-id="60593-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="60593-107">Jedes Beispiel, das Sie an den Writer übergeben, muss einer Eingabe Nummer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="60593-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="60593-108">Jede Eingabe Nummer entspricht einem oder mehreren Datenströmen in dem Profil, das der Writer zum Schreiben der Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="60593-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="60593-109">In einem Profil werden Medienquellen anhand eines Verbindungs Namens identifiziert.</span><span class="sxs-lookup"><span data-stu-id="60593-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="60593-110">Der Writer ordnet dem einzelnen Verbindungs Namen eine Eingabe Nummer zu, wenn Sie das Profil für den Writer festlegen.</span><span class="sxs-lookup"><span data-stu-id="60593-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="60593-111">Bevor Sie Beispiele an den Writer übergeben können, müssen Sie bestimmen, welche Daten von den einzelnen Eingaben erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="60593-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="60593-112">Sie können nicht davon ausgehen, dass die Eingaben in derselben Reihenfolge wie die Datenströme in einem Profil vorliegen, auch wenn dies häufig der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="60593-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="60593-113">Daher ist die einzige zuverlässige Möglichkeit, Eingaben mit Streams abzugleichen, der Verbindungs Name der Eingabe mit dem Verbindungs Namen des Streams zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="60593-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="60593-114">Führen Sie die folgenden Schritte aus, um die Verbindungs Namen und die zugehörigen Eingabe Nummern für ein geladenes Profil zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="60593-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="60593-115">Erstellen Sie ein Writer-Objekt, und legen Sie ein Profil zur Verwendung fest.</span><span class="sxs-lookup"><span data-stu-id="60593-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="60593-116">Weitere Informationen zum Festlegen von Profilen im Writer finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="60593-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="60593-117">Sie sollten die Verbindungs Namen kennen, die für die Datenströme im Profil verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60593-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="60593-118">Sie können den Verbindungs Namen innerhalb des Profils abrufen, indem Sie das Datenstrom-Konfigurationsobjekt für jeden Stream abrufen und [**iwmstreamconfig:: getConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="60593-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="60593-119">Weitere Informationen zu Profilen und Stream-Konfigurationsobjekten finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="60593-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="60593-120">Rufen Sie die Gesamtzahl der Eingaben durch Aufrufen von [**iwmwriter:: getinputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount)ab.</span><span class="sxs-lookup"><span data-stu-id="60593-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="60593-121">Durchlaufen Sie alle Eingaben, und führen Sie jeweils die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="60593-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="60593-122">Rufen Sie die [**iwminputmediarequicenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für die Eingabe ab, indem Sie [**iwmwriter:: GetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)Eigenschaften aufrufen.</span><span class="sxs-lookup"><span data-stu-id="60593-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="60593-123">Rufen Sie den Verbindungs Namen ab, der der Eingabe Nummer entspricht, indem Sie [**iwminputmedia-Eigenschaften:: getConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="60593-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="60593-124">Nachdem Sie den Verbindungs Namen eingegeben haben, kennen Sie die Streams, die mit den vom Writer zugewiesenen Eingabe Nummern verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="60593-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="60593-125">Der folgende Beispielcode zeigt den Verbindungs Namen für jede Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="60593-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="60593-126">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="60593-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="60593-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60593-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60593-128">**Iwmwriter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="60593-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="60593-129">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="60593-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




