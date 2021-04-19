---
description: Eine Transaktion ist ein Objekt, das eine logische Arbeitseinheit definiert.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transaktionen (Kerneltransaktions-Manager)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350187"
---
# <a name="transactions"></a>Transaktionen

Eine Transaktion ist ein Objekt, das eine logische Arbeitseinheit definiert. Die Transaktion ist aktiv, solange ein Handle auf die Transaktion verweist, und Sie gilt als aktiv, wenn für die Transaktion noch kein Commit oder Rollback ausgeführt wurde. Wenn eine Transaktion erstellt wird und alle Handles vor einem Commit oder Rollback geschlossen wurden, wird für die Transaktion ein Rollback ausgeführt.

Stellen Sie sich vor, dass ein transaktionaler Client im Benutzermodus eine Transaktion erstellt, um deren Vorgänge zu begrenzen, und dann Updates für einen oder mehrere Ressourcen-Manager ausführt. Folgendes passiert:

1.  Der Client ruft die Funktion "up [**Transaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) " auf, um die Transaktion zu erstellen, und empfängt ein Handle für diese Transaktion als Rückgabewert.

    Die Transaktion kann von einer beliebigen Anzahl von Prozessen geöffnet oder geerbt werden. Jeder Prozess ist daher an der Transaktion beteiligt. Der Fehler bei einem dieser Prozesse bewirkt, dass die Transaktion abgebrochen wird.

    Diese Transaktion ist möglicherweise noch nicht persistent. Nur Transaktionen, die den vorbereiteten Zustand erreicht haben, müssen über Systemfehler hinweg wieder hergestellt werden, wenn die Transaktion die vermutete Abbruch Protokollierung verwendet.

2.  Der Client muss eine Transaktion explizit an den Ressourcen-Manager übergeben.
3.  Der Client führt alle Transaktions Vorgänge mit einem oder mehreren RMS aus, z. b. transaktiven Dateisystemen.
4.  Der Client ruft die [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) -Funktion auf.
5.  Der Resource Manager empfängt Benachrichtigungen von KTM, um seine Daten vorzubereiten und zu übermitteln.

## <a name="transactions-and-threads"></a>Transaktionen und Threads

Transaktionen sind nicht identisch mit Threads. Mehrere Threads oder Prozesse können Teil einer einzelnen Transaktion sein. Umgekehrt kann ein Thread zu unterschiedlichen Zeitpunkten Teil mehrerer verschiedener Transaktionen sein.

## <a name="transaction-functions"></a>Transaktionsfunktionen

Die folgenden Funktionen werden mit Transaktionen verwendet.



| Funktion                                                            | BESCHREIBUNG                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Fordert an, dass die angegebene Transaktion ein Commit ausgeführt wird.                                         |
| [**Committransaktionasync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Fordert an, dass die angegebene Transaktion ein Commit ausgeführt wird.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Erstellt ein neues Transaktions Objekt.                                                             |
| [**Gettransaktioninformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Gibt die angeforderten Informationen zur angegebenen Transaktion zurück.                            |
| [**Opentransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Öffnet eine vorhandene Transaktion.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird.                                       |
| [**Rollbacktransaktionasync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird. Diese Funktion gibt asynchron zurück. |
| [**Settransaktioninformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Legt die Transaktionsinformationen für die angegebene Transaktion fest.                               |



 

 

 



