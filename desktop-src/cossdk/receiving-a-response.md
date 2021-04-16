---
description: Empfangen einer Antwort
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Empfangen einer Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524179"
---
# <a name="receiving-a-response"></a>Empfangen einer Antwort

Da Komponenten in der Warteschlange für die asynchrone Verwendung entworfen wurden, sollten Client Anwendungen nicht blockieren, während Sie auf eine Antwort von einer Anforderung in der Warteschlange warten. Dennoch ist es oft nützlich, wenn die Client Anwendung oder eine verwandte Anwendung auf dem Client Computer eine Antwort erhalten. Beispielsweise kann ein Client benachrichtigt werden, wenn eine angeforderte Transaktion erfolgreich abgeschlossen wurde.

Es gibt verschiedene Möglichkeiten für eine in der Warteschlange befindliche Komponente, eine Antwort asynchron an den Aufrufer zurückzusenden. Beispielsweise könnte eine e-Mail gesendet werden. Alternativ könnte der Server lose gekoppelte Ereignisse veröffentlichen, die der Client abonnieren könnte.

Eine andere Möglichkeit für einen Client, eine Antwort von einer in der Warteschlange befindlichen Komponente zu erhalten, die auf einem Server ausgeführt wird, besteht darin, dass der Client die aufgerufene Methode als Benachrichtigungs Objekt übergibt. Ein Benachrichtigungs Objekt ist eine Instanz einer in der Warteschlange befindlichen Komponente, die auf dem Client ausgeführt wird. Ein solches Benachrichtigungs Objekt ist möglicherweise sehr einfach und enthält nur eine Ganzzahl, die zur Darstellung eines Fehler Werts verwendet wird, oder es ist recht komplex und enthält alle Informationen, die erforderlich sind, um ein Rollback für eine Transaktion auf dem Client auszuführen. In beiden Fällen übergibt der aufrufende Client ein Benachrichtigungs Objekt als Eingabeparameter, wenn er eine Antwort von einer in der Warteschlange befindlichen Komponente wünscht, die auf einem Server ausgeführt wird. Da das Benachrichtigungs Objekt in die Warteschlange eingereiht wird, kann der Server auf seine Methoden aufzurufen, um seinen Zustand zu ändern, der anschließend vom Client gelesen werden kann. In diesem Szenario wird der in der Warteschlange befindliche com+-Komponenten Dienst sowohl auf dem Client als auch auf dem Server verwendet, um die asynchrone Kommunikation in beide Richtungen zuzulassen.

 

 



