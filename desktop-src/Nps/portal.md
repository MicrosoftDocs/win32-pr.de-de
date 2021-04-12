---
title: Netzwerkrichtlinienserver
description: Der Netzwerk Richtlinien Server (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und-Proxys.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315441"
---
# <a name="network-policy-server"></a>Netzwerkrichtlinienserver

## <a name="purpose"></a>Zweck

Der Netzwerk Richtlinien Server (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und-Proxys. Es ist der Nachfolger von Internet Authentication Service (IAS).

Als RADIUS-Server führt NPS Authentifizierung, Autorisierung und Kontoführung für drahtlose, authentifizier Ende Switches sowie RAS-und VPN-Verbindungen (Virtual Private Network) durch.

NPS ist auch ein Integritäts Bewertungs Server für den Netzwerk Zugriffsschutz (Network Access Protection, NAP). NPS führt die Authentifizierung und Autorisierung von Netzwerk Verbindungs versuchen durch und wertet basierend auf den konfigurierten System Integritäts Richtlinien die Konformität der Computer Integrität aus und bestimmt, wie der Netzwerk Zugriff oder die Kommunikation eines nicht kompatiblen Computers beschränkt wird. Dies ist ein neues Feature, das nur für NPS spezifisch ist. IAS unterstützt dies nicht. Eine umfassende Liste der Features, die neu in NPS sind, finden Sie unter [Internet Authentifizierungsdienst und Netzwerk Richtlinien Server](internet-authentication-service-vs-network-policy-server.md) .

NPS umfasst zwei API-Sätze: NPS Extensions API und SDO (Server Data Objects)-API. Die NPS-Erweiterungs-API und die SDO-API werden auch vom Vorgänger von NPS, dem Internet Authentifizierungsdienst, unterstützt.

Die NPS-Erweiterungs-API kann verwendet werden, um die Authentifizierungs-, Autorisierungs-und Buchhaltungsmethoden zu erweitern, die von NPS und früher von IAS angeboten werden

Die Server Data Objects-API kann verwendet werden, um die Netzwerk Richtlinien Konfiguration auf einem Computer zu bearbeiten, auf dem NPS oder IAS ausgeführt wird.

> [!Note]  
> Netzwerk Richtlinien in NPS entsprechen den RAS-Richtlinien in IAS.

 

## <a name="developer-audience"></a>Entwicklergruppe

Die NPS-Erweiterungs-API ist für die Verwendung durch Programmierer konzipiert, die C/C++-Entwicklungssoftware verwenden. Programmierer sollten mit den Netzwerk Konzepten und dem RADIUS-Protokoll vertraut sein. RADIUS ist in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) und [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)dokumentiert.

Die Server Data Objects-API ist für die Verwendung durch Programmierer konzipiert, die C/C++ oder Visual Basic Entwicklungssoftware verwenden. Programmierer sollten mit RAS ( [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) ) und dem RADIUS-Protokoll vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die NPS-Erweiterungs-API wird auf Windows Server 2008 mit der Installation von Microsoft Commercial Internet Service (MCIS) unterstützt.

Die Server Data Objects-API wird auf Windows Server 2008 unterstützt.

NPS ist unter Windows Server 2008 mit der Installation von Microsoft Commercial Internet Service (MCIS) verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Übersicht](about-network-policy-server.md)
</dt> <dd>

Allgemeine Informationen zu RADIUS, IAS und NPS.

</dd> <dt>

[API für Netzwerk Richtlinien Server-Erweiterungen](ias-extensions.md)
</dt> <dd>

API zum Implementieren von Erweiterungs-DLLs, die für Authentifizierung, Autorisierung und Kontoführung verwendet werden.

</dd> <dt>

[Server Data Objects-API](server-data-objects.md)
</dt> <dd>

API zum Verwalten der Netzwerk Richtlinien Konfiguration.

</dd> <dt>

[SQL-Programmierbarkeit](sql-programmability.md)
</dt> <dd>

Beispiele für gespeicherte Prozeduren, die zum Verwalten der NPS-Protokollierung verwendet werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TechNet: Netzwerk Richtlinien Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: Internet Authentifizierungsdienst](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 