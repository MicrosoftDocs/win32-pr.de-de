---
title: CBEN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, um Anzeigeinformationen zu einem Rückruf Element abzurufen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- Windows-Steuerelemente für CBEN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517384"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="762ba-105">Cben \_ getdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="762ba-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="762ba-106">Wird gesendet, um Anzeigeinformationen zu einem Rückruf Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="762ba-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="762ba-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="762ba-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="762ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="762ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="762ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="762ba-110">Ein Zeiger auf eine [**nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="762ba-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762ba-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="762ba-111">Return value</span></span>

<span data-ttu-id="762ba-112">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="762ba-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="762ba-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="762ba-113">Remarks</span></span>

<span data-ttu-id="762ba-114">Die [**nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) -Struktur enthält eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="762ba-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="762ba-115">Der **Mask** -Member gibt die Informationen an, die vom Steuerelement angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="762ba-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="762ba-116">Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das Steuerelement zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="762ba-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="762ba-117">Wenn Ihr Nachrichten Handler das **Masken** Element der [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur auf cbeif \_ di \_ SetItem festlegt, speichert das Steuerelement die Informationen und fordert Sie nicht erneut an.</span><span class="sxs-lookup"><span data-stu-id="762ba-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="762ba-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="762ba-118">Requirements</span></span>



| <span data-ttu-id="762ba-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="762ba-119">Requirement</span></span> | <span data-ttu-id="762ba-120">Wert</span><span class="sxs-lookup"><span data-stu-id="762ba-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="762ba-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="762ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="762ba-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="762ba-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="762ba-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="762ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="762ba-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="762ba-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="762ba-125">Header</span><span class="sxs-lookup"><span data-stu-id="762ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="762ba-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="762ba-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="762ba-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="762ba-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="762ba-128">**Cben \_ Getdispinfow** (Unicode) und **cben \_ getdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="762ba-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





