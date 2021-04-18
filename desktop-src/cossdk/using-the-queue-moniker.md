---
description: Der Warteschlangen-Moniker wird verwendet, um eine in der Warteschlange befindliche Komponente Programm gesteuert zu aktivieren.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Verwenden des Warteschlangen Monikers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340123"
---
# <a name="using-the-queue-moniker"></a>Verwenden des Warteschlangen Monikers

Der Warteschlangen-Moniker wird verwendet, um eine in der Warteschlange befindliche Komponente Programm gesteuert zu aktivieren. Der warteschlangenmoniker erfordert, dass er die Klassen-ID (CLSID) des Objekts empfängt, das vom neuen Moniker direkt auf der rechten Seite aufgerufen werden soll. Wenn das Präfix linksbündig ist, übergibt der neue Moniker die CLSID auf der linken Seite an den Moniker.

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Der Anzeige Name-Parameter von GetObject ist "Queue:/New:", gefolgt von der Programm-ID oder der Zeichen folgen-Formular-GUID (mit oder ohne geschweifte Klammern) des Server Objekts, das instanziiert werden soll. Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem warteschlangenmoniker:

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

Der Name des [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) -Anzeige namens lautet "Queue:/New:", gefolgt von der Programm-ID oder der Zeichen folgen Formular-GUID mit oder ohne geschweifte Klammern des zu instanzigenden Server Objekts. Die folgenden Beispiele zeigen drei gültige Aktivierungen einer Komponente mit dem warteschlangenmoniker:

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

## <a name="remarks"></a>Bemerkungen

Der warteschlangenmoniker akzeptiert optionale Parameter, die die Eigenschaften der an Message Queuing gesendeten Nachricht ändern. Um z. b. die Message Queuing Nachricht mit der Priorität 6 zu senden, wird die in der Warteschlange befindliche Komponente wie folgt aktiviert:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

In der folgenden Tabelle sind die Warteschlangen-monikerparameter aufgeführt, die die Ziel Warteschlange betreffen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Computername</em><br/></td>
<td>Gibt den Computernamen Teil eines Message Queuing Warteschlangen Pfadnamens an. Der Name des Message Queuing Warteschlangen Pfads ist als <em>Computername</em> \ <em>QueueName</em>formatiert. Wenn nichts angegeben ist, wird der Computername verwendet, der der konfigurierten Anwendung zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><em>QueueName</em><br/></td>
<td>Gibt den Namen der Message Queuing Warteschlange an. Der Name des Message Queuing Warteschlangen Pfads ist als <em>Computername</em> \ <em>QueueName</em>formatiert. Wenn nicht angegeben, wird der der konfigurierten Anwendung zugeordnete Warteschlangen Name verwendet.<br/> Um eine nicht transaktionale Warteschlange zu erhalten, können Sie zuerst den Warteschlangen Namen angeben und dann eine COM+-Anwendung mit demselben Namen erstellen.<br/></td>
</tr>
<tr class="odd">
<td><em>PathName</em><br/></td>
<td>Gibt den Namen des gesamten Message Queuing Warteschlangen Pfads an. Wenn nichts angegeben ist, wird der Message Queuing der konfigurierten Anwendung zugeordnete Warteschlangen Pfadname verwendet. Um den Zielnamen zu überschreiben, kann der Pfad für eine Message Queuing Arbeitsgruppe-Installation im folgenden Format angegeben werden:<br/> Queue:<em>Pfadname</em> = <em>Computername</em>\Private $ \ appname/New: MyProject. CMyClass<br/>
<blockquote>
[!Note]<br />
Sowohl die Programmiersprachen C als auch Microsoft Visual C++ erfordern zwei umgekehrte Schrägstriche zur Darstellung eines umgekehrten Schrägstrichs in Zeichenfolgenliteralen, z. b. in Chicago- \\ Gehalts
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><em>Format Name</em><br/></td>
<td>Wenn Sie eine COM+-Anwendung als in die Warteschlange eingereiht markieren, erstellt com+ eine Message Queuing Warteschlange, deren Name mit der Anwendung übereinstimmt. Der Message Queuing Formatname dieser Warteschlange befindet sich im com+-Katalog, der der com+-Anwendung zugeordnet ist. Um den Zielnamen zu überschreiben, kann der Format Name in der folgenden Form für eine Message Queuing Arbeitsgruppe-Installation angegeben werden:<br/> Queue:<em>Format Name</em>= Direct = OS:<em>Computername</em>\Private $ \ appname/New: ProgID<br/> In einer Active Directory Konfiguration &quot; wird private $ &quot; nicht als Teil des Warteschlangen namens angegeben. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Optionale Warteschlangen-monikerparameter werden von links nach rechts verarbeitet. Geben Sie jedes Schlüsselwort nur einmal an. Wenn Sie den *pathname* -Parameter angeben, werden die Parameter *Computername* und *QueueName* ersetzt. Ein bestimmter *Formatname* -Parameter löscht vorherige Kenntnisse zu den Parametern " *Computername*", " *QueueName*" und " *pathname* ".

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Zuordnen der in der Warteschlange befindlichen Komponenten Listener zu einer bestimmten privaten Warteschlange

Der von com+ in der Warteschlange befindliche Komponenten Listener empfängt nur aus Warteschlangen, die der com+-Anwendung zugeordnet sind. Wenn Sie eine COM+-Anwendung als in die Warteschlange eingereiht markieren, erstellt com+ eine Message Queuing Warteschlange, deren Name mit der Anwendung übereinstimmt. Der Message Queuing Formatname dieser Warteschlange befindet sich im com+-Katalog, der der com+-Anwendung zugeordnet ist. Wenn die COM+-Anwendung gestartet und als lauschen gekennzeichnet ist, wird ein Listener im com+-Anwendungsprozess gestartet und die Warteschlange geöffnet. In der folgenden Tabelle sind die Warteschlangen-monikerparameter aufgeführt, die sich auf die Message Queuing Meldung auswirken.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>AppSpecific</em><br/></td>
<td>Gibt eine ganze Zahl ohne Vorzeichen an, z. b. AppSpecific = 12345.<br/></td>
</tr>
<tr class="even">
<td><em>AuthLevel</em><br/></td>
<td>Gibt die Authentifizierungs Ebene der Nachricht an. Eine authentifizierte Nachricht ist digital signiert und erfordert ein Zertifikat für den Benutzer, der die Nachricht sendet. Gültige Werte:<br/>
<ul>
<li>MQMSG_AUTH_LEVEL_NONE, 0</li>
<li>MQMSG_AUTH_LEVEL_ALWAYS, 1</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Bereitstellung</em><br/></td>
<td>Gibt die Option für die Nachrichtenübermittlung an. Dieser Wert wird bei transaktionalen Warteschlangen ignoriert. Gültige Werte:<br/>
<ul>
<li>MQMSG_DELIVERY_EXPRESS, 0</li>
<li>MQMSG_DELIVERY_RECOVERABLE, 1</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Verschlüsselungs THM</em><br/></td>
<td>Gibt den Verschlüsselungsalgorithmus an, der von Message Queuing zum Verschlüsseln und Entschlüsseln der Nachricht verwendet werden soll. Gültige Werte:<br/>
<ul>
<li>CALG_RC2 CALG_RC4</li>
<li>Ein beliebiger ganzzahliger Wert, der für die Message Queuing eines <em>Verschlüsselungsalgorithmus</em>zulässig ist.</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>HashAlgorithm</em><br/></td>
<td>Gibt eine kryptografiehash-Funktion an. Gültige Werte:<br/>
<ul>
<li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC</li>
<li>Jeder ganzzahlige Wert, der für die Message Queuing eines <em>HashAlgorithm</em>zulässig ist.</li>
</ul></td>
</tr>
<tr class="even">
<td>Journal<br/></td>
<td>Gibt die Message Queuing Nachrichtenjournal Option an. Gültige Werte:<br/>
<ul>
<li>MQMSG_JOURNAL_NONE, 0</li>
<li>MQMSG_DEADLETTER, 1</li>
<li>MQMSG_JOURNAL, 2</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Label</em><br/></td>
<td>Gibt eine Zeichenfolge für die Nachrichten Bezeichnung bis zu MQ_MAX_MSG_LABEL_LEN Zeichen an. <br/></td>
</tr>
<tr class="even">
<td><em>Maxtimetoreachqueue</em><br/></td>
<td>Gibt eine maximale Zeit in Sekunden an, die die Nachricht an die Warteschlange gelangt. <br/> Gültige Werte:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Anzahl von Sekunden</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Maxtimetor eceive</em><br/></td>
<td>Gibt eine maximale Zeit in Sekunden an, die die Nachricht von der Zielanwendung empfangen werden soll. Gültige Werte:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Anzahl von Sekunden</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Priority</em><br/></td>
<td>Gibt die Prioritäts Ebene der Nachricht innerhalb der zulässigen Message Queuing Werte an.<br/> Gültige Werte:<br/>
<ul>
<li>MQ_MIN_PRIORITY, 0</li>
<li>MQ_MAX_PRIORITY, 7</li>
<li>MQ_DEFAULT_PRIORITY, 3</li>
<li>Zahl zwischen 0 und 7</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>PrivLevel</em><br/></td>
<td>Gibt eine Sicherheitsebene an, die zum Verschlüsseln von Nachrichten verwendet wird.<br/> Gültige Werte:<br/>
<ul>
<li>MQMSG_PRIV_LEVEL_NONE, keine, 0</li>
<li>MQMSG_PRIV_LEVEL_BODY, Text,</li>
<li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li>
<li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Ablaufverfolgung</em><br/></td>
<td>Gibt Ablauf Verfolgungs Optionen an, die beim Ablauf Verfolgungs Message Queuing Routing verwendet werden.<br/> Gültige Werte:<br/>
<ul>
<li>MQMSG_TRACE_NONE, 0</li>
<li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</li>
</ul></td>
</tr>
</tbody>
</table>



 

Der gesamte Satz von com+-Verwaltungs-SDK-Funktionen ist mit COM-Objekten verfügbar. Dies ermöglicht es jedem Programm, com+-Anwendungen nach Bedarf zu starten und zu unterbinden.

> [!Note]  
> Wenn eine COM+-Anwendung gestartet wird, ist dies die Anwendung, die ausgeführt wird, nicht die einzelnen Komponenten innerhalb der Anwendung. Wenn eine Anwendung eine Komponente, die keine Warteschlange enthält, aufruft, wird die COM+-Anwendung, die die Komponente enthält, gestartet. Wenn das Kontrollkästchen Listener aktiviert ist, beginnt der Listener auch mit der Verarbeitung von Nachrichten für in der Warteschlange befindliche Komponenten. Obwohl der Dienst für die Warteschlangen Dienste auf diese Weise gestartet werden kann, wenn Sie in einer COM+-Anwendung in der Warteschlange befindliche und nicht in die Warteschlange eingereihte Komponenten packen, sollten Sie sicherstellen, dass in der Warteschlange befindliche Komponenten gestartet werden, wenn eine nicht in der Warteschlange befindliche Komponente ausgeführt wird. Wenn dies nicht der Fall ist, Verpacken Sie die in die Warteschlange eingereihten Komponenten in eine COM+-Anwendung, die von den anderen Komponenten getrennt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten Warteschlangen](activating-component-queues.md)
</dt> </dl>

 

 




