---
description: Ein Mailslot ist ein Mechanismus für die one-way interprocess communications (IPC). Anwendungen können Nachrichten in einem E-Mail-Lot speichern. Der Besitzer des Mailslots kann Nachrichten abrufen, die dort gespeichert sind.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72a4bc50c2cb563894ce9b7c616f9ae86cd9ae6e4abb966c78475c504c75f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716830"
---
# <a name="mailslots"></a>Mailslots

Ein *Mailslot ist* ein Mechanismus für die one-way interprocess communications (IPC). Anwendungen können Nachrichten in einem E-Mail-Lot speichern. Der Besitzer des Mailslots kann Nachrichten abrufen, die dort gespeichert sind. Diese Nachrichten werden in der Regel über ein Netzwerk entweder an einen angegebenen Computer oder an alle Computer in einer angegebenen Domäne gesendet. Eine *Domäne* ist eine Gruppe von Arbeitsstationen und Servern, die einen Gruppennamen gemeinsam verwenden.

-   [Informationen zu Mailslots](about-mailslots.md)
-   [Verwenden von Mailslots](using-mailslots.md)
-   [Mailslot-Referenz](mailslot-reference.md)

Sie können named pipes [oder](named-pipes.md) Windows Sockets anstelle von [Mailslots](/windows/desktop/WinSock/windows-sockets-start-page-2) für die prozessübergreifende Kommunikation verwenden. Named Pipes sind eine einfache Möglichkeit für zwei Prozesse zum Austauschen von Nachrichten. Mailslots sind dagegen eine einfache Möglichkeit für einen Prozess, Nachrichten an mehrere Prozesse zu übertragen. Ein wichtiger Aspekt ist, dass mailslots Broadcastnachrichten mithilfe von Datagrammen sendet. Ein *Datagramm ist* ein kleines Informationspaket, das das Netzwerk über das Netzwerk sendet. Wie bei einer Radio- oder Fernsehsendung bietet ein Datagramm keine Bestätigung des Empfangs. es gibt keine Möglichkeit, zu garantieren, dass ein Datagramm empfangen wurde. Ebenso wie ein Funk- oder Fernsehsignal verloren gehen kann, können große Gebäude oder Beeinträchtigungssignale verhindern, dass ein Datagramm ein bestimmtes Ziel erreicht. Named Pipes sind wie Telefonanrufe: Sie sprechen nur mit einer Partei, wissen aber, dass die Nachricht empfangen wird.

 

 
