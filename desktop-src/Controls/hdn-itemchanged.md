---
title: HDN_ITEMCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass sich die Attribute eines Header Elements geändert haben. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- Windows-Steuerelemente für HDN_ITEMCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040180"
---
# <a name="hdn_itemchanged-notification-code"></a><span data-ttu-id="08b57-105">Hdn \_ ItemChanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="08b57-105">HDN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="08b57-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass sich die Attribute eines Header Elements geändert haben.</span><span class="sxs-lookup"><span data-stu-id="08b57-106">Notifies a header control's parent window that the attributes of a header item have changed.</span></span> <span data-ttu-id="08b57-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="08b57-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="08b57-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08b57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b57-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08b57-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08b57-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement enthält, einschließlich der geänderten Attribute.</span><span class="sxs-lookup"><span data-stu-id="08b57-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control, including the attributes that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b57-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08b57-111">Return value</span></span>

<span data-ttu-id="08b57-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="08b57-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b57-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08b57-113">Requirements</span></span>



| <span data-ttu-id="08b57-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08b57-114">Requirement</span></span> | <span data-ttu-id="08b57-115">Wert</span><span class="sxs-lookup"><span data-stu-id="08b57-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08b57-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08b57-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08b57-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08b57-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08b57-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08b57-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08b57-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08b57-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08b57-120">Header</span><span class="sxs-lookup"><span data-stu-id="08b57-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08b57-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="08b57-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="08b57-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="08b57-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="08b57-123">**Hdn \_ Itemchangedw** (Unicode) und **Hdn \_ itemchangeda** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="08b57-123">**HDN\_ITEMCHANGEDW** (Unicode) and **HDN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



 

 





