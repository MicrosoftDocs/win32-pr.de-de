---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6bda8de3e07f0ac6be3aa3a2a7bd750508dead1f5c2662391a056b258b36d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644100"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Text

Wenn Sie rückwärts und vorwärts tabstoppen, wird dasselbe Element nicht angezeigt. Erwartet, {0} aber empfangen {1}

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Bei Verwendung der standardmäßigen Tastaturnavigation (TAB oder UMSCHALT+TAB) ist es nicht möglich, den Pfad des Durchlaufs durch die Elementstruktur des Überprüfungsziels zu wiederholen, wenn die Richtung des Durchlaufs umgekehrt wird. Wenn Sie z. B. X-Mal vorwärts (Tabulator) von Element A(0) zu Element A(x) und dann rückwärts (UMSCHALT+TAB) x mal tabbieren, erhält Element A(0) den Fokus durch eine andere Gruppe von Zwischenelementen zurück.

Dieses Problem verursacht Probleme für Personen, die sich auf eine Sprachausgabe und Tastatur für die Navigation verlassen, da Traversierungselemente unregelmäßig und unvorhersehbar erscheinen.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Mehrere Elemente oder deren über-elemente sind benutzerdefinierte Steuerelemente, die tabbing nicht ordnungsgemäß implementieren. Beispielsweise ist die MSAA State-Eigenschaft nicht ordnungsgemäß festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 