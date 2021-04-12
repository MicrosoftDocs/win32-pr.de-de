---
title: TDN_NAVIGATED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn eine Navigation aufgetreten ist. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- Windows-Steuerelemente für TDN_NAVIGATED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519049"
---
# <a name="tdn_navigated-notification-code"></a><span data-ttu-id="bdc0d-105">TDN- \_ Navigations Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bdc0d-105">TDN\_NAVIGATED notification code</span></span>

<span data-ttu-id="bdc0d-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn eine Navigation aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-106">Sent by a task dialog when navigation has occurred.</span></span> <span data-ttu-id="bdc0d-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="bdc0d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc0d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdc0d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc0d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bdc0d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdc0d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc0d-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc0d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdc0d-113">Return value</span></span>

<span data-ttu-id="bdc0d-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bdc0d-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc0d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdc0d-115">Requirements</span></span>



| <span data-ttu-id="bdc0d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdc0d-116">Requirement</span></span> | <span data-ttu-id="bdc0d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bdc0d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc0d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdc0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc0d-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc0d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdc0d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdc0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc0d-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc0d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdc0d-122">Header</span><span class="sxs-lookup"><span data-stu-id="bdc0d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc0d-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc0d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





