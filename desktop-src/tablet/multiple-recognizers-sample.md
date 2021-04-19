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
# <a name="multiple-recognizers-sample"></a>Beispiel für mehrere erkenzer

In diesem Beispiel werden erweiterte Funktionen der für die *Handschrift* Erkennung verwendeten API (Application Programming Interface, API) für die Verwendung von mikrosofttablet-APIs veranschaulicht.

Dies umfasst Folgendes:

-   Auflisten der installierten erkenzer
-   Erstellen eines *Erkennungs Kontexts* mit einer bestimmten Spracherkennung
-   Serialisieren von Erkennungs Ergebnissen mit einer Stroke-Auflistung
-   Organisieren von Stroke Collections in eine benutzerdefinierte Sammlung innerhalb des [**InkDisp**](inkdisp-class.md) -Objekts
-   Serialisieren von frei *Hand Objekten in* und Abrufen von frei Hand Objekten aus einer ISF-Datei *(Ink serialisiert Format)*
-   Festlegen von Eingabe Handbüchern für Erkennungs Modul
-   Verwenden der synchronen und asynchronen Erkennung

## <a name="ink-headers"></a>Ink-Header

Fügen Sie zunächst die Header für die Schnittstellen von Tablet PC Automation ein. Diese werden mit dem Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) installiert.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Die Eventsinks. h-Datei definiert die Schnittstellen iinkeventsimpl und iinkrecognitioneventsimpl.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Auflisten der installierten erkenzer

Die loadmenu-Methode der Anwendung füllt das Menü neue Striche erstellen mit den verfügbaren erkenungen auf. Es wird ein [**inkrecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) erstellt. Wenn die [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) -Eigenschaft eines **inkrecognizers** -Objekts nicht leer ist, ist die Erkennung eine *Texterkennung*, und der Wert der [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) -Eigenschaft wird dem Menü hinzugefügt.


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



## <a name="creating-an-ink-collector"></a>Erstellen eines frei Hand Sammlers

Die OnCreate-Methode der Anwendung erstellt ein [**InkCollector**](inkcollector-class.md) -Objekt, verbindet es mit seiner Ereignis Quelle und aktiviert die frei Hand Auflistung.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Erstellen eines Erkennungs Kontexts

Die Methode "kreaterecocontext" der Anwendung erstellt und initialisiert einen neuen Erkennungs Kontext und richtet die von der zugeordneten Sprache unterstützten Führungslinien ein. Die " [**kreaterecognizercontext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) "-Methode des [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekts erstellt ein [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) -Objekt für die Sprache. Bei Bedarf wird der alte Erkennungs Kontext ersetzt. Der Kontext ist mit seiner Ereignis Quelle verbunden. Zum Schluss wird die Eigenschaft " [**Funktionen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) " des erkentekontexts geprüft, welche Führungslinien der Erkennungs Kontext unterstützt.


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Erfassen von Strichen und Anzeigen von Erkennungs Ergebnissen

Die OnStroke-Methode der Anwendung aktualisiert die [**inkstriche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des Ink Collector, bricht vorhandene asynchrone Erkennungs Anforderungen ab und erstellt eine Erkennungs Anforderung für den Erkennungs Kontext.


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



Die-Methode der Anwendung `OnRecognition` sendet die Ergebnisse der Erkennungs Anforderung an die-Methode des Ausgabe Fensters `UpdateString` .


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Löschen von Strichen und Erkennungs Ergebnissen

Die OnClear-Methode der Anwendung löscht alle Striche und Erkennungsergebnisse aus dem [**InkDisp**](inkdisp-class.md) -Objekt und löscht die Fenster. Die Zuordnung der Erkennungs Kontext mit der [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung wird entfernt.


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



## <a name="changing-recognizer-contexts"></a>Ändern von Erkennungs Kontext

Die onnewstrokes-Methode der Anwendung wird aufgerufen, wenn der Benutzer im Menü neue Striche erstellen eine Erkennung auswählt. Die aktuellen [**inkstriche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) werden gespeichert. Wenn eine andere Spracherkennung ausgewählt wurde, wird ein neuer Erkennungs Kontext erstellt. Anschließend wird ein neues **inkstrokes** an den neuen Erkennungs Kontext angefügt.


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



Anschließend wird "startnewstrokecollection" aufgerufen, wodurch ein leeres [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) erstellt und an den Erkennungs Kontext angefügt wird.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Speichern der Striche-Auflistung für einen Erkennungs Kontext

Die-Methode der Anwendung `SaveStrokeCollection` überprüft, ob ein vorhandener Erkennungs Kontext vorhanden ist, und schließt die Erkennung der aktuellen Striche-Auflistung ab. Anschließend wird die Sammlung " [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) " den [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) des Ink-Objekts hinzugefügt.


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



 

 
