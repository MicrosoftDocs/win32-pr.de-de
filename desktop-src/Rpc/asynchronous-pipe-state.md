---
title: Asynchroner Pipezustand
description: Auf dieser Seite wird der asynchrone Pipezustand für RPC-Aufrufe beschrieben.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35e54d9f86228cb4c957f53411c105e20e2109
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468167"
---
# <a name="asynchronous-pipe-state"></a>Asynchroner Pipezustand

Auf dieser Seite wird der asynchrone Pipezustand für RPC-Aufrufe beschrieben.

## <a name="in-pipe"></a>IN Pipe

Clientverhalten


| State | Name des Staats | Aktion | 
|-------|------------|--------|
| C | Rufen Sie auf. | Machen Sie den RPC<ul><li>Bei Erfolg zu Zustand WS wechseln</li><li>Bei Ausnahme zu Ende wechseln</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| P | Push | Pushen<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Bei Erfolg zu WS wechseln</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| WS | Warten auf Senden | Warten auf Benachrichtigung<ul><li>Wenn keine Benachrichtigung angezeigt wird, wechseln Sie zu "Kann".</li><li>Wenn ein <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>erfolgreiches RpcSendComplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, wechseln Sie zu P.</li><li>Wenn ein <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>erfolgreiches RpcSendComplete</strong></a> empfangen wird und keine weitere Daten gesendet werden müssen, gehen Sie an NP.</li><li>Wenn ein Fehler bei <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> empfangen wird, wechseln Sie zu Comp.</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| NP | NULL-Push | Push 0 Bytes (NULL-Push)<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Bei Erfolg zu WComp wechseln</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| Kann | Abbrechen des Anrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>von RpcAsyncCancelCall</strong></a>Go to WComp<br /> | 
| WComp | Warten auf den Abschluss | Warten Sie, bis notificationCall-complete notification empfangen werden soll.<br /> Wechseln Sie zu "Comp".<br /> | 
| Comp | Completion | Problem: <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Zum Ende wechseln<br /> | 
| Ende | 




 

Serververhalten


| State | Name des Staats | Aktion | 
|-------|------------|--------|
| D | Dispatch | Der Aufruf wird von der RPC-Laufzeit an P<br /> To fail fatally (while executing on the RPC thread): Raise exception; Gehe zu Ende<br /> So führen Sie ordnungsgemäß einen Fehler aus: Wechseln Sie zu A.<br /> | 
| P | Pull | Pullen<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Bei erfolgreicher und synchroner Vervollständigung mit gelesenen Bytes, die nicht 0 (null) sind, wechseln Sie zu P.</li><li>Bei erfolgreicher und synchroner Vervollständigung mit null gelesenen Bytes (NULL-Pull) wechseln Sie zu Comp.</li><li>Bei erfolgreicher und asynchroner Vervollständigung (ERROR_IO_PENDING wird zurückgegeben) wechseln Sie zu WP.</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu A.<br /> | 
| WP | Warten auf Pull | Warten auf Benachrichtigung<ul><li>Gehen Sie bei einem Fehler beim Abschluss zu A.</li><li>Wenn ein Fehler vom <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>Typ RpcReceiveComplete empfangen wird, wechseln</strong></a> Sie zu A.</li><li>Wenn ein erfolgreiches <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit gelesenen Bytes von nicht 0 (null) empfangen wird, wechseln Sie zu P.</li><li>Wenn ein erfolgreiches <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete-Objekt</strong></a> mit null gelesenen Bytes (NULL-Pull) empfangen wird, wechseln Sie zu Comp.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu A.</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu A.<br /> | 
| Ein | Abbrechen des Aufrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>von RpcAsyncAbortCall</strong></a>Go to End<br /> | 
| Comp | Completion | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>von RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Ende | 




 

## <a name="out-pipe"></a>OUT Pipe

Clientverhalten


| State | Name des Staats | Aktion | 
|-------|------------|--------|
| C | Rufen Sie auf. | Machen Sie den RPC<ul><li>Wechseln Sie bei Erfolg zu P.</li><li>Wechseln Sie bei einem Fehler zu "Comp".</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| P | Pull | Pullen<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Bei erfolgreicher und synchroner Vervollständigung mit gelesenen Bytes, die nicht 0 (null) sind, wechseln Sie zu P.</li><li>Bei erfolgreicher und synchroner Vervollständigung mit null gelesenen Bytes (NULL-Pull) wechseln Sie zu WComp.</li><li>Bei erfolgreicher und asynchroner Vervollständigung (ERROR_IO_PENDING wird zurückgegeben) wechseln Sie zu WP.</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| WP | Warten auf Pull | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu "Can".</li><li>Wenn ein Fehler <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete</strong></a> empfangen wird, wechseln Sie zu Kann.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit gelesenen Bytes ungleich 0 empfangen wird, wechseln Sie zu P.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit gelesenen Nullbytes empfangen wird (NULL-Pull), wechseln Sie zu Comp.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu Can.</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| Kann | Abbrechen des Aufrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>von RpcAsyncCancelCall</strong></a>Go zu WComp<br /> | 
| WComp | Warten auf Abschluss | Warten Sie auf eine Benachrichtigung. Es sollte eine Benachrichtigung zum Abschließen des Aufrufs empfangen werden.<br /> Wechseln Sie zu "Comp".<br /> | 
| Comp | Completion | Problem <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Ende | 




 

Serververhalten


| State | Name des Staats | Aktion | 
|-------|------------|--------|
| D | Dispatch | Der Aufruf wird von der RPC-Runtime an P gesendet.<br /> So führen Sie einen schwerwiegenden Fehler aus (während der Ausführung im RPC-Thread): Ausnahme auslösen; gehe zu Ende<br /> So schlagen Sie ordnungsgemäß fehl: Wechseln Sie zu A.<br /> | 
| P | Push | Pushen<ul><li>Bei Erfolg wechseln Sie zu WP.</li><li>Gehen Sie bei einem Fehler zu Ende.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| WP | Warten auf Push | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu A.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, wechseln Sie zu P.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> empfangen wird und keine weiteren Daten gesendet werden müssen, wechseln Sie zu NP.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu Comp.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| NP | NULL-Push | Pushen von 0 Bytes<ul><li>on success go to WNP (bei Erfolg zu WNP wechseln)</li><li>Bei Fehler wechseln Sie zu Comp.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| WNP | Warten auf NULL-Push | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu A.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu Comp.</li><li>Wenn ein Erfolg empfangen wird, gehen Sie zu Comp.</li></ul> | 
| Ein | Abbrechen des Aufrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>von RpcAsyncAbortCall</strong></a>; gehe zu Ende | 
| Comp | Completion | Problem <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcAsyncCompleteCall</strong></a>; gehe zu Ende | 
| Ende | 




 

## <a name="in-out-pipe"></a>IN-OUT-Pipe

Clientverhalten


| State | Name des Staats | Aktion | 
|-------|------------|--------|
| C | Tätigen des Aufrufs | Erstellen des RPC<ul><li>Wechseln Sie bei Erfolg zu WS.</li><li>Bei Ausnahme gehe zu Ende</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| PS | Push | Pushen<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Wechseln Sie bei Erfolg zu WS.</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| WS | Warten auf Senden | Warten auf Benachrichtigung<ul><li>Wenn keine Benachrichtigung angezeigt wird, wechseln Sie zu "Can" (Kann).</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie an PS.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> empfangen wird und keine weiteren Daten gesendet werden müssen, wechseln Sie zu NP.</li><li>Wenn ein Fehler <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcCallComplete</strong></a> empfangen wird, wechseln Sie zu Comp.</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| NP | NULL-Push | Push 0 Bytes (NULL-Push)<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Wechseln Sie bei Erfolg zu PL.</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| PL | Pull | Pullen<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Bei erfolgreicher und synchroner Vervollständigung mit gelesenen Bytes ungleich 0 (null) wird PL zurückgegeben.</li><li>Wechseln Sie bei erfolgreicher und synchroner Vervollständigung mit gelesenen Nullbytes (NULL-Pull) zu WComp.</li><li>Wechseln Sie nach erfolgreicher und asynchroner Vervollständigung (ERROR_IO_PENDING zurückgegeben wird) zu WPL.</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| WPL | Warten auf Pull | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu "Can".</li><li>Wenn ein Fehler <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete</strong></a> empfangen wird, wechseln Sie zu Kann.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit gelesenen Bytes ungleich null empfangen wird, wechseln Sie zu PL.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit 0 gelesenen Bytes empfangen wird, wechseln Sie zu Comp.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu Can.</li></ul>Fehler: Wechseln Sie zu "Can" (Kann).<br /> | 
| Kann | Abbrechen des Aufrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>von RpcAsyncCancelCall</strong></a>Go zu WComp<br /> | 
| WComp | Warten auf Abschluss | Warten Sie auf eine Benachrichtigung. Die CallComplete-Benachrichtigung sollte empfangen werden.<br /> Wechseln Sie zu "Comp".<br /> | 
| Comp | Completion | Problem <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Ende | 




 

Serververhalten


| State | Name des Staats | Aktion | 
|-------|------------|--------|
| D | Dispatch | Der Aufruf wird von rpc runtimeGo an PL gesendet.<br /> So führen Sie einen schwerwiegenden Fehler aus (während der Ausführung im RPC-Thread): Ausnahme auslösen; gehe zu Ende<br /> So schlagen Sie ordnungsgemäß fehl: Wechseln Sie zu A.<br /> | 
| PL | Pull | Pullen<ul><li>Gehen Sie bei einem Fehler zu Ende.</li><li>Bei erfolgreicher und synchroner Vervollständigung mit gelesenen Bytes ungleich 0 (null) wird PL zurückgegeben.</li><li>Wechseln Sie bei erfolgreicher und synchroner Vervollständigung mit gelesenen Nullbytes (NULL-Pull) zu PS.</li><li>Wechseln Sie bei erfolgreicher und asynchroner Vervollständigung (ERROR_IO_PENDING zurückgegeben wird) zu WPL.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| WPL | Warten auf Pull | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu A.</li><li>Wenn ein Fehler empfangen <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>wird,</strong></a> wechseln Sie zu A.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit gelesenen Bytes ungleich null empfangen wird, wechseln Sie zu PL.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> mit 0 gelesenen Bytes empfangen wird, wechseln Sie zu PS.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu A.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| PS | Push | Pushen<ul><li>Wechseln Sie bei Erfolg zu WPS.</li><li>Gehen Sie bei einem Fehler zu Ende.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| WPS | Warten auf Push | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu A.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie an PS.</li><li>Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> empfangen wird und keine weiteren Daten gesendet werden müssen, wechseln Sie zu NP.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu Comp.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| NP | NULL-Push | Pushen von 0 Bytes<ul><li>bei Erfolg zu WNP wechseln</li><li>Bei Fehler wechseln Sie zu Comp.</li></ul>Fehler: Wechseln Sie zu A.<br /> | 
| WNP | Warten auf NULL-Push | Warten auf Benachrichtigung<ul><li>Wenn sie nicht abgeschlossen werden kann, wechseln Sie zu A.</li><li>Wenn ein Fehler empfangen wird, wechseln Sie zu Comp.</li><li>Wenn ein Erfolg empfangen wird, gehen Sie zu Comp.</li></ul><br /> | 
| Ein | Abbrechen des Aufrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>von RpcAsyncAbortCall</strong></a>; gehe zu Ende | 
| Comp | Completion | Problem <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcAsyncCompleteCall</strong></a>; gehe zu Ende | 
| Ende | 




 

 

 





