---
title: AccessibleObjectFromPointReturnedNullChildId
description: AccessibleObjectFromPointReturnedNullChildId
ms.assetid: 20511B76-736B-4B43-8DC3-4306DF74CF73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb6ebf33cdfdef7b6e32ec4b9943accc06551d5f37f625fa77cb22e01b913df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994360"
---
# <a name="accessibleobjectfrompointreturnednullchildid"></a>AccessibleObjectFromPointReturnedNullChildId

## <a name="text"></a>Text

AccessibleObjectFromPoint( {0} , ) hat eine UNTERGEORDNETE ID {1} (NULL) zurückgegeben.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Die ChildId der [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Objekts, die für die angegebenen Koordinaten abgerufen wird, ist NULL.

## <a name="possible-causes"></a>Mögliche Ursachen

Die Benutzerinteraktion während der Überprüfung, z. B. das Verschieben des Fokus auf ein Nicht-Ziel-HWND, hat den Überprüfungsprozess beeinträchtigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffertests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




