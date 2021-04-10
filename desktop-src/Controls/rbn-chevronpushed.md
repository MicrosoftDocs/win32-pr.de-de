---
title: RBN_CHEVRONPUSHED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Chevron gepusht wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- Windows-Steuerelemente für RBN_CHEVRONPUSHED Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040588"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="b2b34-105">RBN \_ chevronpushbenachrichtigungen-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b2b34-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="b2b34-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Chevron gepusht wird.</span><span class="sxs-lookup"><span data-stu-id="b2b34-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="b2b34-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b2b34-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b2b34-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2b34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2b34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2b34-110">Zeiger auf die [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur des Bands.</span><span class="sxs-lookup"><span data-stu-id="b2b34-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b34-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2b34-111">Return value</span></span>

<span data-ttu-id="b2b34-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2b34-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b34-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2b34-113">Remarks</span></span>

<span data-ttu-id="b2b34-114">Wenn eine Anwendung diesen Benachrichtigungs Code empfängt, ist Sie für die Anzeige eines Popup Menüs mit Elementen für jedes ausgeblendete Tool verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b2b34-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="b2b34-115">Verwenden Sie das **RC** -Element der [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur, um die richtige Position für das Popup Menü zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b2b34-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b34-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2b34-116">Requirements</span></span>



| <span data-ttu-id="b2b34-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2b34-117">Requirement</span></span> | <span data-ttu-id="b2b34-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b2b34-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b34-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2b34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b34-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2b34-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2b34-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2b34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b34-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2b34-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2b34-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2b34-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2b34-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b34-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





