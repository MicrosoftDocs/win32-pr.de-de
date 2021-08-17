---
description: In Microsoft-Telefonie werden Telefoniedienstanbieter in einem anderen Prozess als Telefonieanwendungen ausgeführt.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Die UI-DLL-Schnittstelle des Telefoniedienstanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6aea6dfd68773dcd96602803230bd160552eab1414135b75a3205a0fac88dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403940"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>Die UI-DLL-Schnittstelle des Telefoniedienstanbieters

In Microsoft-Telefonie werden Telefoniedienstanbieter in einem anderen Prozess als Telefonieanwendungen ausgeführt. Dienstanbieter kommunizieren mit TAPISRV über die Telefonie-Dienstanbieterschnittstelle (Tspi) und führen sie in ihrem Prozess aus. -Anwendungsschnittstelle zu TAPI, die im Anwendungskontext geladen werden.

Die Komponenten von TAPI verwenden verschiedene prozessübergreifende Kommunikationsmechanismen, um Funktionsanforderungen und Nachrichten zwischen Anwendungen und Dienstanbietern zu übermitteln. Die Anwendungen und Dienstanbieter können nicht nur in separaten Prozessen ausgeführt werden, sondern auch auf vollständig separaten Systemen. Dienstanbieter können daher keine Dialogfelder im Prozess oder sogar auf dem Computer anzeigen, auf dem sie ausgeführt werden. Die Benutzeroberfläche muss innerhalb des Anwendungskontexts auf dem Computer aufgerufen werden, auf dem die Anwendung ausgeführt wird.

In diesem Abschnitt wird der Mechanismus definiert, mit dem Dienstanbieter-UI-Funktionen im Anwendungskontext geladen und aufgerufen werden. Außerdem wird ein Mechanismus definiert, mit dem Dienstanbieter Dialogfelder im Anwendungskontext öffnen können, wenn sie andernfalls von der Anwendung nicht erwartet werden. Ein Beispiel für diesen letzteren Fall wäre das Dialogfeld **Talk/Hangup,** das von einem Datenmodem-Dienstanbieter angezeigt wird, wenn das Modem als Wählhilfe für interaktive Sprachanrufe verwendet wird, und der Benutzer muss angewiesen werden, das Telefon abzuholen und den Dienstanbieter zu informieren, wann das Modem in denHook gestellt werden soll.

 

 



