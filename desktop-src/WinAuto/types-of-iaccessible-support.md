---
title: Typen der IAccessible-Unterstützung
description: Typen der IAccessible-Unterstützung
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb38ed0b5f7a306f2551085c77f77a3793efec3bc9281cd44d1d7277abe81fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993980"
---
# <a name="types-of-iaccessible-support"></a>Typen der IAccessible-Unterstützung

Microsoft Active Accessibility Server verfügen über zwei Arten von [**IAccessible-Unterstützung:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativ und proxied. Die in einer Anwendung verwendeten Benutzeroberflächenelemente bestimmen, welche Art von Unterstützung geeignet ist. Viele Server, die heute geschrieben werden, nutzen **IAccessible-Proxys** in vollem Umfang und implementieren **IAccessible** nur für steuerelemente, die nicht von Oleacc.dll übermittelt werden, z. B. fensterlose Steuerelemente oder Steuerelemente mit einem benutzerdefinierten Fensterklassennamen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Native Active Accessibility-Implementierung](native-active-accessibility-implementation.md)
-   [IAccessible-Proxys](iaccessible-proxies.md)

 

 




