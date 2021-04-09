---
title: MCN_GETDAYSTATE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, um Informationen über die Anzeige einzelner Tage anzufordern. Dieser Benachrichtigungs Code wird nur nach Monatskalender-Steuerelementen gesendet, die den MCS \_ daystate-Stil verwenden, und er wird in Form einer WM- \_ Benachrichtigungs Meldung gesendet.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- Windows-Steuerelemente für MCN_GETDAYSTATE Benachrichtigungs
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741689"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="e4936-105">MCN \_ getdaystate-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e4936-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="e4936-106">Wird von einem Monatskalender-Steuerelement gesendet, um Informationen über die Anzeige einzelner Tage anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e4936-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="e4936-107">Dieser Benachrichtigungs Code wird nur nach Monatskalender-Steuerelementen gesendet, die den [**MCS \_ daystate**](month-calendar-control-styles.md) -Stil verwenden, und er wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="e4936-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e4936-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4936-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4936-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4936-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4936-110">Zeiger auf eine [**nmdaystate**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e4936-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="e4936-111">Die Struktur enthält Informationen über den Zeitraum, für den das Steuerelement Informationen benötigt, und empfängt die Adresse eines Arrays, das diese Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e4936-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4936-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4936-112">Return value</span></span>

<span data-ttu-id="e4936-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e4936-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4936-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4936-114">Remarks</span></span>

<span data-ttu-id="e4936-115">Durch die Behandlung dieses Benachrichtigungs Codes kann Ihre Anwendung Ihre Anzeige anpassen, indem Sie angeben, dass bestimmte Tage fett angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e4936-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4936-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4936-116">Requirements</span></span>



| <span data-ttu-id="e4936-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4936-117">Requirement</span></span> | <span data-ttu-id="e4936-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e4936-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4936-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4936-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4936-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4936-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4936-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4936-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4936-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4936-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4936-123">Header</span><span class="sxs-lookup"><span data-stu-id="e4936-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4936-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4936-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





