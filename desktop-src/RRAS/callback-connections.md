---
title: Rückruf Verbindungen
description: RAS unterstützt Verbindungen, bei denen der Remote Server nicht mehr verwendet wird, und ruft dann an den Client zurück, um die Verbindung herzustellen.
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aabe3bf5503f16d7d27e44e02dc19ccb2a6f2e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729824"
---
# <a name="callback-connections"></a>Rückruf Verbindungen

RAS unterstützt Verbindungen, bei denen der Remote Server nicht mehr verwendet wird, und ruft dann an den Client zurück, um die Verbindung herzustellen.

Für jeden Benutzer, der eine Verbindung mit einem RAS-Server herstellen kann, speichert der Server ein Rückruf Attribut, das steuert, wie die Verbindung hergestellt wird. Das Standard Attribut ist kein Rückruf, was bedeutet, dass der Benutzer ohne Rückruf eine Verbindung mit dem RAS-Server herstellen kann. Alternativ kann der Administrator des RAS-Servers einem Benutzer entweder das Voreinstellung-oder das Set-by-caller-Rückruf Attribut zuweisen.

Für einen Benutzer, dem die voreingestellte Einschränkung zugewiesen ist, gibt der Administrator eine Telefonnummer an, die vom RAS-Server zum Herstellen einer Verbindung zurück aufgerufen werden muss. Der Benutzer kann keine andere Zahl angeben, und die Verbindung kann nicht ohne Rückruf hergestellt werden.

Ein vordefinierter Rückruf Vorgang wird automatisch vom RAS-Verbindungs-Manager und dem Remote Server verarbeitet. Die RAS-Client Anwendung muss nichts anderes als das Feedback senden, wenn der Benachrichtigungs Handler während der verschiedenen Zustände des Rückruf Vorgangs aufgerufen wird.

Ein Benutzer, dem die Berechtigung durch Aufrufer festlegen zugewiesen ist, kann entweder mit oder ohne Rückruf eine Verbindung herstellen. Der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Aufruf verwendet den **szcallbacknumber** -Member der [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) -Struktur, um die Auswahl anzugeben.

Der **szcallbacknumber** -Member kann einfach die Rückrufnummer angeben. oder um die Verbindung ohne Rückruf herzustellen, kann **szcallbacknumber** auf eine leere Zeichenfolge ("") verweisen. In beiden Fällen verarbeitet der RAS-Verbindungs-Manager den Verbindungsvorgang automatisch. Wie bei einem vordefinierten Rückruf Vorgang muss der RAS-Client keine andere Aktion als durchführen, um dem Benutzer Feedback zu geben.

Wenn der Aufruf von " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " [angehaltene Zustände](paused-states.md)ermöglicht, kann **szcallbacknumber** auf eine Sternchen-Zeichenfolge ("") zeigen, \* um anzugeben, dass der Verbindungsvorgang einen angehaltenen Zustand aufweisen soll, damit der Benutzer die Rückrufnummer eingeben kann. In diesem Fall wechselt der Verbindungsvorgang für einen Set by caller-Benutzer in einen angehaltenen Zustand, nachdem der Benutzer vom Remote Server authentifiziert wurde. Während des angehaltenen Zustands erhält der RAS-Client die Rückruf Nummern Eingabe vom Benutzer. Anschließend nimmt der Client den Verbindungsvorgang an, indem er einen **zweiten** Wiederholungs Aufruf durchführen, bei dem **szcallbacknumber** die vom Benutzer bereitgestellte Zahl angibt.

> [!Note]  
> Wenn angehaltene Zustände nicht aktiviert sind, gibt es eine andere Bedeutung, wenn **szcallbacknumber** auf eine Sternchen-Zeichenfolge ("") zeigt \* . In diesem Fall gibt das Sternchen an, dass die Rückrufnummer in der durch den Befehl " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " angegebenen Telefonbuchdatei gespeichert wird.

 

Im Fall eines Rückrufs wird der Aufruf von " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " erst zurückgegeben, nachdem der Server den Client zurückgerufen hat.

 

 