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
# <a name="enumerating-system-devices"></a><span data-ttu-id="259f3-103">Auflisten von System Geräten</span><span class="sxs-lookup"><span data-stu-id="259f3-103">Enumerating System Devices</span></span>

<span data-ttu-id="259f3-104">Verwenden Sie die [**iwiadevmgr:: enumdevicumfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (oder [**IWiaDevMgr2:: enumdevicumfo**](-wia-iwiadevmgr2-enumdeviceinfo.md))-Methode, um die auf einem System installierten Windows-Abbild Erfassungsgeräte (WIA) aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="259f3-104">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method to enumerate the Windows Image Acquisition (WIA) devices installed on a system.</span></span> <span data-ttu-id="259f3-105">Diese Methode erstellt ein Enumerationsobjekt für die Eigenschaften der Geräte und gibt einen Zeiger auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle zurück, die das Enumerationsobjekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="259f3-105">This method creates an enumeration object for the properties of the devices, and returns a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface that the enumeration object supports.</span></span>

<span data-ttu-id="259f3-106">Anschließend können Sie die Methoden der [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle verwenden, um für jedes im System installierte Gerät einen [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="259f3-106">You can then use the methods of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointer for each device installed on the system.</span></span>

<span data-ttu-id="259f3-107">Der folgende Code aus der wiassamp-Beispielanwendung veranschaulicht, wie ein Enumerationsobjekt für die Geräte in einem System erstellt und diese Geräte durchlaufen werden:</span><span class="sxs-lookup"><span data-stu-id="259f3-107">The following code from the WiaSSamp sample application demonstrates how to create an enumeration object for the devices on a system and iterate through those devices:</span></span>


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



<span data-ttu-id="259f3-108">WIA (WIA) \_ \_ \_ ist eine WIA-Konstante, die den einzigen gültigen Wert für diesen Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="259f3-108">WIA\_DEVINFO\_ENUM\_LOCAL is a WIA constant that represents the only valid value for this parameter.</span></span>

<span data-ttu-id="259f3-109">Im Beispiel zeigt der Parameter **pwiadevmgr** nach einem vorherigen [cokreateinstance-Code](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf eine Instanz der [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -Schnittstelle (oder der [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)-Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="259f3-109">In the example, the parameter **pWiaDevMgr** points to an instance of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface after a previous call to [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="259f3-110">Die Anwendung ruft die [**iwiadevmgr:: enumdeviceinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (oder [**IWiaDevMgr2:: enumdeviceinfo**](-wia-iwiadevmgr2-enumdeviceinfo.md))-Methode des [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md))-Zeigers **pwiadevmgr** auf, der **pwiaenumdevinfo** mit der Adresse eines Zeigers auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle füllt.</span><span class="sxs-lookup"><span data-stu-id="259f3-110">The application calls the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) pointer **pWiaDevMgr** that fills **pWiaEnumDevInfo** with the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

<span data-ttu-id="259f3-111">Wenn der Aufruf erfolgreich ist, ruft die Anwendung dann die [**ienumwia \_ dev \_ Info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) -Methode des [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Zeigers auf.</span><span class="sxs-lookup"><span data-stu-id="259f3-111">If the call succeeds, the application then calls the [**IEnumWIA\_DEV\_INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer.</span></span> <span data-ttu-id="259f3-112">Die **pwiaenumdebug** -Variable stellt sicher, dass die Enumeration am Anfang beginnt.</span><span class="sxs-lookup"><span data-stu-id="259f3-112">The **pWiaEnumDevInfo** variable ensures that the enumeration starts at the beginning.</span></span>

<span data-ttu-id="259f3-113">Wenn dieser Aufruf erfolgreich ist, durchläuft die Anwendung die Geräte im System durch wiederholtes Aufrufen der [**ienumwia \_ dev \_ Info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) -Methode des [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Zeigers **pwiaenumdevinfo** , bis die Methode nicht mehr S OK zurückgibt \_ , was darauf hinweist, dass die Enumeration abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="259f3-113">If this call succeeds, the application iterates through the devices on the system by repeatedly calling the [**IEnumWIA\_DEV\_INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer **pWiaEnumDevInfo** until the method no longer returns S\_OK, indicating that the enumeration is complete.</span></span>

<span data-ttu-id="259f3-114">Jeder **pwiaenumdevinfo->Next-Befehl** füllt **pwiapropertystorage** mit einem Zeiger auf die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle auf, die Eigenschafts Informationen für ein bestimmtes Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="259f3-114">Each call to **pWiaEnumDevInfo->Next** fills **pWiaPropertyStorage** with a pointer to the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface that contains property information for a specific device.</span></span>

 

 
