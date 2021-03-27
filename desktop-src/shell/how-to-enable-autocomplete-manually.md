---
description: Um eine ausführlichere Kontrolle über das Auto Vervollständigen-Verhalten zu erhalten oder eine benutzerdefinierte Quelle von Auto Vervollständigen-Zeichen folgen hinzuzufügen, müssen Sie das Auto Vervollständigen-Objekt selbst verwalten.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Manuelles Aktivieren von AutoComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979569"
---
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="0fa3f-103">Manuelles Aktivieren von AutoComplete</span><span class="sxs-lookup"><span data-stu-id="0fa3f-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="0fa3f-104">Um eine ausführlichere Kontrolle über das Auto Vervollständigen-Verhalten zu erhalten oder eine benutzerdefinierte Quelle von Auto Vervollständigen-Zeichen folgen hinzuzufügen, müssen Sie das Auto Vervollständigen-Objekt selbst verwalten.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="0fa3f-105">Die automatische Vervollständigung kann auf folgende Weise manuell aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="0fa3f-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="0fa3f-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="0fa3f-107">Erstellen eines einfachen AutoComplete-Objekts</span><span class="sxs-lookup"><span data-stu-id="0fa3f-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="0fa3f-108">In den folgenden Schritten wird gezeigt, wie ein einfaches Auto Vervollständigen-Objekt erstellt und initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="0fa3f-109">Ein einfaches Auto Vervollständigen-Objekt schließt Zeichen folgen aus einer einzelnen Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="0fa3f-110">Die Fehlerüberprüfung wurde in diesem Beispiel absichtlich ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="0fa3f-111">Erstellen Sie das Auto Vervollständigen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="0fa3f-112">Erstellen Sie die Auto Vervollständigen-Quelle.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-112">Create the autocomplete source.</span></span> <span data-ttu-id="0fa3f-113">Sie können eine [vordefinierte Auto Vervollständigen-Quelle](ac-ovw.md) verwenden, oder Sie können eine eigene benutzerdefinierte Quelle schreiben.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="0fa3f-114">Im folgenden Code wird eine der vordefinierten Auto Vervollständigen-Quellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="0fa3f-115">Im folgenden Code wird eine benutzerdefinierte Auto Vervollständigen-Quelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="0fa3f-116">Sie können Ihre eigene Auto Vervollständigen-Quelle schreiben, indem Sie ein-Objekt implementieren, das die [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="0fa3f-117">Das-Objekt kann optional auch die [**iaclist**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) -und [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) -Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="0fa3f-118">Legen Sie die Optionen für die Auto Vervollständigen-Quelle fest (optional).</span><span class="sxs-lookup"><span data-stu-id="0fa3f-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="0fa3f-119">Sie können das Verhalten der Auto Vervollständigen-Quelle anpassen, indem Sie deren Optionen festlegen, wenn die Quelle die [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="0fa3f-120">Bei Verwendung der vordefinierten Auto Vervollständigen-Quellen exportiert nur CLSID \_ aclistisf **IACList2**.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="0fa3f-121">Eine umfassende Liste der Optionen und deren Werte finden Sie unter [**IACList2:: \* toptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="0fa3f-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="0fa3f-122">Initialisieren Sie das Auto Vervollständigen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="0fa3f-123">In diesem Beispiel ist **hwndedit** das Handle des Fensters Bearbeitungs Steuerelement, für das Auto Vervollständigen aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="0fa3f-124">Eine Beschreibung der letzten beiden nicht verwendeten Parameter finden Sie unter [**iautocomplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) .</span><span class="sxs-lookup"><span data-stu-id="0fa3f-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="0fa3f-125">Legen Sie die Optionen für das Auto Vervollständigen-Objekt fest (optional).</span><span class="sxs-lookup"><span data-stu-id="0fa3f-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="0fa3f-126">Sie können das Verhalten des Objekts Auto Vervollständigen anpassen, indem Sie dessen Optionen festlegen.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="0fa3f-127">Eine umfassende Liste der Optionen und deren Werte finden Sie in der Dokumentation zu [**IACList2::-toptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="0fa3f-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="0fa3f-128">Geben Sie die Objekte frei.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="0fa3f-129">Das Auto Vervollständigen-Objekt bleibt auch nach der Freigabe an das Bearbeitungs Steuerelement angefügt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="0fa3f-130">Wenn Sie einen späteren Zugriff auf diese Objekte vorsehen – wenn Sie die Auto Vervollständigen-Optionen zu einem späteren Zeitpunkt ändern möchten, z. b. –, ist es nicht erforderlich, dass Sie Sie an diesem Punkt freigeben.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="0fa3f-131">Erstellen eines Verbund Objekts mit automatischer Vervollständigung</span><span class="sxs-lookup"><span data-stu-id="0fa3f-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="0fa3f-132">Ein zusammengesetztes Auto Vervollständigen-Objekt entspricht Zeichen folgen aus mehreren Quellen.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="0fa3f-133">Beispielsweise wird in der Windows Internet Explorer-Adressleiste ein Verbund Objekt für das automatische vervollständigen verwendet, da der Benutzer möglicherweise mit der Eingabe des Namens einer Datei oder einer URL beginnt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="0fa3f-134">Die meisten Schritte zum Erstellen eines Verbund Objekts mit automatischer Vervollständigung sind identisch mit den Schritten unter "Erstellen eines einfachen Auto Vervollständigen-Objekts".</span><span class="sxs-lookup"><span data-stu-id="0fa3f-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="0fa3f-135">Diese Schritte werden als solche Schritte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="0fa3f-136">Erstellen Sie das Auto Vervollständigen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-136">Create the autocomplete object.</span></span> <span data-ttu-id="0fa3f-137">Dies ist das gleiche wie in Schritt 1 oben.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="0fa3f-138">Erstellen Sie den Auto Vervollständigen-Verbund Quell Objekt-Manager.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="0fa3f-139">Das Auto Vervollständigen-Verbund Quell Objekt ermöglicht das Kombinieren mehrerer Auto Vervollständigen-Quellen zu einer einzelnen Auto Vervollständigen-Quelle.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="0fa3f-140">Erstellen und Festlegen von Optionen für jede der Auto Vervollständigen-Quellen</span><span class="sxs-lookup"><span data-stu-id="0fa3f-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="0fa3f-141">Wiederholen Sie die Schritte 2 und 3 für jede Quelle.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="0fa3f-142">Fügen Sie jede Auto Vervollständigen-Quelle an den Quell Objekt-Manager an.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="0fa3f-143">Initialisieren Sie das Auto Vervollständigen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="0fa3f-144">Dies entspricht Schritt 4 oben, mit der Ausnahme, dass Sie den Verbund Quell Objekt-Manager übergeben, anstatt die einfache Auto Vervollständigen-Quelle an [**iautocomplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="0fa3f-145">Legen Sie die Optionen des Objekts Auto Vervollständigen fest.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="0fa3f-146">Dies entspricht dem oben beschriebenen Schritt 5.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="0fa3f-147">Geben Sie die Objekte frei.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-147">Release the objects.</span></span>

    <span data-ttu-id="0fa3f-148">Wie im einfachen Fall können Sie die Objekte freigeben, sobald Sie Sie verwenden, aber Sie können Sie auch später beibehalten, um die Optionen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0fa3f-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
