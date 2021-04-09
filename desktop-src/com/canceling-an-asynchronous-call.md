---
title: Abbrechen eines asynchronen Aufrufes
description: Ein Client kann einen asynchronen Aufruf abbrechen, der gerade ausgeführt wird, wenn das Aufruf Objekt die icancelmethodcalls-Schnittstelle implementiert.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102423"
---
# <a name="canceling-an-asynchronous-call"></a>Abbrechen eines asynchronen Aufrufes

Ein Client kann einen asynchronen Aufruf abbrechen, der gerade ausgeführt wird, wenn das Aufruf Objekt die [**icancelmethodcalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) -Schnittstelle implementiert. Bei Objekten, die Standardmäßiges Marshalling verwenden, ist **icancelmethodcalls** immer für gemarshallte Aufrufe verfügbar. Bei Objekten, die benutzerdefiniertes Marshalling oder Aufrufe von Server Objekten innerhalb desselben Apartment verwenden, ist diese Funktion nur verfügbar, wenn das Aufruf Objekt **icancelmethodcalls** implementiert.

Der Client kann den Aufruf jederzeit abbrechen, von dem Zeitpunkt, an dem die BEGIN- \_ Methode aufgerufen wird, bis die Finish- \_ Methode zurückgegeben wird. Wenn der Client den Aufruf vor dem Aufrufen der Methode "Finish" \_ abbricht, muss er die "Finish"-Methode aufrufen, \_ um den Status des Aufruf Objekts zu bereinigen. Solange der Client dies nicht erreicht hat, geben alle Aufrufe einer beliebigen BEGIN- \_ Methode für das Aufruf Objekt einen RPC- \_ E- \_ Aufruf \_ aus.

**So brechen Sie einen asynchronen-Befehl ab**

1.  Fragen Sie das Aufruf Objekt für [**icancelmethodcalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls)ab.

2.  Rufen Sie [**icancelmethodcalls:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)auf, und rufen Sie dann [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um den Zeiger freizugeben, den der [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufruf in Schritt 1 erhalten hat.

3.  Wenn der Client die "Finish"- \_ Methode nicht bereits aufgerufen hat, nennen Sie ihn jetzt.

Es gibt keine Garantie dafür, dass der Server die Ausführung des Aufrufes tatsächlich beendet hat. Wenn die weitere Arbeit des Clients von einem Serverstatus abhängig ist, den der-Rückruf möglicherweise geändert hat, sollte der Client diesen Zustand vor dem Fortfahren ermitteln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausführen eines asynchronen Aufrufes](making-an-asynchronous-call.md)
</dt> </dl>

 

 