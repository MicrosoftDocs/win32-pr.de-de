---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: Accessibleobjectfrompointreturnednot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85756504520f7d665c1cd1ba7db7c76c1ec5b12a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310127"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>Accessibleobjectfrompointreturnednot \_ S \_ OK

## <a name="text"></a>Text

Accessibleobjectfrompoint ( {0} , {1} ) wurde zurückgegeben, und es wurden {2} \_ OK erwartet.

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

[**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) hat nicht \_ wie erwartet für die angegebenen Koordinaten S OK zurückgegeben.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffer Tests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




