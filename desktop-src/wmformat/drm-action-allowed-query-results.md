---
title: DRM_ACTION_ALLOWED_QUERY_RESULTS-Enumeration (wmdrmsdk. h)
description: Der \_ \_ Enumerationstyp "DRM-Aktion zulässige \_ Abfrage \_ Ergebnisse" wird von der iwmdrmlicensequery queryAction Allowed-Schnittstelle verwendet, um den Grund anzugeben, warum eine Aktion nicht zulässig ist.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370794"
---
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="79c87-105">\_ \_ \_ Enumeration für zulässige Abfrage \_ Ergebnisse durch DRM-Aktion</span><span class="sxs-lookup"><span data-stu-id="79c87-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="79c87-106">Der Enumerationstyp " **DRM- \_ Aktion \_ zulässige \_ Abfrage \_ Ergebnisse** " wird von der [**iwmdrmlicensequery:: queryAction Allowed**](iwmdrmlicensequery-queryactionallowed.md) -Schnittstelle verwendet, um den Grund anzugeben, warum eine Aktion nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c87-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c87-107">Syntax</span></span>


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a><span data-ttu-id="79c87-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="79c87-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="79c87-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**zulässige Abfrage für DRM- \_ Aktion \_ \_ \_ nicht \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="79c87-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-110">Gibt an, dass die Abfrage Aktion nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="79c87-111">Bei Aktionen, die nicht zulässig sind, ist der zurückgegebene Wert dieser Wert, der in Kombination mit einem bitweisen OR-Operator mit einem oder mehreren der anderen Werte in dieser Enumeration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79c87-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**von der DRM- \_ Aktion zugelassene \_ Abfrage ist \_ \_ \_ \_ keine \_ Lizenz aktiviert**</span><span class="sxs-lookup"><span data-stu-id="79c87-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-113">Gibt an, dass für den angeforderten Inhalt keine Lizenz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**die \_ zulässige Abfrage der DRM-Aktion ist \_ \_ \_ nicht \_ aktiviert \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="79c87-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-115">Gibt an, dass eine Lizenz für den Inhalt vorhanden ist, dass das abgefragte Recht jedoch nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**die \_ zulässige Abfrage der DRM-Aktion ist \_ \_ \_ nicht \_ aktiviert \_ .**</span><span class="sxs-lookup"><span data-stu-id="79c87-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-117">Gibt an, dass das abgefragte Recht durch eine Anzahl eingeschränkt wird und keine weiteren Verwendungen verbleiben.</span><span class="sxs-lookup"><span data-stu-id="79c87-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**die \_ zulässige Abfrage der DRM-Aktion ist \_ \_ \_ nicht \_ aktiviert \_ .**</span><span class="sxs-lookup"><span data-stu-id="79c87-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-119">Gibt an, dass das abgefragte Recht mit einem Ablaufdatum eingeschränkt ist, das vor dem aktuellen Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="79c87-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**die \_ \_ zulässige Abfrage der DRM-Aktion ist nicht \_ \_ \_ aktiviert \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="79c87-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-121">Gibt an, dass das abgefragte Recht mit einem Startdatum eingeschränkt ist, das nach dem aktuellen Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="79c87-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM- \_ Aktion \_ zulässige \_ Abfrage \_ nicht aktiviert, \_ \_ appsec \_ zu \_ niedrig**</span><span class="sxs-lookup"><span data-stu-id="79c87-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-123">Gibt an, dass eine Lizenz für den Inhalt vorhanden ist und dass die Lizenz das abgefragte Recht zulässt, aber dass die Sicherheitsstufe der aufrufenden Anwendung nicht hoch genug ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**von der DRM- \_ Aktion \_ zulässige \_ Abfrage \_ nicht \_ aktiviert \_ req- \_ indiv**</span><span class="sxs-lookup"><span data-stu-id="79c87-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-125">Gibt an, dass eine Lizenz für den Inhalt vorhanden ist und dass die Lizenz das abgefragte Recht zulässt, aber dass das DRM-Subsystem individualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="79c87-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM- \_ Aktion ' \_ zulässige \_ Abfrage nicht aktiviert ' ist \_ \_ \_ \_ \_ zu \_ niedrig.**</span><span class="sxs-lookup"><span data-stu-id="79c87-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-127">Gibt an, dass die Ausgabe Schutz Ebene des Clients zu niedrig ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM- \_ Aktion \_ zulässige Abfrage ist \_ \_ nicht aktiviert, \_ \_ \_ kopieropl \_ ausgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="79c87-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-129">Gibt an, dass die Ausgabe Schutz Ebene des Clients in der Ausschlussliste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**zulässige Abfrage für DRM- \_ Aktion \_ \_ \_ nicht \_ aktiviert, \_ keine \_ Takt \_ Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="79c87-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-131">Gibt an, dass die Lizenz eine sichere Uhr-Unterstützung erfordert und dass Sie vom Client nicht bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="79c87-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**die \_ zulässige DRM-Aktion hat \_ \_ \_ \_ \_ keine \_ Messungs \_ Unterstützung aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="79c87-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-133">Gibt an, dass die abgefragte Aktion von einer Lizenz zugelassen wird. diese Messung ist jedoch erforderlich, und der Client unterstützt die Messung nicht.</span><span class="sxs-lookup"><span data-stu-id="79c87-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="79c87-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM- \_ Aktion " \_ zulässige \_ Abfrage nicht aktiviert"-Kette ist \_ \_ \_ \_ \_ zu \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="79c87-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="79c87-135">Gibt an, dass die Rechte für die abgefragte Aktion nicht bestimmt werden können, weil der Inhalt durch eine verkettete Lizenz abgedeckt ist und die Blatt Lizenz fehlt.</span><span class="sxs-lookup"><span data-stu-id="79c87-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79c87-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79c87-136">Remarks</span></span>

<span data-ttu-id="79c87-137">Die Werte dieses Enumerationstyps geben an, dass eine Aktion nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="79c87-138">Der Wert 0 (null) gibt an, dass die Aktion zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="79c87-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c87-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79c87-139">Requirements</span></span>



| <span data-ttu-id="79c87-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79c87-140">Requirement</span></span> | <span data-ttu-id="79c87-141">Wert</span><span class="sxs-lookup"><span data-stu-id="79c87-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79c87-142">Header</span><span class="sxs-lookup"><span data-stu-id="79c87-142">Header</span></span><br/> | <dl> <span data-ttu-id="79c87-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c87-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c87-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79c87-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c87-145">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="79c87-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





