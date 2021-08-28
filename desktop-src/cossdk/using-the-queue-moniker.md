---
description: Der Warteschlangenmoniker wird verwendet, um eine Warteschlangenkomponente programmgesteuert zu aktivieren.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Verwenden des Warteschlangenmonikers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938b4c0c8afc19e953d7f62f17f95bbd63f387e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473686"
---
# <a name="using-the-queue-moniker"></a>Verwenden des Warteschlangenmonikers

Der Warteschlangenmoniker wird verwendet, um eine Warteschlangenkomponente programmgesteuert zu aktivieren. Der Warteschlangenmoniker erfordert, dass er die Klassen-ID (CLSID) des Objekts erhält, das direkt rechts vom neuen Moniker aufgerufen werden soll. Wenn der neue Moniker links vorangestellt ist, übergibt er die CLSID an den Moniker links davon.

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Der GetObject-Anzeigenamenparameter ist "queue:/new:", gefolgt von der Programm-ID oder Zeichenfolgen-GUID mit oder ohne geschweifte Klammern des zu instanziierten Serverobjekts. Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem Warteschlangenmoniker:

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a>C/C++

Der [**Parameter für den CoGetObject-Anzeigenamen**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) ist "queue:/new:", gefolgt von der Programm-ID oder Zeichenfolgen-GUID mit oder ohne geschweifte Klammern des zu instanziierten Serverobjekts. Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem Warteschlangenmoniker:

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a>Hinweise

Der Warteschlangenmoniker akzeptiert optionale Parameter, die die Eigenschaften der nachricht ändern, die an Message Queuing. Um beispielsweise zu bewirken, dass Message Queuing Nachricht mit der Priorität 6 gesendet wird, wird die in der Warteschlange enthaltene Komponente wie folgt aktiviert:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

In der folgenden Tabelle sind die Warteschlangenmonikerparameter aufgeführt, die sich auf die Zielwarteschlange auswirken.




| Parameter | BESCHREIBUNG | 
|-----------|-------------|
| <em>ComputerName</em><br /> | Gibt den Computernamenteil eines Message Queuing Warteschlangenpfads an. Der Message Queuing Name des Warteschlangenpfads ist als <em>ComputerName QueueName</em> \<em> formatiert. </em> Wenn nicht angegeben, wird der Computername verwendet, der der konfigurierten Anwendung zugeordnet ist.<br /> | 
| <em>QueueName</em><br /> | Gibt den Namen Message Queuing Warteschlange an. Der Message Queuing Name des Warteschlangenpfads ist als <em>ComputerName QueueName</em> \<em> formatiert. </em> Wenn nichts angegeben ist, wird der Warteschlangenname verwendet, der der konfigurierten Anwendung zugeordnet ist.<br /> Um eine nicht transaktionale Warteschlange zu erhalten, können Sie zuerst den Warteschlangennamen angeben und dann eine COM+-Anwendung mit demselben Namen erstellen.<br /> | 
| <em>PathName</em><br /> | Gibt den vollständigen namen Message Queuing Warteschlangenpfad an. Wenn kein Wert angegeben wird, Message Queuing name des Warteschlangenpfads verwendet, der der konfigurierten Anwendung zugeordnet ist. Um den Zielnamen zu überschreiben, kann der Pfad in der folgenden Form für eine Message Queuing arbeitsgruppeninstallation angegeben werden:<br /> Warteschlange:<em>PathName</em> = <em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass<br /><blockquote>[!Note]<br />Sowohl die Programmiersprachen C als auch Microsoft Visual C++ erfordern zwei gegensätzlichen Schrägstriche, um einen gegensätzlichen Schrägstrich innerhalb von Zeichenfolgenliteralen darstellen zu können, z. B. \\ Chicago-Gehaltsabrechnung.</blockquote><br /> | 
| <em>Formatname</em><br /> | Wenn Sie eine COM+-Anwendung als in die Warteschlange gestellt markieren, erstellt COM+ eine Message Queuing-Warteschlange, deren Name mit der Anwendung identisch ist. Der Message Queuing Formatname dieser Warteschlange befindet sich im COM+-Katalog, der der COM+-Anwendung zugeordnet ist. Um den Zielnamen zu überschreiben, kann der Formatname in der folgenden Form für eine Message Queuing arbeitsgruppeninstallation angegeben werden:<br /> Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId<br /> In einer Active Directory-Konfiguration wird "PRIVATE$" nicht als Teil des Warteschlangennamens angegeben. <br /> | 




 

> [!Note]  
> Optionale Warteschlangenmonikerparameter werden von links nach rechts verarbeitet. Geben Sie jedes Schlüsselwort nur einmal an. Wenn Sie den *PathName-Parameter* angeben, werden sowohl die *Parameter ComputerName als* auch *QueueName* ersetzt. Ein bestimmter *FormatName-Parameter* löscht vorherige Kenntnisse eines *ComputerName-,* *QueueName-* und *PathName-Parameters.*

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Zuordnen des Listeners für Warteschlangenkomponenten zu einer bestimmten privaten Warteschlange

Der COM+-Listener für Warteschlangenkomponenten empfängt nur von Warteschlangen, die der als in Warteschlange markierten COM+-Anwendung zugeordnet sind. Wenn Sie eine COM+-Anwendung als in die Warteschlange gestellt markieren, erstellt COM+ eine Message Queuing-Warteschlange, deren Name mit der Anwendung identisch ist. Der Message Queuing Formatname dieser Warteschlange befindet sich im COM+-Katalog, der der COM+-Anwendung zugeordnet ist. Wenn die COM+-Anwendung gestartet und als lauschend markiert wird, wird ein Listener im COM+-Anwendungsprozess gestartet und die Warteschlange geöffnet. In der folgenden Tabelle sind die Warteschlangenmonikerparameter aufgeführt, die sich auf die Message Queuing auswirken.




| Parameter | BESCHREIBUNG | 
|-----------|-------------|
| <em>AppSpecific</em><br /> | Gibt eine ganze Zahl ohne Vorzeichen an, z. B. AppSpecific=12345.<br /> | 
| <em>AuthLevel</em><br /> | Gibt die Nachrichtenauthentifizierungsebene an. Eine authentifizierte Nachricht wird digital signiert und erfordert ein Zertifikat für den Benutzer, der die Nachricht sendet. Gültige Werte:<br /><ul><li>MQMSG_AUTH_LEVEL_NONE,0</li><li>MQMSG_AUTH_LEVEL_ALWAYS,1</li></ul> | 
| <em>Bereitstellung</em><br /> | Gibt die Option für die Nachrichtenzustellung an. Dieser Wert wird für Transaktionswarteschlangen ignoriert. Gültige Werte:<br /><ul><li>MQMSG_DELIVERY_EXPRESS,0</li><li>MQMSG_DELIVERY_RECOVERABLE,1</li></ul> | 
| <em>EncryptAlgorithm</em><br /> | Gibt den Verschlüsselungsalgorithmus an, der von der Message Queuing zum Verschlüsseln und Entschlüsseln der Nachricht verwendet werden soll. Gültige Werte:<br /><ul><li>CALG_RC2, CALG_RC4</li><li>Ein ganzzahliger Wert, der für Message Queuing <em>EncryptAlgorithm zulässig ist.</em></li></ul> | 
| <em>Hashalgorithm</em><br /> | Gibt eine kryptografische Hashfunktion an. Gültige Werte:<br /><ul><li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li><li>Ein ganzzahliger Wert, der für Message Queuing <em>HashAlgorithm zulässig ist.</em></li></ul> | 
| Journal<br /> | Gibt die Option Message Queuing Meldungsjournal an. Gültige Werte:<br /><ul><li>MQMSG_JOURNAL_NONE,0</li><li>MQMSG_DEADLETTER,1</li><li>MQMSG_JOURNAL,2</li></ul> | 
| <em>Label</em><br /> | Gibt eine Meldungsbezeichnungszeichenfolge bis zu MQ_MAX_MSG_LABEL_LEN an. <br /> | 
| <em>MaxTimeToReachQueue</em><br /> | Gibt eine maximale Zeit in Sekunden an, bis die Nachricht die Warteschlange erreicht. <br /> Gültige Werte:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Anzahl der Sekunden</li></ul> | 
| <em>MaxTimeToReceive</em><br /> | Gibt eine maximale Zeit in Sekunden an, bis die Nachricht von der Zielanwendung empfangen wird. Gültige Werte:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Anzahl der Sekunden</li></ul> | 
| <em>Priority</em><br /> | Gibt eine Nachrichtenprioritätsebene innerhalb der Message Queuing zulässigen Werte an.<br /> Gültige Werte:<br /><ul><li>MQ_MIN_PRIORITY,0</li><li>MQ_MAX_PRIORITY,7</li><li>MQ_DEFAULT_PRIORITY,3</li><li>Zahl zwischen 0 und 7</li></ul> | 
| <em>PrivLevel</em><br /> | Gibt eine Datenschutzebene an, die zum Verschlüsseln von Nachrichten verwendet wird.<br /> Gültige Werte:<br /><ul><li>MQMSG_PRIV_LEVEL_NONE, NONE, 0</li><li>MQMSG_PRIV_LEVEL_BODY, BODY,</li><li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li><li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li></ul> | 
| <em>Ablaufverfolgung</em><br /> | Gibt Ablaufverfolgungsoptionen an, die bei der Ablaufverfolgung Message Queuing werden.<br /> Gültige Werte:<br /><ul><li>MQMSG_TRACE_NONE,0</li><li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</li></ul> | 




 

Der vollständige Satz von COM+-Verwaltungs-SDK-Funktionen ist mithilfe von COM-Objekten verfügbar. Dies ermöglicht es jedem Programm, COM+-Anwendungen nach Bedarf zu starten und zu beenden.

> [!Note]  
> Wenn eine COM+-Anwendung gestartet wird, wird die Anwendung ausgeführt, nicht die einzelnen Komponenten in der Anwendung. Wenn eine Anwendung eine Komponente aufruft, die sich nicht in der Warteschlange befindet, wird die COM+-Anwendung gestartet, die die Komponente enthält. Wenn das Kontrollkästchen Listener aktiviert ist, beginnt der Listener auch mit der Verarbeitung von Nachrichten für Komponenten in der Warteschlange. Während der Dienst für Warteschlangenkomponenten auf diese Weise gestartet werden kann, sollten Sie beim Packen von Komponenten in der Warteschlange und nicht in die Warteschlange eingereihten Komponenten in einer einzigen COM+-Anwendung sicherstellen, dass komponenten in der Warteschlange wirklich gestartet werden sollen, wenn eine Nicht-Warteschlangenkomponente ausgeführt wird. Wenn dies nicht der Fall ist, packen Sie die in der Warteschlange eingereihten Komponenten in eine COM+-Anwendung, die von den anderen Komponenten getrennt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von Komponentenwarteschlangen](activating-component-queues.md)
</dt> </dl>

 

 




