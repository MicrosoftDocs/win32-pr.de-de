---
title: Von synchronen suchen zurückgegebene Geräte Sammlungen
description: Geräte Sammlungen sind Objekte, die ein oder mehrere Geräte Objekte enthalten. Eine Geräte Sammlung macht die iupnpdevices-Schnittstelle verfügbar, die Methoden und Eigenschaften zum Durchlaufen der Sammlung und extrahieren einzelner Geräte Objekte bereitstellt.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102051"
---
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="473f7-104">Von synchronen suchen zurückgegebene Geräte Sammlungen</span><span class="sxs-lookup"><span data-stu-id="473f7-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="473f7-105">Geräte Sammlungen sind Objekte, die ein oder mehrere Geräte Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="473f7-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="473f7-106">Eine Geräte Sammlung macht die [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Schnittstelle verfügbar, die Methoden und Eigenschaften zum Durchlaufen der Sammlung und extrahieren einzelner Geräte Objekte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="473f7-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="473f7-107">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="473f7-107">VBScript Example</span></span>

<span data-ttu-id="473f7-108">VBScript-Anwendungen können auf die Objekte in der Auflistung auf zwei Arten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="473f7-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="473f7-109">Zuerst können Sie die Elemente sequenziell durchlaufen, indem Sie eine for...</span><span class="sxs-lookup"><span data-stu-id="473f7-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="473f7-110">alle... nächste Schleife, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="473f7-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="473f7-111">In diesem Beispiel wird davon ausgegangen, dass die Geräte Variable mit dem Ergebnis einer vorherigen Suche initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="473f7-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="473f7-112">Die Schleife durchläuft die Geräte Objekte in der Auflistung und weist der Variablen deviceobj den Wert der einzelnen Geräte Objekte zu.</span><span class="sxs-lookup"><span data-stu-id="473f7-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="473f7-113">Der Text der Schleife kann Code enthalten, der das Geräte Objekt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="473f7-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="473f7-114">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="473f7-114">C++ Example</span></span>

<span data-ttu-id="473f7-115">Das folgende Beispiel zeigt den C++-Code, der für den Zugriff auf die Objekte in einer Auflistung von Geräte Objekten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="473f7-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="473f7-116">Die angezeigte Funktion " **traversicollection**" erhält einen Zeiger auf die Schnittstelle [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="473f7-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="473f7-117">Dieser Schnittstellen Zeiger kann von der [**findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) -Methode oder anderen **Find** -Methoden des Device Finder-Objekts zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="473f7-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



<span data-ttu-id="473f7-118">Der erste Schritt besteht darin, mithilfe der Eigenschaft " [**\_ netwenum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) " einen neuen Enumerator für die Auflistung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="473f7-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="473f7-119">Dadurch wird ein Enumerator als [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="473f7-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="473f7-120">Der Beispielcode ruft [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zum Abrufen der [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="473f7-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="473f7-121">Der Beispielcode legt dann den Enumerator auf den Anfang der Auflistung fest, indem die [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="473f7-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="473f7-122">Schließlich ruft der Beispielcode die [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) -Methode auf, um die Auflistung zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="473f7-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="473f7-123">Die Geräte Objekte in der Sammlung sind in **Variant** -Strukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="473f7-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="473f7-124">Diese Strukturen enthalten Zeiger auf [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen für die Geräte Objekte.</span><span class="sxs-lookup"><span data-stu-id="473f7-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="473f7-125">Zum Abrufen der [**iupnpdevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) -Schnittstelle ruft der Beispielcode **QueryInterface** für die **IDispatch** -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="473f7-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 