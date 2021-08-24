---
description: Verwaltet Metriken für verwaltete Elemente.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5fd976abf5bce91ffbc5581e73f93c2a8422fcdcbe69fd70745511362e504d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694940"
---
# <a name="cim_metricservice-class"></a>CIM \_ MetricService-Klasse

Verwaltet Metriken für verwaltete Elemente.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM \_ MetricService-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ MetricService-Klasse** verfügt über diese Methoden.



| Methode                                                                   | Beschreibung                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ControlMetrics**](cim-metricservice-controlmetrics.md)               | Aktiviert und deaktiviert die Sammlung von Metriken.<br/>                                                                                                                          |
| [**ControlMetricsByClass**](cim-metricservice-controlmetricsbyclass.md) | Aktiviert und deaktiviert die Sammlung von Metriken für eine Klasse.<br/>                                                                                                              |
| [**ControlSampleTimes**](cim-metricservice-controlsampletimes.md)       | Gibt an, wann Metriken erfasst werden.<br/>                                                                                                                                     |
| [**GetMetricValues**](cim-metricservice-getmetricvalues.md)             | Ruft eine gefilterte Liste von Metrikwerten ab.<br/>                                                                                                                              |
| [**ShowMetrics**](cim-metricservice-showmetrics.md)                     | Gibt an, ob die Metriksammlung für die angegebenen verwalteten Elemente aktiviert ist, und gibt die Metriken an, die für die Sammlung für jedes verwaltete Element verfügbar sind.<br/> |
| [**ShowMetricsByClass**](cim-metricservice-showmetricsbyclass.md)       | Gibt an, welche Metriken für die Sammlung für alle Instanzen einer CIM-Klasse verfügbar sind.<br/>                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

 




