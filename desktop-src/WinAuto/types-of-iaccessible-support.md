---
title: Typen von IAccessible-Unterstützung
description: Typen von IAccessible-Unterstützung
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710686"
---
# <a name="types-of-iaccessible-support"></a>Typen von IAccessible-Unterstützung

Für Microsoft Active Accessibility-Server gibt es zwei Typen von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung: Native und Proxy. Die Benutzeroberflächen Elemente, die in einer Anwendung verwendet werden, bestimmen, welche Art von Unterstützung geeignet ist. Viele Server, die heute geschrieben werden, profitieren von der Verwendung von **IAccessible** -Proxys und implementieren nur **IAccessible** für Steuerelemente, die nicht durch Oleacc.dll über einen Proxy verfügen, z. b. fensterlose Steuerelemente oder Steuerelemente mit einem benutzerdefinierten Fenster Klassennamen

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Native Active Accessibility-Implementierung](native-active-accessibility-implementation.md)
-   [Ibarrierefreie Proxys](iaccessible-proxies.md)

 

 




