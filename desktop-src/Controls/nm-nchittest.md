---
title: NM_NCHITTEST Benachrichtigungscode (Commctrl.h)
description: 'NM_NCHITTEST Benachrichtigungscode: Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine WM \_ NCHITTEST-Nachricht empfängt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112318"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="4501e-105">NM \_ NCHITTEST-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="4501e-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="4501e-106">Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht**](/windows/desktop/inputdev/wm-nchittest) empfängt.</span><span class="sxs-lookup"><span data-stu-id="4501e-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="4501e-107">Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="4501e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4501e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4501e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4501e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4501e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4501e-110">Ein Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zum Benachrichtigungscode enthält.</span><span class="sxs-lookup"><span data-stu-id="4501e-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="4501e-111">Das *pt-Member* enthält die Mauskoordinaten der Treffertestnachricht.</span><span class="sxs-lookup"><span data-stu-id="4501e-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4501e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4501e-112">Return value</span></span>

<span data-ttu-id="4501e-113">Geben Sie , sofern nicht anders angegeben, 0 (null) zurück, damit das Steuerelement die Standardverarbeitung der Treffertestnachricht ausführen kann, oder geben Sie einen der unter \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) dokumentierten HT-Werte zurück, um die Standardmäßige Treffertestverarbeitung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4501e-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4501e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4501e-114">Requirements</span></span>



| <span data-ttu-id="4501e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4501e-115">Requirement</span></span> | <span data-ttu-id="4501e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4501e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4501e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4501e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4501e-118">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4501e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4501e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4501e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4501e-120">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4501e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4501e-121">Header</span><span class="sxs-lookup"><span data-stu-id="4501e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4501e-122"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="4501e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

