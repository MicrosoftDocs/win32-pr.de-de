---
description: Gelegentlich tritt eine Situation auf, in der eine Nachricht nicht erfolgreich an das beabsichtigte Ziel übermittelt werden kann, in der Regel aufgrund eines Problems mit dem System oder der Konfiguration.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Behandeln von Fehlern in Komponenten in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314ff367e656043746bb34bcb28b6c5a3dc8db9b86b58a482af45f684fb658c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991080"
---
# <a name="handling-errors-in-queued-components"></a>Behandeln von Fehlern in Komponenten in der Warteschlange

Gelegentlich tritt eine Situation auf, in der eine Nachricht nicht erfolgreich an das beabsichtigte Ziel übermittelt werden kann, in der Regel aufgrund eines Problems mit dem System oder der Konfiguration. Beispielsweise kann die Nachricht an eine Warteschlange geleitet werden, die nicht vorhanden ist, oder die Zielwarteschlange ist möglicherweise nicht in einem zu empfangenden Zustand. Der Nachrichten-Mover ist ein Tool, das alle fehlerhaften nachrichten [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) aus einer Warteschlange in eine andere verschiebt, damit sie wiederholt werden können. Das Nachrichten-Mover-Hilfsprogramm ist ein Automation-Objekt, das mit einem VBScript aufgerufen werden kann.

## <a name="components-services-administrative-tool"></a>Components Services-Verwaltungstool

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Der folgende Beispielcode zeigt, wie Sie ein MessageMover-Objekt erstellen, die erforderlichen Eigenschaften festlegen und die Übertragung initiieren. Fügen Sie einen Verweis auf Visual Basic COM+-Diensttypbibliothek hinzu, um ihn aus dem Dienst zu verwenden.

> [!Note]  
> Um das MessageMover-Objekt verwenden zu können, muss Message Queuing auf Ihrem Computer installiert sein, und für die durch AppName angegebene Anwendung muss Warteschlangen aktiviert sein. Informationen zum Installieren von Message Queuing finden Sie unter Hilfe und Support im **Startmenü.**

 


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



Der folgende Visual Basic zeigt, wie sie die MyMessageMover-Funktion aufruft.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



Der Quellpfad der Nachricht ist die letzte ruheende Warteschlange. Dabei handelt es sich um die Warteschlange für in Message Queuing Warteschlange, die als AppName \_ deadqueue bezeichnet wird. Nachrichten werden hier verschoben, wenn die Transaktion wiederholt abgebrochen wird, wenn versucht wird, in der fünften Wiederholungswarteschlange zu versuchen. Mit dem Tool zum Verschieben von Nachrichten können Sie die Nachricht zurück in die erste Warteschlange verschieben, die als AppName bezeichnet wird. Weitere Informationen zu Wiederholungswarteschlangen finden Sie unter [Serverseitige Fehler.](server-side-errors.md)

Wenn Warteschlangenattribute dies zulassen, verschiebt der Nachrichten-Mover Nachrichten übergangsweise so, dass Nachrichten bei einem Fehler während der Verschiebe nicht verloren gehen oder dupliziert werden. Das Tool behält alle Nachrichteneigenschaften bei, die beim Verschieben von Nachrichten aus einer Warteschlange in eine andere beibehalten werden können.

Wenn die Nachrichten durch COM+-Warteschlangenkomponentenaufrufe generiert werden, behält das Nachrichten-Mover-Hilfsprogramm die Sicherheits-ID des ursprünglichen Aufrufers beim Verschieben von Nachrichten zwischen Warteschlangen bei. Wenn sowohl die Ziel- als auch die Quellwarteschlange transaktional sind, wird der gesamte Vorgang übergangsweise ausgeführt. Wenn die Quell- oder Zielwarteschlangen nicht transaktional sind, wird der Vorgang nicht unter einer Transaktion ausgeführt. Ein unerwarteter Fehler (z. B. ein Absturz) und ein Neustart einer nicht transaktionalen Bewegung könnten die Nachricht duplizieren, die zum Zeitpunkt des Fehlers verschoben wird.

## <a name="cc"></a>C/C++

Der folgende Beispielcode zeigt, wie Sie ein MessageMover-Objekt erstellen, die erforderlichen Eigenschaften festlegen und die Übertragung initiieren. Die ErrorDescription-Methode wird unter [Interpretieren von Fehlercodes beschrieben.](interpreting-error-codes.md)

> [!Note]  
> Um das MessageMover-Objekt verwenden zu können, muss Message Queuing auf Ihrem Computer installiert sein, und für die durch AppName angegebene Anwendung muss Warteschlangen aktiviert sein. Informationen zum Installieren von Message Queuing finden Sie unter Hilfe und Support im **Startmenü.**

 


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



Der folgende C++-Code zeigt, wie sie die MyMessageMover-Funktion aufruft.


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



Der Quellpfad der Nachricht ist die letzte ruheende Warteschlange. Dabei handelt es sich um die Warteschlange für in Message Queuing Warteschlange, die als AppName \_ deadqueue bezeichnet wird. Nachrichten werden hier verschoben, wenn die Transaktion wiederholt abgebrochen wird, wenn versucht wird, in der fünften Wiederholungswarteschlange zu versuchen. Mit dem Tool zum Verschieben von Nachrichten können Sie die Nachricht zurück in die erste Warteschlange verschieben, die als AppName bezeichnet wird. Weitere Informationen zu Wiederholungswarteschlangen finden Sie unter [Serverseitige Fehler.](server-side-errors.md)

Wenn Warteschlangenattribute dies zulassen, verschiebt der Nachrichten-Mover Nachrichten übergangsweise so, dass Nachrichten bei einem Fehler während der Verschiebe nicht verloren gehen oder dupliziert werden. Das Tool behält alle Nachrichteneigenschaften bei, die beim Verschieben von Nachrichten aus einer Warteschlange in eine andere beibehalten werden können.

Wenn die Nachrichten durch COM+-Warteschlangenkomponentenaufrufe generiert werden, behält das Nachrichten-Mover-Hilfsprogramm die Sicherheits-ID des ursprünglichen Aufrufers beim Verschieben von Nachrichten zwischen Warteschlangen bei. Wenn sowohl die Ziel- als auch die Quellwarteschlange transaktional sind, wird der gesamte Vorgang übergangsweise ausgeführt. Wenn die Quell- oder Zielwarteschlangen nicht transaktional sind, wird der Vorgang nicht unter einer Transaktion ausgeführt. Ein unerwarteter Fehler (z. B. ein Absturz) und ein Neustart einer nicht transaktionalen Bewegung könnten die Nachricht duplizieren, die zum Zeitpunkt des Fehlers verschoben wird.

## <a name="remarks"></a>Hinweise

COM+ behandelt serverseitige Abbruche (Player), indem die Nachricht, bei der ein Fehler ausgeführt wird, in eine andere Warteschlange für die endgültige Ruhezeit bewegt wird, um sie aus dem Weg zu bringen. Listener und Player können keine fortlaufende Schleife für eine Nachricht, die abgebrochen wird, schleifen. In vielen Fällen kann die abgebrochene Transaktion durch Ausführen von Aktionen auf dem Server behoben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler bei Komponenten in der Warteschlange](queued-components-errors.md)
</dt> </dl>

 

 



