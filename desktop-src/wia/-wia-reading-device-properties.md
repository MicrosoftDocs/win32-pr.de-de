---
description: Anwendungen verwenden die IWiaPropertyStorage-Schnittstelle eines Geräts, um Geräteeigenschaften zu lesen und zu schreiben. IWiaPropertyStorage erbt alle Methoden der Component Object Model-Schnittstelle (COM) IPropertyStorage.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lesen von Geräteeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf102fb2ade1a13b648e13f56f7f999dd35c41f721ac20d72914219c98311505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669260"
---
# <a name="reading-device-properties"></a>Lesen von Geräteeigenschaften

Anwendungen verwenden die [**IWiaPropertyStorage-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) eines Geräts, um Geräteeigenschaften zu lesen und zu schreiben. **IWiaPropertyStorage** erbt alle Methoden der Component Object Model-Schnittstelle (COM) [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).

Geräteeigenschaften enthalten Informationen zu einem Gerät, die die Funktionen und Einstellungen des Geräts beschreiben. Eine Liste dieser Eigenschaften finden Sie unter [Geräteeigenschaften.](-wia-device-properties.md)

Zu den Geräteeigenschaften, die mithilfe von [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) gelesen werden, gehört die Geräte-ID, die dann zum Erstellen eines WIA-Geräts (Windows Image Acquisition) verwendet wird. Weitere Informationen finden Sie unter [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (oder [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).

Im folgenden Beispiel werden die Geräte-ID, der Gerätename und die Gerätebeschreibung aus dem Array der Geräteeigenschaften gelesen und in der Konsole ausgegeben.


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



In diesem Beispiel richtet die Anwendung [PROPVARIANT-Arrays](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**PropSpec** bzw. **PropVar)** ein, um Eigenschaftsinformationen zu speichern. Diese Arrays werden als Parameter im Aufruf der [IPropertyStorage::ReadMultiple-Methode](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) des [**IWiaPropertyStorage-Zeigers**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg übergeben.** Jedes Element des **PropSpec-Arrays** enthält den Typ und Namen einer Geräteeigenschaft. Bei der Rückgabe enthält jedes Element von **PropVar** den Wert der Geräteeigenschaft, die durch das entsprechende Element des **PropSpec-Arrays dargestellt** wird.

Die Anwendung ruft dann die [IPropertyStorage::ReadMultiple-Eigenschaft](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) des [**IWiaPropertyStorage-Zeigers**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pWiaPropertyStorage** auf, um die Eigenschafteninformationen abzurufen.

Das Verfahren zum Lesen und Festlegen von Geräteeigenschaften ist dasselbe wie bei Elementeigenschaften. Der einzige Unterschied besteht im Typ des WIA-Elements, für das Sie die entsprechenden Methoden aufrufen. Eine Liste der Elementeigenschaften finden Sie unter [Elementeigenschaften](-wia-item-properties.md).

 

 
