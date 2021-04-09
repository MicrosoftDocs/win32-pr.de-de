---
title: Verbindungen mit einem virtuellen privaten Netzwerk
description: Der RAS-Dienst (RAS) unterstützt neben herkömmlichen RAS-Verbindungen auch VPN-Verbindungen (Virtual Private Network), die Point-to-Point-Protokoll (PPP) verwenden.
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f5fc0b80a6eb00e7587e941eea39c056a11d14
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039104"
---
# <a name="virtual-private-network-connections"></a>Verbindungen mit einem virtuellen privaten Netzwerk

Der RAS-Dienst (RAS) unterstützt neben herkömmlichen RAS-Verbindungen auch VPN-Verbindungen (Virtual Private Network), die Point-to-Point-Protokoll (PPP) verwenden. In einer VPN-Verbindung werden die VPN-Pakete in IP-Paketen gekapselt und über ein IP-Netzwerk, z. b. das Internet, gesendet. Daher ist der Zugriff auf ein IP-Netzwerk erforderlich, um eine VPN-Verbindung herzustellen. Wenn der Client Computer über eine Always on-Verbindung mit einem IP-Netzwerk verfügt, z. b. eine Verbindung mit einem IP-LAN, kann der Client die VPN-Verbindung mithilfe eines einzelnen Aufrufes der Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " herstellen.

Wenn der Client Computer nicht über eine Always on-Verbindung mit einem IP-Netzwerk verfügt, sind zwei Aufrufe von " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " erforderlich, um die VPN-Verbindung herzustellen. Der erste-Befehl richtet eine DFÜ-Verbindung zum IP-Netzwerk ein. mit dem zweiten-Rückruf wird die VPN-Verbindung hergestellt.

Der **szlocalphonenumber** -Member der [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) -Struktur für die VPN-Verbindung muss entweder den DNS-Namen oder die IP-Adresse des VPN-Zielservers enthalten.

Jede Verbindung erfordert einen separaten [Telefonbuch](ras-phone-books.md) Eintrag. Der erste Aufrufs von " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " gibt den Telefonbucheintrag für das IP-Netzwerk an. Der zweite Anruf gibt den Telefonbucheintrag für das VPN an.

Die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " übernimmt einen Zeiger auf eine " [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) "-Struktur als Parameter. Diese Struktur gibt die Anmelde Informationen für die Authentifizierung an, die für das durch den Telefonbucheintrag angegebene Netzwerk verwendet werden sollen. Die für den Zugriff auf das IP-Netzwerk erforderlichen Anmelde Informationen unterscheiden sich in der Regel von denen für das VPN. Beim ersten Aufrufe von " **rasdial** " sollten Anmelde Informationen für das IP-Netzwerk angegeben werden. Der zweite-Befehl sollte Anmelde Informationen für das VPN angeben.

Wenn die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " erfolgreich ist, gibt Sie ein Handle für die Verbindung zurück. Verwenden Sie dieses Handle in einem aufzurufenden [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) -Befehl, um die Verbindung zu beenden.

Im vorangehenden Szenario geben die beiden Aufrufe von [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) separate Verbindungs Handles für das IP-Netzwerk und das VPN zurück. Wenn Sie [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) mit dem Handle für die VPN-Verbindung aufrufen, wird die VPN-Verbindung beendet, die Verbindung mit dem IP-Netzwerk bleibt jedoch erhalten.

 

 