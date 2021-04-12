---
title: Streamselectoperation-Klasse
description: Registriert einen Ereignishandler, der aufgerufen wird, wenn der von getmuteasync gestartete asynchrone Vorgang abgeschlossen ist, und stellt eine Methode bereit, die die Ergebnisse des Vorgangs zurückgibt. | Streamselectoperation-Klasse
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- Streamselectoperation-Klasse Medien Streaming-API
- Streamselectoperation-Klasse Medien Streaming-API, beschrieben
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219287"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="eee28-106">Streamselectoperation-Klasse</span><span class="sxs-lookup"><span data-stu-id="eee28-106">StreamSelectOperation class</span></span>

<span data-ttu-id="eee28-107">Registriert einen Ereignishandler, der aufgerufen wird, wenn der von [**getmuteasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) gestartete asynchrone Vorgang abgeschlossen ist, und stellt eine Methode bereit, die die Ergebnisse des Vorgangs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eee28-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="eee28-108">**Streamselectoperation** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eee28-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="eee28-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="eee28-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="eee28-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee28-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eee28-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="eee28-111">Methods</span></span>

<span data-ttu-id="eee28-112">Die **streamselectoperation** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eee28-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="eee28-113">Methode</span><span class="sxs-lookup"><span data-stu-id="eee28-113">Method</span></span>                                                 | <span data-ttu-id="eee28-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee28-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee28-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="eee28-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="eee28-116">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**selectbeststreamasync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="eee28-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eee28-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee28-117">Properties</span></span>

<span data-ttu-id="eee28-118">Die **streamselectoperation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eee28-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="eee28-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eee28-119">Property</span></span>                                                        | <span data-ttu-id="eee28-120">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="eee28-120">Access type</span></span>           | <span data-ttu-id="eee28-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee28-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee28-122">**Abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="eee28-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="eee28-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eee28-123">Read/write</span></span><br/> | <span data-ttu-id="eee28-124">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**selectbeststreamasync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="eee28-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

