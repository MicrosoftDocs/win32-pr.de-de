---
title: Netzwerkrichtlinienservererweiterungen
description: Mit der NPS-Erweiterungs-API können Softwareentwickler Erweiterungs-DLLs schreiben, die für die Authentifizierung, Autorisierung und Buchhaltung verwendet werden können. Die NPS-Erweiterungs-API unterstützt das RADIUS-Protokoll (Remote Authentication Dial-In User Service).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8db32889f266861809a0637dd380eb9f5d2ba7265bdf16d6a9404ed96a5420a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128770"
---
# <a name="network-policy-server-extensions"></a>Netzwerkrichtlinienservererweiterungen

> [!Note]  
> Der Internetauthentifizierungsdienst (Internet Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Mit der NPS-Erweiterungs-API können Softwareentwickler Erweiterungs-DLLs schreiben, die für die Authentifizierung, Autorisierung und Buchhaltung verwendet werden können. Die NPS-Erweiterungs-API unterstützt das RADIUS-Protokoll (Remote Authentication Dial-In User Service).

Die mit der NPS-Erweiterungs-API implementierten Erweiterungs-DLLs können eine verbesserte Sitzungssteuerung und -buchhaltung bieten. Diese DLLs können für Szenarien wie die Steuerung der Anzahl von Endbenutzernetzwerksitzungen, die Verwendung eines Zustandsservers und das Herstellen einer Verbindung mit Domänenauthentifizierungsdatenbanken und Active Directory-Diensten verwendet werden. Die Erweiterungs-DLLs können die vom NPS bereitgestellten Remotezugriffsautorisierungen erweitern, indem sie ihre eigenen Autorisierungen hinzufügen, wenn eine Accept-Antwort an einen authentifizierenden Client zurückgesendet wird.

Die NPS-Erweiterungs-API ist in jeder Computingumgebung anwendbar, in der sie die Effizienz bei der Authentifizierung von Einwählbenutzern über einen Remoteserver verbessern würde. Diese Technologie ist besonders nützlich für Internetdienstanbieter (ISPs).

## <a name="in-this-section"></a>In diesem Abschnitt

[Übersicht](/windows/desktop/Nps/ias-about-internet-authentication-service)

Allgemeine Informationen zu RADIUS und der NPS-Erweiterungs-API.

[Mit](/windows/desktop/Nps/ias-using-internet-authentication-service)

Beispielcode, der die Verwendung der NPS-Erweiterungs-API veranschaulicht.

[Referenz](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Dokumentation der aufzählten Typen, Funktionen und Strukturen, aus denen die NPS-Erweiterungs-API besteht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerkrichtlinienserver (Internetauthentifizierungsdienst)](portal.md)
</dt> <dt>

[Extensible Authentication-Protokoll (EAP)](../eap/eap-start-page.md)
</dt> </dl>

 

 