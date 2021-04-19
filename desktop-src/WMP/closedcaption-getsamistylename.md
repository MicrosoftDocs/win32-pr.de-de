---
title: Closedcaption. getsamistylename-Methode
description: Die getsamistylename-Methode ruft den Namen eines Stils ab, der von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- getsamistylename-Methode, Windows Media Player
- getsamistylename-Methode, Windows Media Player, closedcaption-Klasse
- Closedcaption-Klasse, Windows Media Player, getsamistylename-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359311"
---
# <a name="closedcaptiongetsamistylename-method"></a><span data-ttu-id="e1c7c-106">Closedcaption. getsamistylename-Methode</span><span class="sxs-lookup"><span data-stu-id="e1c7c-106">ClosedCaption.getSAMIStyleName method</span></span>

<span data-ttu-id="e1c7c-107">Die **getsamistylename** -Methode ruft den Namen eines Stils ab, der von der aktuellen Sami-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-107">The **getSAMIStyleName** method retrieves the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c7c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1c7c-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e1c7c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1c7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1c7c-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1c7c-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1c7c-111">**Zahl** (**Long**), die den Index des abzurufenden Format namens angibt.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-111">**Number** (**long**) specifying the index of the style name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1c7c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1c7c-112">Return value</span></span>

<span data-ttu-id="e1c7c-113">Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen des Stils enthält, wie in der Sami-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-113">This method returns a **String** containing the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c7c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1c7c-114">Remarks</span></span>

<span data-ttu-id="e1c7c-115">Die Stile in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e1c7c-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="e1c7c-116">Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="e1c7c-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="e1c7c-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c7c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1c7c-118">Requirements</span></span>



| <span data-ttu-id="e1c7c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1c7c-119">Requirement</span></span> | <span data-ttu-id="e1c7c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e1c7c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c7c-121">Version</span><span class="sxs-lookup"><span data-stu-id="e1c7c-121">Version</span></span><br/> | <span data-ttu-id="e1c7c-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e1c7c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e1c7c-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1c7c-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1c7c-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1c7c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1c7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c7c-126">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="e1c7c-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="e1c7c-127">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e1c7c-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="e1c7c-128">**Closedcaption. samistyle**</span><span class="sxs-lookup"><span data-stu-id="e1c7c-128">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





