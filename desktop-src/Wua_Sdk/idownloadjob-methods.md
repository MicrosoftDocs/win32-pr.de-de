---
description: Die idownloadjob-Schnittstelle definiert die folgenden Methoden.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Idownloadjob-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526702"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="06fa0-103">Idownloadjob-Methoden</span><span class="sxs-lookup"><span data-stu-id="06fa0-103">IDownloadJob Methods</span></span>

<span data-ttu-id="06fa0-104">Die [**idownloadjob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="06fa0-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="06fa0-105">Methode</span><span class="sxs-lookup"><span data-stu-id="06fa0-105">Method</span></span>                                            | <span data-ttu-id="06fa0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06fa0-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06fa0-107">**Bereinigung**</span><span class="sxs-lookup"><span data-stu-id="06fa0-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="06fa0-108">Wartet, bis ein asynchroner Vorgang abgeschlossen ist, und gibt alle Rückrufe frei.</span><span class="sxs-lookup"><span data-stu-id="06fa0-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="06fa0-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="06fa0-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="06fa0-110">Gibt eine [**idownloadprogress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) -Schnittstelle zurück, die den aktuellen Fortschritt eines Downloads beschreibt.</span><span class="sxs-lookup"><span data-stu-id="06fa0-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="06fa0-111">**Requestabort**</span><span class="sxs-lookup"><span data-stu-id="06fa0-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="06fa0-112">Führt eine Anforderung zum Beenden eines asynchronen Downloads aus.</span><span class="sxs-lookup"><span data-stu-id="06fa0-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



