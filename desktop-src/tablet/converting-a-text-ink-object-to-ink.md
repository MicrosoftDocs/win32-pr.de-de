---
description: Implementierung der Umstellung von einem Text frei Hand Objekt (Tink) in frei Hand Eingaben.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Umrechnen eines Text frei Hand Objekts in frei Hand Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c7fe4a7847834fffda2df9c4ab94293756cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214300"
---
# <a name="converting-a-text-ink-object-to-ink"></a>Umrechnen eines Text frei Hand Objekts in frei Hand Eingaben

Implementierung der Umstellung von einem Text frei Hand Objekt (Tink) in frei Hand Eingaben.

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>So konvertieren Sie ein Text frei Hand Objekt in frei Hand Eingaben

1.  Verwenden Sie die [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle, um den Inhalt des Text frei Hand Objekts in einen Stream zu schreiben. Das Text frei Hand Objekt verwendet das frei Hand Format, um in den Stream zu schreiben.
2.  Liest den Inhalt des Streams in ein Bytearray ein.
3.  Verwenden Sie die [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) -Methode des [**InkDisp**](inkdisp-class.md) -Objekts, um den Inhalt des Streams in das **InkDisp** -Objekt zu laden.

## <a name="text-ink-object-to-ink-object-example"></a>Beispiel für Text frei Hand Objekt an Ink-Objekt

Das folgende Code Fragment konvertiert ein Text frei Hand Objekt in frei Hand Eingaben.

Zuerst erhält der Code ein Text frei Hand Objekt.


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



Anschließend erstellt der Code einen Zeiger für den Stream, der den Inhalt des Text frei Hand Objekts enthält.


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



Der Code ruft dann die [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle aus dem Text frei Hand Objekt ab.


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



Anschließend wird im Code die [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle verwendet, um den Inhalt des Text frei Hand Objekts in den Stream zu speichern.


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



Anschließend erstellt der Code ein [**InkCollector**](inkcollector-class.md) -Objekt, erstellt ein [**InkDisp**](inkdisp-class.md) -Objekt für den **InkCollector**, fügt den **InkCollector** an das Anwendungsfenster an und aktiviert die frei Hand Auflistung für den **InkCollector**.


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



Anschließend ruft der Code die Größe des Streams ab und erstellt ein sicheres Array, um den Inhalt des Streams zu speichern.


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



Schließlich greift der Code auf das sichere Array zu und verwendet die [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) -Methode des [**InkDisp**](inkdisp-class.md) -Objekts, um die frei Hand Eingaben aus dem Array zu laden.


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 
