---
title: Netzwerkrichtlinienserver
description: Der Netzwerkrichtlinienserver (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und eines Proxys.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f604d7cea69bcc8866176f612c76d2e6820bc4a00aa58d3760761ef59270b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362306"
---
# <a name="network-policy-server"></a>Netzwerkrichtlinienserver

## <a name="purpose"></a>Zweck

Der Netzwerkrichtlinienserver (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und eines Proxys. Es ist der Nachfolger des Internetauthentifizierungsdiensts (Internet Authentication Service, IAS).

Als RADIUS-Server führt NPS Authentifizierungs-, Autorisierungs- und Kontoführungs-, Authentifizierungsschalter- und Remotezugriffs-DFÜ- und VPN-Verbindungen (Virtuelles privates Netzwerk) durch.

NPS ist auch ein Integritätsauswertungsserver für den Netzwerkzugriffsschutz (Network Access Protection, NAP). NPS führt die Authentifizierung und Autorisierung von Netzwerkverbindungsversuchen durch und wertet basierend auf konfigurierten Systemzustandsrichtlinien die Computer-Integritätskonformität aus und bestimmt, wie der Netzwerkzugriff oder die Kommunikation eines nicht konformen Computers geschränkt werden kann. Dies ist ein neues Feature, das nur für NPS gilt. DIEs wird von IAS nicht unterstützt. Unter [Internetauthentifizierungsdienst und Netzwerkrichtlinienserver](internet-authentication-service-vs-network-policy-server.md) finden Sie eine vollständige Liste der neuen NpS-Features.

NPS umfasst zwei API-Sätze: DIE NPS-Erweiterungs-API und die SDO-API (Server Data Objects). Sowohl die NPS-Erweiterungs-API als auch die SDO-API werden durch nps, den Internetauthentifizierungsdienst, unterstützt.

Die NPS-Erweiterungs-API kann verwendet werden, um die Authentifizierungs-, Autorisierungs- und Buchhaltungsmethoden zu erweitern, die von NPS und früher von IAS angeboten werden.

Die Serverdatenobjekt-API kann verwendet werden, um die Netzwerkrichtlinienkonfiguration auf einem Computer zu bearbeiten, auf dem NPS oder IAS ausgeführt wird.

> [!Note]  
> Netzwerkrichtlinien in NPS sind äquivalent zu Remotezugriffsrichtlinien in IAS.

 

## <a name="developer-audience"></a>Entwicklergruppe

Die NPS-Erweiterungs-API ist für die Verwendung durch Programmierer konzipiert, die C/C++-Entwicklungssoftware verwenden. Programmierer sollten mit Netzwerkkonzepten und dem RADIUS-Protokoll vertraut sein. RADIUS ist in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) und [RFC 2866 dokumentiert.](https://www.ietf.org/rfc/rfc2866.txt)

Die Server Data Objects-API ist für die Verwendung durch Programmierer konzipiert, die C/C++ oder Visual Basic-Entwicklungssoftware verwenden. Programmierer sollten mit dem [Ras-Dienst (RAS)](/windows/desktop/RRAS/remote-access-request-for-comments) und dem RADIUS-Protokoll vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die NPS-Erweiterungs-API wird auf Windows Server 2008 mit der Installation von Microsoft Commercial Internet Service (MCIS) unterstützt.

Die Server Data Objects-API wird auf Windows Server 2008 unterstützt.

NPS ist auf Windows Server 2008 mit der Installation von Microsoft Commercial Internet Service (MCIS) verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Übersicht](about-network-policy-server.md)
</dt> <dd>

Allgemeine Informationen zu RADIUS, IAS und NPS.

</dd> <dt>

[API für Netzwerkrichtlinienservererweiterungen](ias-extensions.md)
</dt> <dd>

API zum Implementieren von Erweiterungs-DLLs, die für Authentifizierung, Autorisierung und Buchhaltung verwendet werden.

</dd> <dt>

[Server Data Objects-API](server-data-objects.md)
</dt> <dd>

API zum Verwalten der Netzwerkrichtlinienkonfiguration.

</dd> <dt>

[SQL Programmierbarkeit](sql-programmability.md)
</dt> <dd>

Beispiele für gespeicherte Prozeduren, die zum Verwalten der NPS-Protokollierung (IAS) verwendet werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TechNet: Netzwerkrichtlinienserver](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: Internetauthentifizierungsdienst](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Netzwerkzugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 