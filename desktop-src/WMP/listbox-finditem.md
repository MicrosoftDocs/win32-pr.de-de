---
title: ListBox. FindItem
description: Die FindItem-Methode sucht nach einer angegebenen Zeichenfolge, beginnend mit dem Element, das dem angegebenen Element Index folgt.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- ListBox. FindItem-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356467"
---
# <a name="listboxfinditem"></a><span data-ttu-id="41ed3-104">ListBox. FindItem</span><span class="sxs-lookup"><span data-stu-id="41ed3-104">LISTBOX.findItem</span></span>

<span data-ttu-id="41ed3-105">Die **FindItem** -Methode sucht nach einer angegebenen Zeichenfolge, beginnend mit dem Element, das dem angegebenen Element Index folgt.</span><span class="sxs-lookup"><span data-stu-id="41ed3-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="41ed3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41ed3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ed3-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Start Index*</span><span class="sxs-lookup"><span data-stu-id="41ed3-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="41ed3-108">**Zahl** (**Long**), die den Index des Elements enthält, an dem die Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="41ed3-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="41ed3-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="41ed3-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="41ed3-110">**Zeichenfolge** , die den zu suchenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="41ed3-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ed3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41ed3-111">Return Value</span></span>

<span data-ttu-id="41ed3-112">Diese Methode gibt eine **Zahl** (**Long**) zurück, die den Index des Elements enthält, das die Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="41ed3-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ed3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41ed3-113">Remarks</span></span>

<span data-ttu-id="41ed3-114">Um die Suche in der ersten Zeile des Listenfeld-Steuer Elements zu starten, verwenden Sie 1 als *startIndex*.</span><span class="sxs-lookup"><span data-stu-id="41ed3-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="41ed3-115">Wenn Sie nach dem Suchen der ersten Zeile nach Text suchen möchten, verwenden Sie den zurückgegebenen Zeilen Index als *startIndex*, und die Suche wird in der nächsten Zeile gestartet.</span><span class="sxs-lookup"><span data-stu-id="41ed3-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="41ed3-116">Diese Methode sucht nach Teil Zeichenfolgen und wird nicht zwischen Groß-und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="41ed3-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ed3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41ed3-117">Requirements</span></span>



| <span data-ttu-id="41ed3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41ed3-118">Requirement</span></span> | <span data-ttu-id="41ed3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="41ed3-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="41ed3-120">Version</span><span class="sxs-lookup"><span data-stu-id="41ed3-120">Version</span></span><br/> | <span data-ttu-id="41ed3-121">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="41ed3-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41ed3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41ed3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ed3-123">**ListBox-Element**</span><span class="sxs-lookup"><span data-stu-id="41ed3-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





