---
title: TDN_HELP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer F1 auf der Tastatur drückt, während das Dialogfeld den Fokus besitzt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- Windows-Steuerelemente für TDN_HELP Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106238"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="52863-105">TDN- \_ Hilfe-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="52863-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="52863-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer F1 auf der Tastatur drückt, während das Dialogfeld den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="52863-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="52863-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="52863-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="52863-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="52863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52863-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52863-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52863-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="52863-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="52863-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52863-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52863-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="52863-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52863-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52863-113">Return value</span></span>

<span data-ttu-id="52863-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="52863-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="52863-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52863-115">Requirements</span></span>



| <span data-ttu-id="52863-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52863-116">Requirement</span></span> | <span data-ttu-id="52863-117">Wert</span><span class="sxs-lookup"><span data-stu-id="52863-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52863-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52863-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52863-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52863-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52863-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52863-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52863-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52863-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52863-122">Header</span><span class="sxs-lookup"><span data-stu-id="52863-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52863-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="52863-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





