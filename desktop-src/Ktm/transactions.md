---
description: Eine Transaktion ist ein Objekt, das eine logische Arbeitseinheit definiert.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transaktionen (Kerneltransaktions-Manager)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471d2ece52d510c1a77baa59ee3af980c4e4630a17d0911fdcbe590bad78903f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913880"
---
# <a name="transactions"></a>Transaktionen

Eine Transaktion ist ein Objekt, das eine logische Arbeitseinheit definiert. Die Transaktion ist aktiv, solange ein Handle vorhanden ist, das auf die Transaktion verweist, und sie gilt als aktiv, wenn für die Transaktion noch kein Commit oder Rollback ausgeführt wurde. Wenn eine Transaktion erstellt und alle Handles für sie geschlossen wurden, bevor ein Commit oder Rollback ausgeführt wird, wird ein Rollback für die Transaktion ausgeführt.

Betrachten Sie den Fall eines Transaktionsclients im Benutzermodus, der eine Transaktion erstellt, um deren Vorgänge zu berücksichtigen, und dann Updates für einen oder mehrere Ressourcen-Manager ausführt. Folgendes passiert:

1.  Der Client ruft die [**CreateTransaction-Funktion**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) auf, um die Transaktion zu erstellen, und empfängt ein Handle für diese Transaktion als Rückgabewert.

    Die Transaktion kann von einer beliebigen Anzahl von Prozessen geöffnet oder geerbt werden. jeder Prozess ist daher an der Transaktion beteiligt. Der Fehler eines dieser Prozesse führt dazu, dass die Transaktion abgebrochen wird.

    Diese Transaktion ist möglicherweise noch nicht persistent. Nur Transaktionen, die den vorbereiteten Zustand erreicht haben, müssen bei Systemfehlern wiederhergestellt werden, wenn die Transaktion die Protokollierung mit dem Verdacht auf Abbruch verwendet.

2.  Der Client muss eine Transaktion explizit an den Ressourcen-Manager übergeben.
3.  Der Client führt alle seine Transaktionsvorgänge mit einem oder mehreren RMs aus, z. B. transaktiven Dateisystemen.
4.  Der Client ruft die [**CommitTransaction-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) auf.
5.  Der Ressourcen-Manager empfängt Benachrichtigungen von EINEM, um seine Daten vorzubereiten und zu committen.

## <a name="transactions-and-threads"></a>Transaktionen und Threads

Transaktionen sind nicht identisch mit Threads. Mehrere Threads oder Prozesse können Teil einer einzelnen Transaktion sein. Umgekehrt kann ein Thread teil von mehreren verschiedenen Transaktionen zu unterschiedlichen Zeiten sein.

## <a name="transaction-functions"></a>Transaktionsfunktionen

Die folgenden Funktionen werden mit Transaktionen verwendet.



| Funktion                                                            | BESCHREIBUNG                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Committransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Fordert an, dass für die angegebene Transaktion ein Commit ausgeführt wird.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Fordert an, dass für die angegebene Transaktion ein Commit ausgeführt wird.                                         |
| [**Createtransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Erstellt ein neues Transaktionsobjekt.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Gibt die angeforderten Informationen zur angegebenen Transaktion zurück.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Öffnet eine vorhandene Transaktion.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird. Diese Funktion gibt asynchron zurück. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Legt die Transaktionsinformationen für die angegebene Transaktion fest.                               |



 

 

 



