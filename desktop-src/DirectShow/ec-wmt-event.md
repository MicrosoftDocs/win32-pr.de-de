---
description: Wird vom WM-ASF-Reader-Filter gesendet, wenn die von Digital Rights Management (DRM) geschützten ASF-Dateien gelesen werden.
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358265"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="487db-103">EC_WMT_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="487db-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="487db-104">Wird vom [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter gesendet, wenn die von Digital Rights Management (DRM) geschützten ASF-Dateien gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="487db-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="487db-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="487db-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="487db-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="487db-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="487db-107">Einer der folgenden **WMT- \_ Status** Werte:</span><span class="sxs-lookup"><span data-stu-id="487db-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="487db-108">Wert</span><span class="sxs-lookup"><span data-stu-id="487db-108">Value</span></span>                         | <span data-ttu-id="487db-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="487db-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="487db-110">WMT-Abruf \_ \_ Lizenz</span><span class="sxs-lookup"><span data-stu-id="487db-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="487db-111">Wird gesendet, wenn der Lizenz Erwerbsprozess von der DRM-Komponente erfolgreich oder erfolglos abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="487db-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="487db-112">WMT \_ Individual</span><span class="sxs-lookup"><span data-stu-id="487db-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="487db-113">Der Sicherheits Upgradevorgang wurde entweder erfolgreich oder erfolglos abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="487db-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="487db-114">WMT \_ erfordert \_ Individualisierung</span><span class="sxs-lookup"><span data-stu-id="487db-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="487db-115">Die Datei erfordert, dass eine Anwendung vor dem Ausführen der angeforderten Aktion ein Sicherheits Upgrade erhält.</span><span class="sxs-lookup"><span data-stu-id="487db-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="487db-116">WMT \_ keine \_ Rechte</span><span class="sxs-lookup"><span data-stu-id="487db-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="487db-117">Die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion für eine Datei auszuführen, die von DRM-Version 1 geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="487db-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="487db-118">WMT \_ keine \_ Rechte \_ Ex</span><span class="sxs-lookup"><span data-stu-id="487db-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="487db-119">Die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion für eine Datei auszuführen, die von DRM-Version 7 geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="487db-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="487db-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="487db-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="487db-121">Zeiger auf eine [**am \_ WMT- \_ Ereignis \_ Daten**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) Struktur, die Informationen über das Ereignis enthält, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="487db-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="487db-122">Der **pData** -Member dieser Struktur verweist auf zusätzliche Daten, deren Typ von dem Wert von **lParam1** abhängt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="487db-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="487db-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="487db-123">lParam1</span></span>                       | <span data-ttu-id="487db-124">AM \_ WMT- \_ Ereignis \_ Daten. pdata</span><span class="sxs-lookup"><span data-stu-id="487db-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="487db-125">WMT-Abruf \_ \_ Lizenz</span><span class="sxs-lookup"><span data-stu-id="487db-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="487db-126">Zeiger auf eine [**WM- \_ get- \_ Lizenz \_ Daten**](/windows/desktop/wmformat/wm-get-license-data) Struktur.</span><span class="sxs-lookup"><span data-stu-id="487db-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="487db-127">Diese Struktur ist im Windows Media-Format-SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="487db-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="487db-128">WMT \_ Individual</span><span class="sxs-lookup"><span data-stu-id="487db-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="487db-129">Zeiger auf eine [**WM- \_ Individualisierungs \_ Status**](/windows/desktop/wmformat/wm-individualize-status) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="487db-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="487db-130">WMT \_ erfordert \_ Individualisierung</span><span class="sxs-lookup"><span data-stu-id="487db-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="487db-131">**Null**.</span><span class="sxs-lookup"><span data-stu-id="487db-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="487db-132">WMT \_ keine \_ Rechte</span><span class="sxs-lookup"><span data-stu-id="487db-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="487db-133">Zeiger auf eine breit Zeichen-Zeichenfolge, die eine Challenge-URL enthält.</span><span class="sxs-lookup"><span data-stu-id="487db-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="487db-134">WMT \_ keine \_ Rechte \_ Ex</span><span class="sxs-lookup"><span data-stu-id="487db-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="487db-135">Zeiger auf eine [**WM- \_ get- \_ Lizenz \_ Daten**](/windows/desktop/wmformat/wm-get-license-data) Struktur.</span><span class="sxs-lookup"><span data-stu-id="487db-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="487db-136">Der Wert von *lParam2* kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="487db-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="487db-137">Überprüfen Sie den Wert, bevor Sie den Zeiger dereferenzieren.</span><span class="sxs-lookup"><span data-stu-id="487db-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="487db-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="487db-138">Remarks</span></span>

<span data-ttu-id="487db-139">Weitere Informationen zum Aktivieren der Wiedergabe von DRM-geschützten Dateien finden Sie in der Dokumentation zum Windows Media-Format SDK.</span><span class="sxs-lookup"><span data-stu-id="487db-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="487db-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="487db-140">Requirements</span></span>



| <span data-ttu-id="487db-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="487db-141">Requirement</span></span> | <span data-ttu-id="487db-142">Wert</span><span class="sxs-lookup"><span data-stu-id="487db-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="487db-143">Header</span><span class="sxs-lookup"><span data-stu-id="487db-143">Header</span></span><br/> | <dl> <span data-ttu-id="487db-144"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="487db-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="487db-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="487db-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487db-146">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="487db-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="487db-147">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="487db-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

