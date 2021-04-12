---
title: RBN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer mit dem Ziehen eines Bands beginnt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- Windows-Steuerelemente für RBN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475339"
---
# <a name="rbn_begindrag-notification-code"></a><span data-ttu-id="99c13-105">RBN \_ BeginDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="99c13-105">RBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="99c13-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer mit dem Ziehen eines Bands beginnt.</span><span class="sxs-lookup"><span data-stu-id="99c13-106">Sent by a rebar control when the user begins dragging a band.</span></span> <span data-ttu-id="99c13-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="99c13-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="99c13-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="99c13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99c13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99c13-110">Zeiger auf eine [**nmrebar**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="99c13-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c13-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99c13-111">Return value</span></span>

<span data-ttu-id="99c13-112">Gibt 0 (null) zurück, damit der Schiebe Bereich den Zieh Vorgang fortsetzen kann, oder ungleich 0 (null), um den Zieh Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="99c13-112">Return zero to allow the rebar to continue the drag operation, or nonzero to abort the drag operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c13-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99c13-113">Requirements</span></span>



| <span data-ttu-id="99c13-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99c13-114">Requirement</span></span> | <span data-ttu-id="99c13-115">Wert</span><span class="sxs-lookup"><span data-stu-id="99c13-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99c13-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99c13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99c13-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99c13-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99c13-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99c13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99c13-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99c13-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99c13-120">Header</span><span class="sxs-lookup"><span data-stu-id="99c13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c13-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c13-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





