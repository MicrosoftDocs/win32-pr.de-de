---
title: EN_PARAGRAPHEXPANDED Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass eine Gliederung erweitert wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- Windows-Steuerelemente für EN_PARAGRAPHEXPANDED Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476980"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="764c6-105">EN \_ paragrapherweiterter Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="764c6-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="764c6-106">Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass eine Gliederung erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="764c6-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="764c6-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="764c6-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="764c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="764c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="764c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="764c6-110">Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="764c6-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="764c6-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="764c6-111">Requirements</span></span>



| <span data-ttu-id="764c6-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="764c6-112">Requirement</span></span> | <span data-ttu-id="764c6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="764c6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="764c6-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="764c6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="764c6-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="764c6-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="764c6-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="764c6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="764c6-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="764c6-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="764c6-118">Header</span><span class="sxs-lookup"><span data-stu-id="764c6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="764c6-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="764c6-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 





