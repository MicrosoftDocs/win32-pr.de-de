---
description: Ein Eigenschaften Anbieter verwendet die IWbemPropertyProvider-Methoden als primäre Schnittstelle zu WMI. Mit IWbemPropertyProvider können Sie den Code implementieren, um Klassen-und Instanzeigenschaften abzurufen und zu ändern.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Eigenschaften Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351807"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a>Implementieren der primären Schnittstelle für einen Eigenschaften Anbieter

Ein Eigenschaften Anbieter verwendet die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Methoden als primäre Schnittstelle zu WMI. Mit **IWbemPropertyProvider** können Sie den Code implementieren, um Klassen-und Instanzeigenschaften abzurufen und zu ändern.

In der folgenden Tabelle sind die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Methoden aufgelistet, die Sie für einen Eigenschaften Anbieter implementieren können.



| Methode                                                   | Funktion      |
|----------------------------------------------------------|--------------|
| [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | Auslagerung    |
| [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | Modifikation (Modification) |



 

> [!Note]  
> Sie müssen einen Eigenschaften Anbieter als in-Process-Anbieter implementieren. WMI initialisiert Eigenschaften Anbieter, die als Dienste oder ausführbare Dateien geschrieben werden, aber nie Ihre [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) -und [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) -Methoden aufrufen.

 

Wenn Sie eine dieser Methoden nicht unterstützen, kann der Anbieter eine Stubimplementierung bereitstellen, die den **WBEM \_ E- \_ Anbieter \_ nicht \_** unterstützt.

Ein Eigenschaften Anbieter identifiziert eine verwaltete Klasse oder Instanz durch einen Satz von drei Qualifizierern: **propertycontext**, **InstanceContext** und **ClassContext**. WMI übergibt Zeichen folgen Konstanten, die diese drei Qualifizierer für ihren Eigenschaften Anbieter beschreiben.

Der Eigenschaften Anbieter muss darauf vorbereitet sein, die folgenden Typen von Kontext Qualifizierern zu verarbeiten:

-   Der **InstanceContext** -Qualifizierer ist an eine-Instanz angefügt und enthält Informationen, die für jede Eigenschaft in der Instanz gelten.
-   Der **ClassContext** -Qualifizierer ist an eine Klasse angefügt und enthält Informationen, die für jede Instanz in der Klasse gelten. In einer Klasse, die zum Speichern von Daten verwendet wird, die vom Registrierungs Anbieter bereitgestellt werden, kann **ClassContext** z. b. der Pfad zum Registrierungsschlüssel sein, der die zu gemeldeten Eigenschaften enthält.
-   Der **propertycontext** -Qualifizierer gibt kontextspezifische Informationen an, die sich auf die-Eigenschaft beziehen. In einer Klasse zum Speichern von Daten, die vom Registrierungs Anbieter bereitgestellt werden, gibt **propertycontext** z. b. den Namen des Registrierungs Werts an, der von der-Eigenschaft gespeichert werden soll.

Diese Qualifizierer können zusammenarbeiten. Sie können sowohl einen **InstanceContext** -als auch einen **propertycontext** -Wert festlegen, um dem Anbieter mitzuteilen, wie bestimmte Typen von Instanzen behandelt werden sollen. Beispielsweise können Sie Instanzen markieren, die der Anbieter als lesbar erkennt, aber nur eine beschreibbare Eigenschaft besitzt.

Der am häufigsten verwendete Qualifizierer ist **propertycontext**. Daher stellt WMI den **dyn-** Eigenschaften Qualifizierer als Verknüpfung bereit. WMI betrachtet jede Eigenschaft in einer Instanz, die mit **dyn-** Eigenschaften gekennzeichnet ist, auch über die Qualifizierer " **Dynamic**", " [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)" und " **propertycontext**

 

 



