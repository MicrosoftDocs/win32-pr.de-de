---
title: RBN_DELETEDBAND Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, nachdem ein Band gelöscht wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- Windows-Steuerelemente für RBN_DELETEDBAND Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859066"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="b507f-105">RBN- \_ deletedband-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b507f-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="b507f-106">Wird von einem Grund leisten-Steuerelement gesendet, nachdem ein Band gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b507f-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="b507f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b507f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b507f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b507f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b507f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b507f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b507f-110">Zeiger auf eine [**nmrebar**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="b507f-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b507f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b507f-111">Return value</span></span>

<span data-ttu-id="b507f-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b507f-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b507f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b507f-113">Requirements</span></span>



| <span data-ttu-id="b507f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b507f-114">Requirement</span></span> | <span data-ttu-id="b507f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b507f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b507f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b507f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b507f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b507f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b507f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b507f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b507f-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b507f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b507f-120">Header</span><span class="sxs-lookup"><span data-stu-id="b507f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b507f-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b507f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





