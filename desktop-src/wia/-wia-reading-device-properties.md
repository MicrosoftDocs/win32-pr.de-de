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
# <a name="reading-device-properties"></a><span data-ttu-id="477c6-104">Lesen von Geräteeigenschaften</span><span class="sxs-lookup"><span data-stu-id="477c6-104">Reading Device Properties</span></span>

<span data-ttu-id="477c6-105">Anwendungen verwenden die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle eines Geräts, um Geräteeigenschaften zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="477c6-105">Applications use a device's [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to read and write device properties.</span></span> <span data-ttu-id="477c6-106">**Iwiapropertystorage** erbt alle Methoden der [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)-Schnittstelle der Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="477c6-106">**IWiaPropertyStorage** inherits all of the methods of the Component Object Model (COM) interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span></span>

<span data-ttu-id="477c6-107">Zu den Geräteeigenschaften zählen Informationen zu einem Gerät, das die Funktionen und Einstellungen des Geräts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="477c6-107">Device properties include information about a device that describe the device's capabilities and settings.</span></span> <span data-ttu-id="477c6-108">Eine Liste dieser Eigenschaften finden Sie unter [Geräteeigenschaften](-wia-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="477c6-108">For a list of these properties, see [Device Properties](-wia-device-properties.md).</span></span>

<span data-ttu-id="477c6-109">Unter den Geräteeigenschaften, die mit [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) gelesen werden, handelt es sich um die Geräte-ID, die dann verwendet wird, um ein Windows-Abbild Erfassungsgerät (WIA) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="477c6-109">Among the device properties that are read using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) is the device ID, that is then used to create a Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="477c6-110">Weitere Informationen finden Sie unter [**iwiadevmgr:: kreatedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (oder [**IWiaDevMgr2:: kreatedevice**](-wia-iwiadevmgr2-createdevice.md)).</span><span class="sxs-lookup"><span data-stu-id="477c6-110">For more information, see [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span></span>

<span data-ttu-id="477c6-111">Im folgenden Beispiel werden die Geräte-ID, der Gerätename und die Geräte Beschreibung aus dem Array mit den Geräteeigenschaften gelesen, und diese Eigenschaften werden in der Konsole ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="477c6-111">The following example reads the device ID, the device name, and the device description from the array of device properties, and prints these properties to the console.</span></span>


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



<span data-ttu-id="477c6-112">In diesem Beispiel richtet die Anwendung [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Arrays (**PROPSPEC** bzw. **propvar**) zum Speichern von Eigenschafts Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="477c6-112">In this example, the application sets up [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) arrays (**PropSpec** and **PropVar**, respectively) to hold property information.</span></span> <span data-ttu-id="477c6-113">Diese Arrays werden im Aufrufen der [IPropertyStorage:: Read Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) -Methode des [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Zeigers **piwiapropstg** als Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="477c6-113">These arrays are passed as parameters in the call to [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) method of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pIWiaPropStg**.</span></span> <span data-ttu-id="477c6-114">Jedes Element des **PROPSPEC** -Arrays enthält den Typ und den Namen einer Geräte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="477c6-114">Each element of the **PropSpec** array contains the type and name of a device property.</span></span> <span data-ttu-id="477c6-115">Bei der Rückgabe enthält jedes Element des **propvar** den Wert der Geräte Eigenschaft, die durch das entsprechende Element des **PROPSPEC** -Arrays dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="477c6-115">Upon return, each element of the **PropVar** contains the value of the device property represented by the corresponding element of the **PropSpec** array.</span></span>

<span data-ttu-id="477c6-116">Die Anwendung ruft dann die [IPropertyStorage:: Read Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) -Eigenschaft des [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Zeigers **pwiapropertystorage** auf, um die Eigenschafts Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="477c6-116">The application then calls [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) property of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pWiaPropertyStorage** to retrieve the property information.</span></span>

<span data-ttu-id="477c6-117">Das Verfahren zum Lesen und Festlegen von Geräteeigenschaften ist das gleiche wie bei Element Eigenschaften, der einzige Unterschied ist der Typ des WIA-Elements, für das die entsprechenden Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="477c6-117">The technique used to read and set device properties is the same as that for item properties, the only difference is the type of the WIA item on which you call the appropriate methods.</span></span> <span data-ttu-id="477c6-118">Eine Liste der Element Eigenschaften finden Sie unter [Element Eigenschaften](-wia-item-properties.md).</span><span class="sxs-lookup"><span data-stu-id="477c6-118">For a list of item properties, see [Item Properties](-wia-item-properties.md).</span></span>

 

 
