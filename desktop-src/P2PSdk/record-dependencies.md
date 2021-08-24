---
description: Die Peerinfrastruktur garantiert nicht die Reihenfolge für den Empfang und die Verarbeitung von Datensätzen.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Datensatzabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8121c22525a3a2d8065014eaf27143a324b2f6410f194d3257ec3b840958d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675020"
---
# <a name="record-dependencies"></a>Datensatzabhängigkeiten

Die Peerinfrastruktur garantiert nicht die Reihenfolge für den Empfang und die Verarbeitung von Datensätzen. Wenn Ihre Anwendung Über Datensatzabhängigkeiten verfügt, was bedeutet, dass die Verarbeitung oder Überprüfung eines Datensatzes von einem anderen Datensatz abhängig ist, muss Ihre Anwendung in der Lage sein, Situationen zu verarbeiten, in denen Datensätze in einer beliebigen und unvorhersehbaren Reihenfolge empfangen werden können. Beispielsweise kann eine Chatanwendung zwei Arten von Datensätzen aufweisen: einen Datensatz, der Informationen zu einem bestimmten Benutzer enthält, und einen Datensatz, der eine Chatnachricht enthält, die auf den Benutzerdatensatz verweist.

Eine Anwendung muss in der Lage sein, die Situation zu behandeln, in der ein Chatnachrichtendatensatz vor dem Benutzerdatensatz für die Chatnachricht empfangen wird. Eine Möglichkeit, die Situation zu bewältigen, besteht darin, auf den Benutzerdatensatz zu warten, indem sie eine Liste für **die Bereitschaftsliste** oder einen Cache und einen Timer verwenden. Die Anwendung kann in regelmäßigen Abständen jeden Datensatz in der Liste oder im Cache untersuchen und dann die Situation behandeln, in der der erforderliche Benutzerdatensatz empfangen wird.

Um Datensatzabhängigkeiten zu verarbeiten, besteht eine gut entworfene Anwendung aus folgenden Komponenten:

-   Überprüft immer auf Datensatzabhängigkeiten, bevor eine Aktion ausgeführt wird.
-   Erwartet Bedingungen, die auftreten können, wenn Datensätze in einer unerwarteten Reihenfolge empfangen werden, und behandelt dann die Situation.

 

 



