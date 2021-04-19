---
description: Das TLS-Daten Satz Protokoll (Transport Layer Security) sichert Anwendungsdaten mit den Schlüsseln, die während des Handshakes erstellt werden.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: TLS-Daten Satz Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356957"
---
# <a name="tls-record-protocol"></a>TLS-Daten Satz Protokoll

Das TLS-Daten Satz Protokoll ( [*Transport Layer Security*](../secgloss/t-gly.md) ) sichert Anwendungsdaten mit den Schlüsseln, die während des [Handshakes](tls-handshake-protocol.md)erstellt werden. Das Daten Satz Protokoll ist für das Sichern von Anwendungsdaten und das Überprüfen der [*Integrität*](../secgloss/i-gly.md) und des Ursprungs zuständig. Folgendes wird verwaltet:

-   Aufteilen ausgehender Nachrichten in verwaltbare Blöcke und Wiederherstellen eingehender Nachrichten.
-   Komprimieren von ausgehenden Blöcken und das Komprimieren eingehender Blöcke (optional).
-   Anwenden eines [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (Mac) auf ausgehende Nachrichten und Überprüfen eingehender Nachrichten mit dem Mac.
-   Verschlüsseln von ausgehenden Nachrichten und entschlüsseln eingehender Nachrichten.

Wenn das Datensatz-Protokoll fertiggestellt ist, werden die ausgehenden verschlüsselten Daten für den Transport an die TCP-Schicht (Transmission Control Protocol) weitergegeben.

 

 
