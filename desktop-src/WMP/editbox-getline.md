---
title: EditBox. getline
description: Die getline-Methode ruft den Text für die Zeile mit dem angegebenen Index ab.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- EditBox. getline-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357952"
---
# <a name="editboxgetline"></a><span data-ttu-id="cf0b3-104">EditBox. getline</span><span class="sxs-lookup"><span data-stu-id="cf0b3-104">EDITBOX.getLine</span></span>

<span data-ttu-id="cf0b3-105">Die **getline** -Methode ruft den Text für die Zeile mit dem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="cf0b3-105">The **getLine** method retrieves the text for the line with the specified index.</span></span>

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a><span data-ttu-id="cf0b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf0b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0b3-107"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="cf0b3-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="cf0b3-108">**Zahl** (**Long**), die den Index der abzurufenden Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="cf0b3-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf0b3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf0b3-109">Return Value</span></span>

<span data-ttu-id="cf0b3-110">Diese Methode gibt eine **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf0b3-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf0b3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf0b3-111">Remarks</span></span>

<span data-ttu-id="cf0b3-112">Wenn der Index ungültig ist, wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf0b3-112">If the index is not valid, an empty string is returned.</span></span> <span data-ttu-id="cf0b3-113">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="cf0b3-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf0b3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf0b3-114">Requirements</span></span>



| <span data-ttu-id="cf0b3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf0b3-115">Requirement</span></span> | <span data-ttu-id="cf0b3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cf0b3-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="cf0b3-117">Version</span><span class="sxs-lookup"><span data-stu-id="cf0b3-117">Version</span></span><br/> | <span data-ttu-id="cf0b3-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="cf0b3-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf0b3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf0b3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0b3-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="cf0b3-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="cf0b3-121">**EditBox. getlinefromchar**</span><span class="sxs-lookup"><span data-stu-id="cf0b3-121">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="cf0b3-122">**EditBox. getlineingedex**</span><span class="sxs-lookup"><span data-stu-id="cf0b3-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





