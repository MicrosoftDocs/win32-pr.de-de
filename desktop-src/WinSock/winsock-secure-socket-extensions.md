---
description: Die Secure Socket-Erweiterungen für Winsock ermöglichen es einer socketanwendung, die Sicherheit des Datenverkehrs über ein Netzwerk zu steuern.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Winsock Secure Socket Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041720"
---
# <a name="winsock-secure-socket-extensions"></a>Winsock Secure Socket Extensions

Die Secure Socket-Erweiterungen für Winsock ermöglichen es einer socketanwendung, die Sicherheit des Datenverkehrs über ein Netzwerk zu steuern. Diese Erweiterungen ermöglichen es einer Anwendung, Sicherheitsrichtlinien und Anforderungen für den Netzwerk Datenverkehr bereitzustellen und die angewendeten Sicherheitseinstellungen abzufragen. Beispielsweise kann eine Anwendung diese Erweiterungen verwenden, um das Peer-Sicherheits Token abzufragen, das zum Ausführen von Zugriffs Überprüfungen auf Anwendungsebene verwendet werden kann.

Die Secure Socket-Erweiterungen dienen dazu, die von IPSec bereitgestellten Dienste und andere Sicherheitsprotokolle mit dem Winsock-Framework zu integrieren. Vor Windows Vista wurde IPSec unter Windows Server 2003 und Windows XP von einem Administrator über lokale und Domänen Richtlinien konfiguriert. Unter Windows Vista ermöglichen die Secure Socket Extensions stattdessen, dass Anwendungen die Sicherheit Ihres Netzwerk Datenverkehrs auf Socketebene ganz oder teilweise zu konfigurieren und zu steuern.

Anwendungen können den Netzwerk Datenverkehr bereits mithilfe von öffentlichen APIs sichern, z. b. IPSec-Verwaltung, Windows-Filter Plattform und Security Support Provider Interface (SSPI). Allerdings kann die Verwendung dieser APIs die Entwicklung der Anwendung erschweren und das Konfigurieren und Bereitstellen erschweren. Die Winsock Secure Socket Extensions wurden entwickelt, um die Entwicklung von Netzwerkanwendungen zu vereinfachen, die sicheren Netzwerk Datenverkehr erfordern, da Winsock den größten Teil der Komplexität bewältigen lässt.

Diese Secure Socket Extensions sind unter Windows Vista und höher verfügbar.

## <a name="secure-socket-functions"></a>Secure Socket-Funktionen

Die Funktionen der Secure Socket-Erweiterung lauten wie folgt:

-   [**Wsadeletesocketpeer-TargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**Wsaidentität atesocketpeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**Wsaquerysocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**Wsarevertimpersonations**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**Wsasetsocketpeer-TargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**Wsasetsocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> Die Secure Socket-Funktionen unterstützen derzeit nur das IPSec-Protokoll und sind unter Windows Vista und höher verfügbar.

 

Die von den Secure Socket Functions verwendeten Strukturen und Enumerationen lauten wie folgt:

-   [**\_Name des socketpeers \_ \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**\_ \_ socketsicherheitsprotokoll**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**\_Informationen zur \_ socketsicherheitsabfrage \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**\_socketsicherheitsabfrage- \_ \_ Vorlage**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**\_ \_ socketsicherheitseinstellungen**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**\_ \_ socketsicherheitseinstellungen \_ IPSec**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

Die sicheren Socketfunktionen können für normale Anwendungen einfach verwendet werden und sind flexibel genug für Anwendungen, die ein hohes Maß an Kontrolle über Ihre Sicherheit benötigen. Diese Funktionen ermöglichen es, den zugrunde liegenden Sicherheitsmechanismus vor der Anwendung zu verbergen. Eine Anwendung kann generische Sicherheitsanforderungen angeben und den Administrator das Sicherheitsprotokoll steuern lassen, das zur Unterstützung der Anforderungen verwendet wird. Obwohl es möglich ist, diese Funktionen zu erweitern, um andere Sicherheitsprotokolle hinzuzufügen, wird derzeit nur IPSec in die Secure Socket-Funktionen integriert.

Mit der [**wsasetsocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) -Funktion kann eine Anwendung die Sicherheit aktivieren und Sicherheitseinstellungen anwenden, bevor eine Verbindung hergestellt wird.

Die Funktion [**wsasetsocketpeertargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) ermöglicht es einer Anwendung, den Zielnamen anzugeben, der einer Peer Entität entspricht. Das ausgewählte Sicherheitsprotokoll verwendet diese Informationen, wenn der Peer authentifiziert wird. Diese Funktion behandelt Aspekte von vertrauenswürdigen man-in-the-Middle-Angriffen.

Die Funktion [**wsadeletesocketpeertargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) wird verwendet, um einen zuvor angegebenen Peernamen für einen Socket zu löschen.

Nachdem eine Verbindung hergestellt wurde, ermöglicht die [**wsaquerysocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) -Funktion einer Anwendung, die Sicherheitseigenschaften der Verbindung abzufragen, die den Peer Zugriff oder das Computer Zugriffs Token enthalten kann.

Nachdem eine Verbindung hergestellt wurde, kann eine Anwendung mithilfe der [**wsaidentität atesocketpeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) -Funktion die Identität des Sicherheits Prinzipals, der einem socketpeer entspricht, annehmen, um die Autorisierung auf Anwendungsebene auszuführen.

Mit [**wsarevertimpersonations**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) kann eine Anwendung den Identitätswechsel eines socketpeers beenden.

## <a name="secure-socket-architecture"></a>Secure Socket-Architektur

![grundlegende Architektur der Winsock Secure Socket Extensions](images/ss-arch.png)

-   Eine Anwendung ruft die Secure Socket-Funktionen auf, um die Sicherheitseinstellungen für einen Socket festzulegen oder abzufragen.
-   Bei den sicheren Socketfunktionen handelt es sich um einen Satz von typsicheren Erweiterungsfunktionen, die Aufrufe der [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mithilfe von neu definierten Werten für den in Windows Vista und höher verfügbaren *dwIoControlCode* -Parameter umschließen. Diese IOCTLs werden vom Netzwerk Stapel verarbeitet.
-   Der Netzwerk Stapel leitet den aufzurufenden [Anwendungs ebenenerzwingungs Vorgang (ALE)](../fwp/application-layer-enforcement--ale-.md) zusammen mit dem Endpunkt Handle weiter. Für die Funktionen [**wsadeletesocketetstargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**wsasetsocketetertargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)und [**wsasetsocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) konfiguriert ALE die Einstellungen der Anwendung auf dem lokalen Endpunkt. Bei der [**wsaquerysocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) -Funktion liest ALE die angeforderten Informationen von den anwendbaren lokalen und Remote Endpunkten.
-   Basierend auf socketereignissen erzwingt die Erzwingung der Anwendungsschicht Richtlinien für die sichere socketarchitektur mithilfe der Windows-Filter Plattform. Weitere Informationen finden Sie unter Informationen [zur Windows-Filter Plattform](../fwp/about-windows-filtering-platform.md) und zur [Durchsetzung der Anwendungsschicht](../fwp/application-layer-enforcement--ale-.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Windows-Filter Plattform](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Erweiterte Winsock-Beispiele mit Secure Socket Extensions](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[IPSec-Konfiguration](../fwp/ipsec-configuration.md)
</dt> <dt>

[IPSec-Funktionen](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Sichere Winsock-Programmierung](secure-winsock-programming.md)
</dt> <dt>

[Security Support Provider Interface (SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Verwenden von Secure Socket Extensions](using-secure-socket-extensions.md)
</dt> <dt>

[Windows-Filterplattform](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[API-Funktionen der Windows-Filter Plattform](../fwp/fwp-functions.md)
</dt> </dl>

 

 
