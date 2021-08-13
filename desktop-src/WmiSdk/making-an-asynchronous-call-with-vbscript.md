---
description: Durch einen asynchronen Aufruf einer WMI-Methode oder einer Anbietermethode kann ein Skript weiterhin ausgeführt werden, während Objekte an ein SWbemSink-Objekt zurückkehren und von Methoden wie SWbemSink.OnObjectReady behandelt werden.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Ausführen eines asynchronen Aufrufs mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee8c4737ff7513441532275e24f2cfe20f8e30fa2932e854cc566eb032c49d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555140"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Ausführen eines asynchronen Aufrufs mit VBScript

Durch einen asynchronen Aufruf einer [](gloss-p.md) [*WMI-Methode*](gloss-w.md) oder einer Anbietermethode kann ein Skript weiterhin ausgeführt werden, während Objekte an ein [**SWbemSink-Objekt**](swbemsink.md) zurückkehren und von Methoden wie [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md)verarbeitet werden. asynchrone Aufrufe werden jedoch nicht empfohlen, da die Daten möglicherweise nicht auf der gleichen Sicherheitsebene wie der Aufruf zurückgegeben werden.

Wenn Sie asynchrone Senkenaufrufe wie [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) verwenden, um zurückgegebene Daten zu erhalten, können Sie den folgenden Registrierungswert festlegen.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

Durch Festlegen dieses Registrierungswerts wird die Authentifizierung der Datenobjekte sichergestellt, die an die Senke zurückgegeben werden. Wenn **UnsecAppAccessControlDefault** auf eins (1) festgelegt ist, führt WMI eine Zugriffsüberprüfung der Datenzusenz durch. Mit Zugriffsüberprüfungen wird überprüft, ob die Daten aus der richtigen Quelle stammen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md)von .

Asynchrone Methoden mit Namen, die auf "Async" enden, werden immer sofort nach dem Aufruf zurückgegeben, damit die Ausführung eines Programms \_ fortgesetzt werden kann. Beispielsweise ist [**SWbemServices.ExecQuery**](swbemservices-execquery.md) synchron und blockiert die Ausführung, bis alle Objekte zurückgegeben werden. Die [**SWbemServices.ExecQueryAsync-Methode**](swbemservices-execqueryasync.md) ist die nicht blockierende asynchrone Version. Eine sicherere Möglichkeit, den Aufruf vonSWbemServices.Exe **cQuery** nicht zu blockieren, besteht darin, den Aufruf [*semisynchron zu machen.*](gloss-s.md) Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md) und Ausführen eines [semisynchronen Aufrufs mit VBScript.](making-a-semisynchronous-call-with-vbscript.md)

Der *iFlags-Parameter* für asynchrone Aufrufe ist standardmäßig null (0). Asynchrone Methoden geben keine [**SWbemObjectSet-Auflistung**](swbemobjectset.md) für die Senkenunterroutine an. Stattdessen empfängt [**die SWbemSink.OnObjectReady-Ereignisunterroutine**](swbemsink-onobjectready.md) in Ihrem Skript oder Ihrer Anwendung jedes Objekt, wie es bereitgestellt wird.

Wenn der ursprüngliche asynchrone Aufruf abgeschlossen ist, ruft er das [**SWbemSink.OnCompleted-Ereignis**](swbemsink-oncompleted.md) der Objektsenke auf und führt den Code aus, den Sie dort platzieren, um das Ergebnis des Aufrufs zu verarbeiten.

> [!Note]  
> Eine Active Server Page (ASP) als Skripthost unterstützt keinen asynchronen Aufruf.

 

Im folgenden Verfahren wird beschrieben, wie Sie einen asynchronen Aufruf mit VBScript ausführen.

**So nehmen Sie einen asynchronen Aufruf mit VBScript vor**

1.  Verbinden WMI, und erhalten Sie ein [**SWbemServices-Objekt.**](swbemservices.md)

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Erstellen Sie die Objektsenke entweder mit [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) oder (nur für Windows Script Host 2.0) das OBJECT-Tag mit einem ereignisattribut, das auf **TRUE festgelegt ist.**

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    Oder

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Erstellen Sie eine Unterroutine für jedes Ereignis, das ein asynchrones Ereignis auslösen kann. Diese Ereignisse werden als Methoden für [**SWbemObject definiert.**](swbemobject.md) WMI macht beispielsweise einen Rückruf an [**SWbemSink.OnObjectReady,**](swbemsink-onobjectready.md) wenn jede Instanz zurückgegeben wird.

    Wenn Sie die Unterroutine erstellen, platzieren Sie Code in der Unterroutine, um jedes Ereignis zu behandeln, wenn es empfangen wird.

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    Überprüfen Sie den vom [**OnCompleted-Ereignis**](swbemsink-oncompleted.md) zurückgegebenen *iHresult-Parameter,* um zu bestimmen, ob der asynchrone Aufruf erfolgreich ist oder ob ein Fehler aufgetreten ist. Bei Erfolg ist der im *iHresult-Parameter* übergebene Wert gleich 0 (null). Jeder andere Wert kann auf einen Fehler hinweisen, und Sie sollten die Werte im Fehlerobjekt überprüfen, das im *objErrorObject-Parameter zurückgegeben* wird.

4.  Nehmen Sie einen asynchronen Aufruf vor, und übergeben Sie den Namen Ihrer Senke im *parameter objWbemSink.*

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Nehmen Sie einen Aufruf vor, der verhindert, dass das Skript beendet wird, bevor alle Ereignisse empfangen werden. Wenn Ihr Skript mit einer Bildschirmschnittstelle ausgeführt werden kann, besteht eine einfache Möglichkeit in der Verwendung eines WSH-Befehls (Windows Script Host), wie im folgenden Beispiel `Echo` gezeigt.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Wenn Sie dieses Skript ausführen, wird die erste Instanz möglicherweise vor der Meldung **Warten** auf Instanzen oder danach angezeigt. Dies ist die Art der asynchronen Verarbeitung. Wenn Sie das **Meldungsfeld Warten auf Instanzen** zu früh schließen, werden möglicherweise nicht alle Instanzen angezeigt.

6.  Wenn Sie Ergebnisse aus mehreren verschiedenen asynchronen Aufrufen haben, die an dieselbe Senke zurückgegeben werden, speichern Sie alle erforderlichen unterscheidenden Daten im *Kontextparameter objWbemAsyncContext.*

7.  Wenn Sie mit der Senke fertig sind, brechen Sie den asynchronen Aufruf mit der [**Cancel-Methode**](swbemsink-cancel.md) ab.

    ```VB
    objwbemsink.Cancel()
    ```

    

    Die [**Cancel-Methode**](swbemsink-cancel.md) weist WSH an, alle asynchronen Aufrufe abzubricht, die einem bestimmten Senkenobjekt zugeordnet sind. Daher können Sie separate Senken für asynchrone Vorgänge verwenden, die unabhängig sein müssen.

8.  Geben Sie das Senkenobjekt frei, indem Sie das Senkenobjekt `Nothing` zuweisen.

    ```VB
    set objwbemsink= Nothing
    ```

    

Das folgende Codebeispiel zeigt eine asynchrone Abfrage für alle Instanzen des [**\_ Win32-Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) auf dem lokalen Computer. Eine semisynchrone Version derselben Methode finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

 
