---
title: Sicherheitsüberlegungen für den Geräte Host
description: Durch die Verwendung des Geräte Hosts werden Sicherheitsprobleme verursacht.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473404"
---
# <a name="device-host-security-considerations"></a>Sicherheitsüberlegungen für den Geräte Host

Durch die Verwendung des Geräte Hosts werden Sicherheitsprobleme aufgrund folgender Aktionen verursacht:

-   Geräte, die auf einem Computer unter Windows XP gehostet werden, senden Ankündigungen in allen Netzwerken.
-   Geräte, die auf einem Computer unter Windows XP gehostet werden, ermöglichen die Steuerung der Geräte aus allen Netzwerken.

Dies erhöht das Risiko für Heimanwender, weil Geräte, wie z. b. eine Media Player-oder eine über brückbare Beleuchtung oder ein HVAC-System, das auf einem Computer mit Windows XP gehostet wird, sichtbar sind und von Steuerungs Punkten außerhalb der Startseite gesteuert werden können.

Wenn Sie ein gehosteter Gerät erstellen, müssen Sie einige Sicherheitsprobleme berücksichtigen.

-   Um den Umfang der Ermittlung und des Angriffs von UPnP-basierten Geräten zu reduzieren, ist die Gültigkeitsdauer aller SSDP-Nachrichten 1. Dies bedeutet, dass ein registriertes Gerät nur von Steuerungs Punkten im gleichen Netzwerk erkannt wird. Sie können eine höhere Gültigkeitsdauer in der Registrierung konfigurieren.
-   Zum Registrieren eines Geräts, das nicht ausgeführt wird, müssen Sie die Anwendung "Device. dll" vorab mit com registrieren, was Administratorrechte erfordert.
-   Zum Registrieren eines laufenden Geräts sind die Berechtigungen Administrator, lokaler Dienst oder lokales System erforderlich.
-   Wenn der Geräte Host gestartet wird, wird er als [LocalService](/windows/desktop/Services/localservice-account)ausgeführt. Dadurch erhält das Gerät die Möglichkeit, Überwachungen zu generieren und den Registrierungsschlüssel für den **lokalen HKEY- \_ \_ Computer** zu lesen. Das Gerät hat Zugriff auf den **aktuellen HKEY- \_ \_ Benutzer**. Das LocalService-Konto kann Ressourcen verwenden, denen LocalService Zugriff gewährt wurde, sowie diejenigen, die Zugriff auf authentiereduser gewähren. Das Gerät verfügt über eingeschränkten Zugriff auf den Dateisystem Zugriff.
-   Die Dateisystem-ACLs müssen aktualisiert werden, damit [LocalService](/windows/desktop/Services/localservice-account) auf das Ressourcenverzeichnis zugreifen kann.
-   Wenn Ihr Gerät über mehr Sicherheits Zugriff verfügen muss, können Sie einen eigenen Prozess für das Gerät erstellen und es mithilfe von [**iupnpregistranar:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)registrieren.

 

 