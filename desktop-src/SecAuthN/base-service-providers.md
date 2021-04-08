---
description: Diese Dienstanbieter stellen die grundlegenden Smartcardfunktionen bereit.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Basis Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dfa6c190e7a09ed4dfceafb983878906e8e3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959967"
---
# <a name="base-service-providers"></a>Basis Dienstanbieter

Diese [*Dienstanbieter*](/windows/desktop/SecGloss/c-gly) stellen die grundlegenden [*Smartcardfunktionen*](/windows/desktop/SecGloss/s-gly) bereit. Sie können für den Zugriff auf eine einzelne smartcardfunktion verwendet werden, oder Ihre COM-Schnittstellen können kombiniert werden, um mehrere Funktionen in einem einzelnen Dienstanbieter bereitzustellen. Diese Dienstanbieter sind die Bausteine, mit denen Sie zusätzliche Funktionen für andere Dienstanbieter entwickeln können.

Die folgenden Aufgaben können von den Basis Dienstanbieter-Schnittstellen ausgeführt werden, die vom Smartcard SDK bereitgestellt werden.



| Aufgabe                                                                                                                   | Grundlegende Dienstanbieter Schnittstellen         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Stellen Sie eine Verbindung mit einer Smartcard her, implementieren Sie Transaktionen, schließen Sie Verbindungen, usw.                                         | [**Iscard**](iscard.md)                 | Scardssp |
| Warten Sie einen Befehl APDU und [*Reply APDU*](/windows/desktop/SecGloss/r-gly).          | [**Iscardcmd**](iscardcmd.md)           | Scardssp |
| Fragen Sie die [*Smartcard-Datenbank*](/windows/desktop/SecGloss/s-gly)ab. | [**Iscarddatabase**](iscarddatabase.md) | Scardssp |
| Suchen Sie eine Smartcard oder einen Reader.                                                                                         | [**Iscardsuche**](iscardlocate.md)     | Scardssp |
| Erstellen Sie einen ISO7816-4-Befehl APDU.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | Scardssp |
| Wrappen Sie einen IStream-Puffer mithilfe Visual Basic – kompatiblen Typs.                                                         | [**Ibytebuffer**](ibytebuffer.md)       | Scardssp |



 

Das folgende Verfahren zeigt eine typische Verwendung dieser Basis Dienstanbieter-Schnittstellen. In diesem Beispiel werden die Schnittstellen [**iscard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)und [**iscardcmd**](iscardcmd.md) verwendet, um eine Transaktion auszuführen.

**So führen Sie eine Transaktion aus**

1.  Erstellen Sie eine Instanz für alle benötigten Basis Dienstanbieter-Schnittstellen (z. b. [**iscard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)und [**iscardcmd**](iscardcmd.md)).
2.  Stellen Sie mithilfe der Methoden in der [**iscard**](iscard.md) -Schnittstelle eine Verbindung mit einer bestimmten Smartcard her.
3.  Erstellen Sie mithilfe von [**ISCardISO7816**](iscardiso7816.md) und einem [**iscardcmd**](iscardcmd.md) -Objekt einen ISO 7816-4-Befehl, indem Sie die **ISCardISO7816** -Methode aufrufen. Der Befehl ist in **iscardcmd** als Befehl APDU enthalten.
4.  Führen Sie eine Transaktion mit der Karte aus, indem Sie die [**iscard**](iscard.md) -Transaktions Methode aufrufen und das erstellte [**iscardcmd**](iscardcmd.md) -Objekt übergeben. Wenn die Transaktion abgeschlossen ist, werden die Ergebnisse im **iscardcmd** -Antwort-APDU gespeichert.
5.  Interpretieren Sie das [**iscardcmd**](iscardcmd.md) -Antwort-APDU und wiederholen Sie den Vorgang
6.  Gibt alle Schnittstellen frei, wenn Vorgänge beendet sind.

Weitere Informationen zu dem in den DLLs erstellten APDU-Befehl finden Sie unter [Erstellen eines ISO7816-4-APDU-Befehls](building-an-iso7816-4-apdu-command.md).

 

 
