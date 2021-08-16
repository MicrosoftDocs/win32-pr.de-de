---
description: In diesem Beispiel werden erweiterte Features der MicrosoftTablet-PC-Automatisierungs-API (Application Programming Interface, Anwendungsprogrammierschnittstelle) veranschaulicht, die für die Handschrifterkennung verwendet wird.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Beispiel für mehrere Erkennungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d687f1bddd1f3c57cc482070b8e5826126b6e5b0f716fa3649df01ad6eab30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856549"
---
# <a name="multiple-recognizers-sample"></a>Beispiel für mehrere Erkennungen

In diesem Beispiel werden erweiterte Features der MicrosoftTablet-PC-Automatisierungs-API (Application Programming Interface, Anwendungsprogrammierschnittstelle) veranschaulicht, die für *die Handschrifterkennung* verwendet wird.

Dies umfasst Folgendes:

-   Aufzählen der installierten Erkennungen
-   Erstellen eines *Erkennungskontexts* mit einer bestimmten Spracherkennung
-   Serialisieren von Erkennungsergebnissen mit einer Strichsammlung
-   Organisieren von Strichsammlungen in einer benutzerdefinierten Auflistung im [**InkDisp-Objekt**](inkdisp-class.md)
-   Serialisieren von *Ink-Objekten* in und Abrufen aus einer *ISF-Datei (Ink Serialized Format)*
-   Festlegen von Eingabehandbüchern für die Erkennung
-   Verwenden der synchronen und asynchronen Erkennung

## <a name="ink-headers"></a>Ink-Header

Schließen Sie zunächst die Header für Tablet PC Automation-Schnittstellen ein. Diese werden mit dem Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) installiert.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Die Datei EventSinks.h definiert die Schnittstellen IInkEventsImpl und IInkRecognitionEventsImpl.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Aufzählen der installierten Erkennungen

Die LoadMenu-Methode der Anwendung füllt das Menü Neue Striche erstellen mit den verfügbaren Erkennungen auf. Ein [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) wird erstellt. Wenn die [**Languages-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) eines **InkRecognizers-Objekts** nicht leer ist, ist die Erkennung eine *Texterkennung,* und der Wert der [**Name-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) wird dem Menü hinzugefügt.


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



## <a name="creating-an-ink-collector"></a>Erstellen eines Ink Collectors

Die OnCreate-Methode der Anwendung erstellt ein [**InkCollector-Objekt,**](inkcollector-class.md) verbindet es mit seiner Ereignisquelle und aktiviert die Ink-Sammlung.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Erstellen eines Erkennungskontexts

Die CreateRecoContext-Methode der Anwendung erstellt und initialisiert einen neuen Erkennungskontext und richtet die Leitfäden ein, die von der zugeordneten Sprache unterstützt werden. Die [**CreateRecognizerContext-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) des [**IInkRecognizer-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) erstellt ein [**IInkRecognizerContext2-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) für die Sprache. Bei Bedarf wird der alte Erkennungskontext ersetzt. Der Kontext ist mit seiner Ereignisquelle verbunden. Schließlich wird die [**Capabilities-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) des Erkennungskontexts überprüft, für die vom Erkennungskontext unterstützte Leitfäden unterstützt werden.


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Sammeln von Strichen und Anzeigen von Erkennungsergebnissen

Die OnStroke-Methode der Anwendung aktualisiert die [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des Ink-Collectors, bricht vorhandene asynchrone Erkennungsanforderungen ab und erstellt eine Erkennungsanforderung für den Erkennungskontext.


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



Die -Methode der Anwendung `OnRecognition` sendet die Ergebnisse der Erkennungsanforderung an die -Methode des Ausgabefensters. `UpdateString`


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Löschen von Strichen und Erkennungsergebnissen

Die OnClear-Methode der Anwendung löscht alle Striche und Erkennungsergebnisse aus dem [**InkDisp-Objekt**](inkdisp-class.md) und löscht die Fenster. Die Zuordnung des Erkennungskontexts zu seiner [**InkStrokes-Sammlung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wird entfernt.


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



## <a name="changing-recognizer-contexts"></a>Ändern von Erkennungskontexten

Die OnNewStrokes-Methode der Anwendung wird aufgerufen, wenn der Benutzer im Menü Neue Striche erstellen eine Erkennung auswählt. Die aktuellen [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) werden gespeichert. Wenn eine andere Spracherkennung ausgewählt wurde, wird ein neuer Erkennungskontext erstellt. Anschließend wird ein neues **InkStrokes** an den neuen Erkennungskontext angefügt.


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



Anschließend ruft sie StartNewStrokeCollection auf, wodurch leere [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) erstellt und an den Erkennungskontext angefügt werden.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Speichern der Strichsammlung für einen Erkennungskontext

Die -Methode der Anwendung `SaveStrokeCollection` überprüft auf einen vorhandenen Erkennungskontext und finalisiert die Erkennung der aktuellen Strichauflistung. Anschließend wird die [**Sammlung InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) den [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) des Ink-Objekts hinzugefügt.


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



 

 
