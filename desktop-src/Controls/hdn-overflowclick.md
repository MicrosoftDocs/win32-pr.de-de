---
title: HDN_OVERFLOWCLICK Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf die Überlauf Schaltfläche des Headers geklickt wird Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- Windows-Steuerelemente für HDN_OVERFLOWCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858943"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="68b45-105">\_Benachrichtigungs Code für den über Fluss von Hdn</span><span class="sxs-lookup"><span data-stu-id="68b45-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="68b45-106">Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf die Überlauf Schaltfläche des Headers geklickt wird</span><span class="sxs-lookup"><span data-stu-id="68b45-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="68b45-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="68b45-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="68b45-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68b45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b45-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68b45-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b45-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die den Benachrichtigungs Code beschreibt.</span><span class="sxs-lookup"><span data-stu-id="68b45-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="68b45-111">Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen, einschließlich der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="68b45-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="68b45-112">Legen Sie die Member der **NMHDR** -Struktur fest, einschließlich des *Code* Members, der auf den Hdn-overflowclick festgelegt werden muss \_ .</span><span class="sxs-lookup"><span data-stu-id="68b45-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="68b45-113">Legen Sie den **iItem** -Member der [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur auf den Index des ersten Header Elements fest, das nicht sichtbar ist und daher bei einem Überlauf angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="68b45-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b45-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68b45-114">Return value</span></span>

<span data-ttu-id="68b45-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="68b45-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b45-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68b45-116">Remarks</span></span>

<span data-ttu-id="68b45-117">Der Benachrichtigungs Empfänger wandelt **LPARAM** ein, um die [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="68b45-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="68b45-118">**WParam** enthält die ID des Steuer Elements, das die Benachrichtigung sendet.</span><span class="sxs-lookup"><span data-stu-id="68b45-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="68b45-119">Diese Meldung wird nur gesendet, wenn für das Header Steuerelement Style [**HDS \_ Overflow**](header-control-styles.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68b45-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b45-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68b45-120">Requirements</span></span>



| <span data-ttu-id="68b45-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68b45-121">Requirement</span></span> | <span data-ttu-id="68b45-122">Wert</span><span class="sxs-lookup"><span data-stu-id="68b45-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68b45-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68b45-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68b45-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68b45-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68b45-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68b45-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68b45-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68b45-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68b45-127">Header</span><span class="sxs-lookup"><span data-stu-id="68b45-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b45-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b45-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





