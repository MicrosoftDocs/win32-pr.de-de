---
title: HDN_FILTERCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, dass die Attribute eines Header Steuerelement Filters geändert oder bearbeitet werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- Windows-Steuerelemente für HDN_FILTERCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475378"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="43391-105">Hdn- \_ FilterChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="43391-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="43391-106">Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, dass die Attribute eines Header Steuerelement Filters geändert oder bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="43391-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="43391-107">Dieser Benachrichtigungs Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="43391-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="43391-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43391-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43391-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43391-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43391-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Header Element enthält, einschließlich der Attribute, die gerade geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43391-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43391-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43391-111">Return value</span></span>

<span data-ttu-id="43391-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="43391-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="43391-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43391-113">Requirements</span></span>



| <span data-ttu-id="43391-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43391-114">Requirement</span></span> | <span data-ttu-id="43391-115">Wert</span><span class="sxs-lookup"><span data-stu-id="43391-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43391-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43391-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43391-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43391-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43391-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43391-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43391-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43391-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43391-120">Header</span><span class="sxs-lookup"><span data-stu-id="43391-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43391-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="43391-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43391-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43391-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43391-123">**HDM \_ setfilterchangetimeout**</span><span class="sxs-lookup"><span data-stu-id="43391-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





