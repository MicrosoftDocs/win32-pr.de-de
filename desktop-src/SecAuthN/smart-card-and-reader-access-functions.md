---
description: Stellen Sie eine Verbindung mit einer bestimmten Smartcard her und kommunizieren Sie.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Smartcard-und Reader-Zugriffs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363299"
---
# <a name="smart-card-and-reader-access-functions"></a>Smartcard-und Reader-Zugriffs Funktionen

Die folgenden Funktionen stellen eine Verbindung mit einer bestimmten [*Smartcard*](../secgloss/s-gly.md)her und kommunizieren mit Ihnen. E/a-Vorgänge für die Karte verwenden einen Puffer zum Senden oder empfangen von Daten sowie eine Struktur, die Protokoll Steuerungsinformationen enthält. Die Struktur der Protokoll Steuerungsinformationen beginnt immer mit einer " [**SCard \_ IO \_ Request**](scard-io-request.md) "-Struktur.



| Thema                                                  | BESCHREIBUNG                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scardconnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Herstellen einer Verbindung mit einer Karte                                                                                                                                                                                                                         |
| [**Scardreconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Stellen Sie eine Verbindung wieder her.                                                                                                                                                                                                                  |
| [**"Scarddisconnect"**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Beenden Sie eine Verbindung.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Starten Sie eine [*Transaktion*](../secgloss/t-gly.md), und blockieren Sie den Zugriff auf eine Karte durch andere Anwendungen.                                                                                            |
| [**"SCardEndTransaction"**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Beenden Sie eine Transaktion, sodass andere Anwendungen auf eine Karte zugreifen können.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Geben Sie den aktuellen Status des Readers an.                                                                                                                                                                                                  |
| [**Scardüberträgt**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Fordert den Dienst an und empfängt Daten mit [*t = 0*](../secgloss/t-gly.md), [*t = 1*](../secgloss/t-gly.md)und unformatierten Protokollen von einer Karte zurück. |



 

 

 
