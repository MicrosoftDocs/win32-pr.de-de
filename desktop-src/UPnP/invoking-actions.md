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
# <a name="invoking-actions"></a>Aufrufen von Aktionen

Mit der [**iupnpservice:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) -Methode können Aktionen für Dienst Objekte aufgerufen werden. Diese Methode verfügt über zwei Eingabeparameter: den Namen einer Aktion und ein Array von Eingabe Argumenten für diese Aktion. Die-Methode verfügt über zwei Parameter:

-   Parameter One – ein Eingabe-/Ausgabeparameter: ein Array von Ausgabe Argumenten für diese Aktion.
-   Parameter Two – ein Ausgabeparameter: ein Rückgabewert.

Die-Methode bewirkt, dass die Aktion auf dem Gerät aufgerufen wird. Das Gerät generiert Ereignis Benachrichtigungen, wenn die Statusvariablen des Geräts durch die Aktion geändert werden.

## <a name="vbscript-example"></a>VBScript-Beispiel

Im folgenden VBScript-Codebeispiel werden zwei Aktionen für ein Dienst Objekt aufgerufen. Die erste Aktion, *gettrackinfo*, übernimmt ein Eingabe Argument, eine Nachverfolgung. Die *gettrackinfo* -Aktion gibt die Länge des Titels als Rückgabewert zurück. Die Aktion verfügt auch über ein Output-Argument, das den Titel des Titels enthält, wenn die Methode Erfolg zurückgibt.

Nachdem Sie die *gettrackinfo* -Aktion aufgerufen haben, ruft das Beispiel die Play-Aktion auf, die keine Argumente annimmt. Da die Syntax von [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) jedoch ein Array von Eingabe-und Ausgabe Argumenten erfordert, muss im Beispiel ein leeres Array, *emptyargs*, ohne Elemente erstellt werden. Im Beispiel wird dieses Array zusammen mit dem Namen der Aktion sowohl für Eingabe-als auch für Ausgabe Argumente an **InvokeAction** weitergeleitet.


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



## <a name="c-example"></a>C++-Beispiel

Im folgenden Beispiel wird eine C++-Funktion definiert, die eine Aktion ohne Argumente aufruft. Da [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Argumenten erfordert, die übergeben werden, erstellt dieses Beispiel ein leeres **SAFEARRAY**. Da von dieser Aktion kein Wert zurückgegeben wird oder keine Ausgabe Argumente vorhanden sind, werden die letzten beiden [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) -Werte, die an **InvokeAction** übermittelt wurden, ignoriert.

Das Gerät generiert Ereignis Benachrichtigungen, wenn die Statusvariablen des Geräts durch die Aktion geändert werden.


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



Im folgenden Beispiel wird die fiktive *gettrackinfo* -Aktion aufgerufen. Sie nimmt eine Nachverfolgung als Argument, gibt die Tracklänge als Rückgabewert zurück und gibt den Titel des Titels in einem Output-Argument zurück. Der Code ähnelt dem vorherigen Beispiel, mit der Ausnahme, dass anstelle eines leeren [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Eingabe Argumenten in diesem Beispiel eine [**Variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) eingefügt wird, die die Nachverfolgung enthält. Wenn [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) Erfolg zurückgibt, untersucht dieses Beispiel den Rückgabewert und das Array von Ausgabe Argumenten.


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



 

 