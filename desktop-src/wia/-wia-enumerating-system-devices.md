---
description: Verwenden Sie die IWiaDevMgr::EnumDeviceInfo-Methode (oder IWiaDevMgr2::EnumDeviceInfo), um die auf einem System installierten WIA-Geräte (Windows Image Acquisition) aufzulisten.
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Aufzählen von Systemgeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b6587d88b2836e057f0b6d7e31bd7f22d79c6220c51b407b621370d8524b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814260"
---
# <a name="enumerating-system-devices"></a>Aufzählen von Systemgeräten

Verwenden Sie die [**Methode IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (oder [**IWiaDevMgr2::EnumDeviceInfo),**](-wia-iwiadevmgr2-enumdeviceinfo.md)um die auf einem System installierten WIA-Geräte (Windows Image Acquisition) aufzulisten. Diese Methode erstellt ein Enumerationsobjekt für die Eigenschaften der Geräte und gibt einen Zeiger auf die [**IEnumWIA \_ DEV \_ INFO-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) zurück, die das Enumerationsobjekt unterstützt.

Anschließend können Sie die Methoden der [**IEnumWIA \_ DEV \_ INFO-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) verwenden, um einen [**IWiaPropertyStorage-Schnittstellenzeiger**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) für jedes auf dem System installierte Gerät abzurufen.

Der folgende Code aus der WiaSSamp-Beispielanwendung veranschaulicht, wie Sie ein Enumerationsobjekt für die Geräte auf einem System erstellen und diese Geräte durchlaufen:


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



WIA \_ DEVINFO \_ ENUM \_ LOCAL ist eine WIA-Konstante, die den einzigen gültigen Wert für diesen Parameter darstellt.

Im Beispiel zeigt der **Parameter pWiaDevMgr** nach einem vorherigen Aufruf von [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf eine Instanz der [**Schnittstelle IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2).**](-wia-iwiadevmgr2.md)

Die Anwendung ruft die [**IWiaDevMgr::EnumDeviceInfo-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (oder [**IWiaDevMgr2::EnumDeviceInfo)**](-wia-iwiadevmgr2-enumdeviceinfo.md)des [**IWiaDevMgr-Zeigers**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2)**](-wia-iwiadevmgr2.md) **pWiaDevMgr** auf, der **pWiaEnumDevInfo** mit der Adresse eines Zeigers auf die [**IEnumWIA \_ DEV \_ INFO-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) füllt.

Wenn der Aufruf erfolgreich ist, ruft die Anwendung die [**IEnumWIA \_ DEV \_ INFO::Reset-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) des [**IEnumWIA \_ DEV \_ INFO-Zeigers**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) auf. Die **Variable pWiaEnumDevInfo** stellt sicher, dass die Enumeration am Anfang beginnt.

Wenn dieser Aufruf erfolgreich ist, durchläuft die Anwendung die Geräte im System, indem sie wiederholt die [**IEnumWIA \_ DEV \_ INFO::Next-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) des [**IEnumWIA \_ DEV \_ INFO-Zeigers**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** aufruft, bis die Methode S OK nicht mehr zurückgibt, \_ was angibt, dass die Enumeration abgeschlossen ist.

Jeder Aufruf von **pWiaEnumDevInfo->Next** füllt **pWiaPropertyStorage** mit einem Zeiger auf die [**IWiaPropertyStorage-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) aus, die Eigenschafteninformationen für ein bestimmtes Gerät enthält.

 

 
