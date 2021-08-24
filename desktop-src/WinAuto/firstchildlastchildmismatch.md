---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3f168357cd67a7f22e81e985042a4983e7d8291bb6a0e2e343753959bcd6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828952"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Text

Beim Navigieren durch Aufrufen {0} des getesteten Knotens und anschließendes wiederholtes Aufrufen von haben wir das folgende untergeordnete Element {1} abgeschlossen: {2} . Dies stimmte nicht mit dem Ergebnis des Aufrufs auf {3} dem getesteten Knoten überein, was folgende Ergebnisse lieferte: {4} . Stattdessen sollte das untergeordnete Element als übergeordnetes Element den Testknoten melden.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Beim Navigieren zwischen den untergeordneten Elementen des Elements liegt ein Problem vor. 1. Eine falsche oder ungültige Benutzeroberflächenautomatisierung Implementierung.

Dieses Problem kann zu Navigationsproblemen bei automatisierten Tools führen, da das Durchlaufen von Elementen unregelmäßig und unvorhersehbar sein kann.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige Benutzeroberflächenautomatisierung Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




