---
title: Generieren von Fehlerinformationen
description: Wenn bei einem Server oder einer Anwendung beim Aufrufen über RPC ein schwerwiegender Fehler auftritt, sollte er der RPC-Laufzeit anzeigen, dass ein Fehler aufgetreten ist, und im Idealfall Informationen über den Fehler hinzufügen, um die Problembehandlung zu vereinfachen.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7eb6868dfe11318e09b30217d5410a94ce32983ce64e75521c55fc5cc060ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020910"
---
# <a name="generating-error-information"></a>Generieren von Fehlerinformationen

Wenn bei einem Server oder einer Anwendung beim Aufrufen über RPC ein schwerwiegender Fehler auftritt, sollte er der RPC-Laufzeit anzeigen, dass ein Fehler aufgetreten ist, und im Idealfall Informationen über den Fehler hinzufügen, um die Problembehandlung zu vereinfachen.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Angeben schwerwiegender Fehler bei der RPC-Laufzeit

Um einen Fehler bei der RPC-Laufzeit anzugeben, rufen Sie die [**RpcRasyncException-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) auf, während im RPC-Thread die Ausnahme aufgerufen wurde, oder [**RpcAsyncAbortCall,**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) wenn der Aufruf asynchron in einem anderen Thread verarbeitet wird. Die Rückgabe eines Fehlercodes aus der Serverroutine, z. B. der Managerroutine, ist nicht ausreichend. Gemäß der RPC-Spezifikation verfügt der Rückgabewert der Funktion unabhängig von den idl/acf-Dateieinstellungen über keine Fehlersemantik auf dem Server.

Wenn in Ihrer Komponente ein schwerwiegender Fehler auftritt, führen Sie eine Bereinigung durch, die als erforderlich angesehen wird, und rufen Sie dann die [**RpcRerklärexception-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) mit dem Fehlercode auf. Der einzige Unterschied zwischen **RpcRerklärException** und der Rückgabe eines Fehlercodes ist, dass die Out-Parameter nicht gemarshallt werden, wenn die **RpcRerklärexception** aufgerufen wird. Dies ist in der Regel ein Vorteil, da das Vermeiden nicht initialisierter out-Parameter unnötig wird.

## <a name="generating-additional-extended-error-information"></a>Generieren zusätzlicher erweiterter Fehlerinformationen

So wie die RPC-Laufzeit eine Kette von Fehlerdatensätzen erstellt, kann Ihr Server oder Ihre Anwendung der Kette eigene Datensätze hinzufügen. Dieser Ansatz hilft häufig bei der Problembehandlung. Beispielsweise kann ein Server versuchen, eine bestimmte Datei zu öffnen und einen Dateifehler nicht gefunden zu erhalten. Die einfache Rückgabe von Fehler 2 wäre nicht hilfreich, um zu bestimmen, welche Datei fehlt.

Stattdessen könnte Ihr Server die [**RpcErrorAddRecord-Funktion**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) aufrufen und im Fehlerdatensatz einen Zeichenfolgenparameter (ANSI oder Unicode) angeben, der den vollständigen Pfad der gesuchten Datei angibt. Wenn alle diese Informationen auf dem Benutzerbildschirm auf einem Remotecomputer angezeigt werden, wird die Problembehandlung trivial. Eine einfache Überprüfung, ob die Datei vorhanden ist, kann durchgeführt werden, insbesondere, da der Name des computers bereits von der RPC-Laufzeit bereitgestellt wird.

Der [**RpcErrorAddRecord-Funktionsaufruf**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) kann fehlschlagen, wenn nicht genügend Arbeitsspeicher verfügbar ist, obwohl nur wenige Bytes Heapspeicher benötigt werden. Außerdem sammeln sich von **RpcErrorAddRecord hinzugefügte** Datensätze in einem bestimmten Thread an. Die Runtime bereinigt diese Datensätze normalerweise, bevor sie Ihre Serverroutine aufruft. Wenn jedoch erweiterte Fehlerinformationen außerhalb von RPC verwendet werden, bereinigen Sie den akkumulierten erweiterten Fehler im Thread, indem Sie [**RpcErrorClearInformation aufrufen.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation)

 

 




