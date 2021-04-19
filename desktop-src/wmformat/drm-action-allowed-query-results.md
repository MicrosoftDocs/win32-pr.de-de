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
# <a name="drm_action_allowed_query_results-enumeration"></a>\_ \_ \_ Enumeration für zulässige Abfrage \_ Ergebnisse durch DRM-Aktion

Der Enumerationstyp " **DRM- \_ Aktion \_ zulässige \_ Abfrage \_ Ergebnisse** " wird von der [**iwmdrmlicensequery:: queryAction Allowed**](iwmdrmlicensequery-queryactionallowed.md) -Schnittstelle verwendet, um den Grund anzugeben, warum eine Aktion nicht zulässig ist.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**zulässige Abfrage für DRM- \_ Aktion \_ \_ \_ nicht \_ aktiviert**
</dt> <dd>

Gibt an, dass die Abfrage Aktion nicht zulässig ist. Bei Aktionen, die nicht zulässig sind, ist der zurückgegebene Wert dieser Wert, der in Kombination mit einem bitweisen OR-Operator mit einem oder mehreren der anderen Werte in dieser Enumeration verwendet wird.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**von der DRM- \_ Aktion zugelassene \_ Abfrage ist \_ \_ \_ \_ keine \_ Lizenz aktiviert**
</dt> <dd>

Gibt an, dass für den angeforderten Inhalt keine Lizenz vorhanden ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**die \_ zulässige Abfrage der DRM-Aktion ist \_ \_ \_ nicht \_ aktiviert \_ \_ .**
</dt> <dd>

Gibt an, dass eine Lizenz für den Inhalt vorhanden ist, dass das abgefragte Recht jedoch nicht zulässig ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**die \_ zulässige Abfrage der DRM-Aktion ist \_ \_ \_ nicht \_ aktiviert \_ .**
</dt> <dd>

Gibt an, dass das abgefragte Recht durch eine Anzahl eingeschränkt wird und keine weiteren Verwendungen verbleiben.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**die \_ zulässige Abfrage der DRM-Aktion ist \_ \_ \_ nicht \_ aktiviert \_ .**
</dt> <dd>

Gibt an, dass das abgefragte Recht mit einem Ablaufdatum eingeschränkt ist, das vor dem aktuellen Datum liegt.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**die \_ \_ zulässige Abfrage der DRM-Aktion ist nicht \_ \_ \_ aktiviert \_ \_ .**
</dt> <dd>

Gibt an, dass das abgefragte Recht mit einem Startdatum eingeschränkt ist, das nach dem aktuellen Datum liegt.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM- \_ Aktion \_ zulässige \_ Abfrage \_ nicht aktiviert, \_ \_ appsec \_ zu \_ niedrig**
</dt> <dd>

Gibt an, dass eine Lizenz für den Inhalt vorhanden ist und dass die Lizenz das abgefragte Recht zulässt, aber dass die Sicherheitsstufe der aufrufenden Anwendung nicht hoch genug ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**von der DRM- \_ Aktion \_ zulässige \_ Abfrage \_ nicht \_ aktiviert \_ req- \_ indiv**
</dt> <dd>

Gibt an, dass eine Lizenz für den Inhalt vorhanden ist und dass die Lizenz das abgefragte Recht zulässt, aber dass das DRM-Subsystem individualisiert werden muss.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM- \_ Aktion ' \_ zulässige \_ Abfrage nicht aktiviert ' ist \_ \_ \_ \_ \_ zu \_ niedrig.**
</dt> <dd>

Gibt an, dass die Ausgabe Schutz Ebene des Clients zu niedrig ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM- \_ Aktion \_ zulässige Abfrage ist \_ \_ nicht aktiviert, \_ \_ \_ kopieropl \_ ausgeschlossen**
</dt> <dd>

Gibt an, dass die Ausgabe Schutz Ebene des Clients in der Ausschlussliste enthalten ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**zulässige Abfrage für DRM- \_ Aktion \_ \_ \_ nicht \_ aktiviert, \_ keine \_ Takt \_ Unterstützung**
</dt> <dd>

Gibt an, dass die Lizenz eine sichere Uhr-Unterstützung erfordert und dass Sie vom Client nicht bereitgestellt wird.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**die \_ zulässige DRM-Aktion hat \_ \_ \_ \_ \_ keine \_ Messungs \_ Unterstützung aktiviert.**
</dt> <dd>

Gibt an, dass die abgefragte Aktion von einer Lizenz zugelassen wird. diese Messung ist jedoch erforderlich, und der Client unterstützt die Messung nicht.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM- \_ Aktion " \_ zulässige \_ Abfrage nicht aktiviert"-Kette ist \_ \_ \_ \_ \_ zu \_ hoch**
</dt> <dd>

Gibt an, dass die Rechte für die abgefragte Aktion nicht bestimmt werden können, weil der Inhalt durch eine verkettete Lizenz abgedeckt ist und die Blatt Lizenz fehlt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Werte dieses Enumerationstyps geben an, dass eine Aktion nicht zulässig ist. Der Wert 0 (null) gibt an, dass die Aktion zulässig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





