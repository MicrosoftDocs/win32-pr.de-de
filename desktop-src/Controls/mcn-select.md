---
title: MCN_SELECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn der Benutzer eine explizite Datumsauswahl innerhalb eines Monatskalender-Steuer Elements vornimmt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- Windows-Steuerelemente für MCN_SELECT Benachrichtigungs
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040239"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="1d232-105">MCN- \_ Benachrichtigungs Code auswählen</span><span class="sxs-lookup"><span data-stu-id="1d232-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="1d232-106">Wird von einem Monatskalender-Steuerelement gesendet, wenn der Benutzer eine explizite Datumsauswahl innerhalb eines Monatskalender-Steuer Elements vornimmt.</span><span class="sxs-lookup"><span data-stu-id="1d232-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="1d232-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="1d232-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1d232-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d232-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d232-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d232-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d232-110">Ein Zeiger auf eine [**nmselchange**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) -Struktur, die Informationen über den aktuell ausgewählten Datumsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="1d232-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d232-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d232-111">Return value</span></span>

<span data-ttu-id="1d232-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1d232-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d232-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d232-113">Remarks</span></span>

<span data-ttu-id="1d232-114">Der **MCN- \_ Select** -Benachrichtigungs Code ähnelt [**MCN \_ selChange**](mcn-selchange.md), aber **MCN \_ Select** wird nur als Antwort auf die explizite Datumsauswahl eines Benutzers gesendet.</span><span class="sxs-lookup"><span data-stu-id="1d232-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="1d232-115">**MCN \_ SelChange** gilt für beliebige Auswahl Änderungen.</span><span class="sxs-lookup"><span data-stu-id="1d232-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d232-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d232-116">Requirements</span></span>



| <span data-ttu-id="1d232-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d232-117">Requirement</span></span> | <span data-ttu-id="1d232-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1d232-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d232-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d232-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d232-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d232-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d232-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d232-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d232-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d232-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d232-123">Header</span><span class="sxs-lookup"><span data-stu-id="1d232-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d232-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d232-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





