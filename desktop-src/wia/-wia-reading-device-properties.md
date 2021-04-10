---
description: Anwendungen verwenden die iwiapropertystorage-Schnittstelle eines Geräts, um Geräteeigenschaften zu lesen und zu schreiben. Iwiapropertystorage erbt alle Methoden der IPropertyStorage-Schnittstelle der Component Object Model (com).
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lesen von Geräteeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958965"
---
# <a name="reading-device-properties"></a>Lesen von Geräteeigenschaften

Anwendungen verwenden die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle eines Geräts, um Geräteeigenschaften zu lesen und zu schreiben. **Iwiapropertystorage** erbt alle Methoden der [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)-Schnittstelle der Component Object Model (com).

Zu den Geräteeigenschaften zählen Informationen zu einem Gerät, das die Funktionen und Einstellungen des Geräts beschreibt. Eine Liste dieser Eigenschaften finden Sie unter [Geräteeigenschaften](-wia-device-properties.md).

Unter den Geräteeigenschaften, die mit [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) gelesen werden, handelt es sich um die Geräte-ID, die dann verwendet wird, um ein Windows-Abbild Erfassungsgerät (WIA) zu erstellen. Weitere Informationen finden Sie unter [**iwiadevmgr:: kreatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (oder [**IWiaDevMgr2:: kreatedevice**](-wia-iwiadevmgr2-createdevice.md)).

Im folgenden Beispiel werden die Geräte-ID, der Gerätename und die Geräte Beschreibung aus dem Array mit den Geräteeigenschaften gelesen, und diese Eigenschaften werden in der Konsole ausgegeben.


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



In diesem Beispiel richtet die Anwendung [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Arrays (**PROPSPEC** bzw. **propvar**) zum Speichern von Eigenschafts Informationen ein. Diese Arrays werden im Aufrufen der [IPropertyStorage:: Read Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) -Methode des [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Zeigers **piwiapropstg** als Parameter übergeben. Jedes Element des **PROPSPEC** -Arrays enthält den Typ und den Namen einer Geräte Eigenschaft. Bei der Rückgabe enthält jedes Element des **propvar** den Wert der Geräte Eigenschaft, die durch das entsprechende Element des **PROPSPEC** -Arrays dargestellt wird.

Die Anwendung ruft dann die [IPropertyStorage:: Read Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) -Eigenschaft des [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Zeigers **pwiapropertystorage** auf, um die Eigenschafts Informationen abzurufen.

Das Verfahren zum Lesen und Festlegen von Geräteeigenschaften ist das gleiche wie bei Element Eigenschaften, der einzige Unterschied ist der Typ des WIA-Elements, für das die entsprechenden Methoden aufgerufen werden. Eine Liste der Element Eigenschaften finden Sie unter [Element Eigenschaften](-wia-item-properties.md).

 

 
