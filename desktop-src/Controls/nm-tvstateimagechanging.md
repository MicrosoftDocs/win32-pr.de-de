---
title: NM_TVSTATEIMAGECHANGING Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement an das übergeordnete Fenster gesendet, das von dem Zustands Bild geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- Windows-Steuerelemente für NM_TVSTATEIMAGECHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103343"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="e567e-105">NM \_ tvstatueimagechanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e567e-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="e567e-106">Wird von einem Strukturansicht-Steuerelement an das übergeordnete Fenster gesendet, das von dem Zustands Bild geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e567e-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="e567e-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="e567e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e567e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e567e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e567e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e567e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e567e-110">Ein Zeiger auf eine [**nmtvstatueimagechanging**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="e567e-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e567e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e567e-111">Return value</span></span>

<span data-ttu-id="e567e-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e567e-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e567e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e567e-113">Requirements</span></span>



| <span data-ttu-id="e567e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e567e-114">Requirement</span></span> | <span data-ttu-id="e567e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e567e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e567e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e567e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e567e-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e567e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e567e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e567e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e567e-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e567e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e567e-120">Header</span><span class="sxs-lookup"><span data-stu-id="e567e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e567e-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e567e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





