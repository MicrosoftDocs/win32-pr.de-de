---
title: TBN_RESTORE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wieder hergestellt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- Windows-Steuerelemente für TBN_RESTORE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478084"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="d86fd-105">TBN- \_ Wiederherstellungs Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d86fd-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="d86fd-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d86fd-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="d86fd-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d86fd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d86fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d86fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d86fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d86fd-110">Zeiger auf eine [**nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d86fd-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d86fd-111">Return value</span></span>

<span data-ttu-id="d86fd-112">Die Anwendung sollte NULL als Antwort auf den ersten **TBN- \_ Wiederherstellungs** Benachrichtigungs Code zurückgeben, der zu Beginn des Wiederherstellungs Vorgangs empfangen wurde, damit die Schaltflächen Informationen weiterhin wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d86fd-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="d86fd-113">Wenn die Anwendung einen Wert ungleich 0 (null) zurückgibt, wird der Wiederherstellungs Vorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d86fd-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="d86fd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d86fd-114">Remarks</span></span>

<span data-ttu-id="d86fd-115">Die Anwendung empfängt diesen Benachrichtigungs Code einmal zu Beginn des Wiederherstellungs Vorgangs und einmal für jede Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d86fd-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="d86fd-116">Mit diesem Benachrichtigungs Code können Sie die Informationen aus dem Datenstrom extrahieren, den Sie zuvor gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="d86fd-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="d86fd-117">Wenn Sie keine Informationen gespeichert haben, ignorieren Sie den Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="d86fd-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="d86fd-118">Eine ausführlichere Erläuterung zur Handhabung der **TBN- \_ Wiederherstellung** finden Sie unter [Symbolleisten Anpassung](toolbar-controls-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="d86fd-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d86fd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d86fd-119">Requirements</span></span>



| <span data-ttu-id="d86fd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d86fd-120">Requirement</span></span> | <span data-ttu-id="d86fd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d86fd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d86fd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d86fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d86fd-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d86fd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d86fd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d86fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d86fd-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d86fd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d86fd-126">Header</span><span class="sxs-lookup"><span data-stu-id="d86fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d86fd-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86fd-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





