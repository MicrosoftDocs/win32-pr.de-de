---
title: Abbrechen eines asynchronen Aufrufs
description: Ein Client kann einen asynchronen Aufruf abbrechen, der ausgeführt wird, wenn das Aufrufobjekt die ICancelMethodCalls-Schnittstelle implementiert.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d2751400d631c62c19f68f2cab841c0845b432df676abe60befed1f231e103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737114"
---
# <a name="canceling-an-asynchronous-call"></a>Abbrechen eines asynchronen Aufrufs

Ein Client kann einen asynchronen Aufruf abbrechen, der ausgeführt wird, wenn das Aufrufobjekt die [**ICancelMethodCalls-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) implementiert. Für Objekte, die standardmäßiges Marshalling verwenden, **ist ICancelMethodCalls** immer für gemarshallte Aufrufe verfügbar. Für Objekte, die benutzerdefiniertes Marshalling verwenden, oder für Aufrufe von Serverobjekten innerhalb desselben Apartments ist diese Funktionalität nur verfügbar, wenn das Aufrufobjekt **ICancelMethodCalls implementiert.**

Der Client kann den Aufruf jederzeit abbrechen, vom Aufruf der Begin-Methode \_ bis zur Rückgabe der \_ Finish-Methode. Wenn der Client den Aufruf vor dem Aufruf der Finish-Methode abbricht, muss er die Finish-Methode aufrufen, um den Zustand des \_ \_ Aufrufobjekts zu bereinigt. Bis der Client dies getan hat, geben alle Aufrufe einer Begin-Methode für das Aufrufobjekt \_ RPC E CALL PENDING \_ \_ \_ zurück.

**So brechen Sie einen asynchronen Aufruf ab**

1.  Fragen Sie das Aufrufobjekt für [**ICancelMethodCalls ab.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls)

2.  Rufen [**Sie ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)auf, und rufen Sie dann [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um den Zeiger frei zu geben, der durch den [**QueryInterface-Aufruf**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) in Schritt 1 erhalten wurde.

3.  Wenn der Client die Finish-Methode noch nicht \_ aufgerufen hat, rufen Sie sie jetzt auf.

Es gibt keine Garantie, dass der Server die Ausführung des Aufrufs tatsächlich beendet hat. Wenn die weitere Arbeit des Clients von einem Serverstatus abhängt, den der Aufruf möglicherweise geändert hat, sollte der Client diesen Zustand ermitteln, bevor er fortfahren kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausführen eines asynchronen Aufrufs](making-an-asynchronous-call.md)
</dt> </dl>

 

 