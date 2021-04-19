---
title: Extern. selecteditemid
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. selecteditemid
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Extern. selecteditemid-Fenster Media Player
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369544"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="3c019-105">Extern. selecteditemid</span><span class="sxs-lookup"><span data-stu-id="3c019-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="3c019-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="3c019-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3c019-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c019-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3c019-108">Die **selecteditemid** -Eigenschaft ruft den Bezeichner des Medien Elements ab, das derzeit in Windows Media Player ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3c019-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c019-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c019-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="3c019-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="3c019-110">Possible Values</span></span>

<span data-ttu-id="3c019-111">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3c019-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c019-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c019-112">Remarks</span></span>

<span data-ttu-id="3c019-113">Diese Eigenschaft wird in Kombination mit der Eigenschaft [extern. selecteditemtype](external-selecteditemtype.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c019-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="3c019-114">Wenn **selecteditemtype** beispielsweise cptrackid entspricht, ist **selecteditemid** die ID des ausgewählten Titels. Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="3c019-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="3c019-115">Bestimmte Sichten in Windows Media Player ein bestimmtes Medien Element, das ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3c019-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="3c019-116">Nehmen wir beispielsweise an, dass die aktuelle Ansicht ein Album darstellt.</span><span class="sxs-lookup"><span data-stu-id="3c019-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="3c019-117">Ein Album ist ein Container von Spuren, weshalb **selecteditemtype** gleich cptrackid und **selecteditemid** die ID des ausgewählten Titels ist. Andere Sichten verfügen über kein ausgewähltes Medien Element.</span><span class="sxs-lookup"><span data-stu-id="3c019-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="3c019-118">Wenn der Benutzer z. b. auf den Stamm Knoten des Online Stores im Strukturansicht-Steuerelement klickt, zeigt Windows Media Player eine vom Online Store bereitgestellte Ermittlungs Seite an.</span><span class="sxs-lookup"><span data-stu-id="3c019-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="3c019-119">Der Player zeigt in der Benutzeroberfläche des Players keinen Container von Medien Elementen an.</span><span class="sxs-lookup"><span data-stu-id="3c019-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="3c019-120">In diesem Fall ist **selecteditemtype** gleich unknownlocation, und **selecteditemid** ist gleich der leeren Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3c019-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c019-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c019-121">Requirements</span></span>



| <span data-ttu-id="3c019-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c019-122">Requirement</span></span> | <span data-ttu-id="3c019-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3c019-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c019-124">Version</span><span class="sxs-lookup"><span data-stu-id="3c019-124">Version</span></span><br/> | <span data-ttu-id="3c019-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3c019-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="3c019-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3c019-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c019-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c019-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c019-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c019-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c019-129">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="3c019-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3c019-130">**Extern. selecteditemtype**</span><span class="sxs-lookup"><span data-stu-id="3c019-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="3c019-131">**Speicherort und ausgewähltes Element**</span><span class="sxs-lookup"><span data-stu-id="3c019-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





