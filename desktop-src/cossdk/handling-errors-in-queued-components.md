---
description: Gelegentlich tritt eine Situation auf, in der eine Nachricht nicht erfolgreich an das beabsichtigte Ziel übermittelt werden kann. Dies ist normalerweise auf ein Problem mit dem System oder der Konfiguration zurückzuführen.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Behandeln von Fehlern in in der Warteschlange befindlichen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523872"
---
# <a name="handling-errors-in-queued-components"></a>Behandeln von Fehlern in in der Warteschlange befindlichen Komponenten

Gelegentlich tritt eine Situation auf, in der eine Nachricht nicht erfolgreich an das beabsichtigte Ziel übermittelt werden kann. Dies ist normalerweise auf ein Problem mit dem System oder der Konfiguration zurückzuführen. Beispielsweise kann die Nachricht an eine Warteschlange weitergeleitet werden, die nicht vorhanden ist, oder die Ziel Warteschlange befindet sich möglicherweise nicht in einem Zustand, der empfangen werden kann. Der Nachrichten Verschiebungsvorgang ist ein Tool, das alle fehlgeschlagenen [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Nachrichten von einer Warteschlange in eine andere verschiebt, damit Sie wiederholt werden können. Das Hilfsprogramm für den Nachrichten Verschiebungsvorgang ist ein Automatisierungs Objekt, das mit einem VBScript aufgerufen werden kann.

## <a name="components-services-administrative-tool"></a>Komponenten Dienste-Verwaltungs Tool

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Der folgende Beispielcode zeigt, wie ein messagemover-Objekt erstellt, die erforderlichen Eigenschaften festgelegt und die Übertragung initiiert wird. Um es aus Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.

> [!Note]  
> Um das messagemover-Objekt verwenden zu können, müssen Message Queuing auf dem Computer installiert sein, und für die in appname angegebene Anwendung muss die Warteschlange aktiviert sein. Weitere Informationen zum Installieren von Message Queuing finden Sie unter Hilfe und Support im **Startmenü** .

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



Der folgende Visual Basic Code zeigt, wie die mymessagemover-Funktion aufgerufen wird.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



Der Quellpfad der Nachricht ist die letzte ruhende Warteschlange. Dabei handelt es sich um die Warteschlange für unzustellbare Nachrichten, bei der es sich um eine private Message Queuing Warteschlange handelt und \_ Nachrichten werden hier verschoben, wenn die Transaktion bei einem Versuch in der fünften Wiederholungs Warteschlange wiederholt abgebrochen wird. Mit dem Message Verschiebungs Tool können Sie die Nachricht zurück in die erste Warteschlange verschieben, die als appname bezeichnet wird. Weitere Informationen zu Wiederholungs Warteschlangen finden Sie unter [Server seitige Fehler](server-side-errors.md).

Wenn Queue-Attribute zulässig sind, verschiebt der Nachrichten Verschiebungs Vorgang die Nachrichten transitiv, sodass Nachrichten im Fall eines Fehlers während der Verschiebung nicht verloren gehen oder dupliziert werden. Das Tool behält alle Nachrichten Eigenschaften bei, die beibehalten werden können, wenn Nachrichten von einer Warteschlange in eine andere verschoben werden.

Wenn die Nachrichten von com+-in der Warteschlange befindlichen Komponenten aufgerufen werden, behält das Nachrichten verschiebungsprogramm die Sicherheits-ID des ursprünglichen Aufrufers bei, während Nachrichten zwischen Warteschlangen Wenn sowohl die Ziel-als auch die Quell Warteschlange transaktional sind, erfolgt der gesamte Vorgang transitiv. Wenn die Quell-oder Ziel Warteschlange nicht transaktional sind, wird der Vorgang nicht unter einer Transaktion ausgeführt. Ein unerwarteter Fehler (z. b. ein Absturz) und ein Neustart eines nicht transaktionalen Verschiebens können das Verschieben der Nachricht zum Zeitpunkt des Fehlers duplizieren.

## <a name="cc"></a>C/C++

Der folgende Beispielcode zeigt, wie ein messagemover-Objekt erstellt, die erforderlichen Eigenschaften festgelegt und die Übertragung initiiert wird. Die ErrorDescription-Methode wird unter [Interpretieren von Fehler Codes](interpreting-error-codes.md)beschrieben.

> [!Note]  
> Um das messagemover-Objekt verwenden zu können, müssen Message Queuing auf dem Computer installiert sein, und für die in appname angegebene Anwendung muss die Warteschlange aktiviert sein. Weitere Informationen zum Installieren von Message Queuing finden Sie unter Hilfe und Support im **Startmenü** .

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



Der folgende C++-Code zeigt, wie die mymessagemover-Funktion aufgerufen wird.


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



Der Quellpfad der Nachricht ist die letzte ruhende Warteschlange. Dabei handelt es sich um die Warteschlange für unzustellbare Nachrichten, bei der es sich um eine private Message Queuing Warteschlange handelt und \_ Nachrichten werden hier verschoben, wenn die Transaktion bei einem Versuch in der fünften Wiederholungs Warteschlange wiederholt abgebrochen wird. Mit dem Message Verschiebungs Tool können Sie die Nachricht zurück in die erste Warteschlange verschieben, die als appname bezeichnet wird. Weitere Informationen zu Wiederholungs Warteschlangen finden Sie unter [Server seitige Fehler](server-side-errors.md).

Wenn Queue-Attribute zulässig sind, verschiebt der Nachrichten Verschiebungs Vorgang die Nachrichten transitiv, sodass Nachrichten im Fall eines Fehlers während der Verschiebung nicht verloren gehen oder dupliziert werden. Das Tool behält alle Nachrichten Eigenschaften bei, die beibehalten werden können, wenn Nachrichten von einer Warteschlange in eine andere verschoben werden.

Wenn die Nachrichten von com+-in der Warteschlange befindlichen Komponenten aufgerufen werden, behält das Nachrichten verschiebungsprogramm die Sicherheits-ID des ursprünglichen Aufrufers bei, während Nachrichten zwischen Warteschlangen Wenn sowohl die Ziel-als auch die Quell Warteschlange transaktional sind, erfolgt der gesamte Vorgang transitiv. Wenn die Quell-oder Ziel Warteschlange nicht transaktional sind, wird der Vorgang nicht unter einer Transaktion ausgeführt. Ein unerwarteter Fehler (z. b. ein Absturz) und ein Neustart eines nicht transaktionalen Verschiebens können das Verschieben der Nachricht zum Zeitpunkt des Fehlers duplizieren.

## <a name="remarks"></a>Bemerkungen

Com+ verarbeitet serverseitige (Player-) Abbrüche, indem die Nachricht, bei der ein Fehler auftritt, in eine andere "abschließende ruhende" Warteschlange verschoben wird, um Sie zu erhalten. Der Listener und der Player können eine Nachricht, die abgebrochen wird, nicht fortlaufend Schleifen. In vielen Fällen kann die abgebrochene Transaktion korrigiert werden, indem eine Aktion auf dem Server ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten Fehler in der Warteschlange](queued-components-errors.md)
</dt> </dl>

 

 



