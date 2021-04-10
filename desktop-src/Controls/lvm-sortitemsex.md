---
title: LVM_SORTITEMSEX Meldung (kommstrg. h)
description: Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren. Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros "mentemsex" senden.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Windows-Steuerelemente für LVM_SORTITEMSEX Meldung
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040175"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="16961-106">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="16961-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="16961-107">Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="16961-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="16961-108">Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="16961-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="16961-109">Sie können diese Nachricht explizit oder mithilfe des ListView-Makros " [**\_ mentemsex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) " senden.</span><span class="sxs-lookup"><span data-stu-id="16961-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="16961-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="16961-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16961-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16961-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16961-112">Der von der Anwendung definierte Wert, der an die Vergleichsfunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="16961-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="16961-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16961-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16961-114">Zeiger auf eine Anwendungs definierte Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="16961-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="16961-115">Sie wird während des Sortier Vorgangs jedes Mal aufgerufen, wenn die relative Reihenfolge zweier Listenelemente verglichen werden muss.</span><span class="sxs-lookup"><span data-stu-id="16961-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16961-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16961-116">Return value</span></span>

<span data-ttu-id="16961-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="16961-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="16961-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16961-118">Remarks</span></span>

<span data-ttu-id="16961-119">Die Vergleichsfunktion weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="16961-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="16961-120">Diese Meldung ähnelt LVM- [**Elementen \_**](lvm-sortitems.md), mit Ausnahme der Art von Informationen, die an die Vergleichsfunktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="16961-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="16961-121">Mit **LVM \_**-Element-Sexualität ist *lParam1* der aktuelle Index des ersten Elements, und *lParam2* ist der aktuelle Index des zweiten Elements.</span><span class="sxs-lookup"><span data-stu-id="16961-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="16961-122">Wenn erforderlich, können Sie eine [**LVM- \_ GetItemText**](lvm-getitemtext.md) -Nachricht senden, um weitere Informationen zu einem Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16961-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="16961-123">Die Vergleichsfunktion muss einen negativen Wert zurückgeben, wenn das erste Element dem zweiten vorangestellt wird, ein positiver Wert, wenn das erste Element der zweiten folgt, oder 0 (null), wenn die beiden Elemente äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="16961-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="16961-124">Während des Sortier Vorgangs sind die Inhalte der Listenansicht instabil.</span><span class="sxs-lookup"><span data-stu-id="16961-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="16961-125">Wenn die Rückruffunktion Nachrichten von [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) an das Listenansicht-Steuerelement sendet, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="16961-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16961-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16961-126">Requirements</span></span>



| <span data-ttu-id="16961-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16961-127">Requirement</span></span> | <span data-ttu-id="16961-128">Wert</span><span class="sxs-lookup"><span data-stu-id="16961-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16961-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16961-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16961-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16961-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16961-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16961-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16961-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16961-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16961-133">Header</span><span class="sxs-lookup"><span data-stu-id="16961-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="16961-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="16961-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





