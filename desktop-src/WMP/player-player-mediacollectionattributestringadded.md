---
title: Player. mediacollectionattributestringadded-Ereignis
description: Das mediacollectionattributestringadded-Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird. | Player. mediacollectionattributestringadded-Ereignis
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Media Player für mediacollectionattributestringadded-Ereignisfenster
- Mediacollectionattributestringadded-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, mediacollectionattributestringadded-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371285"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="9282d-107">Player. mediacollectionattributestringadded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9282d-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="9282d-108">Das **mediacollectionattributestringadded** -Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9282d-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="9282d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9282d-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="9282d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9282d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9282d-111">*bstrattribname*</span><span class="sxs-lookup"><span data-stu-id="9282d-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="9282d-112">**Zeichenfolge** , die den Namen des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="9282d-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="9282d-113">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="9282d-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="9282d-114">*bstrattribval*</span><span class="sxs-lookup"><span data-stu-id="9282d-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9282d-115">Eine **Zeichenfolge** , die den Wert des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="9282d-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9282d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9282d-116">Return value</span></span>

<span data-ttu-id="9282d-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9282d-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9282d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9282d-118">Remarks</span></span>

<span data-ttu-id="9282d-119">Wenn der Bibliothek ein Medien Element hinzugefügt wird, werden die zugehörigen Metadaten dem **mediacollection** -Objekt hinzugefügt, und dieses Ereignis wird für jedes hinzugefügte Attribut ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9282d-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="9282d-120">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="9282d-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="9282d-121">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="9282d-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="9282d-122">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9282d-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9282d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9282d-123">Requirements</span></span>



| <span data-ttu-id="9282d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9282d-124">Requirement</span></span> | <span data-ttu-id="9282d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9282d-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9282d-126">Version</span><span class="sxs-lookup"><span data-stu-id="9282d-126">Version</span></span><br/> | <span data-ttu-id="9282d-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9282d-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9282d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9282d-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9282d-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9282d-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9282d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9282d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9282d-131">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="9282d-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="9282d-132">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="9282d-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="9282d-133">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="9282d-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





