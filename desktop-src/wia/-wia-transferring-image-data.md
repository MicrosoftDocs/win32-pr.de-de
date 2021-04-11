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
# <a name="transferring-image-data-in-wia-10"></a>Übertragen von Bilddaten in WIA 1,0

> [!Note]  
> In diesem Tutorial geht es um das Übertragen von Image Daten in Anwendungen, die unter Windows XP oder früher ausgeführt werden. Informationen zum Übertragen von Bilddaten in Anwendungen, die unter Windows Vista oder höher ausgeführt werden, finden Sie unter über [tragen von Bilddaten in WIA 2,0](-wia-transferring-image-data-in-wia2.md) .

 

Verwenden Sie die Methoden der [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle zum Übertragen von Daten von einem Windows-Abbild Erfassungsgerät (WIA) 1,0 an eine Anwendung. Diese Schnittstelle unterstützt ein frei gegebenes Speicherfenster, um Daten aus dem Geräte Objekt an die Anwendung zu übertragen und unnötige Datenkopien beim Marshalling auszuschließen.

Anwendungen müssen ein Bildelement Abfragen, um einen Zeiger auf seine [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle zu erhalten, wie im folgenden Codebeispiel:


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



Im vorherigen Code wird davon ausgegangen, dass **pwiaitem** ein gültiger Zeiger auf die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle ist. Der [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufrufe füllt **pwiadatatransfer** mit einem Zeiger auf die [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle des Elements, auf das **pwiaitem** verweist.

Die Anwendung legt dann die [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Strukturmember fest. Weitere Informationen finden Sie unter STGMEDIUM und [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Wenn Sie einen Dateinamen angeben, sollte dieser die richtige Dateierweiterung enthalten. WIA 1,0 bietet keine Dateierweiterungen. Wenn das **lpszfilename** -Element von **STGMEDIUM** **null** ist, generiert WIA 1,0 einen zufälligen Dateinamen und einen Pfad für die übertragenen Daten. Verschieben oder kopieren Sie diese Datei vor dem Aufruf von ReleaseStgMedium, da diese Funktion die Datei löscht.

Die Anwendung ruft dann die [**iwiadatatransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) -Methode auf, um die Datenübertragung auszuführen:


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



Beim Aufrufen von [**iwiadatatransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)gibt der zweite Parameter einen Zeiger auf die [**iwiadatacallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) -Schnittstelle an. Anwendungen müssen diese Schnittstelle implementieren, um Rückrufe während der Datenübertragung zu empfangen. Weitere Informationen zum Implementieren dieser Schnittstelle finden Sie unter [**iwiadatacallback:: BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

Die Anwendung gibt dann die Zeiger auf die [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) -Schnittstelle frei und gibt alle Daten frei, die in der [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur zugeordnet sind.

Die Anwendung kann das Image auch mithilfe von Datenübertragungen im Arbeitsspeicher anstelle von Dateiübertragungen übertragen. In diesem Fall verwendet die Anwendung die idtGetBandedData-Methode anstelle der idtGetData-Methode.

Hier ist das Beispiel für die komplette Datenübertragung:


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



 

 
