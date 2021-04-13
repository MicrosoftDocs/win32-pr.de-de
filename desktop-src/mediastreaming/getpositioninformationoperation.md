---
title: Getpositioninformationoperation-Klasse
description: Registriert einen Ereignishandler, der aufgerufen wird, wenn der von getpositioninformationasync gestartete asynchrone Vorgang abgeschlossen ist, und stellt eine Methode bereit, die die Ergebnisse des Vorgangs zurückgibt.
ms.assetid: 57DDE3B2-EFA9-4FEB-B701-D987C58F5CEA
keywords:
- Getpositioninformationoperation-Klasse Medien Streaming-API
- Getpositioninformationoperation-Klasse Medien Streaming-API, beschrieben
topic_type:
- apiref
api_name:
- GetPositionInformationOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d62de60e1e3f7f2965b1248e173ed9962b73361d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473004"
---
# <a name="getpositioninformationoperation-class"></a><span data-ttu-id="f5528-105">Getpositioninformationoperation-Klasse</span><span class="sxs-lookup"><span data-stu-id="f5528-105">GetPositionInformationOperation class</span></span>

<span data-ttu-id="f5528-106">Registriert einen Ereignishandler, der aufgerufen wird, wenn der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) gestartete asynchrone Vorgang abgeschlossen ist, und stellt eine Methode bereit, die die Ergebnisse des Vorgangs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f5528-106">Registers an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="f5528-107">**Getpositioninformationoperation** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f5528-107">**GetPositionInformationOperation** has these types of members:</span></span>

-   [<span data-ttu-id="f5528-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f5528-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="f5528-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5528-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f5528-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f5528-110">Methods</span></span>

<span data-ttu-id="f5528-111">Die **getpositioninformationoperation** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f5528-111">The **GetPositionInformationOperation** class has these methods.</span></span>



| <span data-ttu-id="f5528-112">Methode</span><span class="sxs-lookup"><span data-stu-id="f5528-112">Method</span></span>                                                           | <span data-ttu-id="f5528-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5528-113">Description</span></span>                                                                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5528-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="f5528-114">**GetResults**</span></span>](getpositioninformationoperation-getresults.md) | <span data-ttu-id="f5528-115">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="f5528-115">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span> <br/> |



 

### <a name="properties"></a><span data-ttu-id="f5528-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5528-116">Properties</span></span>

<span data-ttu-id="f5528-117">Die **getpositioninformationoperation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f5528-117">The **GetPositionInformationOperation** class has these properties.</span></span>



| <span data-ttu-id="f5528-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f5528-118">Property</span></span>                                                                  | <span data-ttu-id="f5528-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f5528-119">Access type</span></span>           | <span data-ttu-id="f5528-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5528-120">Description</span></span>                                                                                                                                                                                          |
|:--------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5528-121">**Abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="f5528-121">**Completed**</span></span>](getpositioninformationoperation-completed.md)<br/> | <span data-ttu-id="f5528-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f5528-122">Read/write</span></span><br/> | <span data-ttu-id="f5528-123">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f5528-123">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) is completed.</span></span> <br/> |



 

 

