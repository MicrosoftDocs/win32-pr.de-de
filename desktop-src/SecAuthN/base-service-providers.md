---
description: Diese Dienstanbieter stellen die grundlegenden Smartcardfunktionen bereit.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Basisdienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07fab7f7406b4932ed5c08ab2c8743f8ebde57893aed4564f8fdf40758b5af4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883570"
---
# <a name="base-service-providers"></a>Basisdienstanbieter

Diese [*Dienstanbieter*](/windows/desktop/SecGloss/c-gly) stellen die grundlegenden [*Smartcardfunktionen*](/windows/desktop/SecGloss/s-gly) bereit. Sie können verwendet werden, um auf eine einzelne Smartcardfunktion zuzugreifen, oder ihre COM-Schnittstellen können kombiniert werden, um mehrere Funktionen innerhalb eines einzelnen Dienstanbieters bereitzustellen. Diese Dienstanbieter sind die Bausteine für die Entwicklung zusätzlicher Funktionen für andere Dienstanbieter.

Die folgenden Aufgaben können von Denkschnittstellen des Basisdienstanbieters ausgeführt werden, die vom Smartcard-SDK bereitgestellt werden.



| Aufgabe                                                                                                                   | Grundlegende Dienstanbieterschnittstellen         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Verbinden zu einer Smartcard, Implementieren von Transaktionen, Schließen von Verbindungen usw.                                         | [**ISCard**](iscard.md)                 | SCardSSP |
| Verwalten Sie eine Befehls-APDU und [*eine Antwort-APDU.*](/windows/desktop/SecGloss/r-gly)          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Fragen Sie die [*Smartcard-Datenbank ab.*](/windows/desktop/SecGloss/s-gly) | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Suchen Sie eine Smartcard oder einen Leser.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Erstellen Sie eine ISO7816-4-Befehls-APDU.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| Umschließen Sie einen Istreampuffer mit Visual Basic kompatiblen Typen.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

Das folgende Verfahren zeigt eine typische Verwendung dieser Basisdienstanbieterschnittstellen. In diesem Beispiel werden die Schnittstellen [**ISCard,**](iscard.md) [**ISCardISO7816**](iscardiso7816.md)und [**ISCardCmd**](iscardcmd.md) zum Ausführen einer Transaktion verwendet.

**So führen Sie eine Transaktion aus**

1.  Erstellen Sie eine Instanz für alle erforderlichen Basisdienstanbieterschnittstellen (z. B. [**ISCard,**](iscard.md) [**ISCardISO7816**](iscardiso7816.md)und [**ISCardCmd).**](iscardcmd.md)
2.  Verbinden mithilfe der Methoden in der [**ISCard-Schnittstelle**](iscard.md) zu einer bestimmten Smartcard.
3.  Erstellen Sie mit [**ISCardISO7816**](iscardiso7816.md) und einem [**ISCardCmd-Objekt**](iscardcmd.md) einen ISO 7816-4-Befehl, indem Sie die **ISCardISO7816-Methode** aufrufen. Der Befehl ist in **ISCardCmd** als Befehls-APDU enthalten.
4.  Durchführen einer Transaktion mit der Karte durch Aufrufen der [**ISCard-Transaktionsmethode**](iscard.md) und Übergeben des erstellten [**ISCardCmd-Objekts.**](iscardcmd.md) Wenn die Transaktion abgeschlossen ist, werden die Ergebnisse im **ISCardCmd-Antwort-APDU** gespeichert.
5.  Interpretieren Sie die [**ISCardCmd-Antwort-APDU,**](iscardcmd.md) und wiederholen Sie sie.
6.  Geben Sie alle Schnittstellen frei, wenn die Vorgänge abgeschlossen sind.

Informationen zum APDU-Befehl, der in den DLLs erstellt wurde, finden Sie unter [Erstellen eines ISO7816-4-APDU-Befehls.](building-an-iso7816-4-apdu-command.md)

 

 
