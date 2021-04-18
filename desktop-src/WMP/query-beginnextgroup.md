---
title: Query. beginnextgroup-Methode
description: Die beginnextgroup-Methode beginnt mit einer neuen Bedingungs Gruppe. | Query. beginnextgroup-Methode
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- beginnextgroup-Methode, Windows-Media Player
- beginnextgroup-Methode, Windows Media Player, Abfrage Klasse
- Query-Klasse, Windows Media Player, beginnextgroup-Methode
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361631"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="baeaf-107">Query. beginnextgroup-Methode</span><span class="sxs-lookup"><span data-stu-id="baeaf-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="baeaf-108">Die **beginnextgroup** -Methode beginnt mit einer neuen Bedingungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="baeaf-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="baeaf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="baeaf-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="baeaf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="baeaf-110">Parameters</span></span>

<span data-ttu-id="baeaf-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="baeaf-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="baeaf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baeaf-112">Return value</span></span>

<span data-ttu-id="baeaf-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="baeaf-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="baeaf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baeaf-114">Remarks</span></span>

<span data-ttu-id="baeaf-115">Das Starten einer neuen Bedingungs Gruppe impliziert, dass Sie die aktuelle Bedingungs Gruppe abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="baeaf-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="baeaf-116">Die neue Bedingungs Gruppe wird immer mit der-oder-Logik mit der vorherigen Bedingungs Gruppe verkettet.</span><span class="sxs-lookup"><span data-stu-id="baeaf-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="baeaf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baeaf-117">Requirements</span></span>



| <span data-ttu-id="baeaf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baeaf-118">Requirement</span></span> | <span data-ttu-id="baeaf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="baeaf-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="baeaf-120">Version</span><span class="sxs-lookup"><span data-stu-id="baeaf-120">Version</span></span><br/> | <span data-ttu-id="baeaf-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="baeaf-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="baeaf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="baeaf-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="baeaf-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baeaf-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baeaf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baeaf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baeaf-125">**Mediacollection. kreatequery**</span><span class="sxs-lookup"><span data-stu-id="baeaf-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="baeaf-126">**Mediacollection. getplaylistbyquery**</span><span class="sxs-lookup"><span data-stu-id="baeaf-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="baeaf-127">**Mediacollection. getstringcollectionbyquery**</span><span class="sxs-lookup"><span data-stu-id="baeaf-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="baeaf-128">**Query-Objekt**</span><span class="sxs-lookup"><span data-stu-id="baeaf-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="baeaf-129">**Query. addcondition**</span><span class="sxs-lookup"><span data-stu-id="baeaf-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





