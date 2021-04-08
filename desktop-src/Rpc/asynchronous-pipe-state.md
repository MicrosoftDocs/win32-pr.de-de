---
title: Asynchroner Pipe-Zustand
description: Auf dieser Seite wird der asynchrone Pipezustand für RPC-Aufrufe beschrieben.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038565"
---
# <a name="asynchronous-pipe-state"></a>Asynchroner Pipe-Zustand

Auf dieser Seite wird der asynchrone Pipezustand für RPC-Aufrufe beschrieben.

## <a name="in-pipe"></a>IN Pipe

Client Verhalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Staats</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Ausführen des Aufrufes</td>
<td>Erstellen des RPC
<ul>
<li>Bei Erfolg gehe zu Status WS</li>
<li>Bei Ausnahme gehe zu Ende</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Push</td>
<td>Push tätigen
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg gehe zu WS</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Auf senden warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie eine Benachrichtigung erhalten, gehen Sie zu</li>
<li>Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu P.</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</li>
<li>Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpccallcomplete</strong></a> " empfangen wird, gehen Sie zu Comp</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>NULL-Push</td>
<td>Push 0 bytes (null Push)
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg gehe zu wcomp</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="odd">
<td>Kann</td>
<td>Abbrechen des Aufrufes</td>
<td>Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp<br/></td>
</tr>
<tr class="even">
<td>Wcomp</td>
<td>Auf Abschluss warten</td>
<td>Warten Sie, bis eine notificationcallbenachrichtigung gesendet wurde.<br/> Gehe zu Comp<br/></td>
</tr>
<tr class="odd">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"<br/></td>
</tr>
<tr class="even">
<td>Ende</td>


</tr>
</tbody>
</table>



 

Server Verhalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Staats</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>Der Aufruf wird von der RPC-Laufzeit an "P" gesendet.<br/> So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende<br/> So führen Sie einen fehlerhaften Fehler aus: Gehe zu A<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Pull</td>
<td>Pull erstellen
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg und synchrone Vervollständigung mit bytes, die ungleich NULL sind, wechseln Sie zu P.</li>
<li>Bei Erfolg und synchroner Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu Comp</li>
<li>Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) gehe zu WP</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Auf Pull warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie einen Abschluss erhalten, wechseln Sie zu</li>
<li>Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, wechseln Sie zu</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu "P".</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird (null-Pull), wechseln Sie zu comp.</li>
<li>Wenn ein Fehler aufgetreten ist, wechseln Sie zu</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>Abbrechen des Aufrufes</td>
<td>Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>rpcasyncabortcallgo</strong></a>zum Ende<br/></td>
</tr>
<tr class="odd">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>zum Ende<br/></td>
</tr>
<tr class="even">
<td>Ende</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>Out-Pipe

Client Verhalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Staats</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Ausführen des Aufrufes</td>
<td>Erstellen des RPC
<ul>
<li>Bei Erfolg gehe zu P</li>
<li>Bei Fehler wechseln Sie zu Comp</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Pull</td>
<td>Pull erstellen
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg und synchrone Vervollständigung mit bytes, die ungleich NULL sind, wechseln Sie zu P.</li>
<li>Bei Erfolg und synchronen Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu wcomp</li>
<li>Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) gehe zu WP</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Auf Pull warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Bei einem Fehler, der abgeschlossen werden kann, gehen Sie zu</li>
<li>Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, gehen Sie zu</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu "P".</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird (null-Pull), wechseln Sie zu comp.</li>
<li>Wenn ein Fehler aufgetreten ist, können Sie</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>Kann</td>
<td>Abbrechen des Aufrufes</td>
<td>Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp<br/></td>
</tr>
<tr class="odd">
<td>Wcomp</td>
<td>Auf Abschluss warten</td>
<td>Warten Sie auf eine Benachrichtigung. Eine Benachrichtigung zum Abschluss des Aufrufes sollte empfangen werden.<br/> Gehe zu Comp<br/></td>
</tr>
<tr class="even">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"<br/></td>
</tr>
<tr class="odd">
<td>Ende</td>


</tr>
</tbody>
</table>



 

Server Verhalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Staats</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>Der Aufruf wird von der RPC-Laufzeit an "P" gesendet.<br/> So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende<br/> So führen Sie einen fehlerhaften Fehler aus: Gehe zu A<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Push</td>
<td>Push tätigen
<ul>
<li>Bei Erfolg gehe zu WP</li>
<li>Bei Fehler "Gehe zu Ende"</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Auf Push warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie einen Abschluss erhalten, wechseln Sie zu</li>
<li>Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu P.</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</li>
<li>Wenn ein Fehler auftritt, gehen Sie zu Comp</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>NULL-Push</td>
<td>Push 0 Bytes
<ul>
<li>bei Erfolg gehe zu wnp</li>
<li>bei Fehler wechseln Sie zu Comp</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="odd">
<td>Wnp</td>
<td>Auf NULL-Push warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie einen Abschluss erhalten, wechseln Sie zu</li>
<li>Wenn ein Fehler auftritt, gehen Sie zu Comp</li>
<li>Wenn eine Erfolgsmeldung empfangen wird, gehen Sie zu Comp</li>
</ul></td>
</tr>
<tr class="even">
<td>A</td>
<td>Abbrechen des Aufrufes</td>
<td><a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>Rpcasyncabortcall;</strong></a>aufzurufen Gehe zu Ende</td>
</tr>
<tr class="odd">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall;</strong></a>" Gehe zu Ende</td>
</tr>
<tr class="even">
<td>Ende</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>IN-Out-Pipe

Client Verhalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Staats</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Ausführen des Aufrufes</td>
<td>Erstellen des RPC
<ul>
<li>Bei Erfolg gehe zu WS</li>
<li>Bei Ausnahme gehe zu Ende</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Push</td>
<td>Push tätigen
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg gehe zu WS</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Auf senden warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie eine Benachrichtigung erhalten, gehen Sie zu</li>
<li>Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu PS</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</li>
<li>Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpccallcomplete</strong></a> " empfangen wird, gehen Sie zu Comp</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>NULL-Push</td>
<td>Push 0 bytes (null Push)
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg gehe zu PL</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>Pull</td>
<td>Pull erstellen
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg und synchroner Abschluss mit bytes, die ungleich 0 (null) sind, gehe zu PL</li>
<li>Bei Erfolg und synchronen Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu wcomp</li>
<li>Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) wechseln Sie zu WPL.</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="even">
<td>WPL</td>
<td>Auf Pull warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Bei einem Fehler, der abgeschlossen werden kann, gehen Sie zu</li>
<li>Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, gehen Sie zu</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu pl.</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird, gehen Sie zu comp.</li>
<li>Wenn ein Fehler aufgetreten ist, können Sie</li>
</ul>
Fehler: Gehe zu<br/></td>
</tr>
<tr class="odd">
<td>Kann</td>
<td>Abbrechen des Aufrufes</td>
<td>Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp<br/></td>
</tr>
<tr class="even">
<td>Wcomp</td>
<td>Auf Abschluss warten</td>
<td>Warten Sie auf eine Benachrichtigung. Die callcomplete-Benachrichtigung sollte empfangen werden.<br/> Gehe zu Comp<br/></td>
</tr>
<tr class="odd">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"<br/></td>
</tr>
<tr class="even">
<td>Ende</td>


</tr>
</tbody>
</table>



 

Server Verhalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Name des Staats</th>
<th>Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>Der Aufruf wird vom RPC-runtimego an pl gesendet.<br/> So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende<br/> So führen Sie einen fehlerhaften Fehler aus: Gehe zu A<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>Pull</td>
<td>Pull erstellen
<ul>
<li>Bei Fehler "Gehe zu Ende"</li>
<li>Bei Erfolg und synchroner Abschluss mit bytes, die ungleich 0 (null) sind, gehe zu PL</li>
<li>Bei Erfolg und synchroner Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu PS</li>
<li>Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) wechseln Sie zu WPL.</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="odd">
<td>WPL</td>
<td>Auf Pull warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie einen Abschluss erhalten, wechseln Sie zu</li>
<li>Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, wechseln Sie zu</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu pl.</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird, gehen Sie zu PS</li>
<li>Wenn ein Fehler auftritt, gehen Sie wie folgt vor:</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Push</td>
<td>Push tätigen
<ul>
<li>Bei Erfolg gehe zu WPS</li>
<li>Bei Fehler "Gehe zu Ende"</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="odd">
<td>WPS</td>
<td>Auf Push warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie einen Abschluss erhalten, wechseln Sie zu</li>
<li>Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu PS</li>
<li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</li>
<li>Wenn ein Fehler auftritt, gehen Sie zu Comp</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>NULL-Push</td>
<td>Push 0 Bytes
<ul>
<li>bei Erfolg gehe zu wnp</li>
<li>bei Fehler wechseln Sie zu Comp</li>
</ul>
Fehler: Wechseln Sie zu einem<br/></td>
</tr>
<tr class="odd">
<td>Wnp</td>
<td>Auf NULL-Push warten</td>
<td>Auf Benachrichtigung warten
<ul>
<li>Wenn Sie einen Abschluss erhalten, wechseln Sie zu</li>
<li>Wenn ein Fehler auftritt, gehen Sie zu Comp</li>
<li>Wenn eine Erfolgsmeldung empfangen wird, gehen Sie zu Comp</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>Abbrechen des Aufrufes</td>
<td><a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>Rpcasyncabortcall;</strong></a>aufzurufen Gehe zu Ende</td>
</tr>
<tr class="odd">
<td>Zuschreiben</td>
<td>Completion</td>
<td>Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall;</strong></a>" Gehe zu Ende</td>
</tr>
<tr class="even">
<td>Ende</td>


</tr>
</tbody>
</table>



 

 

 





