---
title: HDN_ITEMKEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass eine Taste mit einem ausgewählten Element gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- Windows-Steuerelemente für HDN_ITEMKEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040993"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="d898f-105">Hdn \_ itemkeydown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d898f-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="d898f-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass eine Taste mit einem ausgewählten Element gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="d898f-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="d898f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d898f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d898f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d898f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d898f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d898f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d898f-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die zusätzliche Informationen über den gedrückten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="d898f-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d898f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d898f-111">Return value</span></span>

<span data-ttu-id="d898f-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d898f-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d898f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d898f-113">Requirements</span></span>



| <span data-ttu-id="d898f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d898f-114">Requirement</span></span> | <span data-ttu-id="d898f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d898f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d898f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d898f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d898f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d898f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d898f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d898f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d898f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d898f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d898f-120">Header</span><span class="sxs-lookup"><span data-stu-id="d898f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d898f-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d898f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





