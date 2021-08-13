---
title: Native IAccessible-Unterstützung
description: Oleacc.dll implementiert IAccIdentity im Auftrag von OBJID \_ CLIENT \ 160;IAccessible-Schnittstellenzeiger und deren unmittelbar untergeordnete Elemente.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad499b96c668349cc481efd388a780ba094eff2ef6eb4ae52ab041aabea70fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565050"
---
# <a name="native-iaccessible-support"></a>Native IAccessible-Unterstützung

Oleacc.dll implementiert [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) im Namen von [**OBJID \_ CLIENT**](object-identifiers.md) IAccessible-Schnittstellenzeigern und deren unmittelbar untergeordneten Elementen. [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Ein **OBJID \_ CLIENT** **IAccessible-Schnittstellenzeiger** wird zurückgegeben, wenn WM [**\_ GETOBJECT**](wm-getobject.md) mit *lParam*  =  **OBJID \_ CLIENT** an ein **HWND** gesendet wird, das den Clientbereich des Fensters oder des Steuerelements als Ganzes darstellt. Das übergeordnete Element eines solchen **IAccessible-Schnittstellenzeigers** hat in der Regel die Rolle [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) und ist das **IAccessible-Objekt,** das zurückgegeben wird, wenn **WM \_ GETOBJECT** mit *lParam*  =  [**OBJID \_ WINDOW**](object-identifiers.md) an einen hwnd gesendet wird.

Diese [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) treten in der Regel auf, wenn ein Oleacc.dll Proxy untergliedert ist oder wenn ein einfaches benutzerdefiniertes Steuerelement (z. B. ein Container **IAccessible** plus eine Ebene einfacher Elementelemente) eine native **IAccessible-Implementierung** bereitstellt.

Kompliziertere native [**IAccessible-Implementierungen,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) z. B. wo eine Hierarchie von **IAccessible** s vorhanden ist oder wo benutzerdefinierte Objekt-IDs verwendet werden, müssen [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) selbst implementieren.

 

 




