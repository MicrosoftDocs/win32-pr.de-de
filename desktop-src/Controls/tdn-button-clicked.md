---
title: TDN_BUTTON_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehls Link im Aufgaben Dialogfeld auswählt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- Windows-Steuerelemente für TDN_BUTTON_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957182"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="e84d4-105">TDN-Schaltfläche, auf die \_ \_ geklickt wird</span><span class="sxs-lookup"><span data-stu-id="e84d4-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="e84d4-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehls Link im Aufgaben Dialogfeld auswählt.</span><span class="sxs-lookup"><span data-stu-id="e84d4-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="e84d4-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e84d4-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e84d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e84d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e84d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e84d4-110">Ein **int** -Wert, der die ID der ausgewählten Schaltfläche oder des Befehl-Links angibt.</span><span class="sxs-lookup"><span data-stu-id="e84d4-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="e84d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e84d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e84d4-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e84d4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84d4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e84d4-113">Return value</span></span>

<span data-ttu-id="e84d4-114">Um zu verhindern, dass das Aufgaben Dialogfeld geschlossen wird, muss die Anwendung **S \_ false** zurückgeben. andernfalls wird das Aufgaben Dialogfeld geschlossen, und die Schaltflächen-ID wird über den ursprünglichen Anwendungs Befehl zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="e84d4-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84d4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e84d4-115">Requirements</span></span>



| <span data-ttu-id="e84d4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e84d4-116">Requirement</span></span> | <span data-ttu-id="e84d4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e84d4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e84d4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e84d4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e84d4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e84d4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e84d4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e84d4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e84d4-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e84d4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e84d4-122">Header</span><span class="sxs-lookup"><span data-stu-id="e84d4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84d4-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e84d4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





