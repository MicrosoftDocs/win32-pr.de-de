---
title: Empfangen von angefordertem Datenverkehr über Teredo
description: Teredo bietet eine globale Konnektivität mithilfe von IPv6-und NAT-Traversale-Funktionen.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729041"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Empfangen von angefordertem Datenverkehr über Teredo

[Teredo](about-teredo.md) bietet eine globale Konnektivität mithilfe von IPv6-und NAT-Traversale-Funktionen. Viele Anwendungen, einschließlich Peer-to-Peer, erfordern jedoch, dass Teredo nicht angeforderten Datenverkehr aus dem Internet empfängt. Eine Anwendung kann so programmiert werden, dass Sie Datenverkehr über eine einzelne IPv6-Schnittstelle oder alle IPv6-fähigen Schnittstellen empfängt. Diese Dokumentation beschreibt die Anforderungen für Anwendungen, die die Teredo-Schnittstelle verwenden, um nicht angeforderten IPv6-Datenverkehr zu empfangen.

Eine Anwendung empfängt den nicht angeforderten Datenverkehr über die Teredo-Schnittstelle nur dann, wenn die Anwendung bei der [Windows-Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page)registriert ist. Um nicht angeforderten Datenverkehr zu empfangen, muss Folgendes eintreten:

-   Benutzer müssen angewiesen werden, mit der Microsoft Management Console (MMC) die Option "Edge-Traversal" für eine Anwendung zu aktivieren. Diese Option ist unter Windows-Firewall Snap-In--> <application name> -> Registerkarte "Erweitert" verfügbar. Die Option "Edge-Traversal" muss für jede Anwendung einzeln aktiviert werden.

-   Die Option "Edge-Traversal" wird von der Anwendung aktiviert. Anwendungen, die nicht angeforderten Datenverkehr empfangen können, um sich bei der Windows-Firewall für "Edge-Traversal" zu registrieren und nicht angeforderten Datenverkehr über die Teredo-Schnittstelle empfangen zu können Zu diesem Zweck muss eine Anwendung die [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) -API mit der Option "Edge Traversal" (Edgeausnahme) auf Variant true aufzurufen \_ . Die Benutzer Zustimmung ist für diesen API-Rückruf erforderlich, bevor eine Anwendung auf den Datenverkehr lauschen darf.

-   Die Anwendung legt die Winsock [IPv6 \_ - \_ schutzebenensocketoption](/windows/desktop/WinSock/ipv6-protection-level) auf eine **\_ \_ uneingeschränkte Schutz Ebene** über [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)fest. Dadurch kann die Anwendung Edge-Traversal-Datenverkehr empfangen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfangen von angeforderten Datenverkehr über Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 