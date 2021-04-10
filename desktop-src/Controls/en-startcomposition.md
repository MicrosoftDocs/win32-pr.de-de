---
title: EN_STARTCOMPOSITION Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer mit der Eingabe mit dem IME-oder Text Dienst Framework begonnen
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- Windows-Steuerelemente für EN_STARTCOMPOSITION Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105555"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="3d356-104">EN \_ StartComposition-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="3d356-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="3d356-105">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer mit der Eingabe mit dem IME-oder [Text Dienst Framework](/windows/desktop/TSF/text-services-framework)begonnen</span><span class="sxs-lookup"><span data-stu-id="3d356-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3d356-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d356-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d356-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d356-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d356-108">Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d356-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d356-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d356-109">Requirements</span></span>



| <span data-ttu-id="3d356-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d356-110">Requirement</span></span> | <span data-ttu-id="3d356-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3d356-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d356-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d356-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3d356-113">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d356-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3d356-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d356-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3d356-115">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d356-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d356-116">Header</span><span class="sxs-lookup"><span data-stu-id="3d356-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d356-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d356-117"><dt>Richedit.h</dt></span></span> </dl> |



 

