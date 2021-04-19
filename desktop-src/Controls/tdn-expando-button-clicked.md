---
title: TDN_EXPANDO_BUTTON_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird vom Aufgaben Dialogfeld gesendet, wenn der Benutzer auf die Expando-Schaltfläche des Dialog Felds klickt. Diese Benachrichtigung wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- Windows-Steuerelemente für TDN_EXPANDO_BUTTON_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346765"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="61c83-105">TDN- \_ expando- \_ Schaltfläche mit \_ Klick</span><span class="sxs-lookup"><span data-stu-id="61c83-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="61c83-106">Wird vom Aufgaben Dialogfeld gesendet, wenn der Benutzer auf die Expando-Schaltfläche des Dialog Felds klickt.</span><span class="sxs-lookup"><span data-stu-id="61c83-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="61c83-107">Diese Benachrichtigung wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="61c83-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="61c83-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61c83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c83-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61c83-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61c83-110">Ein **boolescher** Wert, der **true** ist, wenn das Dialogfeld erweitert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="61c83-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="61c83-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61c83-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61c83-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="61c83-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61c83-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61c83-113">Return value</span></span>

<span data-ttu-id="61c83-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="61c83-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="61c83-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61c83-115">Remarks</span></span>

<span data-ttu-id="61c83-116">Das Beispiel im Abschnitt Syntax zeigt die Umwandlung in wParam vor dem Senden der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="61c83-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="61c83-117">**LPARAM** wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="61c83-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c83-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61c83-118">Requirements</span></span>



| <span data-ttu-id="61c83-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61c83-119">Requirement</span></span> | <span data-ttu-id="61c83-120">Wert</span><span class="sxs-lookup"><span data-stu-id="61c83-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61c83-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61c83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61c83-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61c83-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61c83-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61c83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61c83-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61c83-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61c83-125">Header</span><span class="sxs-lookup"><span data-stu-id="61c83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="61c83-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="61c83-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





