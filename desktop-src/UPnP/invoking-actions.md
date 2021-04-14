---
title: Aufrufen von Aktionen
description: Die iupnpservice InvokeAction-Methode ermöglicht das Aufrufen von Aktionen für Dienst Objekte.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390760"
---
# <a name="invoking-actions"></a><span data-ttu-id="ff0e7-103">Aufrufen von Aktionen</span><span class="sxs-lookup"><span data-stu-id="ff0e7-103">Invoking Actions</span></span>

<span data-ttu-id="ff0e7-104">Mit der [**iupnpservice:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) -Methode können Aktionen für Dienst Objekte aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="ff0e7-105">Diese Methode verfügt über zwei Eingabeparameter: den Namen einer Aktion und ein Array von Eingabe Argumenten für diese Aktion.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="ff0e7-106">Die-Methode verfügt über zwei Parameter:</span><span class="sxs-lookup"><span data-stu-id="ff0e7-106">The method has two parameters:</span></span>

-   <span data-ttu-id="ff0e7-107">Parameter One – ein Eingabe-/Ausgabeparameter: ein Array von Ausgabe Argumenten für diese Aktion.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="ff0e7-108">Parameter Two – ein Ausgabeparameter: ein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="ff0e7-109">Die-Methode bewirkt, dass die Aktion auf dem Gerät aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="ff0e7-110">Das Gerät generiert Ereignis Benachrichtigungen, wenn die Statusvariablen des Geräts durch die Aktion geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="ff0e7-111">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff0e7-111">VBScript Example</span></span>

<span data-ttu-id="ff0e7-112">Im folgenden VBScript-Codebeispiel werden zwei Aktionen für ein Dienst Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="ff0e7-113">Die erste Aktion, *gettrackinfo*, übernimmt ein Eingabe Argument, eine Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="ff0e7-114">Die *gettrackinfo* -Aktion gibt die Länge des Titels als Rückgabewert zurück.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="ff0e7-115">Die Aktion verfügt auch über ein Output-Argument, das den Titel des Titels enthält, wenn die Methode Erfolg zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="ff0e7-116">Nachdem Sie die *gettrackinfo* -Aktion aufgerufen haben, ruft das Beispiel die Play-Aktion auf, die keine Argumente annimmt.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="ff0e7-117">Da die Syntax von [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) jedoch ein Array von Eingabe-und Ausgabe Argumenten erfordert, muss im Beispiel ein leeres Array, *emptyargs*, ohne Elemente erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="ff0e7-118">Im Beispiel wird dieses Array zusammen mit dem Namen der Aktion sowohl für Eingabe-als auch für Ausgabe Argumente an **InvokeAction** weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a><span data-ttu-id="ff0e7-119">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff0e7-119">C++ Example</span></span>

<span data-ttu-id="ff0e7-120">Im folgenden Beispiel wird eine C++-Funktion definiert, die eine Aktion ohne Argumente aufruft.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="ff0e7-121">Da [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Argumenten erfordert, die übergeben werden, erstellt dieses Beispiel ein leeres **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="ff0e7-122">Da von dieser Aktion kein Wert zurückgegeben wird oder keine Ausgabe Argumente vorhanden sind, werden die letzten beiden [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) -Werte, die an **InvokeAction** übermittelt wurden, ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="ff0e7-123">Das Gerät generiert Ereignis Benachrichtigungen, wenn die Statusvariablen des Geräts durch die Aktion geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



<span data-ttu-id="ff0e7-124">Im folgenden Beispiel wird die fiktive *gettrackinfo* -Aktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="ff0e7-125">Sie nimmt eine Nachverfolgung als Argument, gibt die Tracklänge als Rückgabewert zurück und gibt den Titel des Titels in einem Output-Argument zurück.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="ff0e7-126">Der Code ähnelt dem vorherigen Beispiel, mit der Ausnahme, dass anstelle eines leeren [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Eingabe Argumenten in diesem Beispiel eine [**Variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) eingefügt wird, die die Nachverfolgung enthält.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="ff0e7-127">Wenn [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) Erfolg zurückgibt, untersucht dieses Beispiel den Rückgabewert und das Array von Ausgabe Argumenten.</span><span class="sxs-lookup"><span data-stu-id="ff0e7-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 