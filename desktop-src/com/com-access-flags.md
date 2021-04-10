---
title: Zugriffsflags ("AccCtrl. h")
description: Diese Werte geben an, ob ein Eintrag in der Zugriffsliste Rechte beschreibt, die zugelassen oder verweigert werden.
ms.assetid: 460d2c72-3315-4b4c-928e-4bb0640acbe5
topic_type:
- apiref
api_name:
- ACTRL_ACCESS_ALLOWED
- ACTRL_ACCESS_DENIED
api_location:
- AccCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5972bf95efc675d6dd9c2e58c0b7d25c8c305371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106322"
---
# <a name="access-flags"></a><span data-ttu-id="8cf94-103">Zugriffsflags</span><span class="sxs-lookup"><span data-stu-id="8cf94-103">Access Flags</span></span>

<span data-ttu-id="8cf94-104">Diese Werte geben an, ob ein Eintrag in der Zugriffsliste Rechte beschreibt, die zugelassen oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="8cf94-104">These values indicate whether an entry in the access list describes rights that are allowed or denied.</span></span>



| <span data-ttu-id="8cf94-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="8cf94-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="8cf94-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cf94-106">Description</span></span>                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="ACTRL_ACCESS_ALLOWED"></span><span id="actrl_access_allowed"></span><dl> <span data-ttu-id="8cf94-107"><dt>**Actrl \_ Zugriff \_ zulässig**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="8cf94-107"><dt>**ACTRL\_ACCESS\_ALLOWED**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="8cf94-108">Gibt einen Zugriffs zulässigen Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="8cf94-108">Indicates an access-allowed entry.</span></span><br/> |
| <span id="ACTRL_ACCESS_DENIED"></span><span id="actrl_access_denied"></span><dl> <span data-ttu-id="8cf94-109"><dt>**Actrl \_ Zugriff \_ verweigert**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="8cf94-109"><dt>**ACTRL\_ACCESS\_DENIED**</dt> <dt>0x10000000</dt></span></span> </dl>    | <span data-ttu-id="8cf94-110">Gibt den Eintrag "Zugriff verweigert" an.</span><span class="sxs-lookup"><span data-stu-id="8cf94-110">Indicates an access-denied entry.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="8cf94-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cf94-111">Requirements</span></span>



| <span data-ttu-id="8cf94-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cf94-112">Requirement</span></span> | <span data-ttu-id="8cf94-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf94-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf94-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cf94-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf94-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf94-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8cf94-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cf94-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf94-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf94-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8cf94-118">Header</span><span class="sxs-lookup"><span data-stu-id="8cf94-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf94-119"><dt>"AccCtrl. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8cf94-119"><dt>AccCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf94-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cf94-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf94-121">**actrl- \_ Zugriffs \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="8cf94-121">**ACTRL\_ACCESS\_ENTRY**</span></span>](/windows/desktop/api/AccCtrl/ns-accctrl-actrl_access_entrya)
</dt> </dl>

 

 





