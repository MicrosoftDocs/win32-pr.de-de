---
description: Verwenden des Checkv4.exe Hilfsprogramms, um die IPv4-Anwendung zur Unterstützung von IPv6 zu ändern.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Verwenden des Checkv4.exe Hilfsprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570663"
---
# <a name="using-the-checkv4exe-utility"></a>Verwenden des Checkv4.exe Hilfsprogramms

> [!IMPORTANT]
> Das *Checkv4.exe* -Hilfsprogramm wird nicht im Windows Software Development Kit (SDK) für Windows 8 und nicht in späteren Versionen des Windows SDK ausgeliefert.

Mit dem *Checkv4.exe* -Hilfsprogramm können Sie einen Code Portierungs Partner bereitstellen. ein Hilfsprogramm, das die Codebasis für Sie durchläuft, potenzielle Probleme identifiziert oder Code hervorhebt, der von IPv6-fähigen Funktionen oder Strukturen profitieren kann, und Empfehlungen gibt. Mit dem Checkv4.exe-Hilfsprogramm wird die Aufgabe, eine vorhandene IPv4-Anwendung zur Unterstützung von IPv6 zu ändern, viel einfacher.

Das *Checkv4.exe* -Hilfsprogramm wird als Teil des Microsoft Windows Software Development Kit (SDK) installiert, das für Windows Vista und spätere SDKs (bis einschließlich, das Windows Software Development Kit (SDK) für Windows 8) veröffentlicht wurde.

Eine frühere Version des *Checkv4.exe* Hilfsprogramms mit eingeschränkteren Features wurde auch als Teil der früheren Microsoft IPv6-Technologievorschau für Windows 2000 zur Verfügung gestellt.

In den folgenden Abschnitten wird beschrieben, wie Sie das *Checkv4.exe* -Hilfsprogramm verwenden und dann die empfohlene Vorgehensweise zum Ändern einer vorhandenen IPv4-Anwendung zur Unterstützung von IPv6 erläutern.

## <a name="recommendations-for-running-checkv4exe"></a>Empfehlungen zum Ausführen von Checkv4.exe

-   Das *Checkv4.exe* -Hilfsprogramm ist unkompliziert. Führen Sie *Checkv4.exe* einfach an der Befehlszeile mit dem Namen der Datei aus, die Sie als Parameter überprüfen möchten. *Checkv4.exe* analysiert die Datei und liefert Feedback darüber, wo in dieser Datei Probleme mit der IPv6-Portierung vorliegen. Wenn Sie die *Checkv4.exe* in den Pfad Ihres Computers platzieren, wird das Ausführen des *Checkv4.exe* Hilfsprogramms von überall in der Quell Code Verzeichnisstruktur erheblich vereinfacht. Wenn Sie *Checkv4.exe* z. b. in% windir% platzieren, können Sie *Checkv4.exe* aus einem beliebigen Verzeichnis auf dem Computer starten, ohne den Pfad zu einschließen.

-   Geben Sie den folgenden Befehl an der Eingabeaufforderung aus, um die Datei simplec. c zu analysieren:

    **Checkv4 simplec. c**

    Beachten Sie, dass einige der Empfehlungen, die das *Checkv4.exe* -Hilfsprogramm vornimmt, Strukturen erfordern, die nur in den letzten Versionen der *Ws2tcpip. h* -Header Datei verfügbar sind, wie z. b. die **sockaddr \_ IN6** Diese Header Dateien sind in der Windows SDK enthalten, die für Windows Vista und höher veröffentlicht wurden. Diese Header Dateien sind auch im früheren Platform Software Development Kit (SDK) enthalten, das für Windows Server 2003 veröffentlicht wurde. Diese Header Dateien sind auch als Teil eines MSDN-Abonnements oder durch Download enthalten.

    Der folgende Screenshot zeigt die Ergebnisse der Verwendung des *Checkv4.exe* Hilfsprogramms in der Datei simplec. c, die in Anhang A enthalten ist:

    ![checkv4.exe meldet die IPv6-Inkompatibilitäten in der simplec. c-Datei.](images/portingguide002.jpg)

    Der folgende Screenshot zeigt die Ergebnisse der Verwendung des *Checkv4.exe* -Hilfsprogramms für die Datei "simples. c", die auch in Anhang A enthalten ist:

    ![checkv4.exe meldet die IPv6-Inkompatibilitäten in der simples. c-Datei.](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>Der Anwendungs Änderungsprozess: Start Seite

Es gibt eine empfohlene Vorgehensweise für das Hinzufügen von IPv6-Funktionen zu Anwendungen. Das Befolgen dieser Sequenz ist vorteilhaft, da Entwickler sicherstellen können, dass alle erforderlichen Schritte zum Ändern einer vorhandenen IPv4-Anwendung zur Unterstützung von IPv6 erstellt werden. Bestimmte Anwendungen erfordern möglicherweise eine ausführlichere Aufmerksamkeit auf eine dieser Sequenzen. Beispielsweise würde ein-Systemdienst wahrscheinlich weniger Probleme mit der Benutzeroberfläche aufweisen als bei einem grafischen Dateiübertragungsprogramm (FTP).

**So ändern Sie IPv4-Anwendungen zur Unterstützung von IPv6**

1.  Korrektur von Strukturen und Deklarationen zum Aktivieren der IPv6-und IPv4-Kompatibilität.
2.  Ändern Sie Funktionsaufrufe, um von IPv6-aktivierten Funktionen zu profitieren, wie z. b. die Funktionen [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .
3.  Überprüfen Sie den Quellcode für die Verwendung von hart codierten IPv4-Adressen, z. b. der Loopback Adresse oder der Verwendung anderer Literalzeichenfolgen.
4.  Führen Sie eine gründliche Überprüfung der Benutzeroberfläche durch, einschließlich der Informations Dialogfelder. Denken Sie daran, ob es für IPv6-aktivierte Anwendungen geeignet ist, IP-Adress basierte Informationen anzugeben oder anzugeben.
5.  Stellen Sie fest, ob Ihre Anwendung von zugrunde liegenden Protokollen (z. b. RPC) abhängig ist, und nehmen Sie entsprechende programmgesteuerte Änderungen vor, um IPv6
6.  Verwenden Sie das Kompilierzeit-Flag IPV6STRICT beim Kompilieren von Anwendungen unter Windows XP und höher. Dieses Flag führt dazu, dass nicht kompatibler Code kompiliert wird, wie im folgenden dargestellt:

    Windows Sockets 1. x-Anwendungen mit inkompatiblem Code können nicht kompiliert werden, und die Fehlermeldung "Winsock2 required" wird zurückgegeben.

    Windows Sockets 2. x-Anwendungen mit inkompatiblem Code verursachen einen Kompilierzeitfehler für jede Instanz von inkompatiblem Code. Eine Fehlermeldung wird im folgenden Format generiert:

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Beispiel:

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



