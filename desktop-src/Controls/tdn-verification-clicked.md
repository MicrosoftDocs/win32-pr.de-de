---
title: TDN_VERIFICATION_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf das Kontrollkästchen Aufgaben Dialogfeld Überprüfung klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- Windows-Steuerelemente für TDN_VERIFICATION_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957177"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="f5884-105">TDN- \_ Verifizierungs- \_ Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f5884-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="f5884-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf das Kontrollkästchen Aufgaben Dialogfeld Überprüfung klickt.</span><span class="sxs-lookup"><span data-stu-id="f5884-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="f5884-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f5884-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f5884-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5884-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5884-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5884-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5884-110">Ein **boolescher** Wert, der den Status des Kontrollkästchens angibt.</span><span class="sxs-lookup"><span data-stu-id="f5884-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="f5884-111">Es ist **true** , wenn das Kontrollkästchen Überprüfung aktiviert ist, oder **false** , wenn es nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5884-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="f5884-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5884-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5884-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f5884-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5884-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5884-114">Return value</span></span>

<span data-ttu-id="f5884-115">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f5884-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5884-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5884-116">Requirements</span></span>



| <span data-ttu-id="f5884-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5884-117">Requirement</span></span> | <span data-ttu-id="f5884-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f5884-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5884-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5884-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5884-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5884-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5884-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5884-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5884-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5884-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5884-123">Header</span><span class="sxs-lookup"><span data-stu-id="f5884-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5884-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5884-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5884-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5884-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5884-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f5884-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5884-127">*Taskdialogcallbackproc*</span><span class="sxs-lookup"><span data-stu-id="f5884-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

