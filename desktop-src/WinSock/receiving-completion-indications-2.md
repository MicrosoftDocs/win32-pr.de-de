---
description: 'Zum Empfangen von Vervollständigungs hinweisen stehen mehrere Optionen zur Verfügung, sodass Anwendungen mit einem angemessenen Maß an Flexibilität bereitgestellt werden. Hierzu gehören: warten (oder blockieren) von Ereignis Objekten, Abrufen von Ereignis Objekten und Socket-e/a-Abschluss Routinen.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Empfangende Vervollständigungs Hinweise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd05d8297af17c26393b5db113fac283b39fcbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350069"
---
# <a name="receiving-completion-indications"></a>Empfangende Vervollständigungs Hinweise

Zum Empfangen von Vervollständigungs hinweisen stehen mehrere Optionen zur Verfügung, sodass Anwendungen mit einem angemessenen Maß an Flexibilität bereitgestellt werden. Hierzu gehören: warten (oder blockieren) von Ereignis Objekten, Abrufen von Ereignis Objekten und Socket-e/a-Abschluss Routinen.

## <a name="blocking-and-waiting-for-completion-indication"></a>Blockieren und warten auf Abschluss Anzeige

Anwendungen können blockieren, während darauf gewartet wird, dass ein oder mehrere Ereignis Objekte mithilfe der [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) -Funktion festgelegt werden. Bei Windows-Implementierungen wird der Prozess oder Thread tatsächlich blockiert. Da Windows Sockets 2-Ereignis Objekte als Windows-Ereignisse implementiert werden, kann die systemeigene Windows-Funktion [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) auch zu diesem Zweck verwendet werden. Dies ist besonders nützlich, wenn der Thread sowohl auf Socket-als auch auf nicht-Socket-Ereignisse warten muss.

## <a name="polling-for-completion-indication"></a>Abrufen der Vervollständigungs Angabe

Anwendungen, die nicht blockieren möchten, können die [**wsagetverlappedresult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) -Funktion verwenden, um den Abschluss Status abzurufen, der mit einem bestimmten Ereignis Objekt verknüpft ist. Diese Funktion gibt an, ob der überlappende Vorgang abgeschlossen wurde, und ordnet, wenn er abgeschlossen wurde, die [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion an, um den Fehlerstatus des überlappenden Vorgangs abzurufen.

## <a name="using-socket-io-completion-routines"></a>Verwenden von Socket-e/a-Vervollständigungs Routinen

Die Funktionen, die zum Initiieren von überlappenden e/a-Vorgängen ( [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) verwendet werden, nehmen *lpCompletionRoutine* als optionalen Eingabeparameter an. Dies ist ein Zeiger auf eine anwendungsspezifische Funktion, die aufgerufen wird, nachdem ein erfolgreich initiierter e/a-Vorgang abgeschlossen wurde (erfolgreich oder anderweitig). Die Vervollständigungs Routine befolgt die gleichen Regeln wie für die Windows-Datei-e/a-Vervollständigungs Routinen. Das heißt, die Vervollständigungs Routine wird erst aufgerufen, wenn sich der Thread in einem wartewartewartezustand befindet, z. b. wenn die Funktion " [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) " mit dem `fAlertable` festgelegten Flag aufgerufen wird. Eine Anwendung, die die Vervollständigungs Routine Option für eine bestimmte überlappende e/a-Anforderung verwendet, verwendet möglicherweise nicht die Wait-Option von [**wsagetoverlappedresult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) für dieselbe überlappende e/a-Anforderung.

Mithilfe der Transporte kann eine Anwendung Sende-und Empfangs Vorgänge aus dem Kontext der Socket-e/a-Abschluss Routine aufrufen und sicherstellen, dass die e/a-Abschluss Routinen für einen bestimmten Socket nicht geschachtelt werden. Dadurch können zeitkritische Datenübertragungen vollständig in einem präemptiven Kontext erfolgen.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Zusammenfassung der Überlapp enden Vervollständigungs Anzeige Mechanismen

Der bestimmte überlappende e/a-Abschluss Hinweis, der für einen gegebenen überlappenden Vorgang verwendet werden soll, hängt davon ab, ob die Anwendung einen Zeiger auf eine Vervollständigungsfunktion bereitstellt, ob auf eine [**wsaoverl**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) -Struktur verwiesen wird, und durch den Wert des **hevent** -Members innerhalb der **wsaoverllapp** -Struktur (falls angegeben). In der folgenden Tabelle wird die Vervollständigungs Semantik für einen überlappenden Socket zusammengefasst, und es werden die verschiedenen Kombinationen von *lpoverlgetauscht*, **hevent** und *lpCompletionRoutine* angezeigt:

| *lpoverlgetauscht* | hevent         | *lpCompletionRoutine* | Vervollständigungs Angabe                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Nicht verfügbar | Wird ignoriert.               | Der Vorgang wird synchron abgeschlossen. Sie verhält sich wie ein nicht überlappenden Socket.                                                                                                                                      |
| ! Normal          | NULL           | NULL                  | Der Vorgang wird überlappen abgeschlossen, aber es gibt keinen von Windows Sockets 2 unterstützten Abschlussmechanismus. Der Mechanismus für den Abschluss Port (falls unterstützt) kann in diesem Fall verwendet werden. Andernfalls gibt es keine Abschluss Benachrichtigung. |
| ! Normal          | ! Normal          | NULL                  | Der Vorgang wird überlappende Benachrichtigungen durch Signalisieren von Ereignis Objekten abgeschlossen.                                                                                                                                                  |
| ! Normal          | Wird ignoriert.        | ! Normal                 | Der Vorgang wird überlappende Benachrichtigungen durch Planen der Abschluss Routine abgeschlossen.                                                                                                                                           |



 

 

 
