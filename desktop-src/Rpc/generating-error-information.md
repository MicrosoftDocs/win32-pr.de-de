---
title: Fehlerinformationen werden erzeugt.
description: Wenn ein Server oder eine Anwendung während des Aufrufs über RPC einen schwerwiegenden Fehler feststellt, sollte die RPC-Laufzeit angezeigt werden, dass ein Fehler aufgetreten ist. im Idealfall sollten Informationen zu dem Fehler hinzugefügt werden, um die Problembehandlung zu vereinfachen.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338987"
---
# <a name="generating-error-information"></a>Fehlerinformationen werden erzeugt.

Wenn ein Server oder eine Anwendung während des Aufrufs über RPC einen schwerwiegenden Fehler feststellt, sollte die RPC-Laufzeit angezeigt werden, dass ein Fehler aufgetreten ist. im Idealfall sollten Informationen zu dem Fehler hinzugefügt werden, um die Problembehandlung zu vereinfachen.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Angeben schwerwiegender Fehler für die RPC-Laufzeit

Um einen Fehler bei der RPC-Laufzeit anzugeben, müssen Sie die [**rpcraiseexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) -Funktion aufrufen, während der RPC-Thread, für den die Ausnahme aufgerufen wurde, oder [**rpcasyncabortcallcenter**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) aufrufen, wenn der Aufruf asynchron in einem anderen Thread verarbeitet wird. Das Zurückgeben eines Fehlercodes aus der Server Routine, z. b. der Manager-Routine, ist nicht ausreichend – entsprechend der RPC-Spezifikation hat der Rückgabewert der Funktion keine Fehler Semantik auf dem Server, unabhängig von den Einstellungen der IDL/ACF-Datei.

Wenn in der Komponente ein schwerwiegender Fehler auftritt, führen Sie alle Bereinigungs Anforderungen als notwendig aus, und wenden Sie dann die [**rpcraiseexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) -Funktion mit dem Fehlercode an. Der einzige Unterschied zwischen **rpcraiseexception** und der Rückgabe eines Fehlercodes ist, wenn die **rpcraiseexception** aufgerufen wird und die Out-Parameter nicht gemarshallt werden. Dies ist normalerweise ein Vorteil, da das vermeiden nicht initialisierter out-Parameter unnötig ist.

## <a name="generating-additional-extended-error-information"></a>Zusätzliche erweiterte Fehlerinformationen werden erzeugt.

Ebenso wie die RPC-Laufzeit eine Kette von Fehler Datensätzen erstellt, kann der Server oder die Anwendung eigene Datensätze zur Kette hinzufügen. Dieser Ansatz hilft häufig bei der Problembehandlung. Ein Server kann z. b. versuchen, eine bestimmte Datei zu öffnen und den Fehler "Datei nicht gefunden" zu erhalten. Die einfache Rückgabe von Fehler 2 wäre nicht hilfreich, um zu bestimmen, welche Datei fehlt.

Stattdessen könnte der Server die [**rpcerroraddrecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) -Funktion aufrufen und einen Zeichen folgen Parameter (ANSI oder Unicode) im Fehler Daten Satz angeben, der den vollständigen Pfad der gesuchten Datei angibt. Wenn alle diese Informationen auf dem Benutzer Bildschirm auf einem Remote Computer angezeigt werden, wird die Problembehandlung trivial. eine einfache Überprüfung, ob die Datei vorhanden ist, kann ausgeführt werden. Dies gilt insbesondere, weil der Name des fraglichen Computers bereits von der RPC-Laufzeit bereitgestellt wird.

Der [**rpcerroraddrecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) -Funktions Aufrufvorgang schlägt möglicherweise fehl, wenn nicht genügend Arbeitsspeicher verfügbar ist, auch wenn nur wenige Byte Speicherplatz erforderlich sind. Außerdem häufen sich von **rpcerroraddrecord** hinzugefügte Datensätze in einem bestimmten Thread an. Die Laufzeit bereinigt diese Datensätze normalerweise vor dem Aufrufen der Server Routine, aber wenn erweiterte Fehlerinformationen außerhalb von RPC verwendet werden, achten Sie darauf, den akkumulierten erweiterten Fehler im Thread durch Aufrufen von [**rpcerrorclearinformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation)zu bereinigen.

 

 




