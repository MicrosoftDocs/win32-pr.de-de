---
description: Die Peer Infrastruktur garantiert nicht die Reihenfolge für den Empfang und die Verarbeitung von Datensätzen.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Daten Satz Abhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367942"
---
# <a name="record-dependencies"></a>Daten Satz Abhängigkeiten

Die Peer Infrastruktur garantiert nicht die Reihenfolge für den Empfang und die Verarbeitung von Datensätzen. Wenn Ihre Anwendung Daten Satz Abhängigkeiten aufweist, was bedeutet, dass die Verarbeitung oder Validierung eines Datensatzes von einem anderen Datensatz abhängig ist, muss die Anwendung in der Lage sein, Situationen zu verarbeiten, in denen Datensätze in beliebiger und unvorhersehbarer Reihenfolge empfangen werden können. Eine Chat-Anwendung kann z. b. zwei Arten von Datensätzen aufweisen: einen Datensatz, der Informationen zu einem bestimmten Benutzer enthält, und einen Datensatz, der eine Chat Nachricht enthält, die auf den Benutzerdaten Satz verweist.

Eine Anwendung muss in der Lage sein, die Situation zu behandeln, in der ein Chat Nachrichten Daten Satz vor dem Benutzerdaten Satz für die Chat Nachricht empfangen wird. Eine Möglichkeit, die Situation zu behandeln, besteht darin, auf den Benutzerdaten Satz zu warten, indem eine Liste mit einer **Liste** oder ein Cache und ein Timer verwendet wird. Die Anwendung kann jeden Datensatz in der Liste oder im Cache regelmäßig überprüfen und dann die Situation behandeln, in der der erforderliche Benutzerdaten Satz empfangen wird.

Zum Verarbeiten von Daten Satz Abhängigkeiten besteht eine gut entworfene Anwendung aus folgendem:

-   Sucht vor dem Ausführen einer Aktion stets nach Daten Satz Abhängigkeiten.
-   Erwartet Bedingungen, die auftreten können, wenn Datensätze in unerwarteter Reihenfolge empfangen werden, und dann die Situation behandelt.

 

 



