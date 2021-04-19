---
description: Sie können die Methoden eines "Swap Services"-Objekts verwenden, um Vorgänge für einen Namespace auf einem lokalen Host oder einem Remote Host auszuführen. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: Taubemservices-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 4303b3226acc6d773ed35e77176e05e3a58c567d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372952"
---
# <a name="swbemservices-object"></a>Swap Services-Objekt

Sie können die Methoden eines " **Swap Services** "-Objekts verwenden, um Vorgänge für einen Namespace auf einem lokalen Host oder einem Remote Host auszuführen. Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **Swap Services** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **Swap Services** " verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Assoziatorsof**](swbemservices-associatorsof.md)                           | Ruft die Instanzen verwalteter Ressourcen, die einer angegebenen Ressource zugeordnet sind, über eine oder mehrere Zuordnungs Klassen ab. Sie geben den Objekt Pfad für den ursprünglichen Endpunkt an, und [**associatorsof**](swbemservices-associatorsof.md) gibt die verwalteten Ressourcen am gegenüberliegenden Endpunkt zurück. Die **associatorsof** -Methode führt die gleiche Funktion aus, die die "assoziatoren" der WQL-Abfrage ausführt.<br/>                                                                           |
| [**Associatorsofasync**](swbemservices-associatorsofasync.md)                 | Gibt asynchron eine Auflistung von-Objekten (Klassen oder Instanzen) zurück, die einem angegebenen Objekt zugeordnet sind.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Lösch**](swbemservices-delete.md)                                         | Löscht eine Instanz einer verwalteten Ressource (oder eine Klassendefinition aus dem CIM-Repository).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Löscht asynchron die Klasse oder Instanz, die im Objekt Pfad angegeben ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Bietet eine alternative Möglichkeit zum Ausführen einer Methode, die durch eine verwaltete Ressourcen Klassendefinition definiert wird. Wird hauptsächlich in Situationen verwendet, in denen die Skriptsprache keine out-Parameter unterstützt. JScript unterstützt z. b. keine out-Parameter.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Führt asynchron eine Methode aus, die von einem Methoden Anbieter exportiert wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Führt eine Ereignis Abonnement Abfrage aus, um Ereignisse zu empfangen. Bei einer Ereignis Abonnement Abfrage handelt es sich um eine Abfrage, die eine Änderung an der verwalteten Umgebung definiert, die Sie überwachen möchten. Wenn die Änderung auftritt, stellt die WMI-Infrastruktur ein Ereignis bereit, das die Änderung des aufrufenden Skripts beschreibt.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Führt asynchron eine Abfrage zum Empfangen von Ereignissen aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Führt eine Abfrage zum Abrufen einer Auflistung von Instanzen von WMI-verwalteten Ressourcen (oder Klassendefinitionen) aus. [**ExecQuery**](swbemservices-execquery.md) kann verwendet werden, um eine gefilterte Auflistung von Instanzen abzurufen, die mit den Kriterien übereinstimmen, die Sie in der an **ExecQuery** übergebenen Abfrage definieren.<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Führt asynchron eine Abfrage zum Abrufen von-Objekten aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Erhalten**](swbemservices-get.md)                                               | Ruft eine einzelne Instanz einer verwalteten Ressource (oder einer Klassendefinition) auf Grundlage eines Objekt Pfads ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**GetAsync**](swbemservices-getasync.md)                                     | Ruft asynchron ein-Objekt ab, das entweder eine Klassendefinition oder eine-Instanz ist, basierend auf dem Objekt Pfad.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | Ruft alle Instanzen einer verwalteten Ressource auf Grundlage eines Klassen namens ab. Standardmäßig führt [**InstancesOf**](swbemservices-instancesof.md) einen Deep-Abruf durch. Das heißt, **InstancesOf** Ruft die Instanzen der Ressource ab, die durch den an die-Methode übergebenen Klassennamen identifiziert wird, und ruft außerdem alle Instanzen aller Ressourcen ab, die Unterklassen (unten definiert) der Zielklasse sind.<br/>                                                                                       |
| [**Instancesofasync**](swbemservices-instancesofasync.md)                     | Gibt die Instanzen einer angegebenen Klasse asynchron gemäß den vom Benutzer angegebenen Auswahlkriterien zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Referencesto**](swbemservices-referencesto.md)                             | Gibt alle Zuordnungen zurück, die auf eine angegebene Ressource verweisen. Die beste Möglichkeit, um [**referencesto**](swbemservices-referencesto.md) nachzuvollziehen, besteht darin, Sie mit der [**associatorsof**](swbemservices-associatorsof.md) -Methode zu vergleichen. **Associatorsof** gibt die dynamischen Ressourcen zurück, die sich am gegenüberliegenden Ende einer Zuordnung befinden. **Referencesto** gibt die Zuordnung selbst zurück. Die **referencesto** -Methode führt die gleiche Funktion aus, die von der WQL-Abfrage "Verweise" durchführt.<br/> |
| [**Referencestoasync**](swbemservices-referencesto.md)                        | Gibt asynchron eine Auflistung aller Zuordnungs Klassen oder-Instanzen zurück, die auf eine bestimmte Klasse oder Instanz verweisen.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**Unterklassen von**](swbemservices-subclassesof.md)                             | Ruft alle Unterklassen einer angegebenen Klasse aus dem CIM-Repository ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Subclassesofasync**](swbemservices-subclassesofasync.md)                   | Gibt asynchron eine Auflistung von Unterklassen für eine angegebene Klasse zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Swap Services** " verfügt über diese Eigenschaften.



| Eigenschaft                                                 | Zugriffstyp          | BESCHREIBUNG                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Sicherheit\_**](swbemservices-security-.md)<br/> | Schreibgeschützt<br/> | Wird verwendet, um die Sicherheitseinstellungen für ein **Swap Services** -Objekt zu erhalten oder festzulegen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die-Methoden können entweder im synchronen Modus, im asynchronen Modus oder im semisynchronen Modus aufgerufen werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

**Übersicht**

Die **Austauschdienste** dienen zwei Hauptrollen. Zuerst stellt das Objekt " **Swap Services** " eine authentifizierte Verbindung mit einem WMI-Namespace auf einem Bereitstellungs Zielcomputer dar. Zum anderen handelt es sich bei " **Swap Services** " um das Automatisierungs Objekt, das Sie zum Abrufen von WMI-verwalteten Ressourcen verwenden. Sie können auf eine von zwei Arten einen Verweis auf ein-Objekt vom Typ "- **blobemservices** " abrufen:

-   Wie in den meisten bisher vorgestellten WMI-Skripts gezeigt, können Sie die Funktion "VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) " in Kombination mit dem WMI-Moniker "winmgmts:" verwenden. Das folgende Beispiel ist die einfachste Form einer WMI-Verbindung. Das Beispiel stellt eine Verbindung mit dem Standard Namespace (in der Regel "root \\ CIMv2") auf dem lokalen Computer her:

    `Set objSWbemServices = GetObject("winmgmts:")`

-   Sie können auch die [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode des " [**Swap-Locator**](swbemlocator.md) "-Objekts verwenden, um einen Verweis auf ein " **Swap Services** "-Objekt zu erhalten.

Nachdem Sie einen Verweis auf ein Objekt vom Typ " **Swap Services** " abgerufen haben, rufen Sie mit dem Objekt Verweis 1 von 18 Methoden auf, die mit " **Swap Services**" verfügbar sind. Die **Austauschdienste** können je nach der von Ihnen aufzurufenden Methode eines von drei verschiedenen WMI-skriptingbibliotheks-Objekten ("errbewbjectset", " [**errbewbject**](swbemobject.md)" oder " [**taubemeventsource**](swbemeventsource.md)") zurückgeben.[](swbemobjectset.md) Wenn Sie den Objekttyp kennen, den jede Methode zurückgibt, können Sie den nächsten Schritt bestimmen, den das Skript ausführen muss. Wenn Sie z. b. ein " **errbewbjectset**" zurückgeben, müssen Sie die Auflistung auflisten, um auf die einzelnen "Swap"- **Objekte** in der Auflistung zuzugreifen. Wenn Sie ein **Swap**-Objekt zurückerhalten, können Sie sofort auf die Objektmethoden und-Eigenschaften zugreifen, ohne zuerst die Auflistung aufzählen zu müssen.

**Betriebsmodi**

" **Swap Services** " unterstützt drei Betriebsmodi: "synchron", "asynchron" und "SemiSynchron".

-   **Synchron**. Im synchronen Modus wird das Skript blockiert (hält), bis die Methode " **Swap Services** " abgeschlossen ist. Das Skript wartet nicht nur, aber in Fällen, in denen WMI Instanzen von verwalteten Ressourcen abruft, erstellt WMI das gesamte " [**errbewbjectset**](swbemobjectset.md) " im Arbeitsspeicher, bevor das erste Byte der Daten an das aufrufenden Skript zurückgegeben wird. Dies kann sich negativ auf die Skript Leistung und auf dem Computer auswirken, auf dem das Skript ausgeführt wird. Beispielsweise kann das synchrone abrufen Tausender Ereignisse aus den Windows-Ereignisprotokollen eine lange Zeit in Anspruch nehmen und viel Arbeitsspeicher beanspruchen. Aus diesen Gründen werden synchrone Vorgänge außer den drei Methoden ([**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)und [**Get**](swbemservices-get.md)), die standardmäßig synchron sind, nicht empfohlen. Diese Methoden geben keine großen Datasets zurück, weshalb ein semisynchroner Vorgang nicht erforderlich ist.
-   **Asynchron**. Im asynchronen Modus Ruft das Skript eine der neun asynchronen Methoden auf und gibt sofort zurück. Das heißt, sobald die asynchrone Methode aufgerufen wird, wird Ihr Skript fortgesetzt, wenn die nächste Codezeile ausgeführt wird. Um eine asynchrone Methode zu verwenden, muss Ihr Skript zunächst ein " [**slibemsink**](swbemsink.md) "-Objekt und eine spezielle Unterroutine erstellen, die als Ereignishandler bezeichnet wird. WMI führt den asynchronen Vorgang aus und benachrichtigt das Skript, indem die ereignishandlerunterroutine aufgerufen wird, wenn der Vorgang beendet ist.
-   **SemiSynchron**. Beim semisynchronen Modus handelt es sich um einen Kompromiss zwischen synchronen und asynchronen. Semisynchrone Vorgänge bieten eine bessere Leistung als synchrone Vorgänge, erfordern jedoch nicht die zusätzlichen Wissens-und Skript Schritte, die erforderlich sind, um asynchrone Vorgänge zu verarbeiten. Dies ist der Standard Vorgangstyp für die meisten WMI-Abfragen.

    Im semisynchronen Modus Ruft das Skript eine der sechs Datenabruf Methoden auf und gibt sofort zurück. WMI Ruft die verwalteten Ressourcen im Hintergrund ab, während das Skript weiterhin ausgeführt wird. Wenn die Ressourcen abgerufen werden, werden Sie sofort mithilfe von "errbemubjectset" an das Skript zurückgegeben. Sie können mit dem Zugriff auf die verwalteten Ressourcen beginnen, ohne zu warten, bis die gesamte Sammlung zusammengestellt wird.

    Bei der Arbeit mit verwalteten Ressourcen, die viele Instanzen aufweisen (viele Bedeutungen größer als 1.000), gibt es einen Vorbehalt bei semisynchronen Vorgängen, wie z. b. [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) und [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Der Nachteil ist, dass WMI Instanzen verwalteter Ressourcen behandelt. Für jede Instanz einer verwalteten Ressource erstellt und speichert WMI ein " [**errbewbject**](swbemobject.md) "-Objekt. Wenn eine große Anzahl von Instanzen für eine verwaltete Ressource vorhanden ist, kann der Instanzabruf verfügbare Ressourcen monopolisieren, wodurch die Leistung des Skripts und des Computers verringert wird.

    Um das Problem zu umgehen, können Sie semisynchrone Methodenaufrufe mit dem **wbemFlagForwardOnly** -Flag optimieren. Das Flag **wbemFlagForwardOnly** , in Kombination mit dem **wbemFlagReturnImmediately** -Flag (das standardsemisynchrone Flag), weist WMI an, einen vorwärts gerichteten " [**errbeantibjectset**](swbemobjectset.md)" zurückzugeben, wodurch das große DataSet-Leistungsproblem beseitigt wird. Die Verwendung des Flags " **wbemFlagForwardOnly** " ist jedoch mit Kosten verbunden. Ein vorwärts gesteuerter " **errbewbjectset** " kann nur einmal aufgezählt werden. Nachdem auf die einzelnen [**Austausch**](swbemobject.md) Vorgänge in einem vorwärts gerichteten " **errbewbjectset** " zugegriffen wurde, wird der der Instanz zugeordnete Arbeitsspeicher freigegeben.

Mit Ausnahme der asynchronen Methoden [**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md), [**Get**](swbemservices-get.md)und Nine ist SemiSynchron der standardmäßige und empfohlene Betriebsmodus.

**Häufig verwendete Methoden**

Zu den am häufigsten in System Verwaltungs Skripts verwendeten Methoden gehören " [**InstancesOf**](swbemservices-instancesof.md)", " [**ExecQuery**](swbemservices-execquery.md)", " [**Get**](swbemservices-get.md)" und " [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)". Obwohl es häufig verwendet wird, ist **InstancesOf** nicht notwendigerweise die empfohlene Vorgehensweise zum Abrufen von Informationen (obwohl dies wohl die einfachste Methode ist).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschdienste<br/>                                                         |
| IID<br/>                      | IID \_ iswbemservices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

