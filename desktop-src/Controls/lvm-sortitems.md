---
title: LVM_SORTITEMS Meldung (kommstrg. h)
description: Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren. Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros "mentems" senden.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- Windows-Steuerelemente für LVM_SORTITEMS Meldung
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957265"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="4f75a-106">LVM-Geräte \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="4f75a-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="4f75a-107">Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="4f75a-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="4f75a-108">Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4f75a-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="4f75a-109">Sie können diese Nachricht explizit oder mithilfe des ListView-Makros " [**\_ mentems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) " senden.</span><span class="sxs-lookup"><span data-stu-id="4f75a-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f75a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f75a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f75a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f75a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75a-112">Der von der Anwendung definierte Wert, der an die Vergleichsfunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4f75a-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="4f75a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f75a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f75a-114">Ein Zeiger auf die Anwendungs definierte Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="4f75a-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="4f75a-115">Die Vergleichsfunktion wird beim Sortiervorgang jedes Mal aufgerufen, wenn die relative Reihenfolge zweier Listenelemente verglichen werden muss.</span><span class="sxs-lookup"><span data-stu-id="4f75a-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f75a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f75a-116">Return value</span></span>

<span data-ttu-id="4f75a-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4f75a-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f75a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f75a-118">Remarks</span></span>

<span data-ttu-id="4f75a-119">Die Vergleichsfunktion weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="4f75a-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="4f75a-120">Der *lParam1* -Parameter ist der Wert, der dem ersten zu vergleichenden Element zugeordnet ist, und der *lParam2* -Parameter ist der Wert, der dem zweiten Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4f75a-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="4f75a-121">Dabei handelt es sich um die Werte, die im **LPARAM** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur der Elemente angegeben wurden, als Sie in die Liste eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="4f75a-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="4f75a-122">Der *wParam* -Parameter der [**\_ ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)-Elemente wird als dritter Parameter an die Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="4f75a-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="4f75a-123">Die Vergleichsfunktion muss einen negativen Wert zurückgeben, wenn das erste Element dem zweiten vorangestellt wird, ein positiver Wert, wenn das erste Element der zweiten folgt, oder 0 (null), wenn die beiden Elemente äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="4f75a-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="4f75a-124">Während des Sortier Vorgangs sind die Inhalte der Listenansicht instabil.</span><span class="sxs-lookup"><span data-stu-id="4f75a-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="4f75a-125">Wenn die Rückruffunktion Nachrichten von [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) an das Listenansicht-Steuerelement sendet, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="4f75a-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f75a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f75a-126">Requirements</span></span>



| <span data-ttu-id="4f75a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f75a-127">Requirement</span></span> | <span data-ttu-id="4f75a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4f75a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f75a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f75a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4f75a-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f75a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f75a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f75a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4f75a-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f75a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f75a-133">Header</span><span class="sxs-lookup"><span data-stu-id="4f75a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f75a-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f75a-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





