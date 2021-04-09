---
title: TDN_DIALOG_CONSTRUCTED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, nachdem das Dialogfeld erstellt und vor dem anzeigen angezeigt wurde. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- Windows-Steuerelemente für TDN_DIALOG_CONSTRUCTED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d3360a8cee3542037ea927363de8cab69977e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957181"
---
# <a name="tdn_dialog_constructed-notification-code"></a><span data-ttu-id="75af6-105">Der TDN- \_ Dialog \_ erstellte Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="75af6-105">TDN\_DIALOG\_CONSTRUCTED notification code</span></span>

<span data-ttu-id="75af6-106">Wird von einem Aufgaben Dialogfeld gesendet, nachdem das Dialogfeld erstellt und vor dem anzeigen angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="75af6-106">Sent by a task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="75af6-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="75af6-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DIALOG_CONSTRUCTED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="75af6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="75af6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75af6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75af6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75af6-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="75af6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75af6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75af6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75af6-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="75af6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75af6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75af6-113">Return value</span></span>

<span data-ttu-id="75af6-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="75af6-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="75af6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75af6-115">Requirements</span></span>



| <span data-ttu-id="75af6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75af6-116">Requirement</span></span> | <span data-ttu-id="75af6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="75af6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75af6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75af6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75af6-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75af6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75af6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75af6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75af6-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75af6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75af6-122">Header</span><span class="sxs-lookup"><span data-stu-id="75af6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75af6-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="75af6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





