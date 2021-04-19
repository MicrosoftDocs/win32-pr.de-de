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
# <a name="about-mailslots"></a><span data-ttu-id="cc1bf-103">Info Slots</span><span class="sxs-lookup"><span data-stu-id="cc1bf-103">About Mailslots</span></span>

<span data-ttu-id="cc1bf-104">Ein Mailslot ist eine Pseudo Datei, die sich im Arbeitsspeicher befindet, und Sie verwenden standardmäßige Dateifunktionen, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="cc1bf-105">Die Daten in einer mailslotnachricht können in beliebiger Form vorliegen, dürfen jedoch nicht größer als 424 Bytes sein, wenn Sie zwischen Computern gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="cc1bf-106">Im Gegensatz zu Datenträger Dateien sind Mailslots temporär.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="cc1bf-107">Wenn alle Handles für einen postslot geschlossen werden, werden der Mailslot und alle darin enthaltenen Daten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="cc1bf-108">Ein *Mailslot-Server* ist ein Prozess, der einen Mailslot erstellt und besitzt.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="cc1bf-109">Wenn der Server einen Mailslot erstellt, empfängt er ein Mailslot-handle.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="cc1bf-110">Dieses Handle muss verwendet werden, wenn ein Prozess Nachrichten aus dem Mailslot liest.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="cc1bf-111">Nur der Prozess, der einen postslot erstellt oder den Handle von einem anderen Mechanismus (z. b. Vererbung) abgerufen hat, kann aus dem Mailslot lesen.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="cc1bf-112">Alle Postfächer sind für den Prozess lokal, von dem Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="cc1bf-113">Ein Prozess kann keinen Remote-Mailslot erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="cc1bf-114">Ein *Mailslot-Client* ist ein Prozess, bei dem eine Nachricht in einen Mailslot geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="cc1bf-115">Jeder Prozess, der den Namen eines postslots hat, kann eine Nachricht dort ablegen.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="cc1bf-116">Neue Nachrichten folgen allen vorhandenen Nachrichten im postslot.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="cc1bf-117">Mit Mailslots können Nachrichten innerhalb einer Domäne gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="cc1bf-118">Wenn mehrere Prozesse in einer Domäne jeweils einen Mailslot mit demselben Namen erstellen, wird jede Nachricht, die an diesen Mailslot adressiert und an die Domäne gesendet wird, von den beteiligten Prozessen empfangen.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="cc1bf-119">Da ein Prozess sowohl ein Server-Mailslot-Handle als auch das Client Handle steuern kann, das abgerufen wird, wenn der postslot für einen Schreibvorgang geöffnet wird, können Anwendungen problemlos eine einfache Funktion zur Nachrichten Übergabe innerhalb einer Domäne implementieren.</span><span class="sxs-lookup"><span data-stu-id="cc1bf-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="cc1bf-120">Zum Senden von Nachrichten, die größer als 424 Bytes sind, verwenden Sie stattdessen [Named Pipes](named-pipes.md) oder [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) .</span><span class="sxs-lookup"><span data-stu-id="cc1bf-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc1bf-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc1bf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc1bf-122">Mailslotnamen</span><span class="sxs-lookup"><span data-stu-id="cc1bf-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="cc1bf-123">Mailslotvorgänge</span><span class="sxs-lookup"><span data-stu-id="cc1bf-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
