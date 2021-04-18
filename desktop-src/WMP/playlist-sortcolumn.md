---
title: Playlist. SortColumn
description: Die SortColumn-Methode sortiert die Daten in der angegebenen Spalte.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- Wiedergabeliste. SortColumn-Fenster Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364561"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="9cec8-104">Playlist. SortColumn</span><span class="sxs-lookup"><span data-stu-id="9cec8-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="9cec8-105">Die **SortColumn** -Methode sortiert die Daten in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="9cec8-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="9cec8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cec8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cec8-107"><span id="column"></span><span id="COLUMN"></span>*Kolumne*</span><span class="sxs-lookup"><span data-stu-id="9cec8-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="9cec8-108">**Zahl** (**Long**), die den Index der zu sortierenden Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="9cec8-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cec8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cec8-109">Return Value</span></span>

<span data-ttu-id="9cec8-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9cec8-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cec8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cec8-111">Remarks</span></span>

<span data-ttu-id="9cec8-112">Diese Methode sortiert die angegebene Spalte auf die gleiche Weise wie die Spaltenheader Schaltflächen im **Wiedergabe** Listenelement.</span><span class="sxs-lookup"><span data-stu-id="9cec8-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="9cec8-113">Wenn die Spalte noch nicht sortiert wurde, wird Sie in alphanumerischer Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="9cec8-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="9cec8-114">Wenn Sie sortiert wurde, wird die Reihenfolge umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="9cec8-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="9cec8-115">Damit diese Methode funktioniert, muss das **allowcolumnsortierung** -Attribut auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9cec8-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cec8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cec8-116">Requirements</span></span>



| <span data-ttu-id="9cec8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cec8-117">Requirement</span></span> | <span data-ttu-id="9cec8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9cec8-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9cec8-119">Version</span><span class="sxs-lookup"><span data-stu-id="9cec8-119">Version</span></span><br/> | <span data-ttu-id="9cec8-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9cec8-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9cec8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cec8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cec8-122">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="9cec8-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="9cec8-123">**Wiedergabeliste. allowcolumnsortierung**</span><span class="sxs-lookup"><span data-stu-id="9cec8-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





