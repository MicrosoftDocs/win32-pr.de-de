---
title: Überlegungen zur Gerätehostsicherheit
description: Die Verwendung des Gerätehosts verursacht Sicherheitsprobleme.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e8cdce90cdc5801010833db4cb97c49487c16a3926bf235f126f33e1078f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008090"
---
# <a name="device-host-security-considerations"></a>Überlegungen zur Gerätehostsicherheit

Die Verwendung des Gerätehosts verursacht aus folgendenGründen Sicherheitsprobleme:

-   Geräte, die auf einem Computer mit Windows XP gehostet werden, senden Ankündigungen an alle Netzwerke.
-   Geräte, die auf einem Computer mit Windows XP gehostet werden, ermöglichen die Steuerung von Geräten aus allen Netzwerken.

Dies erhöht das Risiko für Heimverbraucher, da Geräte wie ein Media Player, eine überbrückte Beleuchtung oder ein HVAC-System, das auf einem Computer mit Windows XP gehostet wird, sichtbar sind und von Kontrollpunkten außerhalb des Heims gesteuert werden können.

Wenn Sie ein gehostetes Gerät erstellen, müssen Sie einige Sicherheitsprobleme berücksichtigen.

-   Um den Ermittlungs- und Angriffsbereich von UPnP-basierten Geräten zu reduzieren, beträgt die Tl aller SSDP-Nachrichten 1. Dies bedeutet, dass ein registriertes Gerät nur von Kontrollpunkten im gleichen Netzwerk entdeckt wird. Sie können eine höhere Tl in der Registrierung konfigurieren.
-   Zum Registrieren eines nicht ausgeführten Geräts muss das Gerät vorab registriert .dll COM registriert werden, was Administratorrechte erfordert.
-   Zum Registrieren eines ausgeführten Geräts sind administrator-, lokale Dienst- oder lokale Systemberechtigungen erforderlich.
-   Wenn der Gerätehost gestartet wird, wird er als [LocalService ausgeführt.](/windows/desktop/Services/localservice-account) Dadurch kann das Gerät Überwachungen generieren und den **Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE** lesen. Das Gerät hat Zugriff auf **HKEY \_ CURRENT \_ USER**. Das LocalService-Konto kann Ressourcen verwenden, denen LocalService Zugriff gewährt wurde, sowie ressourcen, die Zugriff auf AuthenticatedUser gewähren. Das Gerät verfügt über eingeschränkten Dateisystemzugriff.
-   Die Dateisystem-ACLs müssen aktualisiert werden, um [LocalService-Zugriff](/windows/desktop/Services/localservice-account) auf das Ressourcenverzeichnis zu ermöglichen.
-   Wenn Ihr Gerät über mehr Sicherheitszugriff verfügen muss, können Sie einen eigenen Prozess für das Gerät erstellen und ihn mithilfe von [**IUPnPRegistrar::RegisterRunningDevice registrieren.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)

 

 