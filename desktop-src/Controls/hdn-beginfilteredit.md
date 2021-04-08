---
title: HDN_BEGINFILTEREDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass eine Filter Bearbeitung begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- Windows-Steuerelemente für HDN_BEGINFILTEREDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957270"
---
# <a name="hdn_beginfilteredit-notification-code"></a><span data-ttu-id="5f72e-105">Hdn \_ beginfilteredit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5f72e-105">HDN\_BEGINFILTEREDIT notification code</span></span>

<span data-ttu-id="5f72e-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass eine Filter Bearbeitung begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="5f72e-106">Notifies a header control's parent window that a filter edit has begun.</span></span> <span data-ttu-id="5f72e-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5f72e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5f72e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f72e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f72e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f72e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f72e-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die zusätzliche Informationen über den Filter enthält, der bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5f72e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f72e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f72e-111">Return value</span></span>

<span data-ttu-id="5f72e-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5f72e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f72e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f72e-113">Requirements</span></span>



| <span data-ttu-id="5f72e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f72e-114">Requirement</span></span> | <span data-ttu-id="5f72e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f72e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f72e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f72e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f72e-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f72e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f72e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f72e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f72e-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f72e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f72e-120">Header</span><span class="sxs-lookup"><span data-stu-id="5f72e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f72e-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f72e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





