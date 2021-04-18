---
description: Signalisiert, dass sich der verfügbare Satz von IDvdControl2-Schnittstellen Methoden geändert hat.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366005"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="429a6-103">\_ \_ gültige \_ UOPs- \_ Änderung für EC-DVD</span><span class="sxs-lookup"><span data-stu-id="429a6-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="429a6-104">Signalisiert, dass sich der verfügbare Satz von [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstellen Methoden geändert hat.</span><span class="sxs-lookup"><span data-stu-id="429a6-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="429a6-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="429a6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="429a6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="429a6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="429a6-107">**DWORD** -Wert, der eine Kombination aus null oder mehr Flags aus der [**gültigen \_ UOP- \_ Flag**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) -Enumeration enthält.</span><span class="sxs-lookup"><span data-stu-id="429a6-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="429a6-108">Die Bits geben an, welche [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Befehle von der DVD-CD explizit deaktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="429a6-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="429a6-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="429a6-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="429a6-110">Keinen.</span><span class="sxs-lookup"><span data-stu-id="429a6-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="429a6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="429a6-111">Remarks</span></span>

<span data-ttu-id="429a6-112">Dieses Ereignis gibt nur an, welche Vorgänge durch den Inhalt auf der DVD-CD explizit deaktiviert werden. Es ist nicht sichergestellt, dass es zulässig ist, nicht deaktivierte Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="429a6-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="429a6-113">Wenn z. b. keine Schaltflächen vorhanden sind, funktioniert die [**IDvdControl2:: activatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) -Methode nicht, obwohl die Methode nicht explizit deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="429a6-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="429a6-114">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="429a6-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="429a6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="429a6-115">Requirements</span></span>



| <span data-ttu-id="429a6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="429a6-116">Requirement</span></span> | <span data-ttu-id="429a6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="429a6-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="429a6-118">Header</span><span class="sxs-lookup"><span data-stu-id="429a6-118">Header</span></span><br/> | <dl> <span data-ttu-id="429a6-119"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="429a6-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="429a6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="429a6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429a6-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="429a6-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="429a6-122">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="429a6-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="429a6-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="429a6-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




