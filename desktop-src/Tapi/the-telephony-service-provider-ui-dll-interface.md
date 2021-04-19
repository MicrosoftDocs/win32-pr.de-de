---
description: In der Microsoft-telefonietelefonie werden Telefoniedienstanbieter in einem separaten Prozess von Telefonieanwendungen ausgeführt.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: UI-Dienstanbieter UI-DLL-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349204"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>UI-Dienstanbieter UI-DLL-Schnittstelle

In der Microsoft-telefonietelefonie werden Telefoniedienstanbieter in einem separaten Prozess von Telefonieanwendungen ausgeführt. Dienstanbieter kommunizieren über die Telefonie-Dienstanbieter Schnittstelle (TSPI) mit tapisrv und führen Sie in Ihrem Prozess aus. Anwendungen stellen eine Schnittstelle zu TAPI dar, die im Anwendungskontext geladen werden.

Die Komponenten von TAPI verwenden verschiedene prozessübergreifende Kommunikationsmechanismen, um Funktionsanforderungen und Nachrichten zwischen Anwendungen und Dienstanbietern zu übermitteln. Die Anwendungen und die Dienstanbieter können nicht nur in separaten Prozessen ausgeführt werden, sondern auf vollständig getrennten Systemen. Dienstanbieter können daher keine Dialogfelder im Prozess oder sogar auf dem Computer anzeigen, auf dem Sie ausgeführt werden. Auf dem Computer, auf dem die Anwendung ausgeführt wird, muss die Benutzeroberfläche innerhalb des Anwendungs Kontexts aufgerufen werden.

In diesem Abschnitt wird der Mechanismus definiert, mit dem die Benutzeroberflächen Funktionen von Dienstanbietern geladen und innerhalb des Anwendungs Kontexts aufgerufen werden. Außerdem wird ein Mechanismus definiert, durch den Dienstanbieter die Dialogfelder im Anwendungskontext spontan öffnen können, wenn Sie von der Anwendung nicht anderweitig erwartet werden. Ein Beispiel für diesen letzteren Fall wäre das Dialogfeld **Talk/hangup** , das von einem Daten-Modem Dienstanbieter angezeigt wird, wenn das Modem als Einwählprogramm für interaktive Sprachanrufe verwendet wird, und der Benutzer muss aufgefordert werden, das Telefon zu übernehmen und den Dienstanbieter darüber zu informieren, wann er den Modem-OnHook platzieren soll.

 

 



