---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf30478d7ca68f823cd3d87158f92af71ae1afb14bf8d17295eedee2b4a144d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829370"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Text

Das Element ist ein verwaistes IAccessible-Element in der Struktur.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Die Adresse der [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Objekts, die für die angegebenen Koordinaten abgerufen wird, ist ein Verweis auf ein verwaistes Element in der Elementstruktur.

Dieses Problem ist ein Problem für Personen, die sich auf eine Sprachausgabe und Tastatur für die Navigation verlassen, da Elemente als unsichtbar behandelt und dem Benutzer nicht angekündigt werden.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. B. das Verschieben des Fokus auf ein Nicht-Ziel-HWND, hat den Überprüfungsprozess beeinträchtigt.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffertests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




