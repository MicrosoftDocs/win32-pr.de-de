---
title: Registrieren eines Rückrufs
description: Wenn die Anwendung eine Benachrichtigung erfordert, wenn sich der Wert einer Zustandsvariablen ändert oder die Dienst Instanz, die Sie darstellt, nicht mehr verfügbar ist, muss die Anwendung eine Rückruffunktion registrieren.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728096"
---
# <a name="registering-a-callback"></a>Registrieren eines Rückrufs

Wenn die Anwendung eine Benachrichtigung erfordert, wenn sich der Wert einer Zustandsvariablen ändert oder die Dienst Instanz, die Sie darstellt, nicht mehr verfügbar ist, muss die Anwendung eine Rückruffunktion registrieren. Verwenden Sie die [**iupnpservice:: addCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) -Methode, um eine Rückruffunktion für das aufzurufende Dienst Objekt zu registrieren. Diese Methode kann verwendet werden, um mehr als einen Rückruf zu registrieren.

Entwickler sollten einen asynchronen Vorgang nicht innerhalb eines asynchronen Rückrufs abbrechen.

> [!Note]  
> Das Hinzufügen eines Rückrufs in Visual Basic unterscheidet sich von der in VBScript verwendeten Methode. Die im VBScript verwendete **getref** -Funktion ist in Visual Basic nicht verfügbar. Daher muss ein Entwickler ein [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Objekt erstellen, das über die Rückruffunktion als Standardmethode verfügt. Weitere Informationen finden Sie [unter Registrieren eines Rückrufs in Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>VBScript-Beispiel

Der folgende VBScript-Code definiert die Rückruffunktion **servicechangecallback**, die aufgerufen werden soll, wenn die Werte von Zustandsvariablen geändert werden oder wenn die Dienst Instanz nicht mehr verfügbar ist. Die Funktion verfügt über vier Argumente.

Das erste Argument für die Funktion gibt den Grund an, warum der Rückruf aufgerufen wird. Sie wird entweder aufgerufen, weil eine Status Variable geändert wurde, oder weil die Dienst Instanz nicht mehr verfügbar ist.

Das zweite Argument ist das Dienst Objekt, für das der Rückruf aufgerufen wird. Wenn der Rückruf für eine Änderung der Statusvariablen aufgerufen wird, wird der Funktion zwei weitere Argumente an die Funktion weitergegeben: der Name der geänderten Variable und der neue Wert.

In diesem Beispiel zeigt der Rückruf einfach ein Meldungs Feld an, das den Namen der geänderten Variablen und ihren neuen Wert anzeigt, und, wenn der Rückruf für eine Änderung der Statusvariablen aufgerufen wurde. Andernfalls wird eine Meldung angezeigt, die angibt, dass die Dienst Instanz nicht mehr verfügbar ist.

Der letzte Teil des Code Fragments zeigt, wie die Rückruffunktion mithilfe der [**addCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) -Methode registriert wird. Es wird davon ausgegangen, dass die Dienst Objektvariablen, *Appservice* und *xportservice* , wie unter Abrufen von [Dienst Objekten](obtaining-service-objects.md)gezeigt, initialisiert wurden.


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a>C++-Beispiel


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 