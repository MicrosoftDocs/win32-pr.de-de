---
title: TDN_TIMER Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld ungefähr alle 200 Millisekunden gesendet.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- Windows-Steuerelemente für TDN_TIMER Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344106"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="b782e-104">TDN-Zeit Geber \_ Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b782e-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="b782e-105">Wird von einem Aufgaben Dialogfeld ungefähr alle 200 Millisekunden gesendet.</span><span class="sxs-lookup"><span data-stu-id="b782e-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="b782e-106">Dieser Benachrichtigungs Code wird gesendet, wenn das TDF- \_ Rückruf- \_ Timer-Flag im **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur festgelegt wurde, die an die [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b782e-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="b782e-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der **TaskDialogIndirect** -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b782e-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b782e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b782e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b782e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b782e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b782e-110">Ein **DWORD** , das die Anzahl der Millisekunden seit der Erstellung des Dialog Felds angibt, oder dieser Benachrichtigungs Code hat den Wert " **\_ false**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b782e-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b782e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b782e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b782e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b782e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b782e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b782e-113">Return value</span></span>

<span data-ttu-id="b782e-114">Zum Zurücksetzen der TickCount-Anwendung muss die Anwendung den Wert " **\_ false**" zurückgeben, andernfalls wird der Wert für "TickCount" weiter erhöht.</span><span class="sxs-lookup"><span data-stu-id="b782e-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="b782e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b782e-115">Requirements</span></span>



| <span data-ttu-id="b782e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b782e-116">Requirement</span></span> | <span data-ttu-id="b782e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b782e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b782e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b782e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b782e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b782e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b782e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b782e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b782e-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b782e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b782e-122">Header</span><span class="sxs-lookup"><span data-stu-id="b782e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b782e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b782e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





