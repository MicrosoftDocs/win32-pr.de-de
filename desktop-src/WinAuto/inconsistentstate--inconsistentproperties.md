---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30533125c342bd80134c9eab45f14917a3b3ad04af9d969140c49502cbfd192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644840"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Text

Ein Steuerelement verfügt über inkonsistente Zustände/Eigenschaften. {0}{1}

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Ein Element gibt inkonsistente oder in Konflikt stehende MSAA-Zustände oder Benutzeroberflächenautomatisierung an. Dies ist beispielsweise der Fall, wenn [**die \_ get accState-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) eine der folgenden Kombinationen zurückgibt.

-   ZUSTANDSSYSTEM \_ \_ ERWEITERT UND \_ ZUSTANDSSYSTEM \_ REDUZIERT
-   STATE \_ SYSTEM SELECTED und nicht STATE SYSTEM \_ \_ \_ SELECTABLE
-   STATE \_ SYSTEM FOCUSED und nicht STATE SYSTEM \_ \_ \_ FOCUSABLE

Dieses Problem verursacht Probleme für Personen, die für die Navigation eine Sprachausgabe und Tastatur verwenden, da dem Benutzer möglicherweise ein falscher Elementzustand gemeldet wird.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das Element oder das übergeordnete Element ist der MSAA-Zustand nicht angemessen festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Objektzustandskonst constants**](object-state-constants.md)
</dt> <dt>

[Zustände und Eigenschaften](uiauto-msaa.md)
</dt> </dl>

 

 




