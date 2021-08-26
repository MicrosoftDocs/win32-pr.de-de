---
title: Schutz vor Reentrancy in Hookfunktionen
description: Während eine Hookfunktion ein Ereignis verarbeitet, können zusätzliche Ereignisse ausgelöst werden. Dies kann dazu führen, dass die Hookfunktion erneut ausgelöst wird, bevor die Verarbeitung für das ursprüngliche Ereignis abgeschlossen ist.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089ac7212823bc64d6c59cdae3d333e96760dfbc25c899cea80071bb39799c17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030750"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Schutz vor Reentrancy in Hookfunktionen

Während eine Hookfunktion ein Ereignis verarbeitet, können zusätzliche Ereignisse ausgelöst werden. Dies kann dazu führen, dass die Hookfunktion erneut ausgelöst wird, bevor die Verarbeitung für das ursprüngliche Ereignis abgeschlossen ist. Das Problem bei der Reentrancy in Hookfunktionen besteht im Out-of-Sequence-Abschluss von Ereignissen, es sei denn, die Hookfunktion behandelt diese Situation.

Stellen Sie sich beispielsweise einen Fall vor, in dem eine Hookfunktion in einem Sprachausgabeprogramm das [**EVENT \_ OBJECT \_ VALUECHANGE-Ereignis**](event-constants.md) für ein Bearbeitungssteuerobjekt verarbeitet. Wenn die Hookfunktion während der Verarbeitung des ersten Wertänderungsereignis erneut einineriert wird, um ein nachfolgendes Wertänderungsereignis zu verarbeiten, wird das zweite Ereignis vor dem ersten Ereignis abgeschlossen. Diese Situation führt dazu, dass die Sprachausgabe dem Benutzer ungenaue Informationen übermittelt.

Da die Ereignisverarbeitung unterbrochen wird, können jedes Mal zusätzliche Ereignisse empfangen werden, wenn die Hookfunktion eine Funktion aufruft, die bewirkt, dass die Nachrichtenwarteschlange des besitzenden Threads überprüft wird. Dies geschieht, wenn eine der folgenden Funktionen innerhalb der Hookfunktion aufgerufen wird:

-   Die Windows [**SendMessage-,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) [**GetMessage-,**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage-,**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) [**DialogBox-**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)oder [**MessageBox-Funktion**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   Die Microsoft Active Accessibility [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromWindow,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Eine [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder eine Component Object Model(COM)-Eigenschaft oder -Methode, die Prozessgrenzen überschreitet

Da Hookfunktionen Eigenschaften und Methoden [**von AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) und [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aufrufen, ist es nicht möglich, den Rückstieg zu verhindern. Die einzige Lösung besteht für Cliententwickler im Hinzufügen von Code in der Hookfunktion, der den Rückstieg erkennt, und entsprechende Maßnahmen zu ergreifen, wenn die Hookfunktion erneut eininnerst wird.

 

 