---
description: Die Hyper-V-Metrik-API definiert die folgenden Programmier Elemente.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Referenz zur Hyper-V-Metrik-API
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd4945bd390d995378c290f846335371fead753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358828"
---
# <a name="hyper-v-metrics-api-reference"></a>Referenz zur Hyper-V-Metrik-API

Die Hyper-V-Metrik-API definiert die folgenden Programmier Elemente.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ aggregationmetricdefinition**](msvm-aggregationmetricdefinition.md)<br/> | Stellt die Definitions Aspekte einer Metrik dar, die von einem anderen Metrikwert abgeleitet ist.<br/>                                                                                                                                                                                                                             |
| [**MSVM \_ aggregationmetricvalue**](msvm-aggregationmetricvalue.md)<br/>           | Stellt den Instanzwert einer Metrik dar, die durch eine Instanz der [**MSVM \_ aggregationmetricdefinition**](msvm-aggregationmetricdefinition.md) -Klasse definiert wird.<br/>                                                                                                                                                         |
| [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md)<br/>               | Stellt die Definitions Aspekte einer Metrik dar.<br/>                                                                                                                                                                                                                                                                       |
| [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md)<br/>                         | Stellt einen Metrikwert dar, der durch eine Instanz der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Klasse definiert wird.<br/>                                                                                                                                                                                       |
| [**MSVM \_ metriccollectionabhängigkeit**](msvm-metriccollectiondependency.md)<br/>   | Stellt die Zuordnung zwischen zwei metrikdefinitionen oder zwei Metrikwerten dar.<br/>                                                                                                                                                                                                                                      |
| [**MSVM \_ metricdefforme**](msvm-metricdefforme.md)<br/>                           | Definiert die Zuordnung zwischen einer [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) und einem [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , um Metriken für letztere zu definieren. Der Definition der Metriken wird vom managedelement Kontext zugewiesen, weshalb die Definition vom Element abhängig ist.<br/> |
| [**MSVM \_ metricforme**](msvm-metricforme.md)<br/>                                 | Diese Zuordnung verknüpft ein verwaltetes Element mit den Metrikwerten, die für das Element beibehalten werden.<br/>                                                                                                                                                                                                                               |
| [**MSVM \_ metricinstance**](msvm-metricinstance.md)<br/>                           | Stellt eine Zuordnung von metrikwertobjekten mit ihren metrikdefinitionen dar.<br/>                                                                                                                                                                                                                                    |
| [**MSVM \_ metricservice**](msvm-metricservice.md)<br/>                             | Bietet die Möglichkeit zum Verwalten von Metriken.<br/>                                                                                                                                                                                                                                                                              |
| [**MSVM \_ metricservicecapabili**](msvm-metricservicecapabilities.md)<br/>     | Beschreibt die Funktionen der zugeordneten [**MSVM- \_ metricservice**](msvm-metricservice.md) -Instanz.<br/>                                                                                                                                                                                                             |
| [**MSVM \_ metricservicesettingdata**](msvm-metricservicesettingdata.md)<br/>       | Stellt die Einstellungen für den metrikdienst dar. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die [**modifyservicesettings**](modifyservicesettings-msvm-metricservice.md) -Methode zum Ändern dieser Eigenschaften aufruft.<br/>                                                              |



 

 

