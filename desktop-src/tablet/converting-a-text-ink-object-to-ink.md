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
# <a name="converting-a-text-ink-object-to-ink"></a><span data-ttu-id="b1820-103">Umrechnen eines Text frei Hand Objekts in frei Hand Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1820-103">Converting a Text Ink Object to Ink</span></span>

<span data-ttu-id="b1820-104">Implementierung der Umstellung von einem Text frei Hand Objekt (Tink) in frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b1820-104">Implementation of converting from a text ink object (tInk) to ink.</span></span>

## <a name="to-convert-from-a-text-ink-object-to-ink"></a><span data-ttu-id="b1820-105">So konvertieren Sie ein Text frei Hand Objekt in frei Hand Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1820-105">To convert from a text ink object to ink</span></span>

1.  <span data-ttu-id="b1820-106">Verwenden Sie die [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle, um den Inhalt des Text frei Hand Objekts in einen Stream zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b1820-106">Use the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to write the contents of the text ink object out to a stream.</span></span> <span data-ttu-id="b1820-107">Das Text frei Hand Objekt verwendet das frei Hand Format, um in den Stream zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b1820-107">The text ink object uses ink serialized format to write to the steam.</span></span>
2.  <span data-ttu-id="b1820-108">Liest den Inhalt des Streams in ein Bytearray ein.</span><span class="sxs-lookup"><span data-stu-id="b1820-108">Read the contents of the stream into a BYTE array.</span></span>
3.  <span data-ttu-id="b1820-109">Verwenden Sie die [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) -Methode des [**InkDisp**](inkdisp-class.md) -Objekts, um den Inhalt des Streams in das **InkDisp** -Objekt zu laden.</span><span class="sxs-lookup"><span data-stu-id="b1820-109">Use the [**InkDisp**](inkdisp-class.md) object's [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) method to load the contents of the stream into the **InkDisp** object.</span></span>

## <a name="text-ink-object-to-ink-object-example"></a><span data-ttu-id="b1820-110">Beispiel für Text frei Hand Objekt an Ink-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1820-110">Text Ink Object to Ink Object Example</span></span>

<span data-ttu-id="b1820-111">Das folgende Code Fragment konvertiert ein Text frei Hand Objekt in frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b1820-111">The following code fragment converts a text ink object to ink.</span></span>

<span data-ttu-id="b1820-112">Zuerst erhält der Code ein Text frei Hand Objekt.</span><span class="sxs-lookup"><span data-stu-id="b1820-112">First, the code obtains a text ink object.</span></span>


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



<span data-ttu-id="b1820-113">Anschließend erstellt der Code einen Zeiger für den Stream, der den Inhalt des Text frei Hand Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="b1820-113">Then, the code creates a pointer for the stream that holds the contents of the text ink object.</span></span>


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



<span data-ttu-id="b1820-114">Der Code ruft dann die [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle aus dem Text frei Hand Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="b1820-114">Then, the code obtains the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface from the text ink object.</span></span>


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



<span data-ttu-id="b1820-115">Anschließend wird im Code die [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle verwendet, um den Inhalt des Text frei Hand Objekts in den Stream zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b1820-115">Then, the code uses the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to save the contents of the text ink object to the stream.</span></span>


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



<span data-ttu-id="b1820-116">Anschließend erstellt der Code ein [**InkCollector**](inkcollector-class.md) -Objekt, erstellt ein [**InkDisp**](inkdisp-class.md) -Objekt für den **InkCollector**, fügt den **InkCollector** an das Anwendungsfenster an und aktiviert die frei Hand Auflistung für den **InkCollector**.</span><span class="sxs-lookup"><span data-stu-id="b1820-116">Then, the code creates an [**InkCollector**](inkcollector-class.md) object, creates an [**InkDisp**](inkdisp-class.md) object for the **InkCollector**, attaches the **InkCollector** to the application window, and enables ink collection on the **InkCollector**.</span></span>


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



<span data-ttu-id="b1820-117">Anschließend ruft der Code die Größe des Streams ab und erstellt ein sicheres Array, um den Inhalt des Streams zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b1820-117">Then, the code retrieves the size of the stream and creates a safe array to hold the contents of the stream.</span></span>


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



<span data-ttu-id="b1820-118">Schließlich greift der Code auf das sichere Array zu und verwendet die [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) -Methode des [**InkDisp**](inkdisp-class.md) -Objekts, um die frei Hand Eingaben aus dem Array zu laden.</span><span class="sxs-lookup"><span data-stu-id="b1820-118">Finally, the code accesses the safe array and uses the [**InkDisp**](inkdisp-class.md) object's [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) method to load the ink from the array.</span></span>


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



 

 
