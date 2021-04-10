---
title: LVN_COLUMNCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Spaltenheader geklickt wurde, während sich das Listenansicht-Steuerelement im Berichtsmodus befand. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- Windows-Steuerelemente für LVN_COLUMNCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040170"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="9e82f-105">LVN- \_ ColumnClick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9e82f-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="9e82f-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Spaltenheader geklickt wurde, während sich das Listenansicht-Steuerelement im Berichtsmodus befand.</span><span class="sxs-lookup"><span data-stu-id="9e82f-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="9e82f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="9e82f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9e82f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e82f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e82f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e82f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e82f-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9e82f-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="9e82f-111">Der **iItem** -Member ist-1, und der **iSubItem** -Member identifiziert die Spalte.</span><span class="sxs-lookup"><span data-stu-id="9e82f-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="9e82f-112">Alle anderen Elemente sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9e82f-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e82f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e82f-113">Return value</span></span>

<span data-ttu-id="9e82f-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="9e82f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e82f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e82f-115">Remarks</span></span>

<span data-ttu-id="9e82f-116">\_Wenn Sie das Format von Spalten Headern in einem Listenansicht-Steuerelement mithilfe von Header Steuerungs Formaten wie z. b. hdf ändern, sendet das Steuerelement beim Klicken auf ein Header Element den [ \_ itemstatueiconfiguration](hdn-itemstateiconclick.md) -Benachrichtigungs Code von Hdn anstelle von LVN \_ ColumnClick.</span><span class="sxs-lookup"><span data-stu-id="9e82f-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e82f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e82f-117">Requirements</span></span>



| <span data-ttu-id="9e82f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e82f-118">Requirement</span></span> | <span data-ttu-id="9e82f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9e82f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e82f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e82f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e82f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e82f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e82f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e82f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e82f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e82f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e82f-124">Header</span><span class="sxs-lookup"><span data-stu-id="9e82f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e82f-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e82f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





