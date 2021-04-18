---
title: Vorgehensweise beim Abfangen von ADSI-Fehlern
description: VBScript bietet nur eine Möglichkeit zum Abfangen von Fehlern Inline-Fehlerbehandlung.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338363"
---
# <a name="how-to-trap-adsi-errors"></a>Vorgehensweise beim Abfangen von ADSI-Fehlern

VBScript bietet nur eine Möglichkeit zum Abfangen von Fehlern: Inline Fehlerbehandlung. Ein Inline Fehlerhandler beginnt mit der **On Error Resume Next** -Anweisung. Da **bei Fehler** fortsetzen weiter die Ausführung des Skripts bis zum Ende des Bereichs, aus dem der **Fehler** fortgesetzt werden soll, von Fehlern beendet wird, müssen Sie den Wert von **Err** an jedem Punkt nach der **On Error Resume Next** -Anweisung überprüfen, um zu erwarten, dass ein Fehler auftritt. Im folgenden Beispiel wird die Inline Fehlerbehandlung in einem ADSI-Skript veranschaulicht:


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



Nach jedem Speicherort, an dem das Skript wahrscheinlich einen Fehler findet, gibt es eine **If Err** -Anweisung. Das **Err** -Objekt enthält den Fehlercode des letzten Fehlers, der während der Ausführung des Skripts aufgetreten ist. Wenn kein Fehler aufgetreten ist, ist **Err** immer NULL (0). Im vorherigen Beispiel bewirkt ein Fehler, dass die Ausführung zur **adsierr** -Unterroutine springt, bei der der Wert von **Err. Number** auf erwartete Fehler überprüft wird. Anstatt mit einer kryptischen Fehlermeldung zu sterben, bietet das Skript eine etwas bessere Erklärung, warum es nicht mehr ausgeführt wird.

Beachten Sie, dass in dem Bereich, in dem "bei Fehler fortsetzen" **Next** aufgerufen wird, alle Fehler ignoriert werden, die nach dem Aufruf **bei "bei Fehler** fortsetzen" auftreten. Dadurch kann das Debuggen eines Skripts erschwert werden, wenn Sie vergessen, den Wert von **Err** an den entsprechenden Speicherorten zu überprüfen. Wenn Sie davon ausgehen, dass ein Fehler wahrscheinlich ist, überprüfen Sie den Wert von **Err**.

(Wenn Sie das Skript zum ersten Mal Debuggen, können Sie das Skript einfach anhalten und die fehlerhafte Zeilennummer bei einem Fehler anzeigen und dann die Fehlerhandler hinzufügen, nachdem der grundlegende Programmablauf korrekt ist.)

 

 




