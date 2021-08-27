---
description: Sie können die Methoden eines SWbemServices-Objekts verwenden, um Vorgänge für einen Namespace auf einem lokalen Host oder einem Remotehost durchzuführen. Dieses Objekt kann nicht durch den VBScript CreateObject-Aufruf erstellt werden.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: SWbemServices-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices
- ISWbemServices
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9a8a73dbe85ce806d955329df3362a8b17dd48cc530939ec2f94ffcff2074614
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097140"
---
# <a name="swbemservices-object"></a>SWbemServices-Objekt

Sie können die Methoden eines **SWbemServices-Objekts** verwenden, um Vorgänge für einen Namespace auf einem lokalen Host oder einem Remotehost durchzuführen. Dieses Objekt kann nicht durch den VBScript **CreateObject-Aufruf erstellt** werden.

## <a name="members"></a>Member

Das **SWbemServices-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemServices-Objekt** verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | Ruft die Instanzen verwalteter Ressourcen ab, die einer angegebenen Ressource über eine oder mehrere Zuordnungsklassen zugeordnet sind. Sie geben den Objektpfad für den ursprünglichen Endpunkt an, und [**AssociatorsOf**](swbemservices-associatorsof.md) gibt die verwalteten Ressourcen am entgegengesetzten Endpunkt zurück. Die **AssociatorsOf-Methode** führt dieselbe Funktion aus wie die WQL-Abfrage "ASSOCIATORS OF".<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | Gibt asynchron eine Auflistung von -Objekten (Klassen oder Instanzen) zurück, die einem angegebenen -Objekt zugeordnet sind.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Löschen**](swbemservices-delete.md)                                         | Löscht eine Instanz einer verwalteten Ressource (oder einer Klassendefinition aus dem CIM-Repository).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Löscht die Im Objektpfad angegebene Klasse oder Instanz asynchron.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Stellt eine alternative Möglichkeit zum Ausführen einer Methode dar, die durch eine Definition einer verwalteten Ressourcenklasse definiert ist. Wird hauptsächlich in Situationen verwendet, in denen die Skriptsprache keine Parameter unterstützt. Beispielsweise unterstützt JScript Parameter nicht.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Führt eine Methode, die von einem Methodenanbieter exportiert wird, asynchron aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Führt eine Ereignisabonnementabfrage aus, um Ereignisse zu empfangen. Eine Ereignisabonnementabfrage ist eine Abfrage, die eine Änderung an der verwalteten Umgebung definiert, die Sie überwachen möchten. Wenn die Änderung auftritt, stellt die WMI-Infrastruktur ein Ereignis zur Verfügung, das die Änderung an das aufrufende Skript beschreibt.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Führt eine Abfrage asynchron aus, um Ereignisse zu empfangen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Führt eine Abfrage aus, um eine Auflistung von Instanzen von WMI-verwalteten Ressourcen (oder Klassendefinitionen) abzurufen. [**ExecQuery**](swbemservices-execquery.md) kann verwendet werden, um eine gefilterte Auflistung von -Instanzen abzurufen, die Kriterien erfüllen, die Sie in der an **ExecQuery übergebenen Abfrage definieren.**<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Führt eine Abfrage asynchron aus, um Objekte abzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Erhalten**](swbemservices-get.md)                                               | Ruft eine einzelne Instanz einer verwalteten Ressource (oder Klassendefinition) basierend auf einem Objektpfad ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**GetAsync**](swbemservices-getasync.md)                                     | Ruft ein Objekt, bei dem es sich entweder um eine Klassendefinition oder eine -Instanz handelt, basierend auf dem Objektpfad asynchron ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | Ruft alle Instanzen einer verwalteten Ressource basierend auf einem Klassennamen ab. Standardmäßig führt [**InstancesOf einen**](swbemservices-instancesof.md) tiefen Abruf durch. Das heißt, **InstancesOf** ruft die Instanzen der Ressource ab, die durch den Klassennamen identifiziert werden, der an die -Methode übergeben wird, und ruft auch alle Instanzen aller Ressourcen ab, die Unterklassen (unterhalb definiert) der Zielklasse sind.<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | Gibt die Instanzen einer angegebenen Klasse gemäß den vom Benutzer angegebenen Auswahlkriterien asynchron zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ReferencesTo**](swbemservices-referencesto.md)                             | Gibt alle Zuordnungen zurück, die auf eine angegebene Ressource verweisen. Die beste Möglichkeit, [**ReferencesTo zu verstehen,**](swbemservices-referencesto.md) ist der Vergleich mit der [**AssociatorsOf-Methode.**](swbemservices-associatorsof.md) **AssociatorsOf gibt** die dynamischen Ressourcen zurück, die sich am entgegengesetzten Ende einer Zuordnung befinden. **ReferencesTo gibt** die Zuordnung selbst zurück. Die **ReferencesTo-Methode** führt dieselbe Funktion aus wie die WQL-Abfrage "REFERENCES OF".<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | Gibt asynchron eine Auflistung aller Zuordnungsklassen oder Instanzen zurück, die auf eine bestimmte Klasse oder Instanz verweisen.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**SubclassesOf**](swbemservices-subclassesof.md)                             | Ruft alle Unterklassen einer angegebenen Klasse aus dem CIM-Repository ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UnterklassenOfAsync**](swbemservices-subclassesofasync.md)                   | Gibt asynchron eine Auflistung von Unterklassen für eine angegebene Klasse zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemServices-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                 | Zugriffstyp          | BESCHREIBUNG                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Sicherheit\_**](swbemservices-security-.md)<br/> | Schreibgeschützt<br/> | Wird verwendet, um die Sicherheitseinstellungen für ein **SWbemServices-Objekt zu** erhalten oder zu festlegen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Methoden können entweder im synchronen Modus, im asynchronen Modus oder im semisynchronen Modus aufgerufen werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

**Übersicht**

**SWbemServices dient** zwei Hauptrollen. Zunächst stellt das **SWbemServices-Objekt** eine authentifizierte Verbindung mit einem WMI-Namespace auf einem Zielcomputer dar. Zweitens ist **SWbemServices das** Automation-Objekt, das Sie zum Abrufen von WMI-verwalteten Ressourcen verwenden. Sie können einen Verweis auf ein **SWbemServices-Objekt** auf zwei Arten abrufen:

-   Wie in den meisten der bisher vorgestellten WMI-Skripts gezeigt, können Sie die VBScript [**GetObject-Funktion**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) in Kombination mit dem WMI-Moniker "winmgmts:" verwenden. Das folgende Beispiel ist die einfachste Form einer WMI-Verbindung. Im Beispiel wird eine Verbindung mit dem Standardnamespace (in der Regel "Root \\ CIMv2") auf dem lokalen Computer erstellt:

    `Set objSWbemServices = GetObject("winmgmts:")`

-   Sie können auch die [**ConnectServer-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) [**des SWbemLocator-Objekts**](swbemlocator.md) verwenden, um einen Verweis auf ein **SWbemServices-Objekt zu** erhalten.

Nachdem Sie einen Verweis auf ein **SWbemServices-Objekt** erhalten haben, rufen Sie mithilfe des Objektverweises 1 von 18 Methoden auf, die mithilfe von **SWbemServices verfügbar sind.** **SWbemServices** kann je nach aufgerufener Methode eines von drei verschiedenen WMI-Skriptbibliotheksobjekten [**(SWbemObjectSet,**](swbemobjectset.md) [**SWbemObject**](swbemobject.md)oder [**SWbemEventSource)**](swbemeventsource.md)zurückgeben. Wenn Sie den Typ des Objekts kennen, das von jeder Methode zurückgegeben wird, können Sie den nächsten Schritt ermitteln, den Ihr Skript ausführen muss. Wenn Sie beispielsweise ein **SWbemObjectSet-Objekt** zurückerstellen, müssen Sie die Auflistung aufzählen, um auf **jedes SWbemObject** in der Sammlung zu zugreifen. Wenn Sie ein **SWbemObject-Objekt** erhalten, können Sie sofort auf die Objektmethoden und -eigenschaften zugreifen, ohne zuerst die Auflistung aufzählen zu müssen.

**Betriebsmodi**

**SWbemServices unterstützt** drei Betriebsmodi: synchron, asynchron und semisynchron.

-   **Synchron.** Im synchronen Modus wird Ihr Skript blockiert (angehalten), bis die **SWbemServices-Methode** abgeschlossen ist. Das Skript wartet nicht nur, sondern in Fällen, in denen WMI Instanzen verwalteter Ressourcen abruft, erstellt WMI das gesamte [**SWbemObjectSet**](swbemobjectset.md) im Arbeitsspeicher, bevor das erste Byte der Daten an das aufrufende Skript zurückgegeben wird. Dies kann sich negativ auf die Skriptleistung und auf den Computer auswirken, auf dem das Skript ausgeführt wird. Beispielsweise kann das synchrone Abrufen von Tausenden von Ereignissen aus den Windows-Ereignisprotokollen sehr lange dauern und viel Arbeitsspeicher nutzen. Aus diesen Gründen werden synchrone Vorgänge nicht empfohlen, mit Ausnahme der drei Methoden ([**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)und [**Get**](swbemservices-get.md)), die standardmäßig synchron sind. Diese Methoden geben keine großen Datensätze zurück, sodass kein semisynchroner Vorgang erforderlich ist.
-   **Asynchron.** Im asynchronen Modus ruft Ihr Skript eine der neun asynchronen Methoden auf und gibt sofort zurück. Das heißt, sobald die asynchrone Methode aufgerufen wird, setzt Ihr Skript die Ausführung der nächsten Codezeile wieder ein. Um eine asynchrone Methode zu verwenden, muss Ihr Skript zunächst ein [**SWbemSink-Objekt**](swbemsink.md) und eine spezielle Unterroutine erstellen, die als Ereignishandler bezeichnet wird. WMI führt den asynchronen Vorgang aus und benachrichtigt das Skript, indem die Unterroutine des Ereignishandlers aufgerufen wird, wenn der Vorgang abgeschlossen ist.
-   **Semisynchrones**. Der semisynchrone Modus ist eine Kompromittierung zwischen synchron und asynchron. Semisynchrone Vorgänge bieten eine bessere Leistung als synchrone Vorgänge, erfordern jedoch nicht die zusätzlichen Kenntnisse und Skriptschritte, die für die Verarbeitung asynchroner Vorgänge erforderlich sind. Dies ist der Standardvorgang für die meisten WMI-Abfragen.

    Im semisynchronen Modus ruft Ihr Skript eine der sechs Datenabrufmethoden auf und kehrt sofort zurück. WMI ruft die verwalteten Ressourcen im Hintergrund ab, während Ihr Skript weiterhin ausgeführt wird. Wenn die Ressourcen abgerufen werden, werden sie sofort über ein SWbemObjectSet an Ihr Skript zurückgegeben. Sie können mit dem Zugriff auf die verwalteten Ressourcen beginnen, ohne darauf zu warten, dass die gesamte Sammlung zusammengestellt wird.

    Bei der Arbeit mit verwalteten Ressourcen mit vielen Instanzen (viele Bedeutungen größer als 1.000), z. B. [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) und [**Win32 \_ NTLogEvent,**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)besteht ein Nachteil bei semisynchronen Vorgängen. Der Nachteil ist das Ergebnis der Art und Weise, wie WMI Instanzen verwalteter Ressourcen behandelt. Für jede Instanz einer verwalteten Ressource erstellt WMI ein [**SWbemObject-Objekt**](swbemobject.md) und speichert es zwischen. Wenn eine große Anzahl von Instanzen für eine verwaltete Ressource vorhanden ist, kann der Instanzabruf verfügbare Ressourcen überlagern, was die Leistung des Skripts und des Computers verringert.

    Um das Problem zu beheben, können Sie semisynchrone Methodenaufrufe mithilfe des **Flags wbemFlagForwardOnly** optimieren. Das **Flag wbemFlagForwardOnly** in Kombination mit dem **Flag wbemFlagReturnImmediately** (dem standardmäßigen semisynchronen Flag) weist WMI an, ein vorwärts gerichtetes [**SWbemObjectSet**](swbemobjectset.md)zurückzurücken, wodurch das Leistungsproblem bei großen Datensets beseitigt wird. Die Verwendung des **Flags wbemFlagForwardOnly** hat jedoch Kosten. Ein vorwärts orientiertes **SWbemObjectSet** kann nur einmal aufzählt werden. Nachdem auf [**jedes SWbemObject**](swbemobject.md) in einem vorwärts orientierten **SWbemObjectSet** zugegriffen wurde, wird der der Instanz zugeordnete Arbeitsspeicher freigegeben.

Mit Ausnahme der asynchronen [**Methoden Delete,**](swbemservices-delete.md) [**ExecMethod,**](swbemservices-execmethod.md) [**Get**](swbemservices-get.md)und neun ist semisynchron der standardmäßige und empfohlene Betriebsmodus.

**Häufig verwendete Methoden**

Die methoden, die am häufigsten in Systemverwaltungsskripts verwendet werden, sind [**InstancesOf,**](swbemservices-instancesof.md) [**ExecQuery,**](swbemservices-execquery.md) [**Get**](swbemservices-get.md)und [**ExecNotificationQuery.**](swbemservices-execnotificationquery.md) Obwohl **instancesOf** häufig verwendet wird, ist dies nicht unbedingt die empfohlene Methode zum Abrufen von Informationen (obwohl dies wohl die einfachste Möglichkeit ist).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

