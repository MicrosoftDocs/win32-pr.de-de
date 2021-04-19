---
description: Signalisiert, dass sich die Anzahl der DVD-Menü Schaltflächen geändert hat oder dass sich die Schaltflächen Auswahl geändert hat.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370259"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="f2e72-103">EC- \_ DVD- \_ Schaltflächen \_ Änderung</span><span class="sxs-lookup"><span data-stu-id="f2e72-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="f2e72-104">Signalisiert, dass sich die Anzahl der DVD-Menü Schaltflächen geändert hat oder dass sich die Schaltflächen Auswahl geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f2e72-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2e72-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e72-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e72-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f2e72-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f2e72-107">**DWORD** -Wert, der die Anzahl der verfügbaren Schaltflächen angibt.</span><span class="sxs-lookup"><span data-stu-id="f2e72-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="f2e72-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f2e72-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f2e72-109">**DWORD** -Wert, der die aktuell ausgewählte Schaltflächen Nummer angibt.</span><span class="sxs-lookup"><span data-stu-id="f2e72-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="f2e72-110">Die ausgewählte Schaltflächen Nummer 0 bedeutet, dass keine Schaltfläche ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="f2e72-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2e72-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2e72-111">Remarks</span></span>

<span data-ttu-id="f2e72-112">Die Schaltflächen Nummern liegen zwischen 1 und 36.</span><span class="sxs-lookup"><span data-stu-id="f2e72-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="f2e72-113">Die aktuell ausgewählte Schaltfläche kann sich automatisch ändern, wenn ein Navigations Befehl auf der Festplatte und mithilfe der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle auf der Festplatte erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2e72-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="f2e72-114">Dieses Ereignis kann allen verfügbaren Schaltflächen Nummern signalisieren.</span><span class="sxs-lookup"><span data-stu-id="f2e72-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="f2e72-115">Diese Zahlen entsprechen nicht immer den für [**IDvdControl2:: selectandactivatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) verwendeten Schaltflächen Nummern, da von dieser Methode nur eine Teilmenge der Schaltflächen aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2e72-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="f2e72-116">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f2e72-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e72-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2e72-117">Requirements</span></span>



| <span data-ttu-id="f2e72-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2e72-118">Requirement</span></span> | <span data-ttu-id="f2e72-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e72-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e72-120">Header</span><span class="sxs-lookup"><span data-stu-id="f2e72-120">Header</span></span><br/> | <dl> <span data-ttu-id="f2e72-121"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e72-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e72-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2e72-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e72-123">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f2e72-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f2e72-124">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="f2e72-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f2e72-125">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2e72-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




