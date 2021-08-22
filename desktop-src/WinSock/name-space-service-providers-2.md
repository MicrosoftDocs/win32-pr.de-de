---
description: Ein Namespaceanbieter implementiert eine Schnittstellenzuordnung zwischen dem Winsock-Namespace SPI und der nativen programmgesteuerten Schnittstelle eines vorhandenen Namensdiensts wie DNS, X.500 oder NetWare-Verzeichnisdienste (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Namespace-Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e6ecc9ad0dcb9667bdd3d08049b9d41c3211de422cae0530506f6103494527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822638"
---
# <a name="namespace-service-providers"></a>Namespace-Dienstanbieter

Ein Namespaceanbieter implementiert eine Schnittstellenzuordnung zwischen dem Winsock-Namespace SPI und der nativen programmgesteuerten Schnittstelle eines vorhandenen Namensdiensts wie DNS, X.500 oder NetWare-Verzeichnisdienste (NDS). Obwohl ein Namespaceanbieter genau einen Namespace unterstützt, ist es möglich, dass mehrere Anbieter für einen bestimmten Namespace installiert werden. Es ist auch möglich, dass eine einzelne DLL eine Instanz mehrerer Namespaceanbieter erstellt. Wenn Namespaceanbieter installiert werden, wird ein Katalog von [**WSANAMESPACE \_ INFO-Strukturen**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) verwaltet. Eine Anwendung kann [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) verwenden, um zu ermitteln, welche Namespaces auf einem Computer unterstützt werden.

Auf Windows Vista und höher werden eine erweiterte [**WSANAMESPACE \_ INFOEX-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) und [**die WSAEnumNameSpaceProvidersEx-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) bereitgestellt.

Auf 64-Bit-Plattformen werden ähnliche [**WSCEnumNameSpaceProviders32-**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) und [**WSCEnumNameSpaceProvidersEx32-Funktionen**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) bereitgestellt, um den 32-Bit-Katalog aufzulisten.

Ausführliche Informationen finden Sie unter [Anforderungen des Winsock-Namespacedienstanbieters.](winsock-namespace-service-provider-requirements.md)

## <a name="legacy-getxbyy-service-providers"></a>Legacy-GetXbyy-Dienstanbieter

Windows Sockets 2 unterstützt vollständig die TCP/IP-spezifischen Namensauflösungsmöglichkeiten in Windows Sockets Version 1.1. Hierzu wird der Satz von **GetXbyY-Funktionen** in die SPI eingeschlossen. Die Behandlung dieser Reihe von Funktionen unterscheidet sich jedoch etwas von den anderen SPI-Funktionen. Den in der SPI angezeigten **GetXbyY-Funktionen** wird GETXBYYSP vorangestellt \_ und in der folgenden Tabelle zusammengefasst.

Funktionen im Stil von California



| SPI-Funktionsname           | Beschreibung                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | Stellt eine [**Hostentstruktur**](/windows/desktop/api/winsock/ns-winsock-hostent) für die angegebene Hostadresse zur Verfügung.        |
| GETXBYYSP \_ gethostbyname    | Stellt eine [**Hostentstruktur**](/windows/desktop/api/winsock/ns-winsock-hostent) für den angegebenen Hostnamen zur Verfügung.           |
| GETXBYYSP \_ getprotobyname   | Stellt eine [**protoent-Struktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für den angegebenen Protokollnamen zur Verfügung.     |
| GETXBYYSP \_ getprotobynumber | Stellt eine [**protoent-Struktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für die angegebene Protokollnummer zur Verfügung.   |
| GETXBYYSP \_ getservbyname    | Stellt eine [**Servent-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) für den angegebenen Dienst nam.e zur Verfügung.        |
| GETXBYYSP \_ getservbyport    | Stellt eine [**servent-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) für den Dienst am angegebenen Port zur Verfügung. |
| GETXBYYSP \_ gethostname      | Gibt den Standardhostnamen für den lokalen Computer zurück.                                   |



 

Asynchrone Stilfunktionen



| SPI-Funktionsname                   | Beschreibung                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Stellt eine [**Hostentstruktur**](/windows/desktop/api/winsock/ns-winsock-hostent) für die angegebene Hostadresse zur Verfügung.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Stellt eine [**Hostentstruktur**](/windows/desktop/api/winsock/ns-winsock-hostent) für den angegebenen Hostnamen zur Verfügung.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Stellt eine [**protoent-Struktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für den angegebenen Protokollnamen zur Verfügung.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Stellt eine [**protoent-Struktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für die angegebene Protokollnummer zur Verfügung.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Stellt eine [**servent-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) für den angegebenen Dienstnamen zur Verfügung.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Stellt eine [**servent-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) für den Dienst am angegebenen Port zur Verfügung. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Bricht einen asynchronen **GetXbyY-Vorgang** ab.                                           |



 

Die Syntax und Semantik dieser **GetXbyY-Funktionen** in der SPI sind identisch mit denen, die in der API-Spezifikation dokumentiert sind, und werden daher hier nicht wiederholt.

Die Windows Sockets 2-DLL ermöglicht genau einem Dienstanbieter, diese Dienste anzubieten. Daher müssen keine Zeiger auf diese Funktionen in die Prozedurtabelle eingeschlossen werden, die beim Start von Dienstanbietern empfangen wurde. In Windows Umgebungen wird der Pfad zur DLL, die diese Funktionen implementiert, aus dem Im folgenden Registrierungspfad gefundenen Wert abgerufen. Dieser Registrierungseintrag ist standardmäßig nicht vorhanden:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **WinSock2** \\ **Parameters** \\ **GetXByYLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In Standard-GetXbyY-Dienstanbieter

Ein **GetXbyY-Standarddienstanbieter** ist in die Standard-Windows Sockets 2-Laufzeitkomponenten integriert. Dieser Standardanbieter implementiert alle oben genannten Funktionen. Daher ist es nicht erforderlich, dass diese Funktionen von einem Namespaceanbieter implementiert werden. Ein Namespaceanbieter kann jedoch eine oder alle dieser Funktionen bereitstellen (und somit die Standardwerte überschreiben), indem er einfach die Zeichenfolge speichert, die den Pfad zur DLL darstellt, die diese Funktionen im angegebenen Registrierungsschlüssel implementiert. Jede der **GetXbyY-Funktionen,** die nicht von der benannten Anbieter-DLL exportiert werden, wird über die integrierten Standardwerte bereitgestellt. Beachten Sie jedoch Folgendes: Wenn ein Anbieter eine der asynchronen Versionen der **GetXbyY-Funktionen** bereitstellen möchte, sollte er alle asynchronen Funktionen bereitstellen, damit der Abbruchvorgang ordnungsgemäß funktioniert.

Die aktuelle Implementierung des **GetXbyY-Standarddienstanbieters** befindet sich innerhalb des Wsock32.dll. Je nachdem, wie die TCP/IP-Einstellungen über Systemsteuerung eingerichtet wurden, erfolgt die Namensauflösung entweder über DNS oder lokale Hostdateien. Wenn DNS verwendet wird, verwendet der **GetXbyY-Standarddienstanbieter** standardmäßige Windows Sockets 1.1-API-Aufrufe für die Kommunikation mit dem DNS-Server. Diese Transaktionen erfolgen mithilfe des TCP/IP-Stapels, der als TCP/IP-Standardstapel konfiguriert ist. Zwei Sonderfälle sollten jedoch besonders erwähnt werden.

Die Standardimplementierungen von GETXBYYSP \_ gethostname rufen den namen des lokalen Hosts aus der Registrierung ab. Dies entspricht dem Namen, der "Arbeitsplatz" zugewiesen ist. Die Standardimplementierungen von GETXBYYSP \_ gethostbyname und GETXBYYSP \_ WSAAsyncGetHostByName vergleichen immer den angegebenen Hostnamen mit dem namen des lokalen Hosts. Wenn sie übereinstimmen, verwendet die Standardimplementierung eine private Schnittstelle, um den TCP/IP-Stapel von Microsoft zu untersuchen, um seine lokale IP-Adresse zu ermitteln. Daher muss ein Namespaceanbieter sowohl GETXBYYSP gethostbyname als auch \_ GETXBYYSP WSAAsyncGetHostByName implementieren, um vollständig unabhängig vom TCP/IP-Stapel von Microsoft zu \_ sein.

 

 



