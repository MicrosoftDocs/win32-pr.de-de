---
title: ListBox. InsertItem
description: Die InsertItem-Methode fügt den angegebenen Text am angegebenen Index im Listenfeld-Steuerelement ein.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- ListBox. InsertItem-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366065"
---
# <a name="listboxinsertitem"></a><span data-ttu-id="96e5b-104">ListBox. InsertItem</span><span class="sxs-lookup"><span data-stu-id="96e5b-104">LISTBOX.insertItem</span></span>

<span data-ttu-id="96e5b-105">Die **InsertItem** -Methode fügt den angegebenen Text am angegebenen Index im Listenfeld-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="96e5b-105">The **insertItem** method inserts the specified text at the specified index in the list box control.</span></span>

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a><span data-ttu-id="96e5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e5b-107"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="96e5b-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="96e5b-108">**Zahl** (**Long**), die den Index der abzurufenden Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="96e5b-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="96e5b-109"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="96e5b-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="96e5b-110">**Zeichenfolge** , die den einzufügenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="96e5b-110">**String** containing the text to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e5b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96e5b-111">Return Value</span></span>

<span data-ttu-id="96e5b-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="96e5b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96e5b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96e5b-113">Remarks</span></span>

<span data-ttu-id="96e5b-114">Wenn eine Zeile eingefügt wird, werden die Zeilen Indizes für die Zeilen unterhalb der eingefügten Zeile um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="96e5b-114">When a line is inserted, the line indexes for the lines below the inserted line increase by one.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e5b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96e5b-115">Requirements</span></span>



| <span data-ttu-id="96e5b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96e5b-116">Requirement</span></span> | <span data-ttu-id="96e5b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="96e5b-117">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="96e5b-118">Version</span><span class="sxs-lookup"><span data-stu-id="96e5b-118">Version</span></span><br/> | <span data-ttu-id="96e5b-119">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="96e5b-119">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96e5b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96e5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e5b-121">**ListBox-Element**</span><span class="sxs-lookup"><span data-stu-id="96e5b-121">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





