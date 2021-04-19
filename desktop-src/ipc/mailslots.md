---
description: Ein Mailslot ist ein Mechanismus für die unidirektionale prozessübergreifende Kommunikation (prozessübergreifende Kommunikation, IPC). Anwendungen können Nachrichten in einem postslot speichern. Der Besitzer des postslots kann die dort gespeicherten Nachrichten abrufen.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Postslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350085"
---
# <a name="mailslots"></a>Postslots

Ein *Mailslot* ist ein Mechanismus für die unidirektionale prozessübergreifende Kommunikation (prozessübergreifende Kommunikation, IPC). Anwendungen können Nachrichten in einem postslot speichern. Der Besitzer des postslots kann die dort gespeicherten Nachrichten abrufen. Diese Nachrichten werden in der Regel über ein Netzwerk an einen bestimmten Computer oder an alle Computer in einer angegebenen Domäne gesendet. Eine *Domäne* ist eine Gruppe von Arbeitsstationen und Servern, die einen Gruppennamen gemeinsam verwenden.

-   [Info Slots](about-mailslots.md)
-   [Verwenden von postslots](using-mailslots.md)
-   [Mailslotreferenz](mailslot-reference.md)

Sie können [Named Pipes](named-pipes.md) oder [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) anstelle von Postfächern für die prozessübergreifende Kommunikation verwenden. Named Pipes sind eine einfache Möglichkeit für zwei Prozesse, Nachrichten auszutauschen. Postfächer hingegen sind eine einfache Möglichkeit für einen Prozess, Nachrichten an mehrere Prozesse zu senden. Ein wichtiger Aspekt ist, dass Mailslots Nachrichten mithilfe von datagrams übertragen. Ein *Datagramm* ist ein kleines Paket von Informationen, die das Netzwerk an die Übertragung sendet. Wie bei einer Radio-oder Fernsehübertragung bietet ein Datagramm keine Bestätigung der Bestätigung. Es gibt keine Möglichkeit, sicherzustellen, dass ein Datagramm empfangen wurde. Ebenso wie Berge, große Gebäude oder Störsignale bewirken, dass ein Radio-oder Fernsehsignal verloren geht, kann es passieren, dass ein Datagramm ein bestimmtes Ziel erreicht. Named Pipes sind wie Telefonanrufe: Sie sprechen nur mit einer Partei, aber Sie wissen, dass die Nachricht empfangen wird.

 

 
