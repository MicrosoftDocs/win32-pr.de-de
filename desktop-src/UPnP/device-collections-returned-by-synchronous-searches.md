---
title: Von synchronen Suchvorgängen zurückgegebene Gerätesammlungen
description: Gerätesammlungen sind Objekte, die mindestens ein Geräteobjekt enthalten. Eine Gerätesammlung macht die IUPnPDevices-Schnittstelle verfügbar, die Methoden und Eigenschaften zum Durchlaufen der Sammlung und Extrahieren einzelner Geräteobjekte enthält.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94901dd2f3988327c32d7c21799ff4db7647e76fd987247e903501bd8937851a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755526"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>Von synchronen Suchvorgängen zurückgegebene Gerätesammlungen

Gerätesammlungen sind Objekte, die mindestens ein Geräteobjekt enthalten. Eine Gerätesammlung macht die [**IUPnPDevices-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) verfügbar, die Methoden und Eigenschaften zum Durchlaufen der Sammlung und Extrahieren einzelner Geräteobjekte enthält.

## <a name="vbscript-example"></a>VBScript-Beispiel

VBScript-Anwendungen können auf zwei Arten auf die Objekte in der Auflistung zugreifen. Zunächst können sie die Elemente sequenziell durchlaufen, indem sie ein für ... Jeder... Next-Schleife, wie im folgenden Beispiel gezeigt:


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



In diesem Beispiel wird davon ausgegangen, dass die Gerätevariable mit dem Ergebnis einer vorherigen Suche initialisiert wurde. Die Schleife durchfing die Geräteobjekte in der Sammlung und weist der Variablen deviceObj wiederum den Wert jedes Geräteobjekts zu. Der Text der Schleife kann Code enthalten, der das Device-Objekt verarbeitet.

## <a name="c-example"></a>C++-Beispiel

Das folgende Beispiel zeigt den C++-Code, der für den Zugriff auf die Objekte in einer Auflistung von Geräteobjekten erforderlich ist. Die gezeigte **Funktion TraverseCollection** empfängt einen Zeiger auf die [**IUPnPDevices-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) als Eingabeparameter. Dieser Schnittstellenzeiger kann von der [**FindByType-Methode**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) oder anderen **Find-Methoden** des Device Finder-Objekts zurückgegeben werden.


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



Der erste Schritt besteht im Anfordern eines neuen Enumerators für die Auflistung mithilfe der [**\_ NewEnum-Eigenschaft.**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) Dadurch wird ein Enumerator als [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) zurückgegeben. Der Beispielcode ruft [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um die [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) zu erhalten. Der Beispielcode legt dann den Enumerator auf den Anfang der Auflistung fest, indem die [**IEnumVARIANT::Reset-Methode aufruft.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) Schließlich ruft der Beispielcode die [**IEnumVARIANT::Next-Methode**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) auf, um die Auflistung zu durchlaufen. Die Geräteobjekte in der Sammlung sind in **VARIANT-Strukturen** enthalten. Diese Strukturen enthalten Zeiger auf [**IDispatch-Schnittstellen**](/windows/win32/api/oaidl/nn-oaidl-idispatch) auf den Geräteobjekten. Um die [**IUPnPDevice-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) zu erhalten, ruft der Beispielcode **QueryInterface** auf der **IDispatch-Schnittstelle** auf.

 

 