---
description: Bei Verwendung mehrerer Viewports bestimmt der Treffertest, welche Viewports von der Benutzereingabe betroffen sind, indem die Bildschirmposition eines Kontakts verwendet und bestimmt wird, welches Viewportrechteck der Kontakt erreicht.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Verwenden mehrerer Viewports in DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: e422d99d8a71fbf24af5fc60641da7ac808b54215c56e5d81b8c222226ef8452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787520"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Verwenden mehrerer Viewports in DirectManipulation

Bei Verwendung mehrerer Viewports bestimmt *der Treffertest,* welche Viewports von der Benutzereingabe betroffen sind, indem die Bildschirmposition eines Kontakts verwendet und bestimmt wird, welches Viewportrechteck der Kontakt erreicht.

Ein häufiges Szenario bei [der direkten Bearbeitung](direct-manipulation-portal.md) besteht darin, einen Viewport in einem anderen zu platzieren, der auch als *Schachtelung von Viewports* bezeichnet wird. Wenn der Kontakt mehrere Viewports erreicht, bestimmt die Reihenfolge der  [**SetContact-Aufrufe**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) durch [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) des Fensters die Über-/Unterordnungsbeziehung der geschachtelten Viewports.

Regel: Das untergeordnete Element sollte [**SetContact aufrufen,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)bevor es das übergeordnete Element aufruft.

![Diagramm der Treffertests](images/dm-art-8.png)

Ein Kontakt wird in einem Viewport angezeigt. [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) sollte zuerst auf dem orangefarbenen (untergeordneten) Viewport und dann auf dem grünen (übergeordneten) Viewport aufgerufen werden, um die richtige Hierarchie einzurichten.

## <a name="targeting-the-correct-viewport"></a>Anzielen des richtigen Viewports

Ein Kontakt kann einer beliebigen Anzahl von Viewports zugeordnet werden, und jeder Kontakt kann einer anderen Gruppe von Viewports zugewiesen werden.

Jeder Viewport kann so konfiguriert werden, dass bei Bedarf bestimmte Interaktionen unterstützt werden.

Basierend auf diesen Einstellungen identifiziert [die direkte Bearbeitung,](direct-manipulation-portal.md) welcher Viewport die Eingabe verarbeitet. Der untergeordnete Viewport in der Treffertesthierarchie hat die erste Möglichkeit, die Eingabe zu verarbeiten. Die Verkettung und übergeordnete Heraufstufung kann jedoch ändern, welcher Viewport die Eingabe verarbeitet.

## <a name="chaining"></a>Verketten

Wenn das Ende des Inhalts während einer Bearbeitung erreicht wird, wendet [die direkte Bearbeitung](direct-manipulation-portal.md) einen Begrenzungseffekt an, um anzugeben, dass der Inhalt nicht weiter gehen kann. Wenn jedoch ein untergeordneter Viewport mit einem übergeordneten Viewport *verkettet* ist, wird dieser Effekt unterdrückt. Stattdessen verarbeitet der nächstgelegene Übergeordnete Viewport in der Treffertesthierarchie, der die Bearbeitung unterstützt, die Eingabe. Wenn die Bearbeitungsrichtung umgekehrt wird, sodass der Vorgänger an den Punkt zurückkehrt, an dem die Verkettung ausgelöst wurde, werden die Manipulationen "entkettet" und die Steuerung wieder an den untergeordneten Viewport übertragen.

![Diagramm der verketteten Manipulation](images/dm-art-9.png)

Wenn der Benutzer den untergeordneten Viewport bis zum Rand des Inhalts schwenkt, "verkettet" die Bearbeitung an den übergeordneten Viewport, und der Benutzer beginnt stattdessen mit dem Schwenken des übergeordneten Inhalts.

> [!Note]  
> Die X- und Y-Achsen verketten sich unabhängig voneinander. Wenn also ein diagonaler Schwenk die x-Grenze vor der y-Grenze erreicht, verschiebt die Bearbeitung das übergeordnete Element in x-Richtung, während das untergeordnete Element weiterhin in die y-Richtung verschoben wird. Um die Verkettung zu aktivieren oder zu deaktivieren, rufen Sie die [**SetChaining-API**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) auf dem untergeordneten Viewport auf.

### <a name="rails"></a>Schienen

Die Angabe von Schienen in der Konfiguration eines Viewports wirkt sich auf die Art und Weise aus, wie Eingaben vom Viewport verkettet werden. Insbesondere kann die Eingabe nicht von einem geschienenen untergeordneten Viewport mit dem übergeordneten Element im "ungeschien" Schwenkmodus von Schienen verkettet werden. Um eingaben zu verketten, wenn Schienen festgelegt sind, muss der Benutzer vertikal oder horizontal schwenkt und an die Schienen gebunden sein.

### <a name="zooming"></a>Zoomen

Wenn ein untergeordneter Viewport innerhalb eines übergeordneten Elements geschachtelt ist und beide für zoom konfiguriert sind, kann eine Zoombearbeitung von untergeordnetem zum übergeordneten Element verkettet werden. Wenn die Bearbeitung jedoch fortgesetzt wird, funktioniert sie nur für das übergeordnete Element und kann die "Entketteung" zum untergeordneten Element nicht aufheben. Wenn der Benutzer einen Zoom vom untergeordneten zum übergeordneten Element verkettet, hält [Direct Manipulation](direct-manipulation-portal.md) das untergeordnete Element an, bis alle Kontakte, die der Bearbeitung zugeordnet sind, vom Bildschirm entfernt werden. An diesem Punkt wird das untergeordnete Element von der Unterbrechung freigegeben, und der Benutzer kann den untergeordneten Viewport schwenken.

## <a name="gesture-targeting-parent-promotion"></a>Ausrichtung auf Gesten: Übergeordnete Heraufstufung

*Die Ausrichtung auf Gesten* ist der Prozess, mit dem [Direkte Bearbeitungsgruppen](direct-manipulation-portal.md) kontaktet und bestimmt, welcher Viewport die Eingabe verarbeitet. *Übergeordnete Heraufstufung* bezieht sich auf Fälle, in denen die Eingabe vom untergeordneten Element zum übergeordneten Element übertragen wird. Wenn ein Benutzer z. B. zwei Kontakte in einen untergeordneten Viewport einrückt, der nur für das Scrollen konfiguriert ist, wird die Eingabe auf das übergeordnete Element heraufgestuft, sodass das Zoomen erfolgt. Die übergeordnete Heraufstufung erfolgt unabhängig davon, ob die Verkettung für den untergeordneten Viewport aktiviert ist.

Im Gegensatz zur Verkettung wird die übergeordnete Heraufstufung nicht umgekehrt. Der übergeordnete Viewport verarbeitet die Interaktionseingabe so lange, bis alle Kontakte entfernt werden (untergeordnete Viewports beenden die Verarbeitung der Eingabe).
