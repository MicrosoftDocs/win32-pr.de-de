---
title: Inkonsistentstate, inkonsistentproperties
description: Inkonsistentstate, inkonsistentproperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708729"
---
# <a name="inconsistentstate-inconsistentproperties"></a>Inkonsistentstate, inkonsistentproperties

## <a name="text"></a>Text

Ein Steuerelement weist Zustände/Eigenschaften auf, {0} die inkonsistent sind. {1}

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element meldet inkonsistente oder widersprüchliche MSAA-Zustände oder Benutzeroberflächenautomatisierungs-Eigenschaften. Wenn z. b. die [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) -Methode eine der folgenden Kombinationen zurückgibt.

-   Zustands \_ System \_ erweitert und Zustands \_ System \_ reduziert
-   Status \_ System \_ ausgewählt und nicht Zustands \_ System \_ auswählbar
-   Zustands \_ System \_ fokussiert und nicht Zustands \_ fähig \_

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da dem Benutzer ein falscher Element Zustand gemeldet werden könnte.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das-Element oder das übergeordnete Element ist ein MSAA-Zustand unpassend festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get- \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Objekt Zustands Konstanten**](object-state-constants.md)
</dt> <dt>

[Zustände und Eigenschaften](uiauto-msaa.md)
</dt> </dl>

 

 




