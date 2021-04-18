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
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351716"
---
# <a name="cim_metricservice-class"></a>CIM \_ metricservice-Klasse

Verwaltet Metriken für verwaltete Elemente.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM \_ metricservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ metricservice** -Klasse verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Controlmetrics**](cim-metricservice-controlmetrics.md)               | Aktiviert und deaktiviert die Auflistung von Metriken.<br/>                                                                                                                          |
| [**Controlmetricsbyclass**](cim-metricservice-controlmetricsbyclass.md) | Aktiviert und deaktiviert die Auflistung von Metriken für eine Klasse.<br/>                                                                                                              |
| [**Controlsampletimes**](cim-metricservice-controlsampletimes.md)       | Gibt an, wann Metriken erfasst werden.<br/>                                                                                                                                     |
| [**Getmetricvalues**](cim-metricservice-getmetricvalues.md)             | Ruft eine gefilterte Liste von Metrikwerten ab.<br/>                                                                                                                              |
| [**Showmetrics**](cim-metricservice-showmetrics.md)                     | Gibt an, ob die metrikauflistung für die angegebenen verwalteten Elemente aktiviert ist, und gibt die Metriken an, die für jedes verwaltete Element für die Auflistung verfügbar sind.<br/> |
| [**Showmetricsbyclass**](cim-metricservice-showmetricsbyclass.md)       | Gibt an, welche Metriken für alle Instanzen einer CIM-Klasse für die Auflistung verfügbar sind.<br/>                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




