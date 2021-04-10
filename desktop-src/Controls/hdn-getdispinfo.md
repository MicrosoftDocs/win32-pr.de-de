---
title: HDN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird an den Besitzer eines Header Steuer Elements gesendet, wenn das Steuerelement Informationen zu einem Rückruf Header Element benötigt. Dieser Benachrichtigungs Code wird als WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- Windows-Steuerelemente für HDN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040181"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="ab32a-105">Hdn \_ getdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ab32a-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="ab32a-106">Wird an den Besitzer eines Header Steuer Elements gesendet, wenn das Steuerelement Informationen zu einem Rückruf Header Element benötigt.</span><span class="sxs-lookup"><span data-stu-id="ab32a-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="ab32a-107">Dieser Benachrichtigungs Code wird als [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ab32a-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ab32a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab32a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab32a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab32a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab32a-110">Ein Zeiger auf eine [**nmhddispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ab32a-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="ab32a-111">Bei der Eingabe geben die Felder der Struktur an, welche Informationen erforderlich sind und welches Element von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="ab32a-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab32a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab32a-112">Return value</span></span>

<span data-ttu-id="ab32a-113">Gibt ein LRESULT zurück.</span><span class="sxs-lookup"><span data-stu-id="ab32a-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab32a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab32a-114">Remarks</span></span>

<span data-ttu-id="ab32a-115">Füllen Sie die entsprechenden Member der-Struktur aus, um die angeforderten Informationen an das Header Steuerelement zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ab32a-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="ab32a-116">Wenn Ihr Nachrichten Handler das **Masken** Element der [**nmhddispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) -Struktur auf HDI \_ di \_ SetItem festlegt, speichert das Header Steuerelement die Informationen und fordert Sie nicht erneut an.</span><span class="sxs-lookup"><span data-stu-id="ab32a-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab32a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab32a-117">Requirements</span></span>



| <span data-ttu-id="ab32a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab32a-118">Requirement</span></span> | <span data-ttu-id="ab32a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ab32a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab32a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab32a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab32a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab32a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab32a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab32a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab32a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab32a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab32a-124">Header</span><span class="sxs-lookup"><span data-stu-id="ab32a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab32a-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab32a-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ab32a-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ab32a-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ab32a-127">**Hdn \_ Getdispinfow** (Unicode) und **Hdn \_ getdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ab32a-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





