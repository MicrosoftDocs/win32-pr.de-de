---
title: API für dynamische Anmerkungen
description: Die API für dynamische Anmerkungen ist eine Erweiterung für Microsoft Active Accessibility, mit der Entwickler die vorhandene IAccessible-Unterstützung anpassen können, ohne fehleranfällige Unterklassen- oder Umbruchtechniken verwenden zu müssen.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca8b95d1175d4a6bd894e79c55f6798a73165fab2d6e6da40e3b952e68824d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115320"
---
# <a name="dynamic-annotation-api"></a>API für dynamische Anmerkungen

Die API für dynamische Anmerkungen ist eine Erweiterung für Microsoft Active Accessibility, mit der Entwickler die vorhandene [**IAccessible-Unterstützung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) anpassen können, ohne fehleranfällige Unterklassen- oder Umbruchtechniken verwenden zu müssen. Mit diesem Mechanismus können Entwickler auch Hinweise oder andere nützliche Informationen an die Proxys Oleacc.dll übergeben.

Dynamische Anmerkungen werden in der Regel verwendet, um eine ungenaue Instanz eines [**IAccessible-Objekts**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zu korrigieren oder zu korrigieren, das von einem vorhandenen Oleacc.dll wird. Sie können sie beispielsweise verwenden, [](name-property.md) um die Eigenschaften Name und [**Rolle**](role-property.md) [](description-property.md) zu [](help-property.md) überschreiben, die vom Standardproxy bereitgestellt werden, und um Beschreibungs- und Hilfeeigenschaften (die möglicherweise nicht vom Standardproxy bereitgestellt werden) zur Verfügung zu stellen.

Mit Windows 7 können Entwickler die API für dynamische Anmerkungen verwenden, um Microsoft Benutzeroberflächenautomatisierung-Eigenschaften sowie Microsoft Active Accessibility-Eigenschaften der Proxyobjekte zu kommentieren, die Oleacc.dll für Standardsteuerelemente Windows erstellt. Die Oleacc.dll Proxyobjekte dienen sowohl Microsoft Active Accessibility als auch Benutzeroberflächenautomatisierung Clients.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Hintergrundinformationen](background-information.md)
-   [Alternativen zur dynamischen Anmerkung](alternatives-to-dynamic-annotation.md)
-   [Typen dynamischer Anmerkungen](types-of-dynamic-annotation.md)
-   [Direkte Anmerkung](direct-annotation.md)
-   [Wertzuordnungsanmerkung](value-map-annotation.md)
-   [Serveranmerkung](server-annotation.md)
-   [Probleme und Einschränkungen](issues-and-limitations.md)

 

 




