---
title: EditBox. getlineingedex
description: Die getlineindex-Methode ruft den Zeichen Index des ersten Zeichens in der Zeile mit dem angegebenen Zeilen Index ab.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- EditBox. getlineingedex-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352176"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="fbe72-104">EditBox. getlineingedex</span><span class="sxs-lookup"><span data-stu-id="fbe72-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="fbe72-105">Die **getlineindex** -Methode ruft den Zeichen Index des ersten Zeichens in der Zeile mit dem angegebenen Zeilen Index ab.</span><span class="sxs-lookup"><span data-stu-id="fbe72-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="fbe72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbe72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe72-107"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="fbe72-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="fbe72-108">**Number** (**Long**) mit dem Index der Zeile, deren Zeichen Index abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbe72-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe72-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbe72-109">Return Value</span></span>

<span data-ttu-id="fbe72-110">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="fbe72-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe72-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbe72-111">Remarks</span></span>

<span data-ttu-id="fbe72-112">Wenn der angegebene Zeilen Index 1 ist, wird die Zeile verwendet, die die Einfügemarke enthält.</span><span class="sxs-lookup"><span data-stu-id="fbe72-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="fbe72-113">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="fbe72-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe72-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbe72-114">Requirements</span></span>



| <span data-ttu-id="fbe72-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbe72-115">Requirement</span></span> | <span data-ttu-id="fbe72-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fbe72-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="fbe72-117">Version</span><span class="sxs-lookup"><span data-stu-id="fbe72-117">Version</span></span><br/> | <span data-ttu-id="fbe72-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="fbe72-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbe72-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbe72-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe72-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="fbe72-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="fbe72-121">**EditBox. getline**</span><span class="sxs-lookup"><span data-stu-id="fbe72-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="fbe72-122">**EditBox. getlinefromchar**</span><span class="sxs-lookup"><span data-stu-id="fbe72-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





