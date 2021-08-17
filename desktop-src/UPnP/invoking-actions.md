---
title: Aufrufen von Aktionen
description: Die IUPnPService InvokeAction-Methode ermöglicht das Aufrufen von Aktionen für Dienstobjekte.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7b294d7f0ed80988e9d4a9f75393764fd0a58b20d84581ab9ab10677efc6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137203"
---
# <a name="invoking-actions"></a>Aufrufen von Aktionen

Die [**IUPnPService::InvokeAction-Methode**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ermöglicht das Aufrufen von Aktionen für Dienstobjekte. Diese Methode verfügt über zwei Eingabeparameter: den Namen einer Aktion und ein Array von Eingabeargumenten für diese Aktion. Die -Methode verfügt über zwei Parameter:

-   Parameter 1 : Ein Eingabe-/Ausgabeparameter: ein Array von Ausgabeargumenten für diese Aktion.
-   Parameter 2 – ein Ausgabeparameter: ein Rückgabewert.

Die -Methode bewirkt, dass die Aktion auf dem Gerät aufgerufen wird. Das Gerät generiert Ereignisbenachrichtigungen, wenn sich die Zustandsvariablen des Geräts durch die Aktion ändern.

## <a name="vbscript-example"></a>VBScript-Beispiel

Im folgenden VBScript-Codebeispiel werden zwei Aktionen für ein Service-Objekt aufgerufen. Die erste Aktion, *GetTrackInfo,* übernimmt ein Eingabeargument, eine Tracknummer. Die *GetTrackInfo-Aktion* gibt die Tracklänge als Rückgabewert zurück. Die Aktion verfügt auch über ein Ausgabeargument, das den Titel der Spur enthält, wenn die Methode erfolgreich zurückgegeben wird.

Nach dem Aufrufen der *GetTrackInfo-Aktion* ruft das Beispiel die Play-Aktion auf, die keine Argumente annimmt. Da die Syntax von [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) jedoch ein Array von Eingabe- und Ausgabeargumenten erfordert, muss im Beispiel ein leeres Array, *emptyArgs,* ohne Elemente erstellt werden. Im Beispiel wird dieses Array für die Eingabe- und Ausgabeargumente zusammen mit dem Namen der Aktion an **InvokeAction** übergeben.


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

Im folgenden Beispiel wird eine C++-Funktion definiert, die eine Aktion ohne Argumente aufruft. Da [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) erfordert, dass ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Argumenten übergeben wird, wird in diesem Beispiel ein leeres **SAFEARRAY** erstellt. Da diese Aktion keinen Wert zurückgibt oder über Ausgabeargumente verfügt, ignoriert dieses Beispiel die letzten beiden [**VARIANT-Werte,**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) die an **InvokeAction** übergeben werden.

Das Gerät generiert Ereignisbenachrichtigungen, wenn sich die Zustandsvariablen des Geräts durch die Aktion ändern.


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



Im folgenden Beispiel wird die fiktive *GetTrackInfo-Aktion* aufgerufen. Er nimmt eine Tracknummer als Argument, gibt die Tracklänge als Rückgabewert zurück und gibt den Titel der Spur in einem Ausgabeargument zurück. Der Code ähnelt dem vorherigen Beispiel, mit dem Unterschied, dass in diesem Beispiel kein leeres [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) mit Eingabeargumenten erstellt wird, sondern ein [**VARIANT-Wert**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) eingefügt wird, der die Tracknummer enthält. Wenn [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) erfolgreich zurückgegeben wird, untersucht dieses Beispiel den Rückgabewert und das Array von Ausgabeargumenten.


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



 

 