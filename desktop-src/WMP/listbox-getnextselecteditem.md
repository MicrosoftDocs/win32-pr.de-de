---
title: ListBox. getnextselecteditem
description: Die getnextselecteditem-Methode ruft das nächste ausgewählte Element im Listenfeld-Steuerelement ab, beginnend mit dem Element, das mit dem angegebenen Index beginnt.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- ListBox. getnextselecteditem-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354154"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="37e61-104">ListBox. getnextselecteditem</span><span class="sxs-lookup"><span data-stu-id="37e61-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="37e61-105">Die **getnextselecteditem** -Methode ruft das nächste ausgewählte Element im Listenfeld-Steuerelement ab, beginnend mit dem Element, das mit dem angegebenen Index beginnt.</span><span class="sxs-lookup"><span data-stu-id="37e61-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="37e61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37e61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37e61-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Start Index*</span><span class="sxs-lookup"><span data-stu-id="37e61-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="37e61-108">**Number** (**Long**) mit dem Index des Elements, das dem abgerufenen Element vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="37e61-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37e61-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37e61-109">Return Value</span></span>

<span data-ttu-id="37e61-110">Diese Methode gibt eine **Zahl** (**Long**) zurück, die den Index des nächsten ausgewählten Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="37e61-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="37e61-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37e61-111">Remarks</span></span>

<span data-ttu-id="37e61-112">Verwenden Sie zum Starten der Suche von Anfang an den Wert 1 für den Start Index.</span><span class="sxs-lookup"><span data-stu-id="37e61-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e61-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37e61-113">Requirements</span></span>



| <span data-ttu-id="37e61-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37e61-114">Requirement</span></span> | <span data-ttu-id="37e61-115">Wert</span><span class="sxs-lookup"><span data-stu-id="37e61-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="37e61-116">Version</span><span class="sxs-lookup"><span data-stu-id="37e61-116">Version</span></span><br/> | <span data-ttu-id="37e61-117">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="37e61-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37e61-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37e61-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e61-119">**ListBox-Element**</span><span class="sxs-lookup"><span data-stu-id="37e61-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





