---
title: TBN_DELETINGBUTTON Meldung (kommstrg. h)
description: Wird von einem Symbolleisten-Steuerelement gesendet, wenn eine Schaltfläche gelöscht wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Windows-Steuerelemente für TBN_DELETINGBUTTON Meldung
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517510"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="b5125-105">TBN- \_ Delta Button-Meldung</span><span class="sxs-lookup"><span data-stu-id="b5125-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="b5125-106">Wird von einem Symbolleisten-Steuerelement gesendet, wenn eine Schaltfläche gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b5125-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="b5125-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b5125-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b5125-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5125-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5125-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5125-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5125-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur, die Informationen über die Schaltfläche enthält, die gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b5125-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="b5125-111">Bei diesem Benachrichtigungs Code sind nur die **HDR** -und **iItem** -Member dieser Struktur gültig.</span><span class="sxs-lookup"><span data-stu-id="b5125-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="b5125-112">Der **iItem** -Member dieser Struktur enthält den Befehls Bezeichner der Schaltfläche, die gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b5125-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5125-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5125-113">Return value</span></span>

<span data-ttu-id="b5125-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b5125-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5125-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5125-115">Requirements</span></span>



| <span data-ttu-id="b5125-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5125-116">Requirement</span></span> | <span data-ttu-id="b5125-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b5125-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5125-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5125-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5125-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5125-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5125-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5125-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5125-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5125-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5125-122">Header</span><span class="sxs-lookup"><span data-stu-id="b5125-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5125-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5125-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





