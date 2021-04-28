---
title: NM_NCHITTEST(Rebar)-Benachrichtigungscode (Commctrl.h)
description: 'NM_NCHITTEST(Rebar)-Benachrichtigungscode: Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine \_ WM-NCHITTEST-Nachricht empfängt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST(Rebar)-Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112328"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="5a29f-105">\_NM-NCHITTEST-Benachrichtigungscode (Rebar)</span><span class="sxs-lookup"><span data-stu-id="5a29f-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="5a29f-106">Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht empfängt.**](/windows/desktop/inputdev/wm-nchittest)</span><span class="sxs-lookup"><span data-stu-id="5a29f-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="5a29f-107">Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="5a29f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5a29f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a29f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a29f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a29f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a29f-110">Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zum Benachrichtigungscode enthält.</span><span class="sxs-lookup"><span data-stu-id="5a29f-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="5a29f-111">Das **dwItemSpec-Element** enthält den Bandindex, über den die Treffertestmeldung aufgetreten ist, und das **pt-Element** enthält die Mauskoordinaten der Treffertestmeldung.</span><span class="sxs-lookup"><span data-stu-id="5a29f-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a29f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a29f-112">Return value</span></span>

<span data-ttu-id="5a29f-113">Geben Sie 0 (null) zurück, damit die Neuleiste die Standardverarbeitung der Treffertestmeldung durchführen kann, oder geben Sie einen der \* unter [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) dokumentierten HT-Werte zurück, um die Standardmäßige Verarbeitung von Treffertests zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5a29f-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a29f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a29f-114">Requirements</span></span>



| <span data-ttu-id="5a29f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a29f-115">Requirement</span></span> | <span data-ttu-id="5a29f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5a29f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a29f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a29f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a29f-118">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a29f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a29f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a29f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a29f-120">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a29f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a29f-121">Header</span><span class="sxs-lookup"><span data-stu-id="5a29f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a29f-122"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="5a29f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

