---
description: Sobald eine Anwendung über die Geräte-ID eines bestimmten Geräts verfügt, kann sie die IWiaDevMgr::CreateDevice oder IWiaDevMgr2::CreateDevicemethod aufrufen, wodurch eine hierarchische Struktur von IWiaItem- oder IWiaItem2-Objekten erstellt wird, die ein Bildverarbeitungsgerät und den Bildscanbereich sowie die auf diesem Gerät enthaltenen Ordner darstellen.
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Erstellen eines Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6319e493c6b99e1f23d8f4ccb9be1e10628fae45e8d4ba7df0aa8112be39dba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965899"
---
# <a name="creating-a-device"></a>Erstellen eines Geräts

Sobald eine Anwendung über die Geräte-ID eines bestimmten Geräts verfügt, kann sie die [**IWiaDevMgr::CreateDevice-**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) oder [**IWiaDevMgr2::CreateDevice-Methode**](-wia-iwiadevmgr2-createdevice.md)aufrufen, die eine hierarchische Struktur von [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) erstellt, die ein Bildverarbeitungsgerät und den Bildscan-Bereich sowie die auf diesem Gerät enthaltenen Ordner darstellen.

Das folgende Beispiel aus der Beispielanwendung WiaSSamp implementiert eine Funktion, die eine Geräte-ID als Parameter akzeptiert. Informationen zum Abrufen einer Geräte-ID für ein bestimmtes Gerät finden Sie unter [Lesen von Geräteeigenschaften.](-wia-reading-device-properties.md)


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



In diesem Beispiel ist **pWiaDevMgr** ein Zeiger auf die [**IWiaDevMgr-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) oder [**IWiaDevMgr2-Schnittstelle,**](-wia-iwiadevmgr2.md) und **ppWiaDevice** ist eine Variable, die nach dem Aufruf von [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (oder [**IWiaDevMgr2::CreateDevice)**](-wia-iwiadevmgr2-createdevice.md)die Adresse eines Zeigers auf das Stammelement der Struktur enthält, das das neu erstellte Gerät darstellt.

 

 



