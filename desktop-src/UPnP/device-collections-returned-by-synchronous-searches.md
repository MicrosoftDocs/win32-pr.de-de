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
# <a name="device-collections-returned-by-synchronous-searches"></a>Von synchronen suchen zurückgegebene Geräte Sammlungen

Geräte Sammlungen sind Objekte, die ein oder mehrere Geräte Objekte enthalten. Eine Geräte Sammlung macht die [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Schnittstelle verfügbar, die Methoden und Eigenschaften zum Durchlaufen der Sammlung und extrahieren einzelner Geräte Objekte bereitstellt.

## <a name="vbscript-example"></a>VBScript-Beispiel

VBScript-Anwendungen können auf die Objekte in der Auflistung auf zwei Arten zugreifen. Zuerst können Sie die Elemente sequenziell durchlaufen, indem Sie eine for... alle... nächste Schleife, wie im folgenden Beispiel gezeigt:


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



In diesem Beispiel wird davon ausgegangen, dass die Geräte Variable mit dem Ergebnis einer vorherigen Suche initialisiert wurde. Die Schleife durchläuft die Geräte Objekte in der Auflistung und weist der Variablen deviceobj den Wert der einzelnen Geräte Objekte zu. Der Text der Schleife kann Code enthalten, der das Geräte Objekt verarbeitet.

## <a name="c-example"></a>C++-Beispiel

Das folgende Beispiel zeigt den C++-Code, der für den Zugriff auf die Objekte in einer Auflistung von Geräte Objekten erforderlich ist. Die angezeigte Funktion " **traversicollection**" erhält einen Zeiger auf die Schnittstelle [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) als Eingabeparameter. Dieser Schnittstellen Zeiger kann von der [**findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) -Methode oder anderen **Find** -Methoden des Device Finder-Objekts zurückgegeben werden.


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



Der erste Schritt besteht darin, mithilfe der Eigenschaft " [**\_ netwenum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) " einen neuen Enumerator für die Auflistung anzufordern. Dadurch wird ein Enumerator als [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle zurückgegeben. Der Beispielcode ruft [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zum Abrufen der [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle auf. Der Beispielcode legt dann den Enumerator auf den Anfang der Auflistung fest, indem die [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) -Methode aufgerufen wird. Schließlich ruft der Beispielcode die [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) -Methode auf, um die Auflistung zu durchlaufen. Die Geräte Objekte in der Sammlung sind in **Variant** -Strukturen enthalten. Diese Strukturen enthalten Zeiger auf [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen für die Geräte Objekte. Zum Abrufen der [**iupnpdevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) -Schnittstelle ruft der Beispielcode **QueryInterface** für die **IDispatch** -Schnittstelle auf.

 

 