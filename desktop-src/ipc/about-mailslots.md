---
description: Ein Mailslot ist eine Pseudodatei, die sich im Arbeitsspeicher befindet, und Sie verwenden Standarddateifunktionen, um darauf zuzugreifen.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Informationen zu Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d009b2e667e5feebedeb4b842fc3f6e1630b39069e717ce08f5d0441ebe25aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756518"
---
# <a name="about-mailslots"></a>Informationen zu Mailslots

Ein Mailslot ist eine Pseudodatei, die sich im Arbeitsspeicher befindet, und Sie verwenden Standarddateifunktionen, um darauf zuzugreifen. Die Daten in einer E-Mail-Nachricht können in beliebiger Form, aber nicht größer als 424 Bytes sein, wenn sie zwischen Computern gesendet werden. Im Gegensatz zu Datenträgerdateien sind Mailslots temporär. Wenn alle Handles für einen Mailslot geschlossen werden, werden der Mailslot und alle darin enthaltenen Daten gelöscht.

Ein *maillot-Server* ist ein Prozess, der einen Mailslot erstellt und besitzt. Wenn der Server einen Mailslot erstellt, erhält er ein mailslot-Handle. Dieses Handle muss verwendet werden, wenn ein Prozess Nachrichten aus dem Maillot liest. Nur der Prozess, der einen Mailslot erstellt oder das Handle durch einen anderen Mechanismus (z. B. Vererbung) abgerufen hat, kann aus dem Maillot lesen. Alle Mailslots sind für den Prozess lokal, der sie erstellt. Ein Prozess kann keinen Remote-Maillot erstellen.

Ein *maillot-Client* ist ein Prozess, der eine Nachricht in einen Maillot schreibt. Jeder Prozess, der den Namen eines Mailslots hat, kann dort eine Nachricht senden. Neue Nachrichten folgen auf alle vorhandenen Nachrichten im Maillot.

Mailslots können Nachrichten innerhalb einer Domäne übertragen. Wenn mehrere Prozesse in einer Domäne jeweils einen Maillot mit dem gleichen Namen erstellen, wird jede Nachricht, die an diesen Maillot adressiert und an die Domäne gesendet wird, von den beteiligten Prozessen empfangen. Da ein Prozess sowohl ein Server-Mailslot-Handle als auch das Clienthandle steuern kann, das beim Öffnen des Maillots für einen Schreibvorgang abgerufen wird, können Anwendungen problemlos eine einfache Funktion für die Nachrichtenübergabe innerhalb einer Domäne implementieren.

Verwenden Sie zum Senden von Nachrichten, die zwischen Computern größer als 424 Bytes sind, stattdessen [Named Pipes](named-pipes.md) oder [Windows Sockets.](/windows/desktop/WinSock/windows-sockets-start-page-2)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Maillot-Namen](mailslot-names.md)
</dt> <dt>

[Mailslot-Vorgänge](mailslot-operations.md)
</dt> </dl>

 

 
