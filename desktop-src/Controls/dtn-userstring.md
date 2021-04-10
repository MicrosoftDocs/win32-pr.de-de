---
title: DTN_USERSTRING Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn ein Benutzer das Bearbeiten einer Zeichenfolge im-Steuerelement beendet.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- Windows-Steuerelemente für DTN_USERSTRING Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858712"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="fea77-104">DTN \_ UserString-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="fea77-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="fea77-105">Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn ein Benutzer das Bearbeiten einer Zeichenfolge im-Steuerelement beendet.</span><span class="sxs-lookup"><span data-stu-id="fea77-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="fea77-106">Dieser Benachrichtigungs Code wird nur von DTP-Steuerelementen gesendet, die auf den [**DTS \_ appcananalyse**](date-and-time-picker-control-styles.md) -Stil festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="fea77-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="fea77-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="fea77-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fea77-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fea77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fea77-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea77-110">Ein Zeiger auf eine [**nmdatetimestring**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) -Struktur, die Informationen über die Instanz des Benachrichtigungs Codes enthält.</span><span class="sxs-lookup"><span data-stu-id="fea77-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea77-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fea77-111">Return value</span></span>

<span data-ttu-id="fea77-112">Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fea77-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fea77-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fea77-113">Remarks</span></span>

<span data-ttu-id="fea77-114">Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer benutzerdefinierte Antworten auf Zeichen folgen bereitstellen, die vom Benutzer in das Steuerelement eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fea77-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="fea77-115">Der Besitzer muss darauf vorbereitet sein, die Eingabe Zeichenfolge zu analysieren und ggf. Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fea77-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea77-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fea77-116">Requirements</span></span>



| <span data-ttu-id="fea77-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fea77-117">Requirement</span></span> | <span data-ttu-id="fea77-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fea77-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fea77-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fea77-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fea77-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea77-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fea77-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fea77-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fea77-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fea77-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fea77-123">Header</span><span class="sxs-lookup"><span data-stu-id="fea77-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea77-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea77-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fea77-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fea77-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fea77-126">**Dtn \_ Userstringw** (Unicode) und **Dtn \_ userstrauch** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fea77-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 





