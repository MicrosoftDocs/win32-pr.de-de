---
description: Eine der wichtigsten Aufgaben eines Datentransport-Dienstanbieters besteht in der Bereitstellung von Hinweisen für den Client, wenn bestimmte Netzwerkereignisse aufgetreten sind.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Benachrichtigung über Netzwerkereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6fb24f746cbb03860bbd28c1028d92d7865a29c44baedaf2c227cb48536cd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794760"
---
# <a name="notification-of-network-events"></a>Benachrichtigung über Netzwerkereignisse

Eine der wichtigsten Aufgaben eines Datentransport-Dienstanbieters besteht in der Bereitstellung von Hinweisen für den Client, wenn bestimmte Netzwerkereignisse aufgetreten sind. Die Liste der definierten Netzwerkereignisse umfasst Folgendes:

-   **FD \_ CONNECT:** Eine Verbindung mit einem Remotehost oder einer Multicastsitzung wurde abgeschlossen.
-   **FD \_ ACCEPT:** Ein Remotehost nimmt eine Verbindungsanforderung vor.
-   **FD \_ READ:** Netzwerkdaten sind eingetroffen, die gelesen werden können.
-   **FD \_ WRITE:** In den Puffern des Dienstanbieters ist Speicherplatz verfügbar, sodass jetzt zusätzliche Daten gesendet werden können.
-   **FD \_ OOB:** Out-of-Band-Daten können gelesen werden.
-   **FD \_ CLOSE**: Der Remotehost hat die Verbindung geschlossen.
-   **FD \_ QOS:** Auf den ausgehandelten QoS-Ebenen ist eine Änderung aufgetreten.
-   **FD \_ GROUP \_ QOS**– Reserviert.
-   **FD \_ ROUTING \_ INTERFACE \_ CHANGE**: Eine lokale Schnittstelle, die verwendet werden soll, um das in **SIO ROUTING INTERFACE CHANGE \_ \_ \_ IOCTL** angegebene Ziel zu erreichen, wurde geändert.
-   **FD \_ ADDRESS \_ LIST \_ CHANGE**: Die Liste der lokalen Adressen, an die die Anwendung gebunden werden kann, wurde geändert.

Die oben aufgeführten Netzwerkereignisse werden manchmal als **FD \_ XXX-Ereignisse** bezeichnet. Je nachdem, wie der Client Benachrichtigungen anfing, kann auf verschiedene Weise angegeben werden, ob ein oder mehrere dieser Netzwerkereignisse auftreten.

 

 



