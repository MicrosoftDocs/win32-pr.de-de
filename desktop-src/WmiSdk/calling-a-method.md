---
description: WMI stellt Methoden in der com-API und der Skript-API bereit, um Informationen zu erhalten oder Objekte in einem Unternehmenssystem zu bearbeiten.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Aufrufen einer WMI-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353997"
---
# <a name="calling-a-wmi-method"></a>Aufrufen einer WMI-Methode

WMI stellt Methoden in der [com-API](com-api-for-wmi.md) und der [Skript-API](scripting-api-for-wmi.md) bereit, um Informationen zu erhalten oder Objekte in einem Unternehmenssystem zu bearbeiten. Die WMI-Skript MethodeSWbemServices.Exez. b. [**cquery**](swbemservices-execquery.md) -Abfragen für-Daten. Außerdem verfügen Anbieter über Methoden, die in den von Ihnen registrierten Klassen definiert sind. Beispiele hierfür sind [**die Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Methoden [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) und [**scheduleautochk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) , die vom [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider)bereitgestellt werden.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [WMI-Methoden im Vergleich zu Anbieter Methoden](#wmi-methods-compared-to-provider-methods)
-   [Methodenaufruf Modi in WMI](#method-calling-modes-in-wmi)
    -   [Synchroner Modus](#synchronous-mode)
    -   [Asynchroner Modus](#asynchronous-mode)
    -   [Semisynchroner Modus](#semisynchronous-mode)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>WMI-Methoden im Vergleich zu Anbieter Methoden

Durch die Verwendung von [*WMI-Methoden*](gloss-w.md) aufrufen in Kombination mit [*Anbieter Methoden*](gloss-p.md) aufrufen können Sie Informationen zu Ihrem Unternehmen abrufen und bearbeiten. Weitere Informationen finden Sie unter [Aufrufen einer WMI-Methode](calling-a-wmi-method.md) und [Aufrufen einer Anbieter Methode](calling-a-provider-method.md).

Die Methoden des WMI-Skript Objekts " [**errbewbject**](swbemobject.md) " haben einen besonderen Status, da Sie auf jede beliebige WMI-Datenklasse angewendet werden können. Weitere Informationen finden Sie unter [Skripterstellung mit "Swap](scripting-with-swbemobject.md)".

Im folgenden Codebeispiel werden sowohl WMI-als auch Provider-Methoden aufgerufen.

Die folgenden WMI-und Anbieter Methoden befinden sich in der [Skript-API für WMI](scripting-api-for-wmi.md):

-   **objWMIService.Execquery** Ruft die WMI-Skript Methode [ **SWbemServices.Execquery** auf.](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objservice. StopService ()** Ruft die Anbieter Methode [ **Win32 \_ Service. Stop Service auf.**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Sie können den Code suchen, der im Abschnitt "Rückgabe Codes" für den [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)möglicherweise im Abschnitt "Return" angezeigt wird.


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





## <a name="method-calling-modes-in-wmi"></a>Method-Calling Modi in WMI

Der semisynchrone Aufruf Modus bietet in der Regel das beste Gleichgewicht zwischen Sicherheit und Leistung.

Weitere Informationen zu den einzelnen möglichen Modi finden Sie in den folgenden Bereichen:

-   [Synchron](#synchronous-mode)
-   [Asynchron](#asynchronous-mode)
-   [Halb synchron](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Synchroner Modus

Der synchrone Modus tritt auf, wenn das Programm oder die Skripts angehalten werden, bis der Methoden aufzurufende das Objekt " [**errbewbjectset**](swbemobjectset.md) WMI erstellt diese Auflistung im Arbeitsspeicher, bevor das Auflistungs Objekt an das aufrufende Programm oder Skript zurückgegeben wird.

Der synchrone Modus kann sich auf den Computer, auf dem das Programm oder das Skript ausgeführt wird, negativ auf die Programm-oder Skript Leistung auswirken Beispielsweise kann das synchrone abrufen Tausender Ereignisse aus dem Ereignisprotokoll sehr lange dauern und viel Arbeitsspeicher beanspruchen, da WMI ein Objekt aus jedem Ereignis erstellt und diese Objekte dann in eine Auflistung einfügt, bevor die Auflistung an die-Methode übergeben wird.

Sie sollten nur Methoden aufzurufen, die keine großen Datasets im synchronen Modus zurückgeben. Die folgenden " [**Swap Services**](swbemservices.md) "-Methoden können im synchronen Modus sicher aufgerufen werden:

-   [**Swap Services. Delete**](swbemservices-delete.md)
-   [**SWbemServices.Execmethod**](swbemservices-execmethod.md)
-   [**Austauschdienste. Get**](swbemservices-get.md)

Alle "Async"- [**Methoden ohne das**](swbemservices.md) Wort "Async" im Namen können im synchronen Modus aufgerufen werden, indem der Wert " **wbemflagreturneincomplete** " im *IFlags* -Parameter festgelegt wird.

### <a name="asynchronous-mode"></a>Asynchroner Modus

Der asynchrone Modus tritt auf, wenn das Programm oder Skript nach dem Aufrufen der-Methode weiter ausgeführt wird. WMI gibt bei der Erstellung jedes Objekts alle Objekte aus der-Methode in ein " [**taubemsink**](swbemsink.md) "-Objekt zurück. Das aufrufende Programm oder Skript muss ein " **slibemsink** "-Objekt und einen " [**slibemsink. onobjectready**](swbemsink-onobjectready.md) "-Ereignishandler aufweisen, um die zurückgegebenen Objekte zu verarbeiten. Weitere Informationen zum Erstellen eines Ereignis Handlers für den asynchronen Modus finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

In diesem Modus gibt es nicht die Leistungs-und Ressourcen Einbuße des synchronen Modus, aber der asynchrone Modus kann zu ernsthaften Sicherheitsrisiken führen, da die im " [**Swap**](swbemsink.md) "-Objekt gespeicherten Ergebnisse möglicherweise nicht aus dem aufrufenden Programm oder Skript stammen. WMI senkt die Authentifizierungs Ebene für das Objekt " **taubemsink** ", bis die Methode erfolgreich ist. Weitere Informationen zum mindern dieser Sicherheitsrisiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Mit dem Wort "Async" angefügte Methoden sind Methoden für den asynchronen Modus. Die folgenden Methoden sind asynchrone Aufrufe:

-   [**Swap Services. associatorsofasync**](swbemservices-associatorsofasync.md)
-   [**"Swap Services. deleteasync"**](swbemservices-deleteasync.md)
-   [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md)
-   [**CqueryasyncSWbemServices.Exe**](swbemservices-execqueryasync.md)
-   [**Swap Services. instancesofasync**](swbemservices-instancesofasync.md)
-   [**"Swap Services. referencestoasync"**](swbemservices-referencesto.md)
-   [**Austausch Services. subclassesofasync**](swbemservices-subclassesofasync.md)

Weitere Informationen zum asynchronen Modus finden Sie unter:

-   [Erstellen eines asynchronen Aufrufes mit C++](making-an-asynchronous-call-with-c--.md)
-   [Erstellen eines asynchronen Aufrufes mit VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Semisynchroner Modus

Der semisynchrone Modus ähnelt dem asynchronen Modus, da das Programm oder Skript nach dem Aufrufen der-Methode weiterhin ausgeführt wird. Im semisynchronen Modus ruft WMI die Objekte im Hintergrund ab, während das Skript oder Programm weiterhin ausgeführt wird. WMI gibt jedes Objekt zurück, das direkt nach dem Erstellen des-Objekts an die Aufruf Methode zurückgegeben wurde.

Da das Objekt von WMI verwaltet wird, ist der semisynchrone Modus sicherer als der asynchrone Modus. Wenn Sie jedoch den semisynchronen Modus mit mehr als 1.000 Instanzen verwenden, kann der Instanzabruf die verfügbaren Ressourcen monopolisieren, wodurch die Leistung des Programms oder Skripts und des Computers mithilfe des Programms oder Skripts beeinträchtigt werden kann. Jedes-Objekt benötigt die erforderlichen Ressourcen, bis der Arbeitsspeicher freigegeben wird.

Um diese Bedingung zu umgehen, können Sie die-Methode mit dem *IFlags* -Parameter festlegen, der mit den **wbemFlagForwardOnly** -und **wbemFlagReturnImmediately** -Flags festgelegt ist, um WMI anzuweisen, ein vorwärts geschütztes-Objekt vom Typ " [**Swap**](swbemobjectset.md)-only" zurückzugeben. Ein vorwärts gesteuerter " **errbewbjectset** " entfernt das von einem großen Dataset verursachte Leistungsproblem, indem der Arbeitsspeicher freigegeben wird, nachdem das Objekt aufgezählt wurde.

Jede [**Methode, die nicht im**](swbemservices.md) synchronen oder asynchronen Modus aufgerufen werden kann, wird im semisynchronen Modus aufgerufen.

Die folgenden Methoden werden im semisynchronen Modus aufgerufen:

-   [**"Taubemservices. associatorsof"**](swbemservices-associatorsof.md)
-   [**Swap Services. Delete**](swbemservices-delete.md)
-   [**SWbemServices.Execmethod**](swbemservices-execmethod.md)
-   [**CnotificationquerySWbemServices.Exe**](swbemservices-execnotificationquery.md)
-   [**CquerySWbemServices.Exe**](swbemservices-execquery.md)
-   [**Austauschdienste. Get**](swbemservices-get.md)
-   [**Swap Services. InstancesOf**](swbemservices-instancesof.md)
-   [**"Swap Services. referencesto"**](swbemservices-referencesto.md)
-   [**Swap Services. SubclassesOf**](swbemservices-subclassesof.md)
-   [**Swap Services. Put**](swbemservicesex-put.md)

Weitere Informationen zum semisynchronen Modus finden Sie unter [Erstellen eines semisynchronen Aufrufes mit C++](making-a-semisynchronous-call-with-c--.md) und [Erstellen eines semisynchronen Aufrufes mit VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der enumerationsleistung](improving-enumeration-performance.md)
</dt> <dt>

[Skripterstellung mit "errbemuject"](scripting-with-swbemobject.md)
</dt> <dt>

[**Wbemflagenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
