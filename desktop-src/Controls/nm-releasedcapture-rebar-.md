---
title: Benachrichtigungs Code für NM_RELEASEDCAPTURE (Rebar) (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Info leisten Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- Windows-Steuerelemente für die NM_RELEASEDCAPTURE (Info Leiste)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f5367a0a5d5fac0948493ef70e4be1140013c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956537"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a><span data-ttu-id="88e67-105">NM \_ releasedcapture (Rebar)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="88e67-105">NM\_RELEASEDCAPTURE (rebar) notification code</span></span>

<span data-ttu-id="88e67-106">Benachrichtigt das übergeordnete Fenster eines Info leisten Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt.</span><span class="sxs-lookup"><span data-stu-id="88e67-106">Notifies a rebar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="88e67-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="88e67-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="88e67-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88e67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88e67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88e67-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="88e67-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e67-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88e67-111">Return value</span></span>

<span data-ttu-id="88e67-112">Das-Steuerelement ignoriert den Rückgabewert aus diesem Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="88e67-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e67-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88e67-113">Requirements</span></span>



| <span data-ttu-id="88e67-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88e67-114">Requirement</span></span> | <span data-ttu-id="88e67-115">Wert</span><span class="sxs-lookup"><span data-stu-id="88e67-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88e67-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88e67-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88e67-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88e67-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88e67-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88e67-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88e67-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88e67-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88e67-120">Header</span><span class="sxs-lookup"><span data-stu-id="88e67-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e67-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="88e67-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





