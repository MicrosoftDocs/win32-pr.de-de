---
title: Empfangen von unerwünschtem Datenverkehr über Teredo
description: Teredo bietet globale Konnektivität mithilfe von IPv6- und NAT-Traversalfunktionen.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca6a4a6580200eee1f039fc87da29515db00a29f94700ff02548c38ba776f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099630"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Empfangen von unerwünschtem Datenverkehr über Teredo

[Teredo](about-teredo.md) bietet globale Konnektivität mithilfe von IPv6- und NAT-Traversalfunktionen. Viele Anwendungen, einschließlich Peer-zu-Peer, erfordern jedoch, dass Teredo nicht angeforderten Datenverkehr aus dem Internet empfängt. Eine Anwendung kann so programmiert werden, dass sie Datenverkehr über eine einzelne IPv6-Schnittstelle oder alle IPv6-fähigen Schnittstellen empfängt. In dieser Dokumentation werden die Anforderungen für Anwendungen beschrieben, die die Teredo-Schnittstelle verwenden, um nicht angeforderten IPv6-Datenverkehr zu empfangen.

Eine Anwendung empfängt nicht angeforderten Datenverkehr über die Teredo-Schnittstelle nur, wenn die Anwendung bei [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page)registriert ist. Um nicht angeforderten Datenverkehr zu empfangen, muss Folgendes auftreten:

-   Benutzer müssen angewiesen werden, die Microsoft Management Console (MMC) zu verwenden, um die Option "Edgedurchlauf" für eine Anwendung zu aktivieren. Diese Option ist unter Windows Registerkarte Firewall Snap-In --> <application name> --> Registerkarte "Erweitert" verfügbar. Die Option "Edgedurchlauf" muss für jede Anwendung einzeln aktiviert werden.

-   Die Option "Edgedurchlauf" wird von der Anwendung aktiviert. Anwendungen, die unerwünschten Datenverkehr empfangen können, können sich bei Windows Firewall für "Edge Traversal" registrieren und nicht angeforderten Datenverkehr über die Teredo-Schnittstelle empfangen. Hierzu muss eine Anwendung die [**INetFwPolicy2-API**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) aufrufen, wobei die Option "Edge Traversal" auf VARIANT TRUE festgelegt \_ ist. Für diesen API-Aufruf ist eine Benutzerzustimmung erforderlich, bevor eine Anwendung auf den Datenverkehr lauschen darf.

-   Die Anwendung legt die Socketoption Winsock [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) über [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **PROTECTION LEVEL \_ \_ UNRESTRICTED** fest. Dadurch kann die Anwendung Edgedurchlaufdatenverkehr empfangen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfangen von angeforderten Datenverkehr über Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 