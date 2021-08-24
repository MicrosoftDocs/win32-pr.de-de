---
title: Abfangen von ADSI-Fehlern
description: VBScript bietet nur eine Möglichkeit, Fehler inlinefehlerbehandlung abzufangen.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082534"
---
# <a name="how-to-trap-adsi-errors"></a>Abfangen von ADSI-Fehlern

VBScript bietet nur eine Möglichkeit zum Abfangen von Fehlern: Inlinefehlerbehandlung. Ein Inlinefehlerhandler beginnt mit der Anweisung **On Error Resume Next** . Da **Bei Fehler Fortsetzen Weiter** alle Fehler daran hindert, die Ausführung des Skripts bis zum Ende des Bereichs zu beenden, aus dem On Error Resume **Next** aufgerufen wird, müssen Sie den Wert von **Err** an jedem Punkt nach der Anweisung On Error Resume **Next** überprüfen, an der Sie einen Fehler erwarten. Im folgenden Beispiel wird die Inlinefehlerbehandlung in einem ADSI-Skript veranschaulicht:


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



Nach jedem Speicherort, an dem für das Skript wahrscheinlich ein Fehler auftritt, gibt es eine **If Err-Anweisung.** Das **Err-Objekt** enthält den Fehlercode des letzten Fehlers, der während der Ausführung des Skripts aufgetreten ist. Wenn kein Fehler aufgetreten ist, ist **Err** immer null (0). Im vorherigen Beispiel führt ein Fehler dazu, dass die Ausführung zur **AdsiErr-Unterroutine** springt, die den Wert von **Err.Number** auf erwartete Fehler überprüft. Anstatt eine kryptische Fehlermeldung zu erhalten, gibt das Skript eine etwas bessere Erklärung dafür, warum die Ausführung beendet wurde.

Beachten Sie, dass innerhalb des Bereichs, in dem **On Error Resume Next** aufgerufen wird, jeder Fehler, der nach dem Aufruf Von Fehler fortsetzen **Weiter** auftritt, ignoriert wird. Dies kann das Debuggen eines Skripts erschweren, wenn Sie vergessen, den Wert von **Err** an den entsprechenden Stellen zu überprüfen. Überprüfen Sie den Wert von **Err,** wenn Sie erwarten, dass ein Fehler wahrscheinlich ist.

(Beim anfänglichen Debuggen des Skripts möchten Sie möglicherweise einfach zulassen, dass das Skript seine Ausführung anzuhalten und die fehlerhafte Zeilennummer bei einem Fehler anzeigt. Fügen Sie dann die Fehlerhandler hinzu, nachdem der grundlegende Programmablauf korrekt ist.)

 

 




