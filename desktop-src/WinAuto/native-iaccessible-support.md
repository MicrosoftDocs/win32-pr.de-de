---
title: Native IAccessible-Unterstützung
description: Oleacc.dll implementiert iaccidentity im Namen von objID- \_ Client \ 160; IAccessible-Schnittstellen Zeigern und deren unmittelbaren, einfachen untergeordneten Elementen.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856428"
---
# <a name="native-iaccessible-support"></a>Native IAccessible-Unterstützung

Oleacc.dll implementiert [**iaccidentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) für den [**objID- \_ Client**](object-identifiers.md), der  [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Schnittstellen Zeiger und seine unmittelbaren einfachen untergeordneten Elemente. Ein **objID- \_ Client**, der  **IAccessible** -Schnittstellen Zeiger ist, wird zurückgegeben, wenn [**WM \_ GetObject**](wm-getobject.md) mit *LPARAM*  =  **objID- \_ Client** an ein **HWND** gesendet wird, das den Client Bereich des Fensters oder das Steuerelement als Ganzes darstellt. **Das über** geordnete Element eines solchen **IAccessible** -Schnittstellen Zeigers verfügt in der Regel über eine Rolle des [**Rollen \_ System \_ Fensters**](object-roles.md) und ist das Objekt, das zurückgegeben wird, wenn **WM \_ GetObject** mit *LPARAM*  =  [**objID- \_ Fenster**](object-identifiers.md) an ein HWND gesendet wird.

Diese [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger treten in der Regel auf, wenn ein Oleacc.dll Proxy untergeordnet ist oder wenn ein einfaches benutzerdefiniertes  Steuerelement (z. b 

Komplexere systemeigene [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierungen, wie z. b. das vorhanden sein einer Hierarchie von **IAccessible**-Objekten oder die Verwendung von benutzerdefinierten Objekt-IDs, müssen [**iaccidentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) selbst implementieren

 

 




