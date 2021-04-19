---
title: Extern. selecteditemtype
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. selecteditemtype
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- Extern. selecteditemtype Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352830"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="ee04c-105">Extern. selecteditemtype</span><span class="sxs-lookup"><span data-stu-id="ee04c-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="ee04c-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="ee04c-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ee04c-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee04c-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ee04c-108">Die **selecteditemtype** -Eigenschaft ruft den Typ des Medien Elements ab, das derzeit in Windows Media Player ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="ee04c-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee04c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee04c-109">Syntax</span></span>

<span data-ttu-id="ee04c-110">Window. extern. selecteditemtype ()</span><span class="sxs-lookup"><span data-stu-id="ee04c-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="ee04c-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ee04c-111">Possible Values</span></span>

<span data-ttu-id="ee04c-112">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die eine der [Bibliotheks Speicherort Konstanten](library-location-constants.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="ee04c-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee04c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee04c-113">Remarks</span></span>

<span data-ttu-id="ee04c-114">Diese Eigenschaft wird in Kombination mit der **externen. selecteditemid** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee04c-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="ee04c-115">Wenn **selecteditemtype** beispielsweise cptrackid entspricht, ist **selecteditemid** die ID des ausgewählten Titels. Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="ee04c-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="ee04c-116">Bestimmte Sichten in Windows Media Player ein bestimmtes Medien Element, das ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="ee04c-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="ee04c-117">Nehmen wir beispielsweise an, dass die aktuelle Ansicht ein Album darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee04c-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="ee04c-118">Ein Album ist ein Container von Spuren, weshalb **selecteditemtype** gleich cptrackid und **selecteditemid** die ID des ausgewählten Titels ist. Andere Sichten verfügen über kein ausgewähltes Medien Element.</span><span class="sxs-lookup"><span data-stu-id="ee04c-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="ee04c-119">Wenn der Benutzer z. b. auf den Stamm Knoten des Online Stores im Strukturansicht-Steuerelement klickt, zeigt Windows Media Player eine vom Online Store bereitgestellte Ermittlungs Seite an.</span><span class="sxs-lookup"><span data-stu-id="ee04c-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="ee04c-120">Der Player zeigt in der Benutzeroberfläche des Players keinen Container von Medien Elementen an.</span><span class="sxs-lookup"><span data-stu-id="ee04c-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="ee04c-121">In diesem Fall ist **selecteditemtype** gleich unknownlocation, und **selecteditemid** ist gleich der leeren Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ee04c-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee04c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee04c-122">Requirements</span></span>



| <span data-ttu-id="ee04c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee04c-123">Requirement</span></span> | <span data-ttu-id="ee04c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ee04c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee04c-125">Version</span><span class="sxs-lookup"><span data-stu-id="ee04c-125">Version</span></span><br/> | <span data-ttu-id="ee04c-126">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ee04c-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ee04c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee04c-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="ee04c-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee04c-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee04c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee04c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee04c-130">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="ee04c-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ee04c-131">**Extern. selecteditemid**</span><span class="sxs-lookup"><span data-stu-id="ee04c-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="ee04c-132">**Speicherort und ausgewähltes Element**</span><span class="sxs-lookup"><span data-stu-id="ee04c-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





