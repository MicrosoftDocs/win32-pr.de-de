---
title: RBN_DELETINGBAND Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Band im Begriff ist, gelöscht zu werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- Windows-Steuerelemente für RBN_DELETINGBAND Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956795"
---
# <a name="rbn_deletingband-notification-code"></a><span data-ttu-id="8c4f2-105">RBN- \_ Delta-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8c4f2-105">RBN\_DELETINGBAND notification code</span></span>

<span data-ttu-id="8c4f2-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Band im Begriff ist, gelöscht zu werden.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-106">Sent by a rebar control when a band is about to be deleted.</span></span> <span data-ttu-id="8c4f2-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8c4f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c4f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c4f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c4f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c4f2-110">Zeiger auf eine [**nmrebar**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c4f2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c4f2-111">Return value</span></span>

<span data-ttu-id="8c4f2-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c4f2-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4f2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c4f2-113">Requirements</span></span>



| <span data-ttu-id="8c4f2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c4f2-114">Requirement</span></span> | <span data-ttu-id="8c4f2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8c4f2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4f2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c4f2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c4f2-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c4f2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c4f2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c4f2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c4f2-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c4f2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c4f2-120">Header</span><span class="sxs-lookup"><span data-stu-id="8c4f2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c4f2-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4f2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





