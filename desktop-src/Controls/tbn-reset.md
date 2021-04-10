---
title: TBN_RESET Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer den Inhalt des Dialog Felds Symbolleiste anpassen zurückgesetzt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- Windows-Steuerelemente für TBN_RESET Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040949"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="101d6-105">TBN-Zurücksetzungs \_ Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="101d6-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="101d6-106">Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer den Inhalt des Dialog Felds Symbolleiste anpassen zurückgesetzt hat.</span><span class="sxs-lookup"><span data-stu-id="101d6-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="101d6-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="101d6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="101d6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="101d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101d6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="101d6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="101d6-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="101d6-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101d6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="101d6-111">Return value</span></span>

<span data-ttu-id="101d6-112">Gibt tbnrf \_ endcustomize zurück, um das Dialogfeld Symbolleiste anpassen zu schließen.</span><span class="sxs-lookup"><span data-stu-id="101d6-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="101d6-113">Alle anderen Rückgabewerte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="101d6-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="101d6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="101d6-114">Requirements</span></span>



| <span data-ttu-id="101d6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="101d6-115">Requirement</span></span> | <span data-ttu-id="101d6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="101d6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="101d6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="101d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="101d6-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="101d6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="101d6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="101d6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="101d6-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="101d6-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="101d6-121">Header</span><span class="sxs-lookup"><span data-stu-id="101d6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="101d6-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="101d6-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





