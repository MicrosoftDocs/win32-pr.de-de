---
title: Accessibleobjectfrompointreturnetdnullilaccessible
description: Accessibleobjectfrompointreturnetdnullilaccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311231"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>Accessibleobjectfrompointreturnetdnullilaccessible

## <a name="text"></a>Text

Accessibleobjectfrompoint ( {0} , {1} ) gab NULL zurück.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Die Adresse der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle des Benutzeroberflächen Elements, die für die angegebenen Koordinaten abgerufen wurde, ist NULL.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffer Tests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




