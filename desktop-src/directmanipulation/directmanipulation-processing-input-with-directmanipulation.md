---
description: Dieser Abschnitt bietet eine Übersicht über das Threadingmodell für die direkte Bearbeitung, die Verarbeitung von Fenstermeldungen durch die direkte Manipulation und die Art und Weise, wie sich der Zustand eines Viewports ändert, wenn die Eingabe Ausgabebewegungen zugeordnet wird.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Verarbeiten von Eingaben mit DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 49b72f88da8978192af402c8b810655c102395d5aad273f34340ed57e2703008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094654"
---
# <a name="processing-input-with-directmanipulation"></a>Verarbeiten von Eingaben mit DirectManipulation

Dieser Abschnitt bietet eine [](direct-manipulation-portal.md) Übersicht über das Threadingmodell für die direkte Bearbeitung, die Verarbeitung von Fenstermeldungen durch die direkte Manipulation und die Art und Weise, wie sich der Zustand eines Viewports ändert, wenn die Eingabe Ausgabebewegungen zugeordnet wird.

- [Eingabefluss](#input-flow)
- [Anmerkungen](#remarks)

[Die direkte Bearbeitung](direct-manipulation-portal.md) verwendet zwei Threads, um asynchrone Vorgänge zu koordinieren:

*UI-Thread:* Der Thread, der das der Eingabe **zugeordnete HWND** besitzt. Dieser Thread besitzt die Initialisierung der direkten [Bearbeitung.](direct-manipulation-portal.md) Die Verarbeitung von Maus- und Tastatureingaben erfolgt auch im UI-Thread.

*Delegatthread:* Der Thread, der erstellt wurde und sich im Besitz [der direkten Bearbeitung befindet.](direct-manipulation-portal.md) Die Toucheingabeverarbeitung erfolgt im Delegatthread.

## <a name="input-flow"></a>Eingabefluss

In einer typischen Konfiguration, bei der Treffertests für den UI-Thread durchgeführt werden, werden Fenstermeldungen von der direkten [Bearbeitung](direct-manipulation-portal.md) in der folgenden Reihenfolge verarbeitet:

![Diagramm, das die Reihenfolge zeigt, in der Nachrichten verarbeitet werden.](images/inputprocessing.png)

Für einen ruhenden Viewport:

1. Eine Reihe von Fenstermeldungen erreicht den Delegatthread.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) und [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) werden vom Delegatthread an den IHT-Thread (Independent Hit Test) gesendet.
3. Wenn [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) aus dem IHT-Thread aufgerufen wird, werden Nachrichten möglicherweise vom Delegatthread an den UI-Thread gesendet, abhängig vom Wert von [**DIRECTMANIPULATION \_ HITTEST \_ TYPE**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) beim Aufrufen von [**RegisterHitTestTarget.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)
4. Wenn [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) nicht aus dem IHT-Thread aufgerufen wird, werden Nachrichten immer vom Delegatthread an den UI-Thread gesendet.
5. Der Client kann [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) über den UI-Thread aufrufen, damit [die direkte Bearbeitung](direct-manipulation-portal.md) eine Manipulation erkennen kann.
6. Wenn eine Manipulation erkannt wird, sendet die direkte [Manipulation](direct-manipulation-portal.md) eine [WM/_POINTERCAPTURECHANGED-Nachricht,](../inputmsg/wm-pointercapturechanged.md) um den Client darüber zu informieren, dass die Eingabe von der direkten Bearbeitung verarbeitet wird. Der Viewportstatus ist auf **RUNNING festgelegt,** und die Ausgabetransformation wird aktualisiert.
7. Wenn eine andere Interaktion als eine Manipulation erkannt wird, sendet [die direkte Bearbeitung](direct-manipulation-portal.md) verbleibende Nachrichten an den UI-Thread.

Bei einem Viewport in Bewegung (mit dem Status RUNNING oder INERTIA) [](direct-manipulation-portal.md) erreicht die Fenstermeldung zuerst den Delegatthread, bei dem die direkte Manipulation Treffertests für alle ausgeführten Viewports durchträgt. Die direkte Manipulation weist den Kontakt automatisch den entsprechenden Viewports zu, die durch Treffertests identifiziert werden. Der Viewportstatus ist RUNNING, und die Ausgabetransformation wird aktualisiert.

In einigen Fällen ist ein Thread der Anwendungsbenutzeroberfläche möglicherweise zu langsam, um auf Treffertests zu reagieren. Ein Treffertestthread kann verwendet werden ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)), damit der Client [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) und [DM/_POINTERHITTEST-Nachrichten in](../inputmsg/dm-pointerhittest.md) einen bestimmten Thread verschieben kann, um Treffertests zu ermöglichen.

## <a name="remarks"></a>Hinweise

In der Regel sendet [die direkte Manipulation](direct-manipulation-portal.md) nur [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) und [DM/_POINTERHITTEST-Nachrichten](../inputmsg/dm-pointerhittest.md) an den UI-Thread, wobei spätere Nachrichten zurückbehalten werden, während auf eine Antwort vom Client gewartet wird. Wenn der Client [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)aufruft, empfängt der UI-Thread beim Erkennen einer Manipulation nur [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) und [DM/_POINTERHITTEST-](../inputmsg/dm-pointerhittest.md)und [WM/_POINTERCAPTURECHANGED-Nachricht.](../inputmsg/wm-pointercapturechanged.md)

Der Client kann [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) bei der Verarbeitung von [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) und [DM/_POINTERHITTEST-Nachrichten nicht](../inputmsg/dm-pointerhittest.md) aufrufen. In diesem Fall sendet [die direkte Bearbeitung](direct-manipulation-portal.md) alle Nachrichten an den UI-Thread, ohne die Nachrichten zu analysieren, um zu prüfen, ob eine Bearbeitung vor liegt. Der Client kann dann einen beliebigen Punkt zum Aufrufen von **SetContact** auswählen und die direkte Bearbeitung damit beginnen lassen, Manipulationen zu erkennen und [WM/_POINTERCAPTURECHANGED-Nachrichten](../inputmsg/wm-pointercapturechanged.md) zu senden, wenn eine solche erkannt wird.

**Windows 10 und höher:** Sie können entscheiden, welche Manipulationen Sie behandeln möchten, indem Sie [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) aufrufen, bevor [**Sie SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) für eine [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) oder [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) aufrufen. **DeferContact stellt** sicher, dass alle nachfolgenden Nachrichten für den angegebenen Zeitraum an den UI-Thread gesendet werden.
