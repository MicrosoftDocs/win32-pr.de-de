---
title: RBN_HEIGHTCHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn sich seine Höhe geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- Windows-Steuerelemente für RBN_HEIGHTCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949816"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="9f327-105">RBN- \_ heightChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9f327-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="9f327-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn sich seine Höhe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9f327-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="9f327-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="9f327-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9f327-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f327-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f327-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f327-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f327-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="9f327-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f327-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f327-111">Return value</span></span>

<span data-ttu-id="9f327-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f327-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f327-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f327-113">Remarks</span></span>

<span data-ttu-id="9f327-114">Grund leisten-Steuerelemente, die den [**CCS- \_ Vert**](common-control-styles.md) -Stil verwenden, senden diesen Benachrichtigungs Code, wenn sich die Breite</span><span class="sxs-lookup"><span data-stu-id="9f327-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f327-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f327-115">Requirements</span></span>



| <span data-ttu-id="9f327-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f327-116">Requirement</span></span> | <span data-ttu-id="9f327-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9f327-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f327-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f327-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9f327-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f327-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f327-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f327-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9f327-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f327-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f327-122">Header</span><span class="sxs-lookup"><span data-stu-id="9f327-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f327-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f327-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





