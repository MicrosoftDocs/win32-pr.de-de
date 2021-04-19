---
description: Signalisiert, dass die aktuelle Teilbild-streamnummer für den Haupttitel geändert wurde.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359305"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="7bbb3-103">Datenstrom Änderung des EC-DVD- \_ \_ subbildes \_ \_</span><span class="sxs-lookup"><span data-stu-id="7bbb3-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="7bbb3-104">Signalisiert, dass die aktuelle Teilbild-streamnummer für den Haupttitel geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bbb3-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bbb3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bbb3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7bbb3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7bbb3-107">**DWORD** -Wert, der die neue Datenstrom Nummer des Benutzer Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="7bbb3-108">Die Werte des subbildstreams reichen von 0 bis 31.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="7bbb3-109">Der Stream 0xFFFFFFFF gibt an, dass kein Stream ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="7bbb3-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7bbb3-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7bbb3-111">Boolescher Wert, der den Zustand "ein/aus" des Teil Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bbb3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bbb3-112">Remarks</span></span>

<span data-ttu-id="7bbb3-113">Das Teilbild kann automatisch geändert werden, wenn ein Navigations Befehl auf der Festplatte und über die Anwendungssteuerung mithilfe von [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="7bbb3-114">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7bbb3-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbb3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bbb3-115">Requirements</span></span>



| <span data-ttu-id="7bbb3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bbb3-116">Requirement</span></span> | <span data-ttu-id="7bbb3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7bbb3-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbb3-118">Header</span><span class="sxs-lookup"><span data-stu-id="7bbb3-118">Header</span></span><br/> | <dl> <span data-ttu-id="7bbb3-119"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbb3-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbb3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bbb3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbb3-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7bbb3-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7bbb3-122">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="7bbb3-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7bbb3-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bbb3-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




