---
description: 'Sobald eine Anwendung über die Geräte-ID eines bestimmten Geräts verfügt, kann Sie die iwiadevmgr:: anatedevice-oder IWiaDevMgr2:: deatedevicemethod-Methode aufrufen, die eine hierarchische Struktur von iwiaitem-oder IWiaItem2-Objekten, die ein Abbild Erstellungs Gerät darstellen, und die auf diesem Gerät enthaltenen Ordner erstellt.'
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Erstellen eines Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349238"
---
# <a name="creating-a-device"></a><span data-ttu-id="f3bfd-103">Erstellen eines Geräts</span><span class="sxs-lookup"><span data-stu-id="f3bfd-103">Creating a Device</span></span>

<span data-ttu-id="f3bfd-104">Sobald eine Anwendung über die Geräte-ID eines bestimmten Geräts verfügt, kann Sie die [**iwiadevmgr:: deatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) -Methode oder die [**IWiaDevMgr2:: deatedevice**](-wia-iwiadevmgr2-createdevice.md)-Methode aufrufen, die eine hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten, die ein Abbild Erstellungs Gerät darstellen, und die auf diesem Gerät enthaltenen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3bfd-104">Once an application has the device ID of a given device, it can call the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)method, which creates a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects that represent an imaging device and the image scanning beds, and folders contained on that device.</span></span>

<span data-ttu-id="f3bfd-105">Im folgenden Beispiel aus der Beispielanwendung wiassamp wird eine Funktion implementiert, die eine Geräte-ID als Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="f3bfd-105">The following example from the sample application WiaSSamp implements a function that takes a device ID as a parameter.</span></span> <span data-ttu-id="f3bfd-106">Informationen dazu, wie Sie eine Geräte-ID für ein bestimmtes Gerät abrufen, finden Sie unter [Lesen von Geräteeigenschaften](-wia-reading-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f3bfd-106">For information about how to obtain a device ID for a particular device, see [Reading Device Properties](-wia-reading-device-properties.md).</span></span>


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



<span data-ttu-id="f3bfd-107">In diesem Beispiel ist **pwiadevmgr** ein Zeiger auf die Schnittstelle [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , und **ppwiadevice** ist eine Variable, die nach dem Aufrufen von [**iwiadevmgr:: anatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (oder zu [**IWiaDevMgr2:: anatedevice**](-wia-iwiadevmgr2-createdevice.md)) die Adresse eines Zeigers auf das Stamm Element der Struktur enthält, das das neu erstellte Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3bfd-107">In this example, **pWiaDevMgr** is a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface, and **ppWiaDevice** is a variable that, after the call to [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or to [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contains the address of a pointer to the root item of the tree that represents the newly created device.</span></span>

 

 



