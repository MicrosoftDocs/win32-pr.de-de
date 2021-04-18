---
title: CBEN_BEGINEDIT Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer die Dropdown Liste aktiviert oder in das Bearbeitungsfeld des Steuer Elements klickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- Windows-Steuerelemente für CBEN_BEGINEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344706"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="f029e-105">Cben \_ BeginEdit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f029e-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="f029e-106">Wird gesendet, wenn der Benutzer die Dropdown Liste aktiviert oder in das Bearbeitungsfeld des Steuer Elements klickt.</span><span class="sxs-lookup"><span data-stu-id="f029e-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="f029e-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f029e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f029e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f029e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f029e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f029e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f029e-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="f029e-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f029e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f029e-111">Return value</span></span>

<span data-ttu-id="f029e-112">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f029e-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f029e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f029e-113">Requirements</span></span>



| <span data-ttu-id="f029e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f029e-114">Requirement</span></span> | <span data-ttu-id="f029e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f029e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f029e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f029e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f029e-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f029e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f029e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f029e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f029e-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f029e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f029e-120">Header</span><span class="sxs-lookup"><span data-stu-id="f029e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f029e-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f029e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





