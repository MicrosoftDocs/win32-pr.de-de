---
description: Im COM+-Programmiermodell können Sie Ihre Komponenten so entwerfen, dass Sie die am besten&\# 8212, das Aktivieren von Geschäftslogik oder das Einrichten einer Datenbankverbindung&\# 8212 und das Transaktions Verarbeitungs Framework von Microsoft Windows zum Automatisieren von Transaktionen verwenden.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Verwalten von automatischen Transaktionen in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524056"
---
# <a name="managing-automatic-transactions-in-com"></a>Verwalten von automatischen Transaktionen in com+

Im COM+-Programmiermodell können Sie Ihre Komponenten so entwerfen, dass Sie Ihre Anforderungen optimal erledigen – indem Sie die Geschäftslogik aktivieren oder eine Datenbankverbindung herstellen – und sich auf das Transaktions Verarbeitungs Framework von Microsoft Windows verlassen, um Transaktionen zu automatisieren.

## <a name="starting-a-transaction"></a>Starten einer Transaktion

Com+ startet automatisch eine Transaktion, wenn eine der folgenden Bedingungen zutrifft:

-   Wenn ein nicht transaktionaler Client eine Komponente aufruft, die eine Transaktion erfordert oder eine neue Transaktion erfordert.
-   Wenn ein transaktionaler Client eine Komponente aufruft, die eine neue Transaktion erfordert.

Wenn com+ feststellt, dass ein Objekt über eine neue Transaktion verfügen soll, beginnt es zuerst mit der Transaktion und fügt dann das Objekt in das Objekt ein. Der Vorgang umfasst folgende Schritte:

1.  Com+ erstellt ein Kontext Objekt, legt sowohl die [JIT-Aktivierungs](com--just-in-time-activation.md) -als auch die- [Synchronisierungs](com--synchronization.md) Attribute auf Required fest und legt die [konsistenten und done-Flags](consistent-and-done-flags.md) auf true bzw. false fest.
2.  Com+ kommuniziert mit dem Distributed Transaction Coordinator (DTC), um eine Transaktion zu starten. Der DTC koordiniert die physische Transaktion.
3.  Der DTC generiert einen Transaktions Bezeichner und übergibt ihn an com+ zurück. Der Transaktions Bezeichner legt eine Transaktionsgrenze fest. Alle an der Transaktion beteiligten Objekte verwenden denselben Bezeichner.
4.  Wenn der Client das Objekt erstellt, aktiviert com+ ihn innerhalb der Transaktionsgrenze.

## <a name="ending-a-transaction"></a>Beenden einer Transaktion

Com+ beendet eine automatische Transaktion, indem ein Commit oder Abbruch ausgeführt wird, wenn eine der folgenden Bedingungen zutrifft:

-   Das Stamm Objekt der Transaktion schließt seine Arbeit ab, und com+ gibt es frei. Nachdem das Stamm Objekt deaktiviert wurde, versucht die Transaktion, einen Commit durchzusetzen.
-   Der Client gibt das Stamm Objekt frei. Ohne einen Verweis wird das Stamm Objekt deaktiviert, und die Transaktion versucht, einen Commit durchzusetzen.
-   Die Transaktion überschreitet den Timeout Schwellenwert. Die Transaktion wird automatisch abgebrochen, wenn nicht innerhalb des Transaktions Timeout Zeitraums ein Commit ausgeführt wird, wobei alle der Transaktion zugeordneten Objekte deaktiviert werden. Der Standardwert für das Transaktions Timeout beträgt 60 Sekunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konsistente und done-Flags](consistent-and-done-flags.md)
</dt> <dt>

[Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[Beenden einer automatischen Transaktion durch Aufrufen von SetComplete](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



