---
description: Verwenden Sie die Methoden der iwiadatatransfer-Schnittstelle zum Übertragen von Daten von einem Windows-Abbild Erfassungsgerät (WIA) 1,0 an eine Anwendung.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Übertragen von Bilddaten in WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00fc7ff76576b6c140358f9af3a0f9d17d4b180e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129396"
---
# <a name="transferring-image-data-in-wia-10"></a><span data-ttu-id="d4ab7-103">Übertragen von Bilddaten in WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="d4ab7-103">Transferring Image Data in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="d4ab7-104">In diesem Tutorial geht es um das Übertragen von Image Daten in Anwendungen, die unter Windows XP oder früher ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-104">This tutorial is about transferring image data in applications that will run Windows XP or earlier.</span></span> <span data-ttu-id="d4ab7-105">Informationen zum Übertragen von Bilddaten in Anwendungen, die unter Windows Vista oder höher ausgeführt werden, finden Sie unter über [tragen von Bilddaten in WIA 2,0](-wia-transferring-image-data-in-wia2.md) .</span><span class="sxs-lookup"><span data-stu-id="d4ab7-105">See [Transferring Image Data in WIA 2.0](-wia-transferring-image-data-in-wia2.md) for information about transferring image data in applications that will run on Windows Vista or later.</span></span>

 

<span data-ttu-id="d4ab7-106">Verwenden Sie die Methoden der [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle zum Übertragen von Daten von einem Windows-Abbild Erfassungsgerät (WIA) 1,0 an eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-106">Use the methods of the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface to transfer data from a Windows Image Acquisition (WIA) 1.0 device to an application.</span></span> <span data-ttu-id="d4ab7-107">Diese Schnittstelle unterstützt ein frei gegebenes Speicherfenster, um Daten aus dem Geräte Objekt an die Anwendung zu übertragen und unnötige Datenkopien beim Marshalling auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-107">This interface supports a shared memory window to transfer data from the device object to the application and eliminate unnecessary data copies during marshalling.</span></span>

<span data-ttu-id="d4ab7-108">Anwendungen müssen ein Bildelement Abfragen, um einen Zeiger auf seine [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle zu erhalten, wie im folgenden Codebeispiel:</span><span class="sxs-lookup"><span data-stu-id="d4ab7-108">Applications must query an image item to obtain a pointer to its [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface, as in the following code sample:</span></span>


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



<span data-ttu-id="d4ab7-109">Im vorherigen Code wird davon ausgegangen, dass **pwiaitem** ein gültiger Zeiger auf die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-109">In the previous code, it is assumed that **pWiaItem** is a valid pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface.</span></span> <span data-ttu-id="d4ab7-110">Der [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufrufe füllt **pwiadatatransfer** mit einem Zeiger auf die [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle des Elements, auf das **pwiaitem** verweist.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-110">The call to [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fills **pWiaDataTransfer** with a pointer to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface of the item referred to by **pWiaItem**.</span></span>

<span data-ttu-id="d4ab7-111">Die Anwendung legt dann die [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Strukturmember fest.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-111">The application then sets the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure members.</span></span> <span data-ttu-id="d4ab7-112">Weitere Informationen finden Sie unter STGMEDIUM und [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span><span class="sxs-lookup"><span data-stu-id="d4ab7-112">For information, see STGMEDIUM and [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span></span>


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



<span data-ttu-id="d4ab7-113">Wenn Sie einen Dateinamen angeben, sollte dieser die richtige Dateierweiterung enthalten. WIA 1,0 bietet keine Dateierweiterungen.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-113">If you supply a filename, it should include the proper file extension; WIA 1.0 does not provide file extensions.</span></span> <span data-ttu-id="d4ab7-114">Wenn das **lpszfilename** -Element von **STGMEDIUM** **null** ist, generiert WIA 1,0 einen zufälligen Dateinamen und einen Pfad für die übertragenen Daten.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-114">If the **lpszFileName** member of **StgMedium** is **NULL**, WIA 1.0 generates a random file name and path for the transferred data.</span></span> <span data-ttu-id="d4ab7-115">Verschieben oder kopieren Sie diese Datei vor dem Aufruf von ReleaseStgMedium, da diese Funktion die Datei löscht.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-115">Move or copy this file before calling ReleaseStgMedium, because this function will delete the file.</span></span>

<span data-ttu-id="d4ab7-116">Die Anwendung ruft dann die [**iwiadatatransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) -Methode auf, um die Datenübertragung auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d4ab7-116">The application then calls the [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) method to run the data transfer:</span></span>


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



<span data-ttu-id="d4ab7-117">Beim Aufrufen von [**iwiadatatransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)gibt der zweite Parameter einen Zeiger auf die [**iwiadatacallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) -Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-117">In the call to [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), the second parameter specifies a pointer to the [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) interface.</span></span> <span data-ttu-id="d4ab7-118">Anwendungen müssen diese Schnittstelle implementieren, um Rückrufe während der Datenübertragung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-118">Applications must implement this interface to receive callbacks during data transfers.</span></span> <span data-ttu-id="d4ab7-119">Weitere Informationen zum Implementieren dieser Schnittstelle finden Sie unter [**iwiadatacallback:: BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="d4ab7-119">For information about implementing this interface, see [**IWiaDataCallback::BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

<span data-ttu-id="d4ab7-120">Die Anwendung gibt dann die Zeiger auf die [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle frei und gibt alle Daten frei, die in der [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-120">The application then releases the pointers to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface and frees any data allocated in the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure.</span></span>

<span data-ttu-id="d4ab7-121">Die Anwendung kann das Image auch mithilfe von Datenübertragungen im Arbeitsspeicher anstelle von Dateiübertragungen übertragen.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-121">The application can also transfer the image using in-memory data transfers instead of file transfers.</span></span> <span data-ttu-id="d4ab7-122">In diesem Fall verwendet die Anwendung die idtGetBandedData-Methode anstelle der idtGetData-Methode.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-122">In this case, the application uses the idtGetBandedData method in place of the idtGetData method.</span></span>

<span data-ttu-id="d4ab7-123">Hier ist das Beispiel für die komplette Datenübertragung:</span><span class="sxs-lookup"><span data-stu-id="d4ab7-123">Here is the complete data transfer sample:</span></span>


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 
