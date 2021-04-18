---
title: MCN_VIEWCHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn sich die aktuelle Ansicht ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- Windows-Steuerelemente für MCN_VIEWCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475549"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="19b62-105">MCN \_ ViewChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="19b62-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="19b62-106">Wird von einem Monatskalender-Steuerelement gesendet, wenn sich die aktuelle Ansicht ändert.</span><span class="sxs-lookup"><span data-stu-id="19b62-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="19b62-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="19b62-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="19b62-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19b62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b62-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19b62-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19b62-110">Ein Zeiger auf eine [**nmviewchange**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) -Struktur, die Informationen über die aktuelle Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="19b62-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b62-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19b62-111">Return value</span></span>

<span data-ttu-id="19b62-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="19b62-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b62-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19b62-113">Requirements</span></span>



| <span data-ttu-id="19b62-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19b62-114">Requirement</span></span> | <span data-ttu-id="19b62-115">Wert</span><span class="sxs-lookup"><span data-stu-id="19b62-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19b62-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19b62-116">Minimum supported client</span></span><br/> | <span data-ttu-id="19b62-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19b62-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19b62-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19b62-118">Minimum supported server</span></span><br/> | <span data-ttu-id="19b62-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19b62-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19b62-120">Header</span><span class="sxs-lookup"><span data-stu-id="19b62-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="19b62-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="19b62-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





