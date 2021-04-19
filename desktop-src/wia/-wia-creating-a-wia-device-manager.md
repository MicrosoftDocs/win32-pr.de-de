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
# <a name="creating-a-wia-device-manager"></a>Erstellen eines WIA-Device Manager

Der erste Schritt bei der Verwendung der Windows-Abbild Erfassungs Dienste (WIA) ist das Abrufen eines [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -Schnittstellen Zeigers (bei der Programmierung für Windows XP oder früher) oder eines [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstellen Zeigers (wenn Sie für Windows Vista oder höher programmieren). Um dies zu erreichen, müssen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit den entsprechenden Parametern aufrufen. Die Beispielanwendung wiassamp erstellt in einer globalen Funktion einen Geräte-Manager, der durch den folgenden Code implementiert wird:


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



In diesem Beispiel sind CLSID \_ wiadevmgr und IID \_ iwiadevmgr WIA-Konstanten, die die Klassen-ID und die Schnittstellen-ID von [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)darstellen. CLSID \_ WiaDevMgr2 und IID \_ IWiaDevMgr2 sind WIA-Konstanten, die die Klassen-ID und die Schnittstellen-ID von [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)darstellen.

Der Wert für das *dwClsContext* -Argument des [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Aufrufes muss "CLSCTX \_ Local Server" lauten \_ . Ein anderer Servertyp wird nicht unterstützt, und Component Object Model (com) lehnt alle anderen Werte für diesen Parameter ab.

 

 
