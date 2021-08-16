---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71963ad564454dcb90266b4fe4c63ba7282dbc514ab286629798420ff1db9f6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327696"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Text

AccessibleObjectFromPoint( {0} , ) hat NULL {1} zurückgegeben.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Die Adresse der [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Benutzeroberflächenelements, die für die angegebenen Koordinaten ermittelt wurde, ist NULL.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. B. das Verschieben des Fokus auf ein HWND ohne Ziel, beeinträchtigt den Überprüfungsprozess.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffertests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




