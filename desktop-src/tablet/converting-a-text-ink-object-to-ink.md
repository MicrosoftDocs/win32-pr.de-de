---
description: Implementierung der Konvertierung von einem Freihandobjekt (tInk) in Freihand.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Konvertieren eines Text-Ink-Objekts in eine Ink-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef543fda3ed53123e99ee042aed67af9cedfef3533ae47bc40d8dd284a73675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941160"
---
# <a name="converting-a-text-ink-object-to-ink"></a>Konvertieren eines Text-Ink-Objekts in eine Ink-Datei

Implementierung der Konvertierung von einem Freihandobjekt (tInk) in Freihand.

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>So konvertieren Sie ein Text-Ink-Objekt in eine Ink-Objekt

1.  Verwenden Sie die [IPersistStream-Schnittstelle,](/windows/win32/api/objidl/nn-objidl-ipersiststream) um den Inhalt des Freihandtextobjekts in einen Stream zu schreiben. Das Text-Ink-Objekt verwendet das serialisierte Format von Ink, um in den "steam" zu schreiben.
2.  Liest den Inhalt des Streams in ein BYTE-Array.
3.  Verwenden Sie die [**Load-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) des [**InkDisp-Objekts,**](inkdisp-class.md) um den Inhalt des Streams in das **InkDisp-Objekt** zu laden.

## <a name="text-ink-object-to-ink-object-example"></a>Beispiel: Text-Ink-Objekt in Ink-Objekt

Das folgende Codefragment konvertiert ein Text-Ink-Objekt in Ink.

Zunächst ruft der Code ein Text-Ink-Objekt ab.


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



Anschließend erstellt der Code einen Zeiger für den Stream, der den Inhalt des Textink-Objekts enthält.


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



Anschließend ruft der Code die [IPersistStream-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersiststream) aus dem Freihandtextobjekt ab.


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



Anschließend verwendet der Code die [IPersistStream-Schnittstelle,](/windows/win32/api/objidl/nn-objidl-ipersiststream) um den Inhalt des Freihandtextobjekts im Stream zu speichern.


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



Anschließend erstellt der Code ein [**InkCollector-Objekt,**](inkcollector-class.md) erstellt ein [**InkDisp-Objekt**](inkdisp-class.md) für **inkCollector,** fügt das **InkCollector-Objekt** an das Anwendungsfenster an und aktiviert die **InkCollector-Auflistung auf dem InkCollector.**


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



Anschließend ruft der Code die Größe des Streams ab und erstellt ein sicheres Array, das den Inhalt des Streams enthält.


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



Schließlich greift der Code auf das sichere Array zu und verwendet die [**Load-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) des [**InkDisp-Objekts,**](inkdisp-class.md) um die Ink-Ink aus dem Array zu laden.


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



 

 
