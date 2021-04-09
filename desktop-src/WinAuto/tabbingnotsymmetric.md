---
title: Tabbingnotsymmetric
description: Tabbingnotsymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101875"
---
# <a name="tabbingnotsymmetric"></a>Tabbingnotsymmetric

## <a name="text"></a>Text

Ein rückwärts-und vorwärts-Tabstopps ergibt nicht dasselbe Element. Erwartet, {0} aber empfangen {1}

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Bei Verwendung der Standardtastatur Navigation (Tab oder UMSCHALT + TAB) ist es nicht möglich, den Pfad des Durchlaufs durch die Elementstruktur des Überprüfungs Ziels zu wiederholen, wenn die Richtung des Durchlaufs umgekehrt ist. Beispielsweise führt das x-fache der Tabulator Taste (Tabulator x) von Element a (0) zu Element a (x) und die anschließende Tab-Taste (UMSCHALT + TAB) x mal dazu, dass Element a (0) den Fokus durch einen anderen Satz von zwischen Elementen wiedererlangt.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da das Durchlaufen von Elementen unberechenbar und unvorhersehbar

## <a name="possible-causes"></a>Mögliche Ursachen

-   Mehrere Elemente oder ihre übergeordneten Elemente sind benutzerdefinierte Steuerelemente, die die Tabstopps nicht ordnungsgemäß implementieren. Beispielsweise ist die Eigenschaft MSAA State nicht ordnungsgemäß festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 