---
description: Beschreibungen von Funktionen, die bei der Arbeit mit Postfächern, Clients und Servern verwendet werden sollen.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Mailslotvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373080"
---
# <a name="mailslot-operations"></a><span data-ttu-id="d8469-103">Mailslotvorgänge</span><span class="sxs-lookup"><span data-stu-id="d8469-103">Mailslot Operations</span></span>

<span data-ttu-id="d8469-104">Bei der Arbeit mit Postfächern sollten Clients und Server nur die Funktionen verwenden, die in den folgenden Tabellen erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="d8469-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="d8469-105">Verwenden Sie keine anderen Funktionen, auch wenn Sie Datei Handles oder Dateinamen als Parameter akzeptieren, da Sie nicht für die Arbeit mit Postfächern konzipiert sind.</span><span class="sxs-lookup"><span data-stu-id="d8469-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="d8469-106">Mailslot-Server Funktionen</span><span class="sxs-lookup"><span data-stu-id="d8469-106">Mailslot Server Functions</span></span>

<span data-ttu-id="d8469-107">Mailslot-Server verwenden die exklusive Verwendung von drei Funktionen, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d8469-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="d8469-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="d8469-108">Function</span></span>                                   | <span data-ttu-id="d8469-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8469-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8469-110">**"Kreatemailslot"**</span><span class="sxs-lookup"><span data-stu-id="d8469-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="d8469-111">Erstellt einen Mailslot und gibt ein Mailslot-Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="d8469-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="d8469-112">**Getmailslotinfo**</span><span class="sxs-lookup"><span data-stu-id="d8469-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="d8469-113">Ruft die maximale Nachrichtengröße, die mailslotgröße, die Größe der nächsten Nachricht im postslot, die Anzahl der Nachrichten im Post Slot und die Zeitspanne ab, die ein Lesevorgang auf eine Nachricht warten kann.</span><span class="sxs-lookup"><span data-stu-id="d8469-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="d8469-114">**Setmailslotinfo**</span><span class="sxs-lookup"><span data-stu-id="d8469-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="d8469-115">Ändert das Lese Timeout für einen postslot.</span><span class="sxs-lookup"><span data-stu-id="d8469-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="d8469-116">Die folgenden Funktionen werden auch von Mail Slot-Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8469-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="d8469-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="d8469-117">Function</span></span>                                                         | <span data-ttu-id="d8469-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8469-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="d8469-119">**Duplialisiehandle**</span><span class="sxs-lookup"><span data-stu-id="d8469-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="d8469-120">Dupliziert das Mailslot-handle.</span><span class="sxs-lookup"><span data-stu-id="d8469-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="d8469-121">" [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)", " [ **infofileex** "](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="d8469-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="d8469-122">Ruft Nachrichten aus einem postslot ab.</span><span class="sxs-lookup"><span data-stu-id="d8469-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="d8469-123">**' GetFileTime '**</span><span class="sxs-lookup"><span data-stu-id="d8469-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="d8469-124">Ruft das Datum und die Uhrzeit der Erstellung eines postslots ab.</span><span class="sxs-lookup"><span data-stu-id="d8469-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="d8469-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="d8469-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="d8469-126">Legt das Datum und die Uhrzeit der Erstellung eines postslots fest.</span><span class="sxs-lookup"><span data-stu-id="d8469-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="d8469-127">**Gethandleinformation**</span><span class="sxs-lookup"><span data-stu-id="d8469-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="d8469-128">Ruft die Eigenschaften des Mailslot-Handles ab.</span><span class="sxs-lookup"><span data-stu-id="d8469-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="d8469-129">**"Ableinformation"**</span><span class="sxs-lookup"><span data-stu-id="d8469-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="d8469-130">Legt die Eigenschaften des postslothandles fest.</span><span class="sxs-lookup"><span data-stu-id="d8469-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="d8469-131">Mailslot-Client Funktionen</span><span class="sxs-lookup"><span data-stu-id="d8469-131">Mailslot Client Functions</span></span>

<span data-ttu-id="d8469-132">Ein Client Prozess verwendet die folgenden Funktionen, wenn er mit einem postslot interagiert.</span><span class="sxs-lookup"><span data-stu-id="d8469-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="d8469-133">Funktion</span><span class="sxs-lookup"><span data-stu-id="d8469-133">Function</span></span>                                                             | <span data-ttu-id="d8469-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8469-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="d8469-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="d8469-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="d8469-136">Schließt ein mailslothandle für einen Client Prozess.</span><span class="sxs-lookup"><span data-stu-id="d8469-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="d8469-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="d8469-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="d8469-138">Erstellt ein mailslothandle für einen Client Prozess.</span><span class="sxs-lookup"><span data-stu-id="d8469-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="d8469-139">**Duplialisiehandle**</span><span class="sxs-lookup"><span data-stu-id="d8469-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="d8469-140">Dupliziert ein Mailslot-handle.</span><span class="sxs-lookup"><span data-stu-id="d8469-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="d8469-141">" [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)", " [ **Write fileex** "](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="d8469-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="d8469-142">Schreibt Daten in einen postslot.</span><span class="sxs-lookup"><span data-stu-id="d8469-142">Writes data to a mailslot.</span></span>                      |



 

 

 
