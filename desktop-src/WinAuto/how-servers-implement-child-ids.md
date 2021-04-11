---
title: Implementierung von untergeordneten IDs durch Server
description: Server Entwickler können sowohl einfachen Elementen als auch barrierefreien Objekten untergeordnete IDs zuweisen. Die empfohlene Vorgehensweise ist jedoch die Unterstützung der Standard-Component Object Model (com)-Schnittstelle IEnumVARIANT in jedem zugänglichen Objekt, das über untergeordnete Elemente verfügt.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948913"
---
# <a name="how-servers-implement-child-ids"></a>Implementierung von untergeordneten IDs durch Server

Server Entwickler können sowohl einfachen Elementen als auch barrierefreien Objekten untergeordnete IDs zuweisen. Die empfohlene Vorgehensweise ist jedoch die Unterstützung der Standard-Component Object Model (com)-Schnittstelle [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in jedem zugänglichen Objekt, das über untergeordnete Elemente verfügt.

Wenn Sie [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)implementieren, müssen Sie folgende Schritte ausführen:

-   Listet alle untergeordneten Elemente auf, sowohl einfache Elemente als auch barrierefreie Objekte. Bereitstellen von untergeordneten IDs für alle einfachen Elemente und Bereitstellen der [**IDispatch**](idispatch-interface.md) für jedes barrierefreie Objekt.
-   Legen Sie für barrierefreie Objekte den **VT** -Member der [**Variante**](variant-structure.md) auf VT \_ Dispatch fest. Der **pdispVal** -Member muss einen Zeiger auf die [**IDispatch**](idispatch-interface.md) -Schnittstelle enthalten. Beachten Sie, dass die **Variante** vom Client zugeordnet und freigegeben wird.
-   Bei einfachen Elementen ist die untergeordnete ID eine beliebige positive ganze Zahl mit 32 Bit. Beachten Sie, dass die NULL-und negativen ganzen Zahlen von Microsoft Active Accessibility reserviert werden. Legen Sie die [**Variant**](variant-structure.md) -Struktur **VT** -Member auf VT \_ I4 und den **LVAL** -Member auf die untergeordnete ID fest.

Wenn Sie [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)nicht unterstützen, müssen Sie untergeordnete IDs zuweisen und die untergeordneten Elemente in jedem Objekt sequenziell beginnend mit einem Objekt angeben.

Es wird empfohlen, dass Clients die Microsoft Active Accessibility-Funktion [**accessiblechildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) verwenden, anstatt die [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle des Servers direkt aufzurufen.

 

 