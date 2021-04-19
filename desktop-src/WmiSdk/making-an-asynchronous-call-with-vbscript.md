---
description: Durch das Ausführen eines asynchronen Aufrufens an eine WMI-Methode oder eine Anbieter Methode kann ein Skript weiter ausgeführt werden, während Objekte zu einem "Swap"-Objekt zurückkehren und von Methoden wie z. b. "Swap. onobjectready" behandelt werden.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Erstellen eines asynchronen Aufrufes mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362256"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Erstellen eines asynchronen Aufrufes mit VBScript

Durch das Ausführen eines asynchronen Aufrufens an eine [*WMI-Methode*](gloss-w.md) oder eine [*Anbieter Methode*](gloss-p.md) kann ein Skript weiter ausgeführt werden, während Objekte zu einem " [**Swap**](swbemsink.md) "-Objekt zurückkehren und von Methoden wie z. b. " [**Swap. onobjectready**](swbemsink-onobjectready.md)" behandelt werden. Asynchrone Aufrufe werden jedoch nicht empfohlen, da die Daten möglicherweise nicht mit derselben Sicherheitsstufe wie der Aufruf zurückgegeben werden.

Wenn Sie asynchrone Sink-Aufrufe wie z. b. " [**taubemsink. onobjectready**](swbemsink-onobjectready.md) " verwenden, um zurückgegebene Daten abzurufen, können Sie den folgenden Registrierungs Wert festlegen.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **unsecappaccesscontroldefault**

Durch Festlegen dieses Registrierungs Werts wird die Authentifizierung der an die Senke zurückgegebenen Datenobjekte sichergestellt. Wenn **unsecappaccesscontroldefault** auf eins (1) festgelegt ist, führt WMI die Zugriffs Überprüfung der Daten Rückgabe aus. Mithilfe von Zugriffs Überprüfungen wird überprüft, ob die Daten aus der richtigen Quelle stammen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Asynchrone Methoden, deren Namen mit "Async" enden, \_ werden immer nach dem Aufruf von zurückgegeben, damit ein Programm weiter ausgeführt werden kann. Beispielsweise [**SWbemServices.Execquery**](swbemservices-execquery.md) synchron ist und die Ausführung blockiert, bis alle-Objekte zurückgegeben werden. Bei der [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md) -Methode handelt es sich um die nicht blockierende asynchrone Version. Eine sicherere Möglichkeit, **SWbemServices.Execquery** -nicht Blockierung aufzurufen, besteht darin, den-Befehl [*halb synchron*](gloss-s.md)zu machen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md) -Befehl und [Erstellen eines semisynchronen Aufrufes mit VBScript](making-a-semisynchronous-call-with-vbscript.md).

Der *IFlags* -Parameter für asynchrone Aufrufe hat immer den Standardwert 0 (null). Asynchrone Methoden stellen keine [**errbewbjectset**](swbemobjectset.md) -Auflistung für die Sink-Unterroutine bereit. Stattdessen empfängt die [**slibemsink. onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine in Ihrem Skript oder in der Anwendung jedes Objekt, sobald es bereitgestellt wird.

Wenn der ursprüngliche asynchrone Aufruf abgeschlossen ist, ruft er das Ereignis " [**slibemsink. OnComplete**](swbemsink-oncompleted.md) " der Objekt Senke auf und führt den Code aus, den Sie dort platzieren, um das Ergebnis des Aufrufs zu verarbeiten.

> [!Note]  
> Eine Active Server Seite (ASP) als Skript Host unterstützt keinen asynchronen-Befehl.

 

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von VBScript einen asynchronen-Befehl ausführen.

**So führen Sie einen asynchronen Befehl mithilfe von VBScript aus**

1.  Stellen Sie eine Verbindung mit WMI her, und erhalten Sie ein Objekt " [**Swap Services**](swbemservices.md) "

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Erstellen Sie die Objekt Senke entweder mithilfe von " [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) " oder (nur für Windows Script Host 2,0) dem Objekttag mit einem Ereignis Attribut, das auf **true** festgelegt ist.

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    Oder

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Erstellen Sie für jedes Ereignis, das von einem asynchronen Ereignis auslöst werden kann, eine Unterroutine. Diese Ereignisse werden als Methoden für " [**errbemubject**](swbemobject.md)" definiert. Beispielsweise sendet WMI einen Rückruf an " [**taubemsink. onobjectready**](swbemsink-onobjectready.md) ", wenn jede Instanz zurückgegeben wird.

    Wenn Sie die Unterroutine erstellen, platzieren Sie Code in der Unterroutine, damit jedes Ereignis beim Empfang verarbeitet wird.

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

    

    Überprüfen Sie den *ihresult* -Parameter, der vom [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis zurückgegeben wurde, um zu bestimmen, ob der asynchrone-Rückruf erfolgreich ist oder ob ein Fehler aufgetreten ist. Bei erfolgreicher Ausführung ist der Wert, der im *ihresult* -Parameter übergeben wird, gleich NULL (0). Jeder andere Wert weist möglicherweise auf einen Fehler hin, und Sie sollten die Werte im Fehler Objekt überprüfen, das im *objerrorobject* -Parameter zurückgegeben wird.

4.  Führen Sie einen asynchronen-Rückruf aus, und übergeben Sie den Namen der Senke im *objwbemsink* -Parameter.

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Führen Sie einen-Rückruf aus, der verhindert, dass das Skript beendet wird, bevor alle Ereignisse empfangen werden. Wenn das Skript mit einer Bildschirm Schnittstelle ausgeführt werden kann, können Sie dazu einen Windows Script Host (WSH)-Befehl verwenden, der `Echo` im folgenden Beispiel gezeigt wird.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Wenn Sie dieses Skript ausführen, sehen Sie möglicherweise, dass die erste Instanz vor der Nachricht, die auf **Instanzen wartet** , zurückgegeben wird, oder Sie wird nach angezeigt. Dabei handelt es sich um die Art der asynchronen Verarbeitung. Wenn Sie das Meldungs Feld **warten auf Instanzen** zu bald schließen, werden möglicherweise nicht alle Instanzen angezeigt.

6.  Wenn Sie Ergebnisse aus mehreren verschiedenen asynchronen Aufrufen haben, die zur gleichen Senke zurückkehren, speichern Sie alle notwendigen unterschiedlichen Daten im *objwbemasynccontext* -Kontext Parameter.

7.  Wenn Sie mit der Senke fertig sind, brechen Sie den asynchronen-Befehl mit der [**Cancel**](swbemsink-cancel.md) -Methode ab.

    ```VB
    objwbemsink.Cancel()
    ```

    

    Die [**Cancel**](swbemsink-cancel.md) -Methode weist WSH an, alle asynchronen Aufrufe abzubrechen, die einem angegebenen Sink-Objekt zugeordnet sind. Daher empfiehlt es sich, separate senken für asynchrone Vorgänge zu verwenden, die unabhängig sein müssen.

8.  Geben Sie das sink-Objekt frei, indem Sie das sink-Objekt zuweisen `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

Das folgende Codebeispiel zeigt eine asynchrone Abfrage für alle Instanzen des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) auf dem lokalen Computer. Eine semisynchrone Version derselben Methode finden Sie unter [Aufrufen einer Methode](calling-a-method.md).


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

 

 
