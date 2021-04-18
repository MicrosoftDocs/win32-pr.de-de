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
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="71a60-103">Vorgehensweise beim Abfangen von ADSI-Fehlern</span><span class="sxs-lookup"><span data-stu-id="71a60-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="71a60-104">VBScript bietet nur eine Möglichkeit zum Abfangen von Fehlern: Inline Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="71a60-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="71a60-105">Ein Inline Fehlerhandler beginnt mit der **On Error Resume Next** -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="71a60-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="71a60-106">Da **bei Fehler** fortsetzen weiter die Ausführung des Skripts bis zum Ende des Bereichs, aus dem der **Fehler** fortgesetzt werden soll, von Fehlern beendet wird, müssen Sie den Wert von **Err** an jedem Punkt nach der **On Error Resume Next** -Anweisung überprüfen, um zu erwarten, dass ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="71a60-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="71a60-107">Im folgenden Beispiel wird die Inline Fehlerbehandlung in einem ADSI-Skript veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="71a60-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


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



<span data-ttu-id="71a60-108">Nach jedem Speicherort, an dem das Skript wahrscheinlich einen Fehler findet, gibt es eine **If Err** -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="71a60-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="71a60-109">Das **Err** -Objekt enthält den Fehlercode des letzten Fehlers, der während der Ausführung des Skripts aufgetreten ist. Wenn kein Fehler aufgetreten ist, ist **Err** immer NULL (0).</span><span class="sxs-lookup"><span data-stu-id="71a60-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="71a60-110">Im vorherigen Beispiel bewirkt ein Fehler, dass die Ausführung zur **adsierr** -Unterroutine springt, bei der der Wert von **Err. Number** auf erwartete Fehler überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="71a60-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="71a60-111">Anstatt mit einer kryptischen Fehlermeldung zu sterben, bietet das Skript eine etwas bessere Erklärung, warum es nicht mehr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71a60-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="71a60-112">Beachten Sie, dass in dem Bereich, in dem "bei Fehler fortsetzen" **Next** aufgerufen wird, alle Fehler ignoriert werden, die nach dem Aufruf **bei "bei Fehler** fortsetzen" auftreten.</span><span class="sxs-lookup"><span data-stu-id="71a60-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="71a60-113">Dadurch kann das Debuggen eines Skripts erschwert werden, wenn Sie vergessen, den Wert von **Err** an den entsprechenden Speicherorten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="71a60-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="71a60-114">Wenn Sie davon ausgehen, dass ein Fehler wahrscheinlich ist, überprüfen Sie den Wert von **Err**.</span><span class="sxs-lookup"><span data-stu-id="71a60-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="71a60-115">(Wenn Sie das Skript zum ersten Mal Debuggen, können Sie das Skript einfach anhalten und die fehlerhafte Zeilennummer bei einem Fehler anzeigen und dann die Fehlerhandler hinzufügen, nachdem der grundlegende Programmablauf korrekt ist.)</span><span class="sxs-lookup"><span data-stu-id="71a60-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 




