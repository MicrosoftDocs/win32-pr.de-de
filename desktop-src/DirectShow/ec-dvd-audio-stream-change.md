---
description: Signalisiert, dass die aktuelle audiostreamnummer für den DVD-Haupttitel geändert wurde.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370265"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="3e1f6-103">Änderung des EC \_ \_ -DVD- \_ Audiostreams \_</span><span class="sxs-lookup"><span data-stu-id="3e1f6-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="3e1f6-104">Signalisiert, dass die aktuelle audiostreamnummer für den DVD-Haupttitel geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e1f6-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e1f6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e1f6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3e1f6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3e1f6-107">**DWORD** -Wert, der die neue audiostreamnummer des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="3e1f6-108">Audiostreamnummern reichen von 0 bis 7.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="3e1f6-109">Der Stream 0xFFFFFFFF gibt an, dass kein Stream ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f6-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3e1f6-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3e1f6-111">Keinen.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e1f6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e1f6-112">Remarks</span></span>

<span data-ttu-id="3e1f6-113">Der aktuelle Audiostream kann sich automatisch ändern, indem ein Navigations Befehl, der auf der Festplatte erstellt wurde, sowie über die Anwendungssteuerung mithilfe der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="3e1f6-114">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3e1f6-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1f6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e1f6-115">Requirements</span></span>



| <span data-ttu-id="3e1f6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e1f6-116">Requirement</span></span> | <span data-ttu-id="3e1f6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3e1f6-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1f6-118">Header</span><span class="sxs-lookup"><span data-stu-id="3e1f6-118">Header</span></span><br/> | <dl> <span data-ttu-id="3e1f6-119"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e1f6-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e1f6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e1f6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1f6-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3e1f6-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="3e1f6-122">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="3e1f6-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3e1f6-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e1f6-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




