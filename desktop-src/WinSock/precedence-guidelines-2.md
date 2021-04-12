---
description: Die zwei (oder mehr) Deskriptoren, die auf einen freigegebenen Socket verweisen, können unabhängig von der e/a-Leistung unabhängig verwendet werden.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Rang folgen Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129137"
---
# <a name="precedence-guidelines"></a>Rang folgen Richtlinien

Die zwei (oder mehr) Deskriptoren, die auf einen freigegebenen Socket verweisen, können unabhängig von der e/a-Leistung unabhängig verwendet werden. Die Windows Sockets-Schnittstelle implementiert jedoch keinen Zugriffs Steuerungstyp, d. h., es geht um die Prozesse, die zum koordinieren ihrer Vorgänge auf einem freigegebenen Socket beteiligt sind. Eine typische Verwendung von freigegebenen Sockets besteht darin, dass ein Prozess, der für das Erstellen von Sockets und das Einrichten von Verbindungen zuständig ist, die Sockets an andere Prozesse übergibt, die für den Informationsaustausch zuständig sind.

Die allgemeine Richtlinie zur Unterstützung mehrerer ausstehender Vorgänge für freigegebene Sockets besteht darin, dass ein Dienstanbieter alle gleichzeitigen Vorgänge für freigegebene Sockets berücksichtigen muss, insbesondere den letzten Vorgang für ein Socketobjekt. Wenn dies erforderlich ist, kann dies auf Kosten der Ausführung einiger vorheriger, aber noch ausstehender Vorgänge auftreten, die in diesem Fall "WSAEINTR" zurückgeben.

 

 



