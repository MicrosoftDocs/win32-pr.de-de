---
description: Verwenden Sie die Methoden der IWiaDataTransfer-Schnittstelle, um Daten von einem Windows WIA 1.0-Gerät (Image Acquisition) an eine Anwendung zu übertragen.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Übertragen von Bilddaten in WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e2c1dfce551f105b0df1627f11e9b4ccb7ee8a420e395f3fd0cc1ba932f136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813670"
---
# <a name="transferring-image-data-in-wia-10"></a>Übertragen von Bilddaten in WIA 1.0

> [!Note]  
> In diesem Tutorial wird das Übertragen von Imagedaten in Anwendungen, die Windows XP oder früher ausgeführt werden, verwendet. Informationen zum Übertragen von Bilddaten in Anwendungen, die auf Windows Vista oder höher ausgeführt werden, finden Sie unter Übertragen von [Bilddaten in WIA 2.0.](-wia-transferring-image-data-in-wia2.md)

 

Verwenden Sie die Methoden der [**IWiaDataTransfer-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) um Daten von einem wia 1.0-Gerät (Windows Image Acquisition) an eine Anwendung zu übertragen. Diese Schnittstelle unterstützt ein Shared Memory-Fenster, um Daten aus dem Geräteobjekt an die Anwendung zu übertragen und unnötige Datenkopien während des Marshallings zu vermeiden.

Anwendungen müssen ein Bildelement abfragen, um einen Zeiger auf seine [**IWiaDataTransfer-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) abzurufen, wie im folgenden Codebeispiel dargestellt:


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



Im vorherigen Code wird davon ausgegangen, dass **pWiaItem** ein gültiger Zeiger auf die [**IWiaItem-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ist. Der Aufruf von [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) füllt **pWiaDataTransfer** mit einem Zeiger auf die [**IWiaDataTransfer-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) des Elements, auf das **pWiaItem** verweist.

Die Anwendung legt dann die [STGMEDIUM-Strukturmember](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) fest. Weitere Informationen finden Sie unter STGMEDIUM und [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Wenn Sie einen Dateinamen bereitstellen, sollte er die richtige Dateierweiterung enthalten. WIA 1.0 bietet keine Dateierweiterungen. Wenn das **lpszFileName-Element** von **StgMedium** **NULL** ist, generiert WIA 1.0 einen zufälligen Dateinamen und Pfad für die übertragenen Daten. Verschieben oder kopieren Sie diese Datei, bevor Sie ReleaseStgMedium aufrufen, da diese Funktion die Datei löscht.

Die Anwendung ruft dann die [**IWiaDataTransfer::idtGetData-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) auf, um die Datenübertragung auszuführen:


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



Beim Aufruf von [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)gibt der zweite Parameter einen Zeiger auf die [**IWiaDataCallback-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) an. Anwendungen müssen diese Schnittstelle implementieren, um Rückrufe während Datenübertragungen zu empfangen. Informationen zum Implementieren dieser Schnittstelle finden Sie unter [**IWiaDataCallback::BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

Die Anwendung gibt dann die Zeiger auf die [**IWiaDataTransfer-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) frei und gibt alle in der [STGMEDIUM-Struktur](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) zugeordneten Daten frei.

Die Anwendung kann das Image auch mithilfe von In-Memory-Datenübertragungen anstelle von Dateiübertragungen übertragen. In diesem Fall verwendet die Anwendung die idtGetBandedData-Methode anstelle der idtGetData-Methode.

Hier ist das vollständige Beispiel für die Datenübertragung:


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



 

 
