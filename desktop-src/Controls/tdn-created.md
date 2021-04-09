---
title: TDN_CREATED Benachrichtigungs Code (kommctrl. h)
description: Wird vom Aufgaben Dialogfeld gesendet, nachdem das Dialogfeld erstellt und vor dem anzeigen angezeigt wurde. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- Windows-Steuerelemente für TDN_CREATED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957183"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="abbe4-105">Von TDN \_ erstellter Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="abbe4-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="abbe4-106">Wird vom Aufgaben Dialogfeld gesendet, nachdem das Dialogfeld erstellt und vor dem anzeigen angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="abbe4-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="abbe4-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="abbe4-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="abbe4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="abbe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abbe4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abbe4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abbe4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="abbe4-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="abbe4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abbe4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abbe4-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="abbe4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abbe4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abbe4-113">Return value</span></span>

<span data-ttu-id="abbe4-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="abbe4-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="abbe4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abbe4-115">Requirements</span></span>



| <span data-ttu-id="abbe4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abbe4-116">Requirement</span></span> | <span data-ttu-id="abbe4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="abbe4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abbe4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abbe4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="abbe4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abbe4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="abbe4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abbe4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="abbe4-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abbe4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abbe4-122">Header</span><span class="sxs-lookup"><span data-stu-id="abbe4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="abbe4-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="abbe4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





