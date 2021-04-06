---
title: TBN_CUSTHELP Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer die Schaltfläche "Hilfe" im Dialogfeld "Symbolleiste anpassen" ausgewählt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- Windows-Steuerelemente für TBN_CUSTHELP Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858754"
---
# <a name="tbn_custhelp-notification-code"></a><span data-ttu-id="cc8f6-105">TBN- \_ custhelp-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="cc8f6-105">TBN\_CUSTHELP notification code</span></span>

<span data-ttu-id="cc8f6-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer die Schaltfläche "Hilfe" im Dialogfeld "Symbolleiste anpassen" ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-106">Notifies a toolbar's parent window that the user has chosen the Help button in the Customize Toolbar dialog box.</span></span> <span data-ttu-id="cc8f6-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cc8f6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc8f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc8f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc8f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc8f6-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc8f6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc8f6-111">Return value</span></span>

<span data-ttu-id="cc8f6-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8f6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc8f6-113">Requirements</span></span>



| <span data-ttu-id="cc8f6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc8f6-114">Requirement</span></span> | <span data-ttu-id="cc8f6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cc8f6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8f6-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc8f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8f6-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc8f6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc8f6-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc8f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8f6-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc8f6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc8f6-120">Header</span><span class="sxs-lookup"><span data-stu-id="cc8f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc8f6-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc8f6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





