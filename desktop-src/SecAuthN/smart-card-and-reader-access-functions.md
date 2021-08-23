---
description: Verbinden und kommunikation mit einer bestimmten Smartcard.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Smartcard- und Lesezugriffsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b571764ae2d31865082e823996e8cc1ecde9d9d3e2dd618f28e528fd465a567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917955"
---
# <a name="smart-card-and-reader-access-functions"></a>Smartcard- und Lesezugriffsfunktionen

Die folgenden Funktionen stellen eine Verbindung mit einer bestimmten [*Smartcard*](../secgloss/s-gly.md)her und kommunizieren mit dieser. E/A-Vorgänge auf der Karte verwenden einen Puffer zum Senden oder Empfangen von Daten und eine Struktur, die Protokollsteuerungsinformationen enthält. Die Struktur der Protokollsteuerungsinformationen beginnt immer mit einer [**SCARD \_ IO \_ REQUEST-Struktur.**](scard-io-request.md)



| Thema                                                  | BESCHREIBUNG                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Verbinden zu einer Karte.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Wiederherstellen einer Verbindung.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Beenden sie eine Verbindung.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Starten Sie eine [*Transaktion,*](../secgloss/t-gly.md)die verhindert, dass andere Anwendungen auf eine Karte zugreifen.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Beenden Sie eine Transaktion, sodass andere Anwendungen auf eine Karte zugreifen können.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Geben Sie den aktuellen Status des Readers an.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Fordert den Dienst an und empfängt Daten mithilfe der Protokolle [*T=0,*](../secgloss/t-gly.md) [*T=1*](../secgloss/t-gly.md)und raw von einer Karte. |



 

 

 
