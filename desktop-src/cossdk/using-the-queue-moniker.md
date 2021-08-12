---
description: Der Warteschlangenmoniker wird verwendet, um eine komponente in der Warteschlange programmgesteuert zu aktivieren.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Verwenden des Warteschlangenmonikers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e83d720478064f1427966de69d98ef06ac82f1da98cc50aa1ec3d3b3ac4c4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305157"
---
# <a name="using-the-queue-moniker"></a>Verwenden des Warteschlangenmonikers

Der Warteschlangenmoniker wird verwendet, um eine komponente in der Warteschlange programmgesteuert zu aktivieren. Der Warteschlangenmoniker erfordert, dass er die Klassen-ID (CLSID) des Objekts empfängt, das vom neuen Moniker direkt rechts davon aufgerufen werden soll. Wenn dem Linken das Präfix vorangestellt ist, übergibt der neue Moniker die CLSID an den Moniker links davon.

## <a name="component-services-administrative-tool"></a>Verwaltungstool "Komponentendienste"

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Der GetObject-Anzeigenamenparameter ist "queue:/new:", gefolgt von der Programm-ID oder zeichenfolgenform-GUID des zu instanziierten Serverobjekts mit oder ohne Klammern. Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem Warteschlangenmoniker:

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

Der [**CoGetObject-Anzeigenamenparameter**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) ist "queue:/new:", gefolgt von der Programm-ID oder zeichenfolgenform-GUID des zu instanziierten Serverobjekts mit oder ohne geschweifte Klammern. Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem Warteschlangenmoniker:

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

Der Warteschlangenmoniker akzeptiert optionale Parameter, die die Eigenschaften der an Message Queuing gesendeten Nachricht ändern. Um beispielsweise zu veranlassen, dass die Message Queuing Nachricht mit Priorität 6 gesendet wird, wird die Komponente in der Warteschlange wie folgt aktiviert:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

In der folgenden Tabelle sind die Warteschlangenmonikerparameter aufgeführt, die sich auf die Zielwarteschlange auswirken.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>ComputerName</em><br/></td>
<td>Gibt den Computernamensteil eines Message Queuing Warteschlangenpfadnamens an. Der Name Message Queuing Warteschlangenpfads wird als <em>ComputerName</em> \ <em>QueueName</em>formatiert. Wenn nicht angegeben, wird der Computername verwendet, der der konfigurierten Anwendung zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><em>QueueName</em><br/></td>
<td>Gibt den Message Queuing Warteschlangennamen an. Der Name Message Queuing Warteschlangenpfads wird als <em>ComputerName</em> \ <em>QueueName</em>formatiert. Wenn keine Angabe erfolgt, wird der Warteschlangenname verwendet, der der konfigurierten Anwendung zugeordnet ist.<br/> Um eine nicht transaktionale Warteschlange abzurufen, können Sie zuerst den Namen der Warteschlange angeben und dann eine COM+-Anwendung mit dem gleichen Namen erstellen.<br/></td>
</tr>
<tr class="odd">
<td><em>PathName</em><br/></td>
<td>Gibt den vollständigen Namen Message Queuing Warteschlangenpfads an. Wenn keine Angabe erfolgt, wird der Message Queuing Warteschlangenpfadname verwendet, der der konfigurierten Anwendung zugeordnet ist. Um den Zielnamen zu überschreiben, kann der Pfad für eine Message Queuing Arbeitsgruppeninstallation im folgenden Format angegeben werden:<br/> Warteschlange:<em>PathName</em> = <em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass<br/>
<blockquote>
[!Note]<br />
Sowohl die Programmiersprachen C als auch Microsoft Visual C++ erfordern zwei umgekehrte Schrägstriche, um einen umgekehrten Schrägstrich innerhalb von Zeichenfolgenliteralen darzustellen, z. \\ B. Chicago-Gehaltsabrechnung.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><em>Formatname</em><br/></td>
<td>Wenn Sie eine COM+-Anwendung als in die Warteschlange eingereiht markieren, erstellt COM+ eine Message Queuing Warteschlange, deren Name mit der Anwendung identisch ist. Der Message Queuing Formatname dieser Warteschlange befindet sich im COM+-Katalog, der der COM+-Anwendung zugeordnet ist. Um den Zielnamen zu überschreiben, kann der Formatname für eine Message Queuing Arbeitsgruppeninstallation im folgenden Format angegeben werden:<br/> Warteschlange:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId<br/> In einer Active Directory-Konfiguration &quot; wird PRIVATE$ &quot; nicht als Teil des Warteschlangennamens angegeben. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Optionale Warteschlangenmonikerparameter werden von links nach rechts verarbeitet. Geben Sie jedes Schlüsselwort nur einmal an. Wenn Sie den *PathName-Parameter* angeben, werden sowohl die Parameter *ComputerName* als auch *QueueName* ersetzt. Ein bestimmter *FormatName-Parameter* löscht Vorkenntnisse zu den Parametern *ComputerName,* *QueueName* und *PathName.*

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Zuordnen des Listeners für Warteschlangenkomponenten zu einer bestimmten privaten Warteschlange

Der COM+-Komponentenlistener in der Warteschlange empfängt nur aus Warteschlangen, die der als in der Warteschlange markierten COM+-Anwendung zugeordnet sind. Wenn Sie eine COM+-Anwendung als in die Warteschlange eingereiht markieren, erstellt COM+ eine Message Queuing Warteschlange, deren Name mit der Anwendung identisch ist. Der Message Queuing Formatname dieser Warteschlange befindet sich im COM+-Katalog, der der COM+-Anwendung zugeordnet ist. Wenn die COM+-Anwendung gestartet und als Lauschen markiert wird, wird ein Listener im COM+-Anwendungsprozess gestartet, und die Warteschlange wird geöffnet. In der folgenden Tabelle sind die Warteschlangenmonikerparameter aufgeführt, die sich auf die Message Queuing Nachricht auswirken.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>AppSpecific</em><br/></td>
<td>Gibt eine ganze Zahl ohne Vorzeichen an, z.B. AppSpecific=12345.<br/></td>
</tr>
<tr class="even">
<td><em>AuthLevel</em><br/></td>
<td>Gibt die Nachrichtenauthentifizierungsebene an. Eine authentifizierte Nachricht wird digital signiert und erfordert ein Zertifikat für den Benutzer, der die Nachricht sendet. Gültige Werte:<br/>
<ul>
<li>MQMSG_AUTH_LEVEL_NONE,0</li>
<li>MQMSG_AUTH_LEVEL_ALWAYS,1</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Bereitstellung</em><br/></td>
<td>Gibt die Nachrichtenübermittlungsoption an. Dieser Wert wird für Transaktionswarteschlangen ignoriert. Gültige Werte:<br/>
<ul>
<li>MQMSG_DELIVERY_EXPRESS,0</li>
<li>MQMSG_DELIVERY_RECOVERABLE,1</li>
</ul></td>
</tr>
<tr class="even">
<td><em>EncryptAlgorithm</em><br/></td>
<td>Gibt den Verschlüsselungsalgorithmus an, der von Message Queuing zum Verschlüsseln und Entschlüsseln der Nachricht verwendet werden soll. Gültige Werte:<br/>
<ul>
<li>CALG_RC2, CALG_RC4</li>
<li>Ein ganzzahliger Wert, der für eine <em>EncryptAlgorithm-Message Queuing</em>zulässig ist.</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Hashalgorithm</em><br/></td>
<td>Gibt eine kryptografische Hashfunktion an. Gültige Werte:<br/>
<ul>
<li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li>
<li>Ein ganzzahliger Wert, der für einen <em>HashAlgorithm</em>Message Queuing werden kann.</li>
</ul></td>
</tr>
<tr class="even">
<td>Journal<br/></td>
<td>Gibt die Option Message Queuing Meldungsjournal an. Gültige Werte:<br/>
<ul>
<li>MQMSG_JOURNAL_NONE,0</li>
<li>MQMSG_DEADLETTER,1</li>
<li>MQMSG_JOURNAL,2</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Label</em><br/></td>
<td>Gibt eine Meldungsbezeichnungszeichenfolge bis zu MQ_MAX_MSG_LABEL_LEN Zeichen an. <br/></td>
</tr>
<tr class="even">
<td><em>MaxTimeToReachQueue</em><br/></td>
<td>Gibt eine maximale Zeit in Sekunden an, bis die Nachricht die Warteschlange erreicht. <br/> Gültige Werte:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Anzahl der Sekunden</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>MaxTimeToReceive</em><br/></td>
<td>Gibt eine maximale Zeit in Sekunden an, bis die Nachricht von der Zielanwendung empfangen werden soll. Gültige Werte:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Anzahl der Sekunden</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Priority</em><br/></td>
<td>Gibt eine Nachrichtenprioritätsebene innerhalb der zulässigen Message Queuing-Werte an.<br/> Gültige Werte:<br/>
<ul>
<li>MQ_MIN_PRIORITY,0</li>
<li>MQ_MAX_PRIORITY,7</li>
<li>MQ_DEFAULT_PRIORITY,3</li>
<li>Zahl zwischen 0 und 7</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>PrivLevel</em><br/></td>
<td>Gibt eine Datenschutzebene an, die zum Verschlüsseln von Nachrichten verwendet wird.<br/> Gültige Werte:<br/>
<ul>
<li>MQMSG_PRIV_LEVEL_NONE, NONE, 0</li>
<li>MQMSG_PRIV_LEVEL_BODY, BODY,</li>
<li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li>
<li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Ablaufverfolgung</em><br/></td>
<td>Gibt Ablaufverfolgungsoptionen an, die bei der Ablaufverfolgung Message Queuing werden.<br/> Gültige Werte:<br/>
<ul>
<li>MQMSG_TRACE_NONE,0</li>
<li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</li>
</ul></td>
</tr>
</tbody>
</table>



 

Der vollständige Satz von COM+-Verwaltungs-SDK-Funktionen ist über COM-Objekte verfügbar. Dies ermöglicht es jedem Programm, COM+-Anwendungen nach Bedarf zu starten und zu beenden.

> [!Note]  
> Wenn eine COM+-Anwendung gestartet wird, wird die Anwendung ausgeführt, nicht die einzelnen Komponenten in der Anwendung. Wenn eine Anwendung eine Komponente aufruft, die sich nicht in der Warteschlange befindet, wird die COM+-Anwendung gestartet, die die Komponente enthält. Wenn das Kontrollkästchen Listener aktiviert ist, beginnt der Listener auch mit der Verarbeitung von Nachrichten für Komponenten in der Warteschlange. Während der Dienst für Warteschlangenkomponenten auf diese Weise gestartet werden kann, sollten Sie beim Packen von Komponenten in der Warteschlange und nicht in die Warteschlange eingereihten Komponenten in einer einzigen COM+-Anwendung sicherstellen, dass komponenten in der Warteschlange wirklich gestartet werden sollen, wenn eine Nicht-Warteschlangenkomponente ausgeführt wird. Wenn dies nicht der Fall ist, packen Sie die in der Warteschlange eingereihten Komponenten in eine COM+-Anwendung, die von den anderen Komponenten getrennt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von Komponentenwarteschlangen](activating-component-queues.md)
</dt> </dl>

 

 




