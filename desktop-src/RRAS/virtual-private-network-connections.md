---
title: Verbindungen mit virtuellen privaten Netzwerken
description: Der RAS (Remote Access Service) unterstützt VPN-Verbindungen (Virtual Private Network) zusätzlich zu herkömmlichen Remotezugriffsverbindungen, die Point-to-Point-Protokoll (VPN) verwenden.
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc532d0873a5c3cb4a50552ca267a8a88b305ad855a1588338786881b3af04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024780"
---
# <a name="virtual-private-network-connections"></a>Verbindungen mit virtuellen privaten Netzwerken

Der RAS (Remote Access Service) unterstützt VPN-Verbindungen (Virtual Private Network) zusätzlich zu herkömmlichen Remotezugriffsverbindungen, die Point-to-Point-Protokoll (VPN) verwenden. Bei einer VPN-Verbindung werden die VPN-Pakete in IP-Pakete gekapselt und über ein IP-Netzwerk wie das Internet gesendet. Daher ist der Zugriff auf ein IP-Netzwerk eine Anforderung, um eine VPN-Verbindung herzustellen. Wenn der Clientcomputer über eine Always On-Verbindung mit einem IP-Netzwerk verfügt, z. B. eine Verbindung mit einem IP-LAN, kann der Client die VPN-Verbindung mithilfe eines einzelnen Aufrufs der [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) herstellen.

Wenn der Clientcomputer keine Always On-Verbindung mit einem IP-Netzwerk hat, sind zwei Aufrufe von [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) erforderlich, um die VPN-Verbindung herzustellen. Der erste Aufruf stellt eine DFÜ-Verbindung mit dem IP-Netzwerk her. Der zweite Aufruf stellt die VPN-Verbindung her.

Das **szLocalPhoneNumber-Element** der [**RASENTRY-Struktur**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) für die VPN-Verbindung sollte entweder den DNS-Namen oder die IP-Adresse des ZIEL-VPN-Servers enthalten.

Für jede Verbindung ist ein separater [Telefonbucheintrag](ras-phone-books.md) erforderlich. Der erste Aufruf von [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) gibt den Telefonbucheintrag für das IP-Netzwerk an. Der zweite Anruf gibt den Telefonbucheintrag für das VPN an.

Die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) verwendet einen Zeiger auf eine [**RASDIALPARAMS-Struktur**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) als Parameter. Diese Struktur gibt die Authentifizierungsanmeldeinformationen an, die für das Netzwerk verwendet werden sollen, das durch den Telefonbucheintrag angegeben wird. Die für den Zugriff auf das IP-Netzwerk erforderlichen Anmeldeinformationen unterscheiden sich in der Regel von denen für das VPN. Beim ersten Aufruf von **RasDial** sollten Anmeldeinformationen für das IP-Netzwerk angegeben werden. Beim zweiten Aufruf sollten Anmeldeinformationen für das VPN angegeben werden.

Wenn die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) erfolgreich ist, gibt sie ein Handle für die Verbindung zurück. Verwenden Sie dieses Handle in einem Aufruf von [**RasHangUp,**](/windows/desktop/api/Ras/nf-ras-rashangupa) um die Verbindung zu beenden.

Im vorherigen Szenario geben die beiden Aufrufe von [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) separate Verbindungshandles für das IP-Netzwerk und das VPN zurück. Wenn [**Sie RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) mit dem Handle für die VPN-Verbindung aufrufen, wird die VPN-Verbindung beendet, die Verbindung mit dem IP-Netzwerk bleibt jedoch intakt.

 

 