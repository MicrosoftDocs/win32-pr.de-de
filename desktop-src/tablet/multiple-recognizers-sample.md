---
description: In diesem Beispiel werden erweiterte Funktionen der für die Handschrifterkennung verwendeten API (Application Programming Interface, API) für die Verwendung von mikrosofttablet-APIs veranschaulicht.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Beispiel für mehrere erkenzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368904"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="7ef82-103">Beispiel für mehrere erkenzer</span><span class="sxs-lookup"><span data-stu-id="7ef82-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="7ef82-104">In diesem Beispiel werden erweiterte Funktionen der für die *Handschrift* Erkennung verwendeten API (Application Programming Interface, API) für die Verwendung von mikrosofttablet-APIs veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7ef82-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="7ef82-105">Dies umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7ef82-105">It includes the following:</span></span>

-   <span data-ttu-id="7ef82-106">Auflisten der installierten erkenzer</span><span class="sxs-lookup"><span data-stu-id="7ef82-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="7ef82-107">Erstellen eines *Erkennungs Kontexts* mit einer bestimmten Spracherkennung</span><span class="sxs-lookup"><span data-stu-id="7ef82-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="7ef82-108">Serialisieren von Erkennungs Ergebnissen mit einer Stroke-Auflistung</span><span class="sxs-lookup"><span data-stu-id="7ef82-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="7ef82-109">Organisieren von Stroke Collections in eine benutzerdefinierte Sammlung innerhalb des [**InkDisp**](inkdisp-class.md) -Objekts</span><span class="sxs-lookup"><span data-stu-id="7ef82-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="7ef82-110">Serialisieren von frei *Hand Objekten in* und Abrufen von frei Hand Objekten aus einer ISF-Datei *(Ink serialisiert Format)*</span><span class="sxs-lookup"><span data-stu-id="7ef82-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="7ef82-111">Festlegen von Eingabe Handbüchern für Erkennungs Modul</span><span class="sxs-lookup"><span data-stu-id="7ef82-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="7ef82-112">Verwenden der synchronen und asynchronen Erkennung</span><span class="sxs-lookup"><span data-stu-id="7ef82-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="7ef82-113">Ink-Header</span><span class="sxs-lookup"><span data-stu-id="7ef82-113">Ink Headers</span></span>

<span data-ttu-id="7ef82-114">Fügen Sie zunächst die Header für die Schnittstellen von Tablet PC Automation ein.</span><span class="sxs-lookup"><span data-stu-id="7ef82-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="7ef82-115">Diese werden mit dem Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7ef82-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="7ef82-116">Die Eventsinks. h-Datei definiert die Schnittstellen iinkeventsimpl und iinkrecognitioneventsimpl.</span><span class="sxs-lookup"><span data-stu-id="7ef82-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="7ef82-117">Auflisten der installierten erkenzer</span><span class="sxs-lookup"><span data-stu-id="7ef82-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="7ef82-118">Die loadmenu-Methode der Anwendung füllt das Menü neue Striche erstellen mit den verfügbaren erkenungen auf.</span><span class="sxs-lookup"><span data-stu-id="7ef82-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="7ef82-119">Es wird ein [**inkrecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="7ef82-120">Wenn die [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) -Eigenschaft eines **inkrecognizers** -Objekts nicht leer ist, ist die Erkennung eine *Texterkennung*, und der Wert der [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) -Eigenschaft wird dem Menü hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a><span data-ttu-id="7ef82-121">Erstellen eines frei Hand Sammlers</span><span class="sxs-lookup"><span data-stu-id="7ef82-121">Creating an Ink Collector</span></span>

<span data-ttu-id="7ef82-122">Die OnCreate-Methode der Anwendung erstellt ein [**InkCollector**](inkcollector-class.md) -Objekt, verbindet es mit seiner Ereignis Quelle und aktiviert die frei Hand Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7ef82-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="7ef82-123">Erstellen eines Erkennungs Kontexts</span><span class="sxs-lookup"><span data-stu-id="7ef82-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="7ef82-124">Die Methode "kreaterecocontext" der Anwendung erstellt und initialisiert einen neuen Erkennungs Kontext und richtet die von der zugeordneten Sprache unterstützten Führungslinien ein.</span><span class="sxs-lookup"><span data-stu-id="7ef82-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="7ef82-125">Die " [**kreaterecognizercontext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) "-Methode des [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekts erstellt ein [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) -Objekt für die Sprache.</span><span class="sxs-lookup"><span data-stu-id="7ef82-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="7ef82-126">Bei Bedarf wird der alte Erkennungs Kontext ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="7ef82-127">Der Kontext ist mit seiner Ereignis Quelle verbunden.</span><span class="sxs-lookup"><span data-stu-id="7ef82-127">The context is connected to its event source.</span></span> <span data-ttu-id="7ef82-128">Zum Schluss wird die Eigenschaft " [**Funktionen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) " des erkentekontexts geprüft, welche Führungslinien der Erkennungs Kontext unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="7ef82-129">Erfassen von Strichen und Anzeigen von Erkennungs Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="7ef82-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="7ef82-130">Die OnStroke-Methode der Anwendung aktualisiert die [**inkstriche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des Ink Collector, bricht vorhandene asynchrone Erkennungs Anforderungen ab und erstellt eine Erkennungs Anforderung für den Erkennungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="7ef82-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



<span data-ttu-id="7ef82-131">Die-Methode der Anwendung `OnRecognition` sendet die Ergebnisse der Erkennungs Anforderung an die-Methode des Ausgabe Fensters `UpdateString` .</span><span class="sxs-lookup"><span data-stu-id="7ef82-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="7ef82-132">Löschen von Strichen und Erkennungs Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="7ef82-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="7ef82-133">Die OnClear-Methode der Anwendung löscht alle Striche und Erkennungsergebnisse aus dem [**InkDisp**](inkdisp-class.md) -Objekt und löscht die Fenster.</span><span class="sxs-lookup"><span data-stu-id="7ef82-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="7ef82-134">Die Zuordnung der Erkennungs Kontext mit der [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="7ef82-135">Ändern von Erkennungs Kontext</span><span class="sxs-lookup"><span data-stu-id="7ef82-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="7ef82-136">Die onnewstrokes-Methode der Anwendung wird aufgerufen, wenn der Benutzer im Menü neue Striche erstellen eine Erkennung auswählt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="7ef82-137">Die aktuellen [**inkstriche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) werden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7ef82-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="7ef82-138">Wenn eine andere Spracherkennung ausgewählt wurde, wird ein neuer Erkennungs Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="7ef82-139">Anschließend wird ein neues **inkstrokes** an den neuen Erkennungs Kontext angefügt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



<span data-ttu-id="7ef82-140">Anschließend wird "startnewstrokecollection" aufgerufen, wodurch ein leeres [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) erstellt und an den Erkennungs Kontext angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7ef82-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="7ef82-141">Speichern der Striche-Auflistung für einen Erkennungs Kontext</span><span class="sxs-lookup"><span data-stu-id="7ef82-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="7ef82-142">Die-Methode der Anwendung `SaveStrokeCollection` überprüft, ob ein vorhandener Erkennungs Kontext vorhanden ist, und schließt die Erkennung der aktuellen Striche-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="7ef82-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="7ef82-143">Anschließend wird die Sammlung " [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) " den [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) des Ink-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ef82-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 
