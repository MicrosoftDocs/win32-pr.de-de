---
description: Die IUpdateSession3-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: IUpdateSession3-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128276"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="4e7cf-103">IUpdateSession3-Methoden</span><span class="sxs-lookup"><span data-stu-id="4e7cf-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="4e7cf-104">Die [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="4e7cf-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="4e7cf-105">Methode</span><span class="sxs-lookup"><span data-stu-id="4e7cf-105">Method</span></span>                                                                           | <span data-ttu-id="4e7cf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e7cf-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e7cf-107">**"Kreateupdateservicemanager"**</span><span class="sxs-lookup"><span data-stu-id="4e7cf-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="4e7cf-108">Gibt einen Zeiger auf eine [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) -Schnittstelle für die Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="4e7cf-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="4e7cf-109">**Queryhistory**</span><span class="sxs-lookup"><span data-stu-id="4e7cf-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="4e7cf-110">Gibt einen Zeiger auf eine [**iupdatehistoryentrycollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4e7cf-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="4e7cf-111">Die-Schnittstelle enthält übereinstimmende Ereignisdaten Sätze auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="4e7cf-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="4e7cf-112">Dadurch wird der Computer von der [**queryhistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) -Methode synchron nach dem Verlauf von Update Ereignissen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="4e7cf-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="4e7cf-113">Informationen zu den Membern, die von dieser Schnittstelle geerbt werden, finden Sie unter den folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="4e7cf-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="4e7cf-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="4e7cf-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="4e7cf-115">**Iupdatesession**</span><span class="sxs-lookup"><span data-stu-id="4e7cf-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



