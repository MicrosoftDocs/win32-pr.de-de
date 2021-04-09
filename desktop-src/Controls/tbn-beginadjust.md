---
title: TBN_BEGINADJUST Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Anpassen einer Symbolleiste begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- Windows-Steuerelemente für TBN_BEGINADJUST Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4708cd205461e3117432cec25e0e4256a6b0d87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858755"
---
# <a name="tbn_beginadjust-notification-code"></a><span data-ttu-id="17131-105">TBN \_ beginanpassungsbenachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="17131-105">TBN\_BEGINADJUST notification code</span></span>

<span data-ttu-id="17131-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Anpassen einer Symbolleiste begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="17131-106">Notifies a toolbar's parent window that the user has begun customizing a toolbar.</span></span> <span data-ttu-id="17131-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="17131-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="17131-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17131-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17131-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17131-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17131-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="17131-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17131-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17131-111">Return value</span></span>

<span data-ttu-id="17131-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="17131-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="17131-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17131-113">Requirements</span></span>



| <span data-ttu-id="17131-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17131-114">Requirement</span></span> | <span data-ttu-id="17131-115">Wert</span><span class="sxs-lookup"><span data-stu-id="17131-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17131-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17131-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17131-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17131-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17131-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17131-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17131-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17131-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17131-120">Header</span><span class="sxs-lookup"><span data-stu-id="17131-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17131-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="17131-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





