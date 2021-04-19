---
title: Player. mediacollectionattributestraningrebewegereignis
description: Das Ereignis mediacollectionattributestraningrebewegt tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird. | Player. mediacollectionattributestraningrebewegereignis
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Ereignisfenster für mediacollectionattributestraningrebewesfenster Media Player
- Mediacollectionattributestraningrebewegereignis-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, mediacollectionattributestraningrebewegereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364038"
---
# <a name="playermediacollectionattributestringremoved-event"></a><span data-ttu-id="f1b8a-107">Player. mediacollectionattributestraningrebewegereignis</span><span class="sxs-lookup"><span data-stu-id="f1b8a-107">Player.MediaCollectionAttributeStringRemoved event</span></span>

<span data-ttu-id="f1b8a-108">Das Ereignis **mediacollectionattributestraningrebewegt** tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-108">The **MediaCollectionAttributeStringRemoved** event occurs when an attribute value is removed from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b8a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1b8a-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="f1b8a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1b8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b8a-111">*bstrattribname*</span><span class="sxs-lookup"><span data-stu-id="f1b8a-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b8a-112">**Zeichenfolge** , die den Namen des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="f1b8a-113">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1b8a-114">*bstrattribval*</span><span class="sxs-lookup"><span data-stu-id="f1b8a-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b8a-115">Eine **Zeichenfolge** , die den Wert des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b8a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1b8a-116">Return value</span></span>

<span data-ttu-id="f1b8a-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b8a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1b8a-118">Remarks</span></span>

<span data-ttu-id="f1b8a-119">Wenn ein Medien Element aus der Bibliothek entfernt wird, werden die zugehörigen Metadaten aus dem **mediacollection** -Objekt entfernt, und dieses Ereignis wird für jedes entfernte Attribut ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-119">When a media item is removed from the library, its metadata is removed from the **MediaCollection** object and this event is fired for each attribute removed.</span></span>

<span data-ttu-id="f1b8a-120">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="f1b8a-121">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="f1b8a-122">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b8a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b8a-123">Requirements</span></span>



| <span data-ttu-id="f1b8a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1b8a-124">Requirement</span></span> | <span data-ttu-id="f1b8a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f1b8a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b8a-126">Version</span><span class="sxs-lookup"><span data-stu-id="f1b8a-126">Version</span></span><br/> | <span data-ttu-id="f1b8a-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f1b8a-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f1b8a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f1b8a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1b8a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1b8a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b8a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1b8a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b8a-131">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f1b8a-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="f1b8a-132">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f1b8a-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f1b8a-133">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="f1b8a-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





