---
title: TVM_SORTCHILDRENCB Meldung (kommstrg. h)
description: Sortiert Struktur Ansichts Elemente mithilfe einer Anwendungs definierten Rückruffunktion, die die Elemente vergleicht. Sie können diese Nachricht explizit oder mit dem TreeView- \_ Makro "SortChildren-CB" senden.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Windows-Steuerelemente für TVM_SORTCHILDRENCB Meldung
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478945"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="4e72c-105">TVM \_ SortChildren-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4e72c-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="4e72c-106">Sortiert Struktur Ansichts Elemente mithilfe einer Anwendungs definierten Rückruffunktion, die die Elemente vergleicht.</span><span class="sxs-lookup"><span data-stu-id="4e72c-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="4e72c-107">Sie können diese Nachricht explizit oder mit dem [**TreeView-Makro " \_ SortChildren-CB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) " senden.</span><span class="sxs-lookup"><span data-stu-id="4e72c-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e72c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e72c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e72c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e72c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e72c-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4e72c-110">Reserved.</span></span> <span data-ttu-id="4e72c-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4e72c-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4e72c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e72c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e72c-113">Zeiger auf eine [**tvsortcb**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4e72c-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="4e72c-114">Der **lpfncompare** -Member ist die Adresse der Anwendungs definierten Rückruffunktion, die während des Sortier Vorgangs aufgerufen wird, wenn die relative Reihenfolge zweier Listenelemente verglichen werden muss.</span><span class="sxs-lookup"><span data-stu-id="4e72c-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="4e72c-115">Weitere Informationen zur Rückruffunktion finden Sie in der Beschreibung von **tvsortcb**.</span><span class="sxs-lookup"><span data-stu-id="4e72c-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e72c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e72c-116">Return value</span></span>

<span data-ttu-id="4e72c-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4e72c-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e72c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e72c-118">Requirements</span></span>



| <span data-ttu-id="4e72c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e72c-119">Requirement</span></span> | <span data-ttu-id="4e72c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4e72c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e72c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e72c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e72c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e72c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e72c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e72c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e72c-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e72c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e72c-125">Header</span><span class="sxs-lookup"><span data-stu-id="4e72c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e72c-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e72c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





