---
description: Ein Namespace Anbieter implementiert eine Schnittstellen Zuordnung zwischen der Winsock-Namespace-SPI und der systemeigenen programmgesteuerten Schnittstelle eines vorhandenen namens Dienstanbieters, z. b. DNS, X. 500 oder NetWare-Verzeichnisdienste (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Namespace-Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e975c7ad0e5df29910624bb8f0b9d94fd24d9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360034"
---
# <a name="namespace-service-providers"></a>Namespace-Dienstanbieter

Ein Namespace Anbieter implementiert eine Schnittstellen Zuordnung zwischen der Winsock-Namespace-SPI und der systemeigenen programmgesteuerten Schnittstelle eines vorhandenen namens Dienstanbieters, z. b. DNS, X. 500 oder NetWare-Verzeichnisdienste (NDS). Obwohl ein Namespace Anbieter genau einen Namespace unterstützt, ist es möglich, dass mehrere Anbieter für einen bestimmten Namespace installiert werden. Es ist auch möglich, dass eine einzelne DLL eine Instanz von mehreren Namespace Anbietern erstellt. Wenn Namespace Anbieter installiert sind, wird ein Katalog mit [**wsanamespace- \_ Informations**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) Strukturen verwaltet. Eine Anwendung kann mithilfe von [**wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) ermitteln, welche Namespaces auf einem Computer unterstützt werden.

Unter Windows Vista und höher werden eine erweiterte [**wsanamespace- \_ INFOEX**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) -Struktur und die [**wsaenumnamespaceprovidersex**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) -Funktion bereitgestellt.

Auf 64-Bit-Plattformen werden ähnliche [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) -und [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) -Funktionen bereitgestellt, um den 32-Bit-Katalog aufzuzählen.

Ausführliche Informationen finden Sie unter Anforderungen an den [Winsock-Namespace-Dienstanbieter](winsock-namespace-service-provider-requirements.md) .

## <a name="legacy-getxbyy-service-providers"></a>Ältere getxbyy-Dienstanbieter

Windows Sockets 2 unterstützt vollständig die TCP/IP-spezifischen Funktionen zur Namensauflösung, die in Windows Sockets Version 1,1 gefunden wurden. Dies erfolgt durch Einschließen des Satzes von **getxbyy** -Funktionen in den SPI. Die Behandlung dieser Funktions Reihe unterscheidet sich jedoch etwas von den restlichen SPI-Funktionen. Die **getxbyy** -Funktionen, die in der SPI angezeigt werden, werden mit getxbyysp \_ vorangestellt und in der folgenden Tabelle zusammengefasst.

Berkeley-Stil Funktionen



| Name der SPI-Funktion           | BESCHREIBUNG                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| Getxbyysp \_ gethostbyaddr    | Stellt eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur für die angegebene Host Adresse bereit.        |
| Getxbyysp \_ gethostbyname    | Stellt eine [**hostenstruktur**](/windows/desktop/api/winsock/ns-winsock-hostent) für den angegebenen Hostnamen bereit.           |
| Getxbyysp \_ getprotobyname   | Stellt eine [**prototypstruktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für den angegebenen Protokollnamen bereit.     |
| Getxbyysp \_ getprotobynumber | Stellt eine [**prototypstruktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für die angegebene Protokollnummer bereit.   |
| Getxbyysp \_ getservbyname    | Stellt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur für den angegebenen Dienst, Nam. e, bereit.        |
| Getxbyysp \_ getservbyport    | Stellt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur für den Dienst am angegebenen Port bereit. |
| Getxbyysp \_ GetHostName      | Gibt den Standard Hostnamen für den lokalen Computer zurück.                                   |



 

Async-Stil Funktionen



| Name der SPI-Funktion                   | BESCHREIBUNG                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Getxbyysp \_ wsaasyncgethostbyaddr    | Stellt eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur für die angegebene Host Adresse bereit.        |
| Getxbyysp \_ wsaasyncgethostbyname    | Stellt eine [**hostenstruktur**](/windows/desktop/api/winsock/ns-winsock-hostent) für den angegebenen Hostnamen bereit.           |
| Getxbyysp \_ wsaasyncgetprotobyname   | Stellt eine [**prototypstruktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für den angegebenen Protokollnamen bereit.     |
| Getxbyysp \_ wsaasyncgetprotobynumber | Stellt eine [**prototypstruktur**](/windows/desktop/api/winsock/ns-winsock-protoent) für die angegebene Protokollnummer bereit.   |
| Getxbyysp \_ wsaasyncgetservbyname    | Stellt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur für den angegebenen Dienstnamen bereit.        |
| Getxbyysp \_ wsaasyncgetservbyport    | Stellt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur für den Dienst am angegebenen Port bereit. |
| Getxbyysp \_ wsacancelasynkrequest    | Bricht einen asynchronen **getxbyy** -Vorgang ab.                                           |



 

Die Syntax und die Semantik dieser **getxbyy** -Funktionen in der SPI entsprechen genau den in der API-Spezifikation dokumentierten und werden daher hier nicht wiederholt.

Mit der DLL für Windows Sockets 2 kann genau ein Dienstanbieter diese Dienste anbieten. Daher müssen Sie keine Zeiger auf diese Funktionen in der Prozedur Tabelle einschließen, die von Dienstanbietern beim Start empfangen wird. In Windows-Umgebungen wird der Pfad zu der dll, die diese Funktionen implementiert, von dem Wert aus dem folgenden Registrierungs Pfad abgerufen. Dieser Registrierungs Eintrag ist standardmäßig nicht vorhanden:

**HKEY \_ LOCAL \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Winsock2** \\ **Parameters** \\ **getxbyylibrarypath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In Standard-getxbyy-Dienstanbieter

Ein standardmäßiger **getxbyy** -Dienstanbieter ist in die standardmäßigen Windows Sockets 2-Laufzeitkomponenten integriert. Dieser Standardanbieter implementiert alle oben genannten Funktionen, daher ist es nicht erforderlich, dass diese Funktionen von einem Namespace Anbieter implementiert werden. Ein Namespace Anbieter kann jedoch eine beliebige oder alle dieser Funktionen bereitstellen (und somit die Standardwerte außer Kraft setzen), indem einfach die Zeichenfolge gespeichert wird. Hierbei handelt es sich um den Pfad zu der dll, die diese Funktionen im angegebenen Registrierungsschlüssel implementiert. Alle **getxbyy** -Funktionen, die nicht von der benannten Anbieter-DLL exportiert werden, werden über die integrierten Standardeinstellungen bereitgestellt. Beachten Sie jedoch Folgendes: Wenn ein Anbieter eine der asynchronen Versionen der **getxbyy** -Funktionen bereitstellt, sollte er alle Async-Funktionen bereitstellen, damit der Abbruch Vorgang ordnungsgemäß funktioniert.

Die aktuelle Implementierung des standardmäßigen **getxbyy** -Dienstanbieters befindet sich innerhalb der Wsock32.dll. Abhängig davon, wie die TCP/IP-Einstellungen über die Systemsteuerung eingerichtet wurden, erfolgt die Namensauflösung entweder mithilfe von DNS-oder lokalen Host Dateien. Wenn DNS verwendet wird, verwendet der standardmäßige **getxbyy** -Dienstanbieter standardmäßige Windows Sockets 1,1-API-Aufrufe, um mit dem DNS-Server zu kommunizieren. Diese Transaktionen werden mit einem beliebigen TCP/IP-Stapel ausgeführt, der als standardmäßiger TCP/IP-Stapel konfiguriert ist. Zwei besondere Fälle sind jedoch besonders erwähnenswert.

Die Standard Implementierung von getxbyysp \_ GetHostName Ruft den lokalen Hostnamen aus der Registrierung ab. Dies entspricht dem Namen, der "Arbeitsplatz" zugewiesen ist. Die Standard Implementierung von getxbyysp \_ gethostbyname und getxbyysp \_ wsaasyncgethostbyname vergleicht immer den angegebenen Hostnamen mit dem lokalen Hostnamen. Wenn Sie einander entsprechen, verwendet die Standard Implementierung eine private Schnittstelle, um den Microsoft TCP/IP-Stapel zu durchsuchen, um die lokale IP-Adresse zu ermitteln. Damit der Microsoft TCP/IP-Stapel vollständig unabhängig ist, muss ein Namespace Anbieter sowohl "getxbyysp \_ gethostbyname" als auch "getxbyysp \_ wsaasyncgethostbyname" implementieren.

 

 



