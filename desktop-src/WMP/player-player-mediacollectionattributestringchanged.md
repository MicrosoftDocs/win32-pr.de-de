---
title: Player. mediacollectionattributestringchanged-Ereignis
description: Das mediacollectionattributestringchanged-Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird. | Player. mediacollectionattributestringchanged-Ereignis
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Media Player für mediacollectionattributestringchanged-Ereignisfenster
- Mediacollectionattributestringchanged-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, mediacollectionattributestringchanged-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360347"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="a08dc-107">Player. mediacollectionattributestringchanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a08dc-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="a08dc-108">Das **mediacollectionattributestringchanged** -Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a08dc-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08dc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08dc-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="a08dc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a08dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08dc-111">*bstrattribname*</span><span class="sxs-lookup"><span data-stu-id="a08dc-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="a08dc-112">**Zeichenfolge** , die den Namen des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="a08dc-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="a08dc-113">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="a08dc-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="a08dc-114">*bstroldattribval*</span><span class="sxs-lookup"><span data-stu-id="a08dc-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a08dc-115">Eine **Zeichenfolge** , die den alten Wert des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="a08dc-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="a08dc-116">*bstraunetwattribval*</span><span class="sxs-lookup"><span data-stu-id="a08dc-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a08dc-117">Eine **Zeichenfolge** , die den neuen Wert des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="a08dc-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08dc-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a08dc-118">Return value</span></span>

<span data-ttu-id="a08dc-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a08dc-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08dc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a08dc-120">Remarks</span></span>

<span data-ttu-id="a08dc-121">Wenn ein Benutzer Bibliotheks Metadaten ändert, wird das **mediacollection** -Objekt aktualisiert, und dieses Ereignis wird für jedes geänderte Attribut ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a08dc-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="a08dc-122">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="a08dc-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a08dc-123">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="a08dc-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a08dc-124">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a08dc-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a08dc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a08dc-125">Requirements</span></span>



| <span data-ttu-id="a08dc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a08dc-126">Requirement</span></span> | <span data-ttu-id="a08dc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a08dc-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a08dc-128">Version</span><span class="sxs-lookup"><span data-stu-id="a08dc-128">Version</span></span><br/> | <span data-ttu-id="a08dc-129">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a08dc-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="a08dc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a08dc-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="a08dc-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08dc-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08dc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a08dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08dc-133">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a08dc-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a08dc-134">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a08dc-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a08dc-135">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="a08dc-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





