---
description: Benennen von postslots und Einfügen von Nachrichten in postslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Mailslotnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749688"
---
# <a name="mailslot-names"></a><span data-ttu-id="13f39-103">Mailslotnamen</span><span class="sxs-lookup"><span data-stu-id="13f39-103">Mailslot Names</span></span>

<span data-ttu-id="13f39-104">Wenn ein Prozess einen Mailslot erstellt, muss der Name des postslots folgende Form aufweisen.</span><span class="sxs-lookup"><span data-stu-id="13f39-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="13f39-105">\\\\.\\ \\ \[ *postslotpfadname* \\ \] </span><span class="sxs-lookup"><span data-stu-id="13f39-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="13f39-106">Der Name des postslots erfordert die folgenden Elemente: zwei umgekehrte Schrägstriche, um den Namen zu beginnen, einen Zeitraum, einen umgekehrten Schrägstrich, der auf den Zeitraum folgt, das Wort "Mailslot" und einen nachfolgenden umgekehrten Schrägstrich.</span><span class="sxs-lookup"><span data-stu-id="13f39-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="13f39-107">Bei Namen wird Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="13f39-107">Names are not case sensitive.</span></span> <span data-ttu-id="13f39-108">Einem postslotnamen kann ein Pfad vorangestellt werden, der aus den Namen eines oder mehrerer Verzeichnisse besteht, die durch umgekehrte Schrägstriche getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="13f39-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="13f39-109">Wenn ein Benutzer beispielsweise Nachrichten für das Subjekt der Steuern von Bob, Pete und Sue erwartet, kann der Benutzer mit der mailslotanwendung für jeden Absender einzelne Postfächer erstellen, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="13f39-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="13f39-110">\\\\.\\ postslot \\ steuert \\ BOSB- \_ Kommentare</span><span class="sxs-lookup"><span data-stu-id="13f39-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="13f39-111">\\\\.\\ postslotsteuern zeigt Kommentare an. \\ \\ \_</span><span class="sxs-lookup"><span data-stu-id="13f39-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="13f39-112">\\\\.\\ postslottaxen unterliegen \\ \\ \_ Kommentaren</span><span class="sxs-lookup"><span data-stu-id="13f39-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="13f39-113">Wenn eine Nachricht in einem postslot abgelegt werden soll, öffnet ein Prozess einen postslot anhand des Namens.</span><span class="sxs-lookup"><span data-stu-id="13f39-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="13f39-114">Um in einen Mailslot auf dem lokalen Computer zu schreiben, kann ein Prozess einen Mailslot-Namen verwenden, der die gleiche Form hat, die zum Erstellen eines postslots verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="13f39-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="13f39-115">Diese Situation ist jedoch relativ ungewöhnlich.</span><span class="sxs-lookup"><span data-stu-id="13f39-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="13f39-116">Häufig verwenden Sie das folgende Formular, um in einen Mailslot auf einem bestimmten Remote Computer zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="13f39-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="13f39-117">\\\\*Computername* \\ \\ \[ *postslotpfadname* \\ \] </span><span class="sxs-lookup"><span data-stu-id="13f39-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="13f39-118">Verwenden Sie das folgende Formular, um eine Nachricht in jedem Mailslot in der angegebenen Domäne mit einem bestimmten Namen zu platzieren:</span><span class="sxs-lookup"><span data-stu-id="13f39-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="13f39-119">\\\\*Domain Name* \\ \\ \[ *postslotpfadname* \\ \] </span><span class="sxs-lookup"><span data-stu-id="13f39-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="13f39-120">Verwenden Sie das folgende Format, um eine Nachricht in jedem postslot mit einem bestimmten Namen in der primären Domäne des Systems zu platzieren:</span><span class="sxs-lookup"><span data-stu-id="13f39-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="13f39-121">\\\\\*\\\\ \[ *postslotpfadname* \\ \] </span><span class="sxs-lookup"><span data-stu-id="13f39-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



