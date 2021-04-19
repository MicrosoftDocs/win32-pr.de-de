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
# <a name="creating-a-device"></a>Erstellen eines Geräts

Sobald eine Anwendung über die Geräte-ID eines bestimmten Geräts verfügt, kann Sie die [**iwiadevmgr:: deatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) -Methode oder die [**IWiaDevMgr2:: deatedevice**](-wia-iwiadevmgr2-createdevice.md)-Methode aufrufen, die eine hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten, die ein Abbild Erstellungs Gerät darstellen, und die auf diesem Gerät enthaltenen Ordner erstellt.

Im folgenden Beispiel aus der Beispielanwendung wiassamp wird eine Funktion implementiert, die eine Geräte-ID als Parameter annimmt. Informationen dazu, wie Sie eine Geräte-ID für ein bestimmtes Gerät abrufen, finden Sie unter [Lesen von Geräteeigenschaften](-wia-reading-device-properties.md).


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



In diesem Beispiel ist **pwiadevmgr** ein Zeiger auf die Schnittstelle [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , und **ppwiadevice** ist eine Variable, die nach dem Aufrufen von [**iwiadevmgr:: anatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (oder zu [**IWiaDevMgr2:: anatedevice**](-wia-iwiadevmgr2-createdevice.md)) die Adresse eines Zeigers auf das Stamm Element der Struktur enthält, das das neu erstellte Gerät darstellt.

 

 



