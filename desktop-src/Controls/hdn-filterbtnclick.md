---
title: HDN_FILTERBTNCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, wenn auf die Filter Schaltfläche geklickt wird, oder als Reaktion auf eine HDM- \_ Nachricht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- Windows-Steuerelemente für HDN_FILTERBTNCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858683"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="ba9d1-105">Hdn \_ filterbtnclick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ba9d1-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="ba9d1-106">Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, wenn auf die Filter Schaltfläche geklickt wird, oder als Reaktion auf eine [**HDM \_**](hdm-setitem.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="ba9d1-107">Dieser Benachrichtigungs Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ba9d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba9d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba9d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba9d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba9d1-110">Ein Zeiger auf eine [**nmhdfilterbtnclick**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) -Struktur, die Informationen über das Header Steuerelement und die Header Filter Schaltfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba9d1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba9d1-111">Return value</span></span>

<span data-ttu-id="ba9d1-112">Wenn Sie " **true**" zurückgeben, wird ein [Hdn- \_ FilterChange](hdn-filterchange.md) -Benachrichtigungs Code an das übergeordnete Fenster des Header Steuer Elements gesendet.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="ba9d1-113">Mit diesem Benachrichtigungs Code erhält das übergeordnete Fenster die Gelegenheit, seine Benutzeroberflächen Elemente zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="ba9d1-114">Gibt **false** zurück, wenn Sie nicht möchten, dass die Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba9d1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba9d1-115">Requirements</span></span>



| <span data-ttu-id="ba9d1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba9d1-116">Requirement</span></span> | <span data-ttu-id="ba9d1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ba9d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9d1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba9d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba9d1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba9d1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba9d1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba9d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba9d1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba9d1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba9d1-122">Header</span><span class="sxs-lookup"><span data-stu-id="ba9d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba9d1-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba9d1-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba9d1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba9d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba9d1-125">**Nmhdfilterbtnclick**</span><span class="sxs-lookup"><span data-stu-id="ba9d1-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





