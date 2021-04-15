---
description: Wenn Sie mehrere Viewports verwenden, bestimmt Treffer testing, welche Viewports von der Benutzereingabe betroffen sind, indem die Bildschirmposition eines Kontakts übernommen wird und festgelegt wird, auf welches viewportrechteck der Kontakt trifft.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Verwenden mehrerer Viewports in directmanipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 627a97a7c9563ca0af9decf79b18340343dda345
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104562590"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Verwenden mehrerer Viewports in directmanipulation

Bei Verwendung mehrerer Viewports bestimmt der *Treffer Test*, welche Viewports von der Benutzereingabe betroffen sind, indem die Bildschirmposition eines Kontakts übernommen wird und festgelegt wird, welches viewportrechteck der Kontakt trifft.

Ein häufiges Szenario bei [direkter Bearbeitung](direct-manipulation-portal.md) besteht darin, einen Viewport in einen anderen anzuzeigen, der auch als Schachtelung von *Viewports* bezeichnet wird. Wenn der Kontakt mehr als einen Viewport erreicht, bestimmt die Reihenfolge von  [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) -aufrufen durch den [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) des Fensters die über-/Unterordnungsbeziehung der Kartenviewports.

Rule: das untergeordnete Element muss [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)aufrufen, bevor das übergeordnete Element aufgerufen wird.

![Diagramm mit der Hierarchie von Treffer Tests](images/dm-art-8.png)

Ein Kontakt wird in einem Viewport angezeigt. [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) sollte zuerst für den orangefarbenen (untergeordneten) Viewport und dann den grünen (übergeordneten) Viewport aufgerufen werden, um die richtige Hierarchie einzurichten.

## <a name="targeting-the-correct-viewport"></a>Ziel des richtigen Viewports

Ein Kontakt kann einer beliebigen Anzahl von Viewports zugeordnet werden, und jeder Kontakt kann einem anderen Satz von Viewports zugewiesen werden.

Jeder Viewport kann so konfiguriert werden, dass er nach Bedarf bestimmte Interaktionen unterstützt.

Basierend auf diesen Einstellungen identifiziert die [direkte Bearbeitung](direct-manipulation-portal.md) , welcher Viewport die Eingabe behandelt. Der untergeordnete-Viewport in der Treffer Test Hierarchie hat die erste Möglichkeit, die Eingabe zu verarbeiten. Die Verkettung und die übergeordnete herauf Stufung können jedoch ändern, welcher Viewport die Eingabe behandelt.

## <a name="chaining"></a>Verketten

Wenn das Ende des Inhalts während einer Bearbeitung erreicht wird, wendet die [direkte Manipulation](direct-manipulation-portal.md) einen Begrenzungs Effekt an, um anzugeben, dass der Inhalt nicht mehr fortfahren kann. Wenn jedoch ein untergeordneter Viewport mit einem übergeordneten Viewport *verkettet* ist, wird dieser Effekt unterdrückt. Stattdessen verarbeitet der nächste übergeordnete Viewport in der Treffer Test Hierarchie, die die Bearbeitung unterstützt, die Eingabe. Wenn die Bearbeitungsrichtung umgekehrt wird, sodass der Vorgänger zu dem Punkt zurückkehrt, an dem die Verkettung ausgelöst wurde, wird die Manipulation "Unchain" und die Steuerung an den untergeordneten Viewport zurückgegeben.

![Diagramm mit verketteter Bearbeitung](images/dm-art-9.png)

Wenn der Benutzer den untergeordneten Viewport bis zum Rand des Inhalts anbricht, wird die Bearbeitung an den übergeordneten Viewport durchlaufen, und der Benutzer beginnt, stattdessen den übergeordneten Inhalt zu schwenken.

> [!Note]  
> Die x-und Y-Achsen Kette unabhängig voneinander. Wenn also eine diagonal-Pan die x-Grenze vor der Y-Grenze erreicht, verschiebt die Manipulation das übergeordnete Element in der x-Richtung, während das untergeordnete Element in Y-Richtung verschoben wird. Um die Verkettung zu aktivieren oder zu deaktivieren, müssen Sie die [**setchaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) -API für den untergeordneten Viewport aufrufen.

### <a name="rails"></a>Ränge

Das Angeben von Rails in der Konfiguration eines Viewports wirkt sich darauf aus, wie Eingaben vom Viewport verkettet werden. Vor allem kann die Eingabe nicht von einem Raten untergeordneten Viewport zu dem übergeordneten Viewport in den "unraelten" Schwenk Modus von Schienen verkettet werden. Zum Verketten von Eingaben, wenn Rails festgelegt ist, muss der Benutzer vertikal oder horizontal schwenken und auf die Schienen gesperrt sein.

### <a name="zooming"></a>Zoomen

Wenn ein untergeordneter Viewport in einem übergeordneten Viewport geschachtelt ist und beide für Zoom konfiguriert sind, kann eine Zoom Bearbeitung vom untergeordneten zum übergeordneten Element verkettet werden. Wenn die Manipulation jedoch fortgesetzt wird, funktioniert Sie nur für das übergeordnete Element und kann nicht mit dem untergeordneten Element verkettet werden. Wenn der Benutzer einen Zoom vom untergeordneten zum übergeordneten Element verkettet, hält die [direkte Bearbeitung](direct-manipulation-portal.md) das untergeordnete Element an, bis alle der Manipulation zugeordneten Kontakte vom Bildschirm entfernt werden. An diesem Punkt wird das untergeordnete Element von der Unterbrechung freigegeben, und der Benutzer kann den untergeordneten Viewport schwenken.

## <a name="gesture-targeting-parent-promotion"></a>Gesten Ausrichtung: übergeordnete herauf Stufung

Die *Gesten Ausrichtung* ist der Prozess, mit dem [direkte Manipulation](direct-manipulation-portal.md) Kontakte gruppiert und bestimmt, welcher Viewport die Eingabe verarbeitet. Über *geordnete* herauf Stufung bezieht sich auf Fälle, in denen die Eingabe vom untergeordneten zum übergeordneten Element übertragen wird. Wenn ein Benutzer beispielsweise zwei Kontakte einfügt und innerhalb eines untergeordneten Viewports pingt, der nur für den Bildlauf konfiguriert ist, wird die Eingabe auf das übergeordnete Element herauf gestuft, sodass das Zoomen erfolgt. Die übergeordnete herauf Stufung erfolgt unabhängig davon, ob die Verkettung für den untergeordneten Viewport aktiviert ist.

Anders als bei der Verkettung wird die übergeordnete herauf Stufung nicht umgekehrt. Der übergeordnete Viewport verarbeitet die Interaktions Eingabe fort, bis alle Kontakte angehoben wurden (untergeordnete Viewports werden die Verarbeitung der Eingabe beendet).
