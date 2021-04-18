---
title: Error-Objekt (WMP-SDK)
description: Das Error-Objekt ermöglicht den Zugriff auf eine Auflistung von ErrorItem-Objekten.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Windows-Fehler Objekt-Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2019
ms.locfileid: "106340475"
---
# <a name="error-object"></a><span data-ttu-id="69c47-104">Error-Objekt</span><span class="sxs-lookup"><span data-stu-id="69c47-104">Error Object</span></span>

<span data-ttu-id="69c47-105">Das **Error** -Objekt ermöglicht den Zugriff auf eine Auflistung von [ErrorItem](erroritem-object.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="69c47-105">The **Error** object provides access to a collection of [ErrorItem](erroritem-object.md) objects.</span></span>

<span data-ttu-id="69c47-106">Das **Error** -Objekt unterstützt die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="69c47-106">The **Error** object supports the following property.</span></span>



| <span data-ttu-id="69c47-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="69c47-107">Property</span></span>                           | <span data-ttu-id="69c47-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69c47-108">Description</span></span>                                        |
|------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="69c47-109">errorCount</span><span class="sxs-lookup"><span data-stu-id="69c47-109">errorCount</span></span>](error-errorcount.md) | <span data-ttu-id="69c47-110">Ruft die Anzahl der Fehler in der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="69c47-110">Retrieves the number of errors in the error queue.</span></span> |



 

<span data-ttu-id="69c47-111">Das **Error** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="69c47-111">The **Error** object supports the following methods.</span></span>



| <span data-ttu-id="69c47-112">Methode</span><span class="sxs-lookup"><span data-stu-id="69c47-112">Method</span></span>                                       | <span data-ttu-id="69c47-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69c47-113">Description</span></span>                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69c47-114">clearerrorqueue</span><span class="sxs-lookup"><span data-stu-id="69c47-114">clearErrorQueue</span></span>](error-clearerrorqueue.md) | <span data-ttu-id="69c47-115">Löscht die Fehler in der Fehler Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="69c47-115">Clears the errors from the error queue.</span></span>                                                         |
| [<span data-ttu-id="69c47-116">item</span><span class="sxs-lookup"><span data-stu-id="69c47-116">item</span></span>](error-item.md)                       | <span data-ttu-id="69c47-117">Ruft ein [ErrorItem](erroritem-object.md) -Objekt aus der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="69c47-117">Retrieves an [ErrorItem](erroritem-object.md) object from the error queue.</span></span>                     |
| [<span data-ttu-id="69c47-118">WebHelp</span><span class="sxs-lookup"><span data-stu-id="69c47-118">webHelp</span></span>](error-webhelp.md)                 | <span data-ttu-id="69c47-119">Hiermit wird die Windows Media Player-Webhilfe Seite gestartet, um weitere Informationen zum Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="69c47-119">Launches the Windows Media Player Web Help page to display further information about the error.</span></span> |



 

<span data-ttu-id="69c47-120">Der Zugriff auf das **Fehler** Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="69c47-120">The **Error** object is accessed through the following property.</span></span>



| <span data-ttu-id="69c47-121">Object</span><span class="sxs-lookup"><span data-stu-id="69c47-121">Object</span></span>                      | <span data-ttu-id="69c47-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="69c47-122">Property</span></span>                  |
|-----------------------------|---------------------------|
| [<span data-ttu-id="69c47-123">Player</span><span class="sxs-lookup"><span data-stu-id="69c47-123">Player</span></span>](player-object.md) | [<span data-ttu-id="69c47-124">error</span><span class="sxs-lookup"><span data-stu-id="69c47-124">error</span></span>](player-error.md) |



 

## <a name="see-also"></a><span data-ttu-id="69c47-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69c47-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c47-126">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="69c47-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




