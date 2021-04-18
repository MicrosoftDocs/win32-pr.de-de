---
title: EditBox. getlinefromchar
description: Die getlinefromchar-Methode ruft den Zeilen Index für den angegebenen Zeichen Index ab.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EditBox. getlinefromchar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365852"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="3bc14-104">EditBox. getlinefromchar</span><span class="sxs-lookup"><span data-stu-id="3bc14-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="3bc14-105">Die **getlinefromchar** -Methode ruft den Zeilen Index für den angegebenen Zeichen Index ab.</span><span class="sxs-lookup"><span data-stu-id="3bc14-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="3bc14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bc14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc14-107"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="3bc14-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="3bc14-108">**Zahl** (**Long**), die den Index des Zeichens enthält, dessen Zeilen Index abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bc14-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc14-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bc14-109">Return Value</span></span>

<span data-ttu-id="3bc14-110">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="3bc14-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc14-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bc14-111">Remarks</span></span>

<span data-ttu-id="3bc14-112">Wenn die angegebene Zeichenposition 1 ist, ruft diese Methode den Zeilen Index der aktuellen Zeile ab.</span><span class="sxs-lookup"><span data-stu-id="3bc14-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="3bc14-113">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="3bc14-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc14-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bc14-114">Requirements</span></span>



| <span data-ttu-id="3bc14-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bc14-115">Requirement</span></span> | <span data-ttu-id="3bc14-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3bc14-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="3bc14-117">Version</span><span class="sxs-lookup"><span data-stu-id="3bc14-117">Version</span></span><br/> | <span data-ttu-id="3bc14-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="3bc14-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3bc14-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bc14-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc14-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="3bc14-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="3bc14-121">**EditBox. getline**</span><span class="sxs-lookup"><span data-stu-id="3bc14-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="3bc14-122">**EditBox. getlineingedex**</span><span class="sxs-lookup"><span data-stu-id="3bc14-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





