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
# <a name="registering-a-callback"></a><span data-ttu-id="993f9-103">Registrieren eines Rückrufs</span><span class="sxs-lookup"><span data-stu-id="993f9-103">Registering a Callback</span></span>

<span data-ttu-id="993f9-104">Wenn die Anwendung eine Benachrichtigung erfordert, wenn sich der Wert einer Zustandsvariablen ändert oder die Dienst Instanz, die Sie darstellt, nicht mehr verfügbar ist, muss die Anwendung eine Rückruffunktion registrieren.</span><span class="sxs-lookup"><span data-stu-id="993f9-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="993f9-105">Verwenden Sie die [**iupnpservice:: addCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) -Methode, um eine Rückruffunktion für das aufzurufende Dienst Objekt zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="993f9-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="993f9-106">Diese Methode kann verwendet werden, um mehr als einen Rückruf zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="993f9-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="993f9-107">Entwickler sollten einen asynchronen Vorgang nicht innerhalb eines asynchronen Rückrufs abbrechen.</span><span class="sxs-lookup"><span data-stu-id="993f9-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="993f9-108">Das Hinzufügen eines Rückrufs in Visual Basic unterscheidet sich von der in VBScript verwendeten Methode.</span><span class="sxs-lookup"><span data-stu-id="993f9-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="993f9-109">Die im VBScript verwendete **getref** -Funktion ist in Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="993f9-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="993f9-110">Daher muss ein Entwickler ein [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Objekt erstellen, das über die Rückruffunktion als Standardmethode verfügt.</span><span class="sxs-lookup"><span data-stu-id="993f9-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="993f9-111">Weitere Informationen finden Sie [unter Registrieren eines Rückrufs in Visual Basic](registering-a-callback-in-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="993f9-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="993f9-112">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="993f9-112">VBScript Example</span></span>

<span data-ttu-id="993f9-113">Der folgende VBScript-Code definiert die Rückruffunktion **servicechangecallback**, die aufgerufen werden soll, wenn die Werte von Zustandsvariablen geändert werden oder wenn die Dienst Instanz nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="993f9-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="993f9-114">Die Funktion verfügt über vier Argumente.</span><span class="sxs-lookup"><span data-stu-id="993f9-114">The function has four arguments.</span></span>

<span data-ttu-id="993f9-115">Das erste Argument für die Funktion gibt den Grund an, warum der Rückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="993f9-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="993f9-116">Sie wird entweder aufgerufen, weil eine Status Variable geändert wurde, oder weil die Dienst Instanz nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="993f9-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="993f9-117">Das zweite Argument ist das Dienst Objekt, für das der Rückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="993f9-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="993f9-118">Wenn der Rückruf für eine Änderung der Statusvariablen aufgerufen wird, wird der Funktion zwei weitere Argumente an die Funktion weitergegeben: der Name der geänderten Variable und der neue Wert.</span><span class="sxs-lookup"><span data-stu-id="993f9-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="993f9-119">In diesem Beispiel zeigt der Rückruf einfach ein Meldungs Feld an, das den Namen der geänderten Variablen und ihren neuen Wert anzeigt, und, wenn der Rückruf für eine Änderung der Statusvariablen aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="993f9-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="993f9-120">Andernfalls wird eine Meldung angezeigt, die angibt, dass die Dienst Instanz nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="993f9-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="993f9-121">Der letzte Teil des Code Fragments zeigt, wie die Rückruffunktion mithilfe der [**addCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) -Methode registriert wird.</span><span class="sxs-lookup"><span data-stu-id="993f9-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="993f9-122">Es wird davon ausgegangen, dass die Dienst Objektvariablen, *Appservice* und *xportservice* , wie unter Abrufen von [Dienst Objekten](obtaining-service-objects.md)gezeigt, initialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="993f9-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


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



## <a name="c-example"></a><span data-ttu-id="993f9-123">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="993f9-123">C++ Example</span></span>


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



 

 