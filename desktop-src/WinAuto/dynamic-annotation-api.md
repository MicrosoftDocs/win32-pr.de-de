---
title: Dynamic-Annotation-API
description: Die API für die dynamische Anmerkung ist eine Erweiterung von Microsoft Active Accessibility, mit der Entwickler die vorhandene IAccessible-Unterstützung anpassen können, ohne fehleranfällige Unterklassen-oder Wrapping Techniken verwenden zu müssen.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948090"
---
# <a name="dynamic-annotation-api"></a>Dynamic-Annotation-API

Die API für die dynamische Anmerkung ist eine Erweiterung von Microsoft Active Accessibility, mit der Entwickler die vorhandene [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung anpassen können, ohne fehleranfällige Unterklassen-oder Wrapping Techniken verwenden zu müssen. Dieser Mechanismus ermöglicht es Entwicklern auch, Hinweise oder andere nützliche Informationen an die Oleacc.dll Proxys zu übergeben.

Dynamische Anmerkung wird normalerweise verwendet, um eine ungenaue Instanz eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts zu korrigieren oder zu ändern, das von einem vorhandenen Oleacc.dll Proxy verfügbar gemacht wird. So können Sie beispielsweise den [**Namen**](name-property.md) und die [**Rollen**](role-property.md) Eigenschaften des Standard Proxys überschreiben und [**Beschreibungen**](description-property.md) und [**Hilfe**](help-property.md) Eigenschaften angeben (die möglicherweise nicht vom Standard Proxy bereitgestellt werden).

Mit Windows 7 können Entwickler die API für dynamische Annotation verwenden, um Eigenschaften der Microsoft-Benutzeroberflächen Automatisierung und Microsoft Active Accessibility Eigenschaften der Proxy Objekte, die Oleacc.dll für Windows-Standard Steuerelemente erstellt, mit Anmerkungen versehen. Die Oleacc.dll Proxy Objekte fungieren sowohl für Microsoft Active Accessibility als auch für Benutzeroberflächenautomatisierungs-Clients.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Hintergrundinformationen](background-information.md)
-   [Alternativen zu dynamischer Anmerkung](alternatives-to-dynamic-annotation.md)
-   [Typen von dynamischer Anmerkung](types-of-dynamic-annotation.md)
-   [Direkte Anmerkung](direct-annotation.md)
-   [Werte Zuordnungs Anmerkung](value-map-annotation.md)
-   [Server Anmerkung](server-annotation.md)
-   [Probleme und Einschränkungen](issues-and-limitations.md)

 

 




