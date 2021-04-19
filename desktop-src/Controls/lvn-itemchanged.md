---
title: LVN_ITEMCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass sich ein Element geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- Windows-Steuerelemente für LVN_ITEMCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345942"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="5bae0-105">LVN \_ ItemChanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5bae0-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="5bae0-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass sich ein Element geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5bae0-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="5bae0-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5bae0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5bae0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bae0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bae0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5bae0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bae0-110">Ein Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die das Element identifiziert und angibt, welche seiner Attribute geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="5bae0-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="5bae0-111">Wenn der **iItem** -Member der Struktur, auf die von *LPARAM* verwiesen wird,-1 ist, wurde die Änderung auf alle Elemente in der Listenansicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="5bae0-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bae0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bae0-112">Return value</span></span>

<span data-ttu-id="5bae0-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5bae0-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bae0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bae0-114">Remarks</span></span>

<span data-ttu-id="5bae0-115">Wenn ein Listenansicht-Steuerelement den [**LVS \_**](list-view-window-styles.md) -Besitzer Daten Stil hat und der Benutzer einen Bereich von Elementen auswählt, indem er die UMSCHALTTASTE gedrückt hält und auf die Maus klickt, werden LVN \_ ItemChanged-Benachrichtigungs Codes nicht für jedes ausgewählte oder ausgewählte Element gesendet.</span><span class="sxs-lookup"><span data-stu-id="5bae0-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="5bae0-116">Stattdessen erhalten Sie einen einzelnen [LVN- \_ odstatechanged](lvn-odstatechanged.md) -Benachrichtigungs Code, der angibt, dass sich der Zustand eines Bereichs von Elementen geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5bae0-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bae0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bae0-117">Requirements</span></span>



| <span data-ttu-id="5bae0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bae0-118">Requirement</span></span> | <span data-ttu-id="5bae0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5bae0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bae0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bae0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5bae0-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bae0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5bae0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bae0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5bae0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bae0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bae0-124">Header</span><span class="sxs-lookup"><span data-stu-id="5bae0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bae0-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bae0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





