---
title: Registrieren eines Rückrufs
description: Wenn die Anwendung eine Benachrichtigung erfordert, wenn sich der Wert einer Zustandsvariablen ändert oder die dienstinstanz, die sie darstellt, nicht mehr verfügbar ist, muss die Anwendung eine Rückruffunktion registrieren.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3dca603e6226d3171aed920311bafcf6844ec9fab5c7aa05deafee7a13fd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768530"
---
# <a name="registering-a-callback"></a>Registrieren eines Rückrufs

Wenn die Anwendung eine Benachrichtigung erfordert, wenn sich der Wert einer Zustandsvariablen ändert oder die dienstinstanz, die sie darstellt, nicht mehr verfügbar ist, muss die Anwendung eine Rückruffunktion registrieren. Verwenden Sie zum Registrieren einer Rückruffunktion für das auf aufrufende Dienstobjekt die [**IUPnPService::AddCallback-Methode.**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) Diese Methode kann verwendet werden, um mehrere Rückrufe zu registrieren.

Entwickler sollten einen asynchronen Vorgang innerhalb eines asynchronen Rückrufs nicht abbrechen.

> [!Note]  
> Das Hinzufügen eines Rückrufs in Visual Basic sich von der in VBScript verwendeten Methode ab. Die im VBScript verwendete **GetRef-Funktion** ist in der Datei nicht Visual Basic. Daher muss ein Entwickler ein [**IDispatch-Objekt**](/windows/win32/api/oaidl/nn-oaidl-idispatch) erstellen, das über die Rückruffunktion als Standardmethode verfügt. Weitere [Informationen finden Sie unter Registrieren eines Rückrufs in Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>VBScript-Beispiel

Der folgende VBScript-Code definiert die Rückruffunktion **serviceChangeCallback,** die aufgerufen wird, wenn sich die Werte der Zustandsvariablen ändern oder wenn die Dienstinstanz nicht mehr verfügbar ist. Die Funktion verfügt über vier Argumente.

Das erste Argument für die Funktion gibt den Grund an, aus dem der Rückruf aufgerufen wird. Sie wird entweder aufgerufen, weil eine Zustandsvariable geändert wurde oder weil die Dienstinstanz nicht mehr verfügbar ist.

Das zweite Argument ist das Dienstobjekt, für das der Rückruf aufgerufen wird. Wenn der Rückruf für eine Änderung der Zustandsvariablen aufgerufen wird, werden der Funktion zwei zusätzliche Argumente übergeben: der Name der geänderten Variablen und ihr neuer Wert.

In diesem Beispiel zeigt der Rückruf einfach ein Meldungsfeld an, in dem der Name der geänderten Variablen und deren neuer Wert angezeigt werden und der Rückruf für eine Änderung der Zustandsvariablen aufgerufen wurde. Andernfalls wird eine Meldung angezeigt, die angibt, dass die Dienstinstanz nicht mehr verfügbar ist.

Der letzte Teil des Codefragments zeigt, wie die Rückruffunktion mithilfe der [**AddCallback-Methode registriert**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) wird. Es wird davon ausgegangen, dass die Dienstobjektvariablen *appService* und *xportService* initialisiert wurden, wie unter [Abrufen von Dienstobjekten gezeigt.](obtaining-service-objects.md)


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



 

 