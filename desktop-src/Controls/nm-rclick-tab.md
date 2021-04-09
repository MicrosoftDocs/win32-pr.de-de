---
title: NM_RCLICK (Registerkarte) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ef2270c0-eef3-4867-8aa3-b6ff7e1a5f0f
keywords:
- Windows-Steuerelemente (Registerkarte) NM_RCLICK
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c74249e2c2984dd11dab7c4eab8147cb572f291
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041018"
---
# <a name="nm_rclick-tab-notification-code"></a><span data-ttu-id="042bc-105">NM \_ rclick-Benachrichtigungs Code (Tab)</span><span class="sxs-lookup"><span data-stu-id="042bc-105">NM\_RCLICK (tab) notification code</span></span>

<span data-ttu-id="042bc-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="042bc-106">Notifies the parent window of a tab control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="042bc-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="042bc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="042bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="042bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="042bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="042bc-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="042bc-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042bc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="042bc-111">Return value</span></span>

<span data-ttu-id="042bc-112">Gibt einen Wert ungleich 0 (null) zurück, um die Standard Verarbeitung nicht zuzulassen, oder NULL, um die Standard Verarbeitung zuzulassen</span><span class="sxs-lookup"><span data-stu-id="042bc-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="042bc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="042bc-113">Requirements</span></span>



| <span data-ttu-id="042bc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="042bc-114">Requirement</span></span> | <span data-ttu-id="042bc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="042bc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="042bc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="042bc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="042bc-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="042bc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="042bc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="042bc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="042bc-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="042bc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="042bc-120">Header</span><span class="sxs-lookup"><span data-stu-id="042bc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="042bc-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="042bc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





