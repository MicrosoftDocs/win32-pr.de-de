---
title: Elementisorphaned
description: Elementisorphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337618"
---
# <a name="elementisorphaned"></a>Elementisorphaned

## <a name="text"></a>Text

Das Element ist ein verwaister IAccessible in der Struktur.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Die Adresse der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle des Objekts, die für die angegebenen Koordinaten abgerufen wurde, ist ein Verweis auf ein verwaistes Element in der Elementstruktur.

Dieses Problem ist ein Problem für Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, da Elemente als unsichtbar behandelt werden und dem Benutzer nicht angekündigt werden.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffer Tests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




