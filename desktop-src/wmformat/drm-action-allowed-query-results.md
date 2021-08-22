---
title: DRM_ACTION_ALLOWED_QUERY_RESULTS -Enumeration (Wmdrmsdk.h)
description: Der DRM ACTION ALLOWED QUERY RESULTS-Enumerationstyp wird von der \_ \_ \_ IWMDRMLicenseQuery QueryActionAllowed-Schnittstelle verwendet, um den Grund anzugeben, aus dem eine Aktion \_ nicht zulässig ist.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS enumeration windows Media Format
- Windows Media-Enumerationsformat
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
ms.openlocfilehash: d66973838bb6d9cf745ae30b885acccf7b4b311834bbe827d96ccbeea501bd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547810"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>DRM \_ ACTION ALLOWED QUERY \_ \_ \_ RESULTS-Enumeration

Der **DRM \_ ACTION ALLOWED QUERY \_ \_ RESULTS-Enumerationstyp \_** wird von der [**IWMDRMLicenseQuery::QueryActionAllowed-Schnittstelle**](iwmdrmlicensequery-queryactionallowed.md) verwendet, um den Grund anzugeben, aus dem eine Aktion nicht zulässig ist.

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

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_DRM-AKTION \_ ZULÄSSIGE ABFRAGE \_ NICHT \_ \_ AKTIVIERT**
</dt> <dd>

Gibt an, dass die Abfrageaktion nicht zulässig ist. Für Aktionen, die nicht zulässig sind, ist der zurückgegebene Wert dieser Wert, der mithilfe eines bitweises OR mit einem oder mehr der anderen Werte in dieser Enumeration kombiniert wird.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM \_ ACTION \_ ALLOWED \_ QUERY \_ NOT \_ ENABLED \_ NO \_ LICENSE**
</dt> <dd>

Gibt an, dass für den angeforderten Inhalt keine Lizenz vorhanden ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM \_ ACTION \_ ALLOWED \_ QUERY \_ NOT \_ ENABLED \_ NO \_ RIGHT**
</dt> <dd>

Gibt an, dass eine Lizenz für den Inhalt vorhanden ist, das abgefragte Recht jedoch nicht zulässig ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_DRM-AKTION \_ ZULÄSSIGE ABFRAGE \_ NICHT \_ \_ \_ AUSGESCHÖPFT**
</dt> <dd>

Gibt an, dass das abgefragte Recht durch eine Anzahl eingeschränkt wird und dass keine weitere Verwendungen verbleiben.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**\_DRM-AKTION \_ ZULÄSSIGE ABFRAGE NICHT AKTIVIERT \_ \_ \_ \_ ABGELAUFEN**
</dt> <dd>

Gibt an, dass das abgefragte Recht auf ein Ablaufdatum beschränkt ist, das vor dem aktuellen Datum liegt.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_DRM-AKTION \_ ZULÄSSIGE ABFRAGE NICHT AKTIVIERT NICHT \_ \_ \_ \_ \_ GESTARTET**
</dt> <dd>

Gibt an, dass das abgefragte Recht mit einem Startdatum eingeschränkt ist, das nach dem aktuellen Datum liegt.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM \_ ACTION ALLOWED QUERY NOT ENABLED APPSEC TOO LOW (DRM-AKTION \_ \_ \_ ZUGELASSENE ABFRAGE NICHT \_ \_ AKTIVIERT) APPSEC \_ ZU \_ NIEDRIG**
</dt> <dd>

Gibt an, dass eine Lizenz für den Inhalt vorhanden ist und dass die Lizenz das abgefragte Recht zulässt, die Sicherheitsstufe der aufrufenden Anwendung jedoch nicht hoch genug ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM \_ ACTION \_ ALLOWED \_ QUERY \_ NOT \_ ENABLED \_ REQ \_ INDIV**
</dt> <dd>

Gibt an, dass eine Lizenz für den Inhalt vorhanden ist und dass die Lizenz das abgefragte Recht zulässt, das DRM-Subsystem jedoch individualisiert werden muss.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM \_ ACTION \_ ALLOWED \_ QUERY \_ NOT \_ ENABLED \_ COPY \_ OPL \_ TOO \_ LOW**
</dt> <dd>

Gibt an, dass die Ausgabeschutzebene des Clients zu niedrig ist.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM \_ ACTION \_ ALLOWED \_ QUERY \_ NOT \_ ENABLED \_ COPY \_ OPL \_ EXCLUDED**
</dt> <dd>

Gibt an, dass sich die Ausgabeschutzebene des Clients in der Ausschlussliste befindet.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM \_ ACTION \_ ALLOWED \_ QUERY \_ NOT \_ ENABLED \_ NO \_ CLOCK \_ SUPPORT**
</dt> <dd>

Gibt an, dass die Lizenz eine sichere Uhrunterstützung erfordert und dass der Client sie nicht angibt.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM ACTION ALLOWED QUERY NOT ENABLED NO METERING SUPPORT (DRM-AKTION \_ \_ \_ \_ ZUGELASSENE ABFRAGE \_ NICHT \_ AKTIVIERT) KEINE \_ \_ MESSUNGSUNTERSTÜTZUNG**
</dt> <dd>

Gibt an, dass die abgefragte Aktion von einer Lizenz zugelassen wird, die Messung jedoch erforderlich ist und der Client keine Messung unterstützt.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**\_DRM-AKTION \_ ERLAUBT ABFRAGE NICHT AKTIVIERT \_ \_ \_ \_ \_ KETTENTIEFE ZU \_ \_ HOCH**
</dt> <dd>

Gibt an, dass die Rechte für die abgefragte Aktion nicht bestimmt werden können, da der Inhalt durch eine verkettete Lizenz abgedeckt ist und die Blattlizenz fehlt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte dieses Enumerationstyps geben an, dass eine Aktion nicht zulässig ist. Der Wert 0 (null) gibt an, dass die Aktion zulässig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





