---
description: Die Hyper-V-Metrik-API definiert die folgenden Programmierelemente.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Referenz zur Hyper-V-Metrik-API
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b833d96d26a3c48183c341ab0f1ff2bc9f5b178ca4439e1c035d82551ec3e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532250"
---
# <a name="hyper-v-metrics-api-reference"></a>Referenz zur Hyper-V-Metrik-API

Die Hyper-V-Metrik-API definiert die folgenden Programmierelemente.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | Stellt die Definitionsaspekte einer Metrik dar, die von einem anderen Metrikwert abgeleitet wird.<br/>                                                                                                                                                                                                                             |
| [**Msvm \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | Stellt den Instanzwert einer Metrik dar, die von einer Instanz der [**Msvm \_ AggregationMetricDefinition-Klasse**](msvm-aggregationmetricdefinition.md) definiert wird.<br/>                                                                                                                                                         |
| [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)<br/>               | Stellt die Definitionsaspekte einer Metrik dar.<br/>                                                                                                                                                                                                                                                                       |
| [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | Stellt einen Metrikwert dar, der von einer Instanz der [**Msvm \_ BaseMetricDefinition-Klasse**](msvm-basemetricdefinition.md) definiert wird.<br/>                                                                                                                                                                                       |
| [**Msvm \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | Stellt die Zuordnung zwischen zwei Metrikdefinitionen oder zwei Metrikwerten dar.<br/>                                                                                                                                                                                                                                      |
| [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | Definiert die Zuordnung zwischen einer [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) und einem [**CIM \_ ManagedElement,**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) um Metriken für letzteres zu definieren. Die Metrikdefinition wird vom ManagedElement kontextabhängig, weshalb die Definition vom -Element abhängig ist.<br/> |
| [**Msvm \_ MetricForME**](msvm-metricforme.md)<br/>                                 | Diese Zuordnung verknüpft ein verwaltetes Element mit den Metrikwerten, die dafür verwaltet werden.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | Stellt eine Zuordnung von Metrikwertobjekten zu ihren Metrikdefinitionen dar.<br/>                                                                                                                                                                                                                                    |
| [**Msvm \_ MetricService**](msvm-metricservice.md)<br/>                             | Bietet die Möglichkeit, Metriken zu verwalten.<br/>                                                                                                                                                                                                                                                                              |
| [**Msvm \_ MetricServiceCapabilities**](msvm-metricservicecapabilities.md)<br/>     | Beschreibt die Funktionen der zugeordneten [**Msvm \_ MetricService-Instanz.**](msvm-metricservice.md)<br/>                                                                                                                                                                                                             |
| [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | Stellt die Einstellungen für den Metrikdienst dar. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-metricservice.md) aufrufen, um eine dieser Eigenschaften zu ändern.<br/>                                                              |



 

 

