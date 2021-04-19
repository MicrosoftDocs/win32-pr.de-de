---
description: Die iupdatesearcher-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Iupdatesearcher-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348425"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="b37ff-103">Iupdatesearcher-Methoden</span><span class="sxs-lookup"><span data-stu-id="b37ff-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="b37ff-104">Die [**iupdatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="b37ff-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="b37ff-105">Methode</span><span class="sxs-lookup"><span data-stu-id="b37ff-105">Method</span></span>                                                              | <span data-ttu-id="b37ff-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b37ff-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b37ff-107">**Beginsearch**</span><span class="sxs-lookup"><span data-stu-id="b37ff-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="b37ff-108">Startet die Ausführung einer asynchronen Suche nach Updates.</span><span class="sxs-lookup"><span data-stu-id="b37ff-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="b37ff-109">Bei der Suche werden die Suchoptionen verwendet, die derzeit konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="b37ff-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="b37ff-110">**Endsuche**</span><span class="sxs-lookup"><span data-stu-id="b37ff-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="b37ff-111">Schließt eine asynchrone Suche nach Updates ab.</span><span class="sxs-lookup"><span data-stu-id="b37ff-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="b37ff-112">**Escapezeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b37ff-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="b37ff-113">Konvertiert eine Zeichenfolge in eine Zeichenfolge, die als Literalwert in einer Such Kriterienzeichenfolge verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b37ff-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="b37ff-114">**Gettotalhistorycount**</span><span class="sxs-lookup"><span data-stu-id="b37ff-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="b37ff-115">Gibt die Anzahl der Update Ereignisse auf dem Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="b37ff-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="b37ff-116">**Queryhistory**</span><span class="sxs-lookup"><span data-stu-id="b37ff-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="b37ff-117">Fragt synchron den Computer nach dem Verlauf von Update Ereignissen ab.</span><span class="sxs-lookup"><span data-stu-id="b37ff-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="b37ff-118">**Search**</span><span class="sxs-lookup"><span data-stu-id="b37ff-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="b37ff-119">Führt eine synchrone Suche nach Updates aus.</span><span class="sxs-lookup"><span data-stu-id="b37ff-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="b37ff-120">Bei der Suche werden die Suchoptionen verwendet, die derzeit konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="b37ff-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 



