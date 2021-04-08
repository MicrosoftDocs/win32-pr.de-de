---
description: 'Verwenden Sie die iwiadevmgr:: enumdevicumfo (oder IWiaDevMgr2:: enumdevicumfo)-Methode, um die auf einem System installierten Windows-Abbild Erfassungsgeräte (WIA) aufzuzählen.'
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Auflisten von System Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959824"
---
# <a name="enumerating-system-devices"></a>Auflisten von System Geräten

Verwenden Sie die [**iwiadevmgr:: enumdevicumfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (oder [**IWiaDevMgr2:: enumdevicumfo**](-wia-iwiadevmgr2-enumdeviceinfo.md))-Methode, um die auf einem System installierten Windows-Abbild Erfassungsgeräte (WIA) aufzuzählen. Diese Methode erstellt ein Enumerationsobjekt für die Eigenschaften der Geräte und gibt einen Zeiger auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle zurück, die das Enumerationsobjekt unterstützt.

Anschließend können Sie die Methoden der [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle verwenden, um für jedes im System installierte Gerät einen [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstellen Zeiger zu erhalten.

Der folgende Code aus der wiassamp-Beispielanwendung veranschaulicht, wie ein Enumerationsobjekt für die Geräte in einem System erstellt und diese Geräte durchlaufen werden:


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



WIA (WIA) \_ \_ \_ ist eine WIA-Konstante, die den einzigen gültigen Wert für diesen Parameter darstellt.

Im Beispiel zeigt der Parameter **pwiadevmgr** nach einem vorherigen [cokreateinstance-Code](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf eine Instanz der [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -Schnittstelle (oder der [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)-Schnittstelle).

Die Anwendung ruft die [**iwiadevmgr:: enumdeviceinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (oder [**IWiaDevMgr2:: enumdeviceinfo**](-wia-iwiadevmgr2-enumdeviceinfo.md))-Methode des [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md))-Zeigers **pwiadevmgr** auf, der **pwiaenumdevinfo** mit der Adresse eines Zeigers auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle füllt.

Wenn der Aufruf erfolgreich ist, ruft die Anwendung dann die [**ienumwia \_ dev \_ Info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) -Methode des [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Zeigers auf. Die **pwiaenumdebug** -Variable stellt sicher, dass die Enumeration am Anfang beginnt.

Wenn dieser Aufruf erfolgreich ist, durchläuft die Anwendung die Geräte im System durch wiederholtes Aufrufen der [**ienumwia \_ dev \_ Info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) -Methode des [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Zeigers **pwiaenumdevinfo** , bis die Methode nicht mehr S OK zurückgibt \_ , was darauf hinweist, dass die Enumeration abgeschlossen ist.

Jeder **pwiaenumdevinfo->Next-Befehl** füllt **pwiapropertystorage** mit einem Zeiger auf die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle auf, die Eigenschafts Informationen für ein bestimmtes Gerät enthält.

 

 
