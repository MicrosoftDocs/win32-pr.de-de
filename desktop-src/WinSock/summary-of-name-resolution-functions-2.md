---
description: 'Die namens Auflösungs Funktionen können in drei Kategorien unterteilt werden: Dienst Installation, Client Abfragen und Hilfsobjekte (mit Makros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Zusammenfassung der namens Auflösungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751400"
---
# <a name="summary-of-name-resolution-functions"></a>Zusammenfassung der namens Auflösungs Funktionen

Die namens Auflösungs Funktionen können in drei Kategorien unterteilt werden: Dienst Installation, Client Abfragen und Hilfsobjekte (mit Makros). In den folgenden Abschnitten werden die Funktionen in den einzelnen Kategorien identifiziert und die beabsichtigte Verwendung kurz beschrieben. Wichtige Datenstrukturen werden ebenfalls beschrieben.

## <a name="service-installation"></a>Dienst Installation

-   [**Wsainstallserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**Wsareviveserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**Wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

Wenn die erforderliche Dienstklasse nicht bereits vorhanden ist, wird von einer Anwendung [**wsainstallserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) verwendet, um eine neue Dienstklasse zu installieren. hierzu werden ein Dienst Klassenname, eine GUID für den Dienst Klassen Bezeichner und eine Reihe von [**wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) -Strukturen bereitgestellt. Diese Strukturen sind jeweils spezifisch für einen bestimmten Namespace und geben allgemeine Werte wie empfohlene TCP-Portnummern oder NetWare-SAP-IDs an. Eine Dienstklasse kann entfernt werden, indem Sie [**wsarewveserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) aufrufen und die GUID angeben, die dem Klassen Bezeichner entspricht.

Sobald eine Dienstklasse vorhanden ist, können bestimmte Instanzen eines Dienstanbieter mithilfe von [**wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)installiert oder entfernt werden. Diese Funktion nimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabeparameter zusammen mit einem Vorgangs Code und Vorgangs Flags an. Der Vorgangs Code gibt an, ob der Dienst installiert oder entfernt wird. Die **wsaqueryset** -Struktur stellt alle relevanten Informationen über den Dienst bereit, einschließlich der Dienst Klassen-ID, des Dienst namens (für diese Instanz), der anwendbaren Namespace-ID und der Protokollinformationen sowie einer Gruppe von Transport Adressen, die vom Dienst überwacht werden. Dienste sollten **wsasetservice** aufrufen, wenn diese initialisiert werden, um Ihre Anwesenheit in dynamischen Namespaces ankündigen zu können.

## <a name="client-query"></a>Client Abfrage

-   [**Wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**Wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

Mithilfe der Funktion [**wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) kann eine Anwendung ermitteln, auf welche Namespaces über die Winsock-namens Auflösungs Funktionen zugegriffen werden kann. Außerdem kann eine Anwendung ermitteln, ob ein bestimmter Namespace von mehreren Namespace Anbietern unterstützt wird, und die Anbieter-ID für einen bestimmten Namespace Anbieter ermitteln. Mithilfe eines Anbieter Bezeichners kann die Anwendung einen Abfrage Vorgang auf einen angegebenen Namespace Anbieter beschränken.

Winsock-Namespace – Abfrage Vorgänge beinhalten eine Reihe von aufrufen: [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), gefolgt von einem oder mehreren Aufrufen von [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) und endend mit einem Aufruf von [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). **Wsalookupservicebegin** übernimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabe, um die Abfrage Parameter zusammen mit einem Satz von Flags zu definieren, um eine zusätzliche Kontrolle über den Suchvorgang bereitzustellen. Es wird ein Abfrage Handle zurückgegeben, das bei nachfolgenden Aufrufen von **WSALookupServiceNext** und **WSALookupServiceEnd** verwendet wird.

Die Anwendung ruft [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) auf, um Abfrageergebnisse abzurufen, wobei Ergebnisse in einem von der Anwendung bereitgestellten [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Puffer bereitgestellt werden. Die Anwendung ruft weiterhin **WSALookupServiceNext** auf, bis der Fehlercode WSA \_ E \_ nicht \_ mehr zurückgegeben wird, was darauf hinweist, dass alle Ergebnisse abgerufen wurden. Die Suche wird dann durch einen [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)-Aufrufvorgang beendet. Die **WSALookupServiceEnd** -Funktion kann auch verwendet werden, um einen aktuell ausstehenden **WSALookupServiceNext** abzubrechen, wenn er von einem anderen Thread aufgerufen wird.

In Windows Sockets 2 werden widersprüchliche Fehlercodes für wsaumomore (10102) und WSA \_ E \_ nicht \_ mehr (10110) definiert. Der Fehlercode wsaeromore wird in einer zukünftigen Version entfernt, und nur WSA \_ E \_ \_ bleibt erhalten. Für Windows Sockets 2 sollten Anwendungen jedoch sowohl auf wsaenomore als auch auf WSA \_ E \_ nicht mehr zugreifen, \_ um die größtmögliche Kompatibilität mit Namespace Anbietern zu ermöglichen, die beide verwenden.

## <a name="helper-functions"></a>Hilfsfunktionen

-   [**Wsagetserviceclassnamebyclassid**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**Wsaadresssstostring**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**Wsagetserviceclassinfo**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

Die Hilfsfunktionen für die Namensauflösung enthalten eine Funktion zum Abrufen eines Dienst Klassen namens mit einer Dienst Klassen Kennung, einem Funktions Paar, mit dem eine Transport Adresse zwischen einer [**sockaddr**](sockaddr-2.md) -Struktur und einer ASCII-Zeichen folgen Darstellung, einer Funktion zum Abrufen der Dienst Klassen Schema Informationen für eine bestimmte Dienstklasse und einer Reihe von Makros für die Zuordnung bekannter Dienste zu vorab zugeordneten GUIDs verwendet wird.

Die folgenden Makros aus Winsock2. h unterstützen die Zuordnung zwischen bekannten Dienst Klassen und diesen Namespaces:

| Makro                                                                                                            | Beschreibung                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Svcid \_ TCP (Port) svcid \_ UDP (Port)<br/> Svcid- \_ NetWare (Objekttyp)<br/>                              | Bei einem Port für TCP/IP oder UDP/IP oder dem Objekttyp im Fall von NetWare wird die GUID (Portnummer in der Reihenfolge der Hosts) zurückgegeben. |
| ist \_ svcid \_ TCP (GUID) ist \_ svcid \_ UDP (GUID)<br/> ist \_ svcid \_ NetWare (GUID)<br/>                          | Gibt **true** zurück, wenn die GUID innerhalb des zulässigen Bereichs liegt.                                                                |
| Festlegen der \_ TCP- \_ svcid (GUID, Port) festlegen der \_ UDP- \_ svcid (GUID, Port)<br/>                                                | Initialisiert eine GUID-Struktur mit der GUID-Entsprechung für eine TCP-oder UDP-Portnummer (die Portnummer muss in der Reihenfolge der Hosts angegeben werden).    |
| Port \_ vom \_ svcid- \_ TCP-Port (GUID) \_ von \_ svcid \_ UDP (GUID)<br/> SAPID \_ von \_ svcid \_ NetWare (GUID)<br/> | Gibt den Port oder Objekttyp zurück, der der GUID (Portnummer in der Host Reihenfolge) zugeordnet ist.                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**Getaddrinfow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**getnameingefo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**Getnameingefow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[Datenstrukturen für die Namensauflösung](name-resolution-data-structures-2.md)
</dt> <dt>

[Namens Auflösungs Modell](name-resolution-model-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**Wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**Wsagetserviceclassnamebyclassid**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**Wsainstallserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**Wsareviveserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**Wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**Wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




