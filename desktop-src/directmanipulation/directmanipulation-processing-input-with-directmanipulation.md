---
description: Dieser Abschnitt enthält eine Übersicht über das Modell der direkten Manipulations Bearbeitung, die Art und Weise, wie Fenster Meldungen durch direkte Bearbeitung verarbeitet werden und wie sich der Zustand eines Viewports ändert, wenn Eingaben Ausgabe Bewegungen zugeordnet werden.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Verarbeiten von Eingaben mit directmanipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 284a0a1866a2082e2c34c65de347b0dcdfab3a64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343553"
---
# <a name="processing-input-with-directmanipulation"></a>Verarbeiten von Eingaben mit directmanipulation

Dieser Abschnitt enthält eine Übersicht über das Modell der [direkten Manipulations](direct-manipulation-portal.md) Bearbeitung, die Art und Weise, wie Fenster Meldungen durch direkte Bearbeitung verarbeitet werden und wie sich der Zustand eines Viewports ändert, wenn Eingaben Ausgabe Bewegungen zugeordnet werden.

- [Eingabe Fluss](#input-flow)
- [Anmerkungen](#remarks)

Die [direkte Manipulation](direct-manipulation-portal.md) verwendet zwei Threads zum Koordinieren von asynchronen Vorgängen:

*UI-Thread* : der Thread, der das **HWND** besitzt, das mit Input verknüpft ist. Dieser Thread besitzt die Initialisierung der [direkten Bearbeitung](direct-manipulation-portal.md). Die Maus-und Tastatureingabe Verarbeitung erfolgt ebenfalls im UI-Thread.

*Delegatthread* -der Thread, der erstellt wurde und sich im Besitz einer [direkten Bearbeitung](direct-manipulation-portal.md)befindet Die Berührungs Eingabe Verarbeitung erfolgt im delegatenthread.

## <a name="input-flow"></a>Eingabe Fluss

In einer typischen Konfiguration, bei der Treffer Tests im UI-Thread durchgeführt werden, werden Fenster Meldungen von [direkter Bearbeitung](direct-manipulation-portal.md) in der folgenden Reihenfolge verarbeitet:

![Diagramm, das die Reihenfolge anzeigt, in der Nachrichten verarbeitet werden.](images/inputprocessing.png)

Für einen Viewport im Ruhezustand:

1. Eine Reihe von Fenster Meldungen erreichen den delegatenthread.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) -und [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) -Nachrichten werden vom delegatenthread an den IHT-Thread (Independent Hit Test) gesendet.
3. Wenn [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) vom IHT-Thread aufgerufen wird, werden Nachrichten möglicherweise vom delegatenthread an den UI-Thread gesendet, abhängig vom Wert des [**directmanipulation- \_ \_ hittesttyps**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) , wenn [**registerhittesttarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) aufgerufen wurde.
4. Wenn [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) nicht vom IHT-Thread aufgerufen wird, werden Nachrichten immer vom delegatenthread an den UI-Thread gesendet.
5. Der Client kann " [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) " aus dem UI-Thread aufrufen, damit die [direkte Manipulation](direct-manipulation-portal.md) eine Manipulation erkennen kann.
6. Wenn eine Manipulation erkannt wird, sendet die [direkte Manipulation](direct-manipulation-portal.md) eine [WM/_POINTERCAPTURECHANGED-](../inputmsg/wm-pointercapturechanged.md) Nachricht, um den Client zu benachrichtigen, dass die Eingabe von direkter Bearbeitung verarbeitet wird. Der viewportstatus wird auf "wird **ausgeführt** " festgelegt, und die Ausgabe Transformation wird aktualisiert.
7. Wenn eine andere Interaktion als eine Manipulation erkannt wird, sendet die [direkte Manipulation](direct-manipulation-portal.md) verbleibende Nachrichten an den UI-Thread.

Für einen Viewport in Bewegung (mit dem Status "wird ausgeführt" oder "Trägheit") erreicht die Fenster Meldung zuerst den delegatenthread, bei dem die [direkte Manipulation](direct-manipulation-portal.md) Tests für alle laufenden Viewports durchführt. Die direkte Bearbeitung weist den Kontakt automatisch den entsprechenden Viewports zu, die durch Treffer Tests identifiziert werden. Der viewportstatus wird ausgeführt, und die Ausgabe Transformation wird aktualisiert.

In einigen Fällen kann ein Anwendungs Benutzeroberflächen Thread zu langsam sein, um auf Treffer Tests zu reagieren. Ein Treffer Test Thread kann verwendet werden,[](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)um dem Client das Verschieben von [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) -und [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) -Nachrichten in einen bestimmten Thread zu ermöglichen, sodass Treffer Tests möglich sind.

## <a name="remarks"></a>Bemerkungen

In der Regel sendet die [direkte Manipulation](direct-manipulation-portal.md) nur die Nachrichten vom Typ " [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) " und " [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) " an den UI-Thread, wobei spätere Nachrichten beim Warten auf eine Antwort vom Client Wenn der Client [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)aufruft, empfängt der UI-Thread nur dann, wenn eine Manipulation erkannt wird, die Informationen [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) und [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)und [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

Beim Verarbeiten von [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) -und [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) -Nachrichten ruft der Client möglicherweise nicht [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) auf. In diesem Fall sendet die [direkte Manipulation](direct-manipulation-portal.md) alle Nachrichten an den UI-Thread, ohne die Nachrichten zu analysieren, um festzustellen, ob eine Bearbeitung vorliegt. Der Client kann dann einen beliebigen Punkt auswählen, um **SetContact** aufzurufen, und die direkte Bearbeitung der Erkennung von Manipulationen und das Senden von [WM/_POINTERCAPTURECHANGED Nachrichten](../inputmsg/wm-pointercapturechanged.md) Nachrichten senden, wenn ein solcher erkannt wird.

**Windows 10 und höher:** Sie können entscheiden, welche Manipulationen Sie behandeln möchten, indem Sie " [**defercontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) " aufrufen, bevor Sie " [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) " in einer [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) oder [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) -Nachricht aufrufen. **Defercontact** stellt sicher, dass alle nachfolgenden Nachrichten für den angegebenen Zeitraum an den UI-Thread gesendet werden.
