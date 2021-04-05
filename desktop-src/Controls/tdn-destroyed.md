---
title: TDN_DESTROYED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn es zerstört wird und sein Fenster Handle nicht mehr gültig ist. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- Windows-Steuerelemente für TDN_DESTROYED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859275"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="e2fdf-105">Von TDN \_ zerstörter Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e2fdf-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="e2fdf-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn es zerstört wird und sein Fenster Handle nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e2fdf-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="e2fdf-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2fdf-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e2fdf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fdf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2fdf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fdf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e2fdf-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2fdf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2fdf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fdf-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e2fdf-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fdf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2fdf-113">Return value</span></span>

<span data-ttu-id="e2fdf-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e2fdf-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fdf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2fdf-115">Requirements</span></span>



| <span data-ttu-id="e2fdf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2fdf-116">Requirement</span></span> | <span data-ttu-id="e2fdf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e2fdf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fdf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2fdf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2fdf-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2fdf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2fdf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2fdf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2fdf-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2fdf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2fdf-122">Header</span><span class="sxs-lookup"><span data-stu-id="e2fdf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2fdf-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2fdf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





