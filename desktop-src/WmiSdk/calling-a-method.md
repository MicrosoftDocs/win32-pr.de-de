---
description: WMI stellt Methoden in der COM-API und der Skript-API bereit, um Informationen zu erhalten oder Objekte in einem Unternehmenssystem zu bearbeiten.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Aufrufen einer WMI-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db6c8a74c8125e0bb1727839b8f59f4b486161d5ae629a0c7351481ade016ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820085"
---
# <a name="calling-a-wmi-method"></a>Aufrufen einer WMI-Methode

WMI stellt Methoden in der [COM-API](com-api-for-wmi.md) und der [Skript-API](scripting-api-for-wmi.md) bereit, um Informationen zu erhalten oder Objekte in einem Unternehmenssystem zu bearbeiten. Die WMI-SkriptmethodeSWbemServices.Exe [**cQuery-Abfragen**](swbemservices-execquery.md) für Daten. Anbieter verfügen auch über Methoden, die in den von ihnen registrierten Klassen definiert sind. Beispiele hierfür sind [**die Win32 \_ LogicalDisk-Methoden**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) und [**ScheduleAutoChk,**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) die vom [Win32-Anbieter bereitgestellt werden.](/windows/desktop/CIMWin32Prov/win32-provider)

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [WMI-Methoden im Vergleich zu Anbietermethoden](#wmi-methods-compared-to-provider-methods)
-   [Methoden aufrufende Modi in WMI](#method-calling-modes-in-wmi)
    -   [Synchroner Modus](#synchronous-mode)
    -   [Asynchroner Modus](#asynchronous-mode)
    -   [Semisynchroner Modus](#semisynchronous-mode)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>WMI-Methoden im Vergleich zu Anbietermethoden

Mithilfe [*von WMI-Methodenaufrufen*](gloss-w.md) in Kombination [*mit*](gloss-p.md) Anbietermethodeaufrufen können Sie Informationen zu Ihrem Unternehmen abrufen und bearbeiten. Weitere Informationen finden Sie unter [Aufrufen einer WMI-Methode und](calling-a-wmi-method.md) Aufrufen einer [Anbietermethode.](calling-a-provider-method.md)

Die Methoden des WMI-Skriptobjekts [**SWbemObject**](swbemobject.md) haben einen besonderen Status, da sie für jede WMI-Datenklasse gelten können. Weitere Informationen finden Sie unter [Skripterstellung mit SWbemObject](scripting-with-swbemobject.md).

Im folgenden Codebeispiel werden sowohl WMI- als auch Anbietermethoden aufruft.

Die folgenden WMI- und Anbietermethoden befinden sich in der [Skripterstellungs-API für WMI:](scripting-api-for-wmi.md)

-   **objWMIService.ExecQuery ruft** die WMI-SkriptmethodeSWbemServices.Exe [ **cQuery auf.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService.StopService() ruft** die Anbietermethode [ **Win32 \_ Service.StopService auf.**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Sie können den Code, der möglicherweise in "Return" angezeigt wird, im Abschnitt Rückgabecodes für [**den Win32-Dienst \_ nachschauen.**](/windows/desktop/CIMWin32Prov/win32-service)


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>Method-Calling-Modi in WMI

Der semisynchrone Aufrufmodus bietet in der Regel das beste Gleichgewicht zwischen Sicherheit und Leistung.

Weitere Informationen zu den einzelnen möglichen Modi finden Sie in den folgenden Themen:

-   [Synchron](#synchronous-mode)
-   [Asynchron](#asynchronous-mode)
-   [Semisynchron](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Synchroner Modus

Der synchrone Modus tritt auf, wenn das Programm oder die Skripts angehalten werden, bis der Methodenaufruf ein [**SWbemObjectSet-Auflistungsobjekt**](swbemobjectset.md) zurückgibt. WMI erstellt diese Auflistung im Arbeitsspeicher, bevor das Sammlungsobjekt an das aufrufende Programm oder Skript zurücksendet.

Der synchrone Modus kann sich negativ auf die Programm- oder Skriptleistung auf dem Computer auswirken, auf dem das Programm oder Skript ausgeführt wird. Beispielsweise kann das synchrone Abrufen von Tausenden von Ereignissen aus dem Ereignisprotokoll sehr lange dauern und viel Arbeitsspeicher nutzen, da WMI ein Objekt aus jedem Ereignis erstellt und diese Objekte dann in eine Sammlung einrückt, bevor die Auflistung an die -Methode übergeben wird.

Sie sollten nur Methoden aufrufen, die keine großen Datensätze im synchronen Modus zurückgeben. Die folgenden [**SWbemServices-Methoden**](swbemservices.md) können im synchronen Modus sicher aufgerufen werden:

-   [**SWbemServices.Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.Get**](swbemservices-get.md)

[**Alle SWbemServices-Methoden**](swbemservices.md) ohne das Wort "Async" im Namen können im synchronen Modus aufgerufen werden, indem der **wbemFlagReturnWhenComplete-Wert** im *iFlags-Parameter angegeben* wird.

### <a name="asynchronous-mode"></a>Asynchroner Modus

Der asynchrone Modus tritt auf, wenn das Programm oder Skript nach dem Aufruf der -Methode weiterhin ausgeführt wird. WMI gibt alle Objekte aus der -Methode an ein [**SWbemSink-Objekt**](swbemsink.md) zurück, wenn jedes Objekt erstellt wird. Das aufrufende Programm oder Skript muss über ein **SWbemSink-Objekt** und einen [**SWbemSink.OnObjectReady-Ereignishandler**](swbemsink-onobjectready.md) verfügen, um die zurückgegebenen Objekte zu verarbeiten. Weitere Informationen zum Erstellen eines Ereignishandlers für den asynchronen Modus finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

In diesem Modus gibt es zwar keine Leistungs- und Ressourcenstrafe des synchronen Modus, der asynchrone Modus kann jedoch zu schwerwiegenden Sicherheitsrisiken führen, da die im [**SWbemSink-Objekt**](swbemsink.md) gespeicherten Ergebnisse möglicherweise nicht aus dem aufrufenden Programm oder Skript stammen. WMI senkt die Authentifizierungsebene für das **SWbemSink-Objekt,** bis die Methode erfolgreich ist. Weitere Informationen zum Mindern dieser Sicherheitsrisiken finden Sie unter [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).

Methoden, die mit dem Wort Async angefügt werden, sind Methoden für den asynchronen Modus. Die folgenden Methoden sind asynchrone Aufrufe:

-   [**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices.DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices.InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices.ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Weitere Informationen zum asynchronen Modus finden Sie unter:

-   [Ausführen eines asynchronen Aufrufs mit C++](making-an-asynchronous-call-with-c--.md)
-   [Ausführen eines asynchronen Aufrufs mit VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Semisynchroner Modus

Der semisynchrone Modus ähnelt dem asynchronen Modus, da das Programm oder Skript nach dem Aufruf der -Methode weiterhin ausgeführt wird. Im semisynchronen Modus ruft WMI die Objekte im Hintergrund ab, während Ihr Skript oder Programm weiterhin ausgeführt wird. WMI gibt jedes Objekt zurück, das direkt nach dem Erstellen des Objekts an die aufrufende Methode zurückgegeben wird.

Da WMI das Objekt verwaltet, ist der semisynchrone Modus sicherer als der asynchrone Modus. Wenn Sie jedoch den semisynchronen Modus mit mehr als 1.000 Instanzen verwenden, kann der Instanzabruf die verfügbaren Ressourcen auslagern, was die Leistung des Programms oder Skripts und des Computers mithilfe des Programms oder Skripts beeinträchtigen kann. Jedes Objekt benötigt die erforderlichen Ressourcen, bis der Arbeitsspeicher freigegeben wird.

Um diese Bedingung zu umkehren, können Sie die -Methode mit dem *iFlags-Parameter* aufrufen, der mit den Flags **wbemFlagForwardOnly** und **wbemFlagReturnImmediately** festgelegt wurde, um WMI anweisen, ein vorwärts gerichtetes [**SWbemObjectSet**](swbemobjectset.md)zurückgibt. Ein vorwärts vorwärts geschaltetes **SWbemObjectSet** beseitigt das Leistungsproblem, das durch ein großes DataSet verursacht wird, indem der Arbeitsspeicher nach dem Aufzählen des Objekts frei wird.

Jede [**SWbemServices-Methode,**](swbemservices.md) die weder im synchronen noch im asynchronen Modus aufgerufen werden kann, wird im semisynchronen Modus aufgerufen.

Die folgenden Methoden werden im semisynchronen Modus aufgerufen:

-   [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices.Get**](swbemservices-get.md)
-   [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices.Put**](swbemservicesex-put.md)

Weitere Informationen zum semisynchronen Modus finden Sie unter Ausführen eines [semisynchronen](making-a-semisynchronous-call-with-c--.md) Aufrufs mit C++ und [Ausführen eines semisynchronen Aufrufs mit VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Enumerationsleistung](improving-enumeration-performance.md)
</dt> <dt>

[Skripterstellung mit SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
