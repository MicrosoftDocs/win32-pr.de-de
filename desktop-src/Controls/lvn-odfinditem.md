---
title: LVN_ODFINDITEM Meldung (kommstrg. h)
description: Wird von einem Virtual List-View-Steuerelement gesendet, wenn der Besitzer ein bestimmtes Rückruf Element finden muss.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Windows-Steuerelemente für LVN_ODFINDITEM Meldung
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104811"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="47389-104">LVN \_ odfinditem-Meldung</span><span class="sxs-lookup"><span data-stu-id="47389-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="47389-105">Wird von einem [Virtual List-View-](list-view-controls-overview.md) Steuerelement gesendet, wenn der Besitzer ein bestimmtes Rückruf Element finden muss.</span><span class="sxs-lookup"><span data-stu-id="47389-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="47389-106">Beispielsweise sendet das Steuerelement diesen Benachrichtigungs Code, wenn er Tastatureingaben empfängt oder eine [**LVM- \_ FindItem**](lvm-finditem.md) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="47389-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="47389-107">Der LVN \_ odfinditem-Benachrichtigungs Code wird in Form einer [**WM- \_**](wm-notify.md) Benachrichtigungs Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="47389-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="47389-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47389-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47389-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47389-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47389-110">Zeiger auf eine [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur, die Informationen enthält, die für die Suche verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47389-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47389-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47389-111">Return value</span></span>

<span data-ttu-id="47389-112">Gibt den Index des gefundenen Elements zurück, oder-1, wenn kein Element gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="47389-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="47389-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47389-113">Remarks</span></span>

<span data-ttu-id="47389-114">Suchinformationen werden in Form einer " [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) "-Struktur gesendet, die ein Member der [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="47389-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="47389-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47389-115">Requirements</span></span>



| <span data-ttu-id="47389-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47389-116">Requirement</span></span> | <span data-ttu-id="47389-117">Wert</span><span class="sxs-lookup"><span data-stu-id="47389-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47389-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47389-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47389-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47389-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47389-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47389-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47389-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47389-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47389-122">Header</span><span class="sxs-lookup"><span data-stu-id="47389-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47389-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="47389-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="47389-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="47389-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="47389-125">**LVN \_ Odfinditemw** (Unicode) und **LVN \_ odfinditema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="47389-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





