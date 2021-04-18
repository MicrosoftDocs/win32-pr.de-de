---
description: Signalisiert die aktuelle Zeit im DVD- \_ hmsf- \_ Zeit Code Format relativ zum Anfang des Titels. Dieses Ereignis wird am Anfang jeder vobu ausgelöst, die alle 0,4 bis 1,0 Sekunden auftritt.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365944"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="1a58a-104">EC- \_ DVD \_ aktuelle \_ hmsf- \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="1a58a-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="1a58a-105">Signalisiert die aktuelle Zeit im [**DVD- \_ hmsf- \_ Zeit Code**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) Format relativ zum Anfang des Titels.</span><span class="sxs-lookup"><span data-stu-id="1a58a-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="1a58a-106">Dieses Ereignis wird am Anfang jeder vobu ausgelöst, die alle 0,4 bis 1,0 Sekunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="1a58a-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a58a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a58a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a58a-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1a58a-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1a58a-109">Ein ULONG-Wert, der die \_ hmsf- \_ Zeit Code Struktur der DVD enthält.</span><span class="sxs-lookup"><span data-stu-id="1a58a-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="1a58a-110">Weisen Sie lParam1 einer ULONG-Variablen zu, und wandeln Sie diese Variable dann in eine DVD- \_ hmsf- \_ Zeit Leitzahl um, um auf ihre Werte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1a58a-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="1a58a-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1a58a-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1a58a-112">Ein ULONG-Wert, der eine Union von [**DVD- \_ \_ timecodeflags**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)enthält.</span><span class="sxs-lookup"><span data-stu-id="1a58a-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a58a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a58a-113">Remarks</span></span>

<span data-ttu-id="1a58a-114">Das \_ hmsf-Zeit \_ Code Format in DVD soll das alte BCD-Format ersetzen, das in den \_ \_ aktuellen Zeit Ereignissen der EC-DVD zurückgegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="1a58a-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="1a58a-115">Die hmsf-Timecodes sind einfacher zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1a58a-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="1a58a-116">Damit der Navigator die aktuellen \_ hmsf-Zeit Ereignisse der EC-DVD und nicht die \_ \_ \_ \_ aktuellen Zeit Ereignisse der EC-DVD sendet \_ \_ , muss eine Anwendung aufgerufen werden `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` .</span><span class="sxs-lookup"><span data-stu-id="1a58a-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="1a58a-117">Wenn dieses Flag festgelegt wird, erwartet der Navigator auch, dass alle Zeitparameter in den [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Methoden als DVD- \_ hmsf-Timecodes übermittelt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1a58a-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="1a58a-118">Dieses Ereignis wird in den Titel Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1a58a-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a58a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a58a-119">Requirements</span></span>



| <span data-ttu-id="1a58a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a58a-120">Requirement</span></span> | <span data-ttu-id="1a58a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1a58a-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a58a-122">Header</span><span class="sxs-lookup"><span data-stu-id="1a58a-122">Header</span></span><br/> | <dl> <span data-ttu-id="1a58a-123"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a58a-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a58a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a58a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a58a-125">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1a58a-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1a58a-126">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="1a58a-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1a58a-127">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a58a-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




