---
description: Ein Vorgang, der asynchron abgeschlossen wird, führt einen Teil seiner Verarbeitung in dem von der Anwendung ausgeführten Funktions Ausdruck und den restlichen Teil in einem unabhängigen Ausführungs Thread aus, nachdem TAPI 2. x vom Funktions Aufrufwert zurückgegeben wurde.
ms.assetid: 37b544e4-6413-4741-b8b6-ec676ce4ca97
title: Asynchrone Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e792a4b1d6a25a4f49fbb2abe2c19ce3071ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349521"
---
# <a name="asynchronous-functions"></a>Asynchrone Funktionen

Ein Vorgang, der asynchron abgeschlossen wird, führt einen Teil seiner Verarbeitung in dem von der Anwendung ausgeführten Funktions Ausdruck und den restlichen Teil in einem unabhängigen Ausführungs Thread aus, nachdem TAPI 2. x vom Funktions Aufrufwert zurückgegeben wurde. Um die Verarbeitung des Aufrufes zu gewährleisten, Vektoren der Dienstanbieter die Anforderung einer anderen aktiven Entität im System – z. b. einem LAN-Server, einer Add-in-Hardware, einem Switch oder einem Netzwerk – und kehrt dann zur Anwendung zurück. Zu diesem Zeitpunkt wird entweder ein negatives Fehler Ergebnis oder ein positiver Anforderungs Bezeichner an die Anwendung zurückgegeben.

Zum Zeitpunkt des asynchronen Abschlusses (der Dienstanbieter hat einen Interrupt von der Hardware erhalten, was bedeutet, dass eine Nachricht zugestellt werden muss), ruft der Dienstanbieter tapisrv auf und meldet, dass das Ereignis *X* soeben stattgefunden hat. Bereitstellung einer geeigneten Nachricht an alle betroffenen Anwendungen. " Wenn tapisrv diese Nachricht empfängt, leitet Sie die Nachricht an die TAPI Dynamic Link Library im Prozess der Anwendung weiter, die wiederum eine Fenster Meldung sendet, ein Ereignis Handle signalisiert oder an einen e/a-Abschlussport sendet, gemäß dem Nachrichten Benachrichtigungs Schema, das von der Anwendung in [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) oder [**phoneinitializeex**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)ausgewählt wurde.

Wenn der asynchrone Teil des Vorgangs abgeschlossen ist, wird eine [**Zeilen \_ Antwort**](./line-reply.md) Nachricht (oder eine [**Telefon \_ Antwort**](./phone-reply.md)) an die Anwendung gesendet. Diese Meldung enthält als einen ihrer Parameter den vom Funktionsbefehl zurückgegebenen Anforderungs Bezeichner. Mit diesem Anforderungs Bezeichner kann die Anwendung bestimmen, welche ursprüngliche Anforderung abgeschlossen wurde. (Anwendungen sollten sich die Anforderungs Bezeichner aller aktuell ausgeführten Anforderungen merken, damit Antwort Nachrichten ordnungsgemäß verarbeitet werden können.) Ein zweiter Parameter für die Zeilen \_ Antwortnachricht (oder Telefon \_ Antwort) ist der asynchrone Rückgabewert. Dies ist entweder ein negativer Wert (bei einem Fehler) oder 0 (null), wenn der Vorgang erfolgreich abgeschlossen wurde. Für asynchrone Vorgänge können alle Rückgabewerte als Teil der Funktions Rückgabe oder als *dwParam2* -Parameter in der Zeilen \_ Antwort oder der Telefon Antwortnachricht zurückgegeben werden \_ . Der Wert 0, der einen Erfolg angibt, wird nur in der Zeilen \_ Antwortnachricht und nie als Rückgabewert der Funktion zurückgegeben.

Die initialisieren-Funktionen ( [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) und [**phoneinitializeex**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)) informieren TAPI darüber, wie diese Nachrichten an die Anwendung gesendet werden.

> [!Note]  
> In einigen Fällen, in denen eine Multithreadanwendung eine asynchrone Funktion von einem anderen Thread als dem Thread aufruft, von dem die Anwendung die Zeile oder das Telefongerät initialisiert hat, erhält die Anwendung möglicherweise die [**Zeilen \_ Antwort**](./line-reply.md) oder [**Telefon \_ Antwort**](./phone-reply.md) Nachricht, bevor die asynchrone Funktion zurückgegeben wurde. In solchen Fällen sollte die Anwendung die Nachrichten Parameter speichern und warten, bis die asynchrone Funktion zurückkehrt und der Anforderungs Bezeichner vor der Verarbeitung der Nachricht bekannt ist.

 

 

 
