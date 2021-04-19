---
description: Ein Mailslot ist eine Pseudo Datei, die sich im Arbeitsspeicher befindet, und Sie verwenden standardmäßige Dateifunktionen, um darauf zuzugreifen.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Info Slots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373375"
---
# <a name="about-mailslots"></a>Info Slots

Ein Mailslot ist eine Pseudo Datei, die sich im Arbeitsspeicher befindet, und Sie verwenden standardmäßige Dateifunktionen, um darauf zuzugreifen. Die Daten in einer mailslotnachricht können in beliebiger Form vorliegen, dürfen jedoch nicht größer als 424 Bytes sein, wenn Sie zwischen Computern gesendet werden. Im Gegensatz zu Datenträger Dateien sind Mailslots temporär. Wenn alle Handles für einen postslot geschlossen werden, werden der Mailslot und alle darin enthaltenen Daten gelöscht.

Ein *Mailslot-Server* ist ein Prozess, der einen Mailslot erstellt und besitzt. Wenn der Server einen Mailslot erstellt, empfängt er ein Mailslot-handle. Dieses Handle muss verwendet werden, wenn ein Prozess Nachrichten aus dem Mailslot liest. Nur der Prozess, der einen postslot erstellt oder den Handle von einem anderen Mechanismus (z. b. Vererbung) abgerufen hat, kann aus dem Mailslot lesen. Alle Postfächer sind für den Prozess lokal, von dem Sie erstellt werden. Ein Prozess kann keinen Remote-Mailslot erstellen.

Ein *Mailslot-Client* ist ein Prozess, bei dem eine Nachricht in einen Mailslot geschrieben wird. Jeder Prozess, der den Namen eines postslots hat, kann eine Nachricht dort ablegen. Neue Nachrichten folgen allen vorhandenen Nachrichten im postslot.

Mit Mailslots können Nachrichten innerhalb einer Domäne gesendet werden. Wenn mehrere Prozesse in einer Domäne jeweils einen Mailslot mit demselben Namen erstellen, wird jede Nachricht, die an diesen Mailslot adressiert und an die Domäne gesendet wird, von den beteiligten Prozessen empfangen. Da ein Prozess sowohl ein Server-Mailslot-Handle als auch das Client Handle steuern kann, das abgerufen wird, wenn der postslot für einen Schreibvorgang geöffnet wird, können Anwendungen problemlos eine einfache Funktion zur Nachrichten Übergabe innerhalb einer Domäne implementieren.

Zum Senden von Nachrichten, die größer als 424 Bytes sind, verwenden Sie stattdessen [Named Pipes](named-pipes.md) oder [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mailslotnamen](mailslot-names.md)
</dt> <dt>

[Mailslotvorgänge](mailslot-operations.md)
</dt> </dl>

 

 
