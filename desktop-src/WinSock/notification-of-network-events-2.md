---
description: Eine der wichtigsten Aufgaben eines Datentransport Dienstanbieters besteht darin, dem Client Hinweise zu geben, wenn bestimmte Netzwerkereignisse aufgetreten sind.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Benachrichtigung über Netzwerkereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862548"
---
# <a name="notification-of-network-events"></a>Benachrichtigung über Netzwerkereignisse

Eine der wichtigsten Aufgaben eines Datentransport Dienstanbieters besteht darin, dem Client Hinweise zu geben, wenn bestimmte Netzwerkereignisse aufgetreten sind. Die Liste der definierten Netzwerkereignisse besteht aus den folgenden Elementen:

-   **FD \_ Connect**– eine Verbindung mit einem Remote Host oder einer Multicast Sitzung wurde abgeschlossen.
-   **FD \_ Accept**– ein Remote Host stellt eine Verbindungsanforderung her.
-   **FD \_ Read**– die Netzwerkdaten sind eingetroffen und können gelesen werden.
-   **FD \_ Write**– Space steht in den Puffer des Dienstanbieters zur Verfügung, sodass jetzt zusätzliche Daten gesendet werden können.
-   **FD \_ OOB**– out-of-Band-Daten sind zum Lesen verfügbar.
-   **FD \_ Close**– der Remote Host hat die Verbindung geschlossen.
-   **FD \_ QoS**– bei ausgehandelten QoS-Ebenen ist eine Änderung aufgetreten.
-   **FD \_ Gruppen- \_ QoS**– reserviert.
-   **FD \_ Routing \_ Schnittstellen \_ Änderung**– eine lokale Schnittstelle, die verwendet werden soll, um das in der " **SIO \_ Routing \_ Interface \_ Change ioctl** " angegebene Ziel zu erreichen, hat sich geändert.
-   **FD \_ Adress \_ Listen \_ Änderung**– die Liste der lokalen Adressen, an die die Anwendung gebunden werden kann, wurde geändert.

Der oben aufgeführte Satz von Netzwerk Ereignissen wird mitunter als **FD \_ xxx** -Ereignisse bezeichnet. Je nachdem, wie der Client eine Benachrichtigung anfordert, kann ein oder mehrere dieser Netzwerkereignisse auf verschiedene Weise angegeben werden.

 

 



