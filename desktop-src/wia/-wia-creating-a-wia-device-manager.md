---
description: Der erste Schritt bei der Verwendung der Windows-Abbild Erfassungs Dienste (WIA) ist das Abrufen eines iwiadevmgr-Schnittstellen Zeigers (bei der Programmierung für Windows XP oder früher) oder eines IWiaDevMgr2-Schnittstellen Zeigers (wenn Sie für Windows Vista oder höher programmieren).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Erstellen eines WIA-Device Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348621"
---
# <a name="creating-a-wia-device-manager"></a><span data-ttu-id="325cb-103">Erstellen eines WIA-Device Manager</span><span class="sxs-lookup"><span data-stu-id="325cb-103">Creating a WIA Device Manager</span></span>

<span data-ttu-id="325cb-104">Der erste Schritt bei der Verwendung der Windows-Abbild Erfassungs Dienste (WIA) ist das Abrufen eines [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -Schnittstellen Zeigers (bei der Programmierung für Windows XP oder früher) oder eines [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstellen Zeigers (wenn Sie für Windows Vista oder höher programmieren).</span><span class="sxs-lookup"><span data-stu-id="325cb-104">The first step in using Windows Image Acquisition (WIA) services is to obtain an [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) interface pointer (if you are programming for Windows XP or earlier) or an [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface pointer (if you are programming for Windows Vista or later).</span></span> <span data-ttu-id="325cb-105">Um dies zu erreichen, müssen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit den entsprechenden Parametern aufrufen.</span><span class="sxs-lookup"><span data-stu-id="325cb-105">To do this, call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the appropriate parameters.</span></span> <span data-ttu-id="325cb-106">Die Beispielanwendung wiassamp erstellt in einer globalen Funktion einen Geräte-Manager, der durch den folgenden Code implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="325cb-106">The sample application WiaSSamp creates a device manager within a global function implemented by the following code:</span></span>


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



<span data-ttu-id="325cb-107">In diesem Beispiel sind CLSID \_ wiadevmgr und IID \_ iwiadevmgr WIA-Konstanten, die die Klassen-ID und die Schnittstellen-ID von [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)darstellen.</span><span class="sxs-lookup"><span data-stu-id="325cb-107">In this example, CLSID\_WiaDevMgr and IID\_IWiaDevMgr are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), respectively.</span></span> <span data-ttu-id="325cb-108">CLSID \_ WiaDevMgr2 und IID \_ IWiaDevMgr2 sind WIA-Konstanten, die die Klassen-ID und die Schnittstellen-ID von [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)darstellen.</span><span class="sxs-lookup"><span data-stu-id="325cb-108">CLSID\_WiaDevMgr2 and IID\_IWiaDevMgr2 are WIA constants that represent the class ID and the interface ID of [**IWiaDevMgr2**](-wia-iwiadevmgr2.md), respectively.</span></span>

<span data-ttu-id="325cb-109">Der Wert für das *dwClsContext* -Argument des [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Aufrufes muss "CLSCTX \_ Local Server" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="325cb-109">The value for the *dwClsContext* argument of the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call must be CLSCTX\_LOCAL\_SERVER.</span></span> <span data-ttu-id="325cb-110">Ein anderer Servertyp wird nicht unterstützt, und Component Object Model (com) lehnt alle anderen Werte für diesen Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="325cb-110">No other server type is supported, and Component Object Model (COM) rejects any other value for this parameter.</span></span>

 

 
