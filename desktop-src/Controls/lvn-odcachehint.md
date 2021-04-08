---
title: LVN_ODCACHEHINT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem virtuellen Listenansicht-Steuerelement gesendet, wenn sich der Inhalt des Anzeige Bereichs geändert hat.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- Windows-Steuerelemente für LVN_ODCACHEHINT Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957258"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="3b14b-104">LVN \_ odcachehint-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="3b14b-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="3b14b-105">Wird von einem virtuellen Listenansicht-Steuerelement gesendet, wenn sich der Inhalt des Anzeige Bereichs geändert hat.</span><span class="sxs-lookup"><span data-stu-id="3b14b-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="3b14b-106">Beispielsweise sendet ein Listenansicht-Steuerelement diesen Benachrichtigungs Code, wenn der Benutzer in der Anzeige des Steuer Elements einen Bildlauf durchführt.</span><span class="sxs-lookup"><span data-stu-id="3b14b-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="3b14b-107">Der LVN \_ odcachehint-Benachrichtigungs Code wird in Form einer [**WM- \_**](wm-notify.md) Benachrichtigungs Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="3b14b-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3b14b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b14b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b14b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b14b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b14b-110">Ein Zeiger auf eine [**nmlvcachehint**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) -Struktur, die Informationen über den Bereich von Elementen enthält, die zwischengespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b14b-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b14b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b14b-111">Return value</span></span>

<span data-ttu-id="3b14b-112">Die Anwendung, die diesen Benachrichtigungs Code empfängt, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3b14b-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b14b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b14b-113">Remarks</span></span>

<span data-ttu-id="3b14b-114">Wenn Sie diese Meldung verarbeiten, kann die Anwendung die im Cache gespeicherten Element Informationen aktualisieren, damit Sie beim Senden eines [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Codes sofort verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3b14b-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="3b14b-115">Beachten Sie, dass es sich bei diesem Benachrichtigungs Code nicht immer um eine exakte Darstellung der Elemente handelt, die von [LVN \_ getdispinfo](lvn-getdispinfo.md)angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3b14b-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="3b14b-116">Wenn das angeforderte Element bei der Behandlung von LVN getdispinfo nicht zwischengespeichert wird \_ , muss die Anwendung daher darauf vorbereitet sein, die angeforderten Informationen aus einer Quelle außerhalb des Caches bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b14b-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b14b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b14b-117">Requirements</span></span>



| <span data-ttu-id="3b14b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b14b-118">Requirement</span></span> | <span data-ttu-id="3b14b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3b14b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b14b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b14b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b14b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b14b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b14b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b14b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b14b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b14b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b14b-124">Header</span><span class="sxs-lookup"><span data-stu-id="3b14b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b14b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b14b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





