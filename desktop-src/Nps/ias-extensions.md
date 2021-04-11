---
title: Erweiterungen für Netzwerk Richtlinien Server
description: Mit der NPS-Erweiterungs-API können Softwareentwickler Erweiterungs-DLLs schreiben, die für Authentifizierung, Autorisierung und Kontoführung verwendet werden können. Die NPS-Erweiterungs-API unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948968"
---
# <a name="network-policy-server-extensions"></a>Erweiterungen für Netzwerk Richtlinien Server

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Mit der NPS-Erweiterungs-API können Softwareentwickler Erweiterungs-DLLs schreiben, die für Authentifizierung, Autorisierung und Kontoführung verwendet werden können. Die NPS-Erweiterungs-API unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service).

Die mit der NPS-Erweiterungs-API implementierten Erweiterungs-DLLs können eine verbesserte Sitzungssteuerung und-Kontoführung bereitstellen. Diese DLLs können für Szenarien wie z. b. das Steuern der Anzahl von Netzwerksitzungen des Endbenutzers, die Verwendung eines Zustands Servers und das Herstellen einer Verbindung mit Domänen Authentifizierungs Datenbanken und Active Directory Diensten verwendet werden. Die Erweiterungs-DLLs können die von NPS bereitgestellten Remote Zugriffs Autorisierungen erweitern, indem Sie Ihre eigenen Autorisierungen hinzufügen, wenn Sie eine Accept-Antwort an einen authentifizier enden Client zurücksenden.

Die NPS-Erweiterungs-API ist in jeder Computerumgebung anwendbar, in der Sie die Effizienz bei der Authentifizierung von einwählbenutzern über einen Remote Server verbessern. Diese Technologie ist besonders nützlich für Internet Dienstanbieter (Internet Service Providers, ISPs).

## <a name="in-this-section"></a>In diesem Abschnitt

[Übersicht](/windows/desktop/Nps/ias-about-internet-authentication-service)

Allgemeine Informationen zu RADIUS und der NPS-Erweiterungs-API.

[Genutzt](/windows/desktop/Nps/ias-using-internet-authentication-service)

Beispielcode, der die Verwendung der NPS-Erweiterungs-API veranschaulicht.

[Verweis](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Dokumentation von enumerierten Typen, Funktionen und Strukturen, die die NPS-Erweiterungs-API bilden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk Richtlinien Server (Internet Authentication Service)](portal.md)
</dt> <dt>

[Extensible Authentication-Protokoll (EAP)](../eap/eap-start-page.md)
</dt> </dl>

 

 