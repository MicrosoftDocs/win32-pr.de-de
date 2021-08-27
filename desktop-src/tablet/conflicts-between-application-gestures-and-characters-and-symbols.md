---
description: Beschreibung von Konflikten zwischen Anwendungsgesten und Zeichen und Symbolen.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Konflikte zwischen Anwendungsgesten und Zeichen und Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5819bfd7013bc39ecb622b09a1ae42816bb969ec63bf062d19597575bb958279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009020"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Konflikte zwischen Anwendungsgesten und Zeichen und Symbolen

Einige Anwendungsgesten können mit Zeichen, Kombinationen von Zeichen, Symbolen, Kombinationen von Zeichen und Symbolen oder ganzen Wörtern in einem einzelnen Strich in Konflikt stehen. Die meisten dieser Konflikte werden durch ein detailliertes Verständnis des Kontexts vermieden, in dem die Anwendungsgeste ausgeführt wird.

Um z. B. eine rechte Geste von einem Bindestrich (-) oder einem Unterstrich () zu unterscheiden, kann eine Anwendung filtern, wie nah die Geste benachbarten Zeichen, der relativen Größe im Vergleich zu Zeichen oder anderen Informationen in einem Paket \_ liegt. Die zeitliche Steuerung der Anwendungsgeste kann auch ein bestimmender Faktor bei der Entscheidung zwischen Gesten und Zeichen sein. Möglicherweise gibt es vor dem Anwenden einer Anwendungsgeste mehr Pausen als vor der Eingabe von Zeichen. Wenn ein Benutzer keine Reihe von Rückgängig- oder Rücktastengesten vor sich geht, kann es auch sein, dass nach einer Geste mehr Pausen als ein Zeichen angezeigt werden.

In den folgenden Themen werden diese Konflikte ausführlich beschrieben:

-   [Konflikte mit lateinischen Zeichen und Symbolen](conflicts-with-latin-characters-and-symbols.md)
-   [Konflikte mit East-Asian Zeichen](conflicts-with-east-asian-characters.md)

 

 



