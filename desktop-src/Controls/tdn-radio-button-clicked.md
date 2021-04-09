---
title: TDN_RADIO_BUTTON_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer einen Optionsfeld-oder Befehls Link im Aufgaben Dialogfeld auswählt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- Windows-Steuerelemente für TDN_RADIO_BUTTON_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c8b16f738e4807c94a060b41b3932d0f3e07ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957178"
---
# <a name="tdn_radio_button_clicked-notification-code"></a><span data-ttu-id="750ad-105">TDN-Optionsfeld, auf das Sie \_ \_ \_ geklickt haben</span><span class="sxs-lookup"><span data-stu-id="750ad-105">TDN\_RADIO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="750ad-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer einen Optionsfeld-oder Befehls Link im Aufgaben Dialogfeld auswählt.</span><span class="sxs-lookup"><span data-stu-id="750ad-106">Sent by a task dialog when the user selects a radio button or command link in the task dialog.</span></span> <span data-ttu-id="750ad-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="750ad-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="750ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="750ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="750ad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="750ad-110">Ein **int** -Wert, der die ID angibt, die dem Optionsfeld entspricht, auf das geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="750ad-110">An **int** that specifies the ID corresponding to the radio button that was clicked.</span></span>

</dd> <dt>

<span data-ttu-id="750ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="750ad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="750ad-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="750ad-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750ad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="750ad-113">Return value</span></span>

<span data-ttu-id="750ad-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="750ad-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="750ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="750ad-115">Requirements</span></span>



| <span data-ttu-id="750ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="750ad-116">Requirement</span></span> | <span data-ttu-id="750ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="750ad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="750ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="750ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="750ad-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="750ad-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="750ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="750ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="750ad-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="750ad-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="750ad-122">Header</span><span class="sxs-lookup"><span data-stu-id="750ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="750ad-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="750ad-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





