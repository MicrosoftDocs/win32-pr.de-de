---
title: TBN_SAVE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- Windows-Steuerelemente für TBN_SAVE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743801"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="a0edc-105">TBN- \_ Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a0edc-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="a0edc-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0edc-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="a0edc-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a0edc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a0edc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0edc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0edc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0edc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0edc-110">Zeiger auf eine [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a0edc-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0edc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0edc-111">Return value</span></span>

<span data-ttu-id="a0edc-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a0edc-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0edc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0edc-113">Remarks</span></span>

<span data-ttu-id="a0edc-114">Die Anwendung empfängt diesen Benachrichtigungs Code einmal zu Beginn des Speicher Vorgangs und einmal für jede Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a0edc-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="a0edc-115">Dieser Benachrichtigungs Code bietet Ihnen die Möglichkeit, eigene Informationen hinzuzufügen, die von der Shell gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="a0edc-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="a0edc-116">Wenn Sie keine Informationen hinzufügen möchten, ignorieren Sie den Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="a0edc-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="a0edc-117">Eine ausführlichere Erläuterung der Handhabung von TBN finden Sie unter Anpassen der [Symbolleiste](toolbar-controls-overview.md) \_ .</span><span class="sxs-lookup"><span data-stu-id="a0edc-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0edc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0edc-118">Requirements</span></span>



| <span data-ttu-id="a0edc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0edc-119">Requirement</span></span> | <span data-ttu-id="a0edc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a0edc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0edc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0edc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0edc-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0edc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0edc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0edc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0edc-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0edc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0edc-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0edc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0edc-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0edc-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0edc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0edc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0edc-128">TBN- \_ Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="a0edc-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





