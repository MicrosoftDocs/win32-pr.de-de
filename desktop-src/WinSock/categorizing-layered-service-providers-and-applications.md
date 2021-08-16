---
title: Kategorisieren von mehrstufigen Dienstanbietern und Apps
description: Winsock 2 unterstützt mehrstufige Protokolle.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993b7a4003b87cf902b9daccbea4742a0bcd0760642429db79b1f1bb0a22600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322391"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Kategorisieren von mehrstufigen Dienstanbietern und Apps

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 und Windows Server 2012 [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Winsock 2 unterstützt mehrstufige Protokolle. Ein mehrstufiges Protokoll ist ein Protokoll, das nur Kommunikationsfunktionen höherer Ebene implementiert, während ein zugrunde liegender Transportstapel für den tatsächlichen Datenaustausch mit einem Remoteendpunkt verwendet wird. Ein Beispiel für ein mehrstufiges Protokoll oder einen mehrstufigen Dienstanbieter wäre eine Sicherheitsschicht, die dem Verbindungseinrichtungsprozess ein Protokoll hinzufügt, um die Authentifizierung durchzuführen und ein sich gegenseitig vereinbartes Verschlüsselungsschema einzurichten. Ein solches Sicherheitsprotokoll würde in der Regel die Dienste eines zugrunde liegenden zuverlässigen Transportprotokolls wie TCP oder SPX erfordern. Der Begriff Basisprotokoll, der vom Basisanbieter implementiert wird, bezieht sich auf einen Winsock-Anbieter, der ein Protokoll wie TCP oder SPX implementiert, das die Datenkommunikation mit einem Remoteendpunkt durchführen kann. Der Begriff mehrstufiges Protokoll wird verwendet, um ein Protokoll zu beschreiben, das nicht eigenständig sein kann. Diese mehrstufigen Protokolle werden als Winsock Layered Service Providers (LSPs) installiert.

Ein Beispiel für einen LSP ist der Microsoft Firewall-Clientdienstanbieter, der als Teil des Internetsicherheits- und Authentifizierungsservers (ISA) auf Clients installiert ist. Der Microsoft Firewall-Clientdienstanbieter installiert über die Winsock-Basisanbieter für TCP und UDP. Eine Dll (Dynamic Link Library) in der ISA-Firewallclientsoftware wird zu einem Winsock-dienstanbieter, der von allen Winsock-Anwendungen transparent verwendet wird. Auf diese Weise kann der ISA-Firewallclient-LSP Winsock-Funktionsaufrufe von Clientanwendungen abfangen und dann eine Anforderung an den ursprünglichen zugrunde liegenden Basisdienstanbieter weiterleiten, wenn das Ziel lokal ist, oder an den Firewalldienst auf einem ISA-Servercomputer, wenn das Ziel remote ist. Ein ähnlicher LSP wird als Teil des Microsoft Forefront Firewall Service und des Threat Management Gateway-Clients (TMG) auf Clients installiert.

Während der LSP-Initialisierung muss der LSP Zeiger auf eine Reihe von SPI-Funktionen (Winsock Service Provider Interface) bereitstellen. Diese Funktionen werden während der normalen Verarbeitung von der Ebene direkt über dem LSP aufgerufen (entweder ein anderer LSP- oder \_ Ws2-32.DLL).

Es ist möglich, LSP-Kategorien basierend auf der Teilmenge der SPI-Funktionen, die ein LSP implementiert, und der Art der zusätzlichen Verarbeitung zu definieren, die für jede dieser Funktionen ausgeführt wird. Durch Klassifizieren von LSPs und Klassifizieren von Anwendungen, die Winsock-Sockets verwenden, kann selektiv ermittelt werden, ob ein LSP zur Laufzeit an einem bestimmten Prozess beteiligt sein soll.

Auf Windows Vista und höher wird eine neue Methode zum Kategorisieren von Winsock Layered Service Providers und Anwendungen bereitgestellt, sodass nur bestimmte LSPs geladen werden. Es gibt mehrere Gründe für das Hinzufügen dieser Features.

Einer der Hauptgründe ist, dass bestimmte systemkritische Prozesse wie winlogon und lsass Sockets erstellen, aber diese Prozesse verwenden diese Sockets nicht, um Datenverkehr im Netzwerk zu senden. Daher sollten die meisten LSPs nicht in diese Prozesse geladen werden. Es wurde auch eine Reihe von Fällen dokumentiert, in denen fehlerhafte LSPs dazu führen *können, dasslsass.exe* abstürzt. Wenn lsass abstürzt, erzwingt das System das Herunterfahren. Ein Nebenauswirkung dieser Systemprozesse, die LSPs laden, besteht darin, dass diese Prozesse nie beendet werden. Wenn also ein LSP installiert oder entfernt wird, ist ein Neustart erforderlich.

Ein sekundärer Grund ist, dass es einige Fälle gibt, in denen Anwendungen bestimmte LSPs möglicherweise nicht laden möchten. Beispielsweise möchten einige Anwendungen möglicherweise keine kryptografischen LSPs laden, was verhindern könnte, dass die Anwendung mit anderen Systemen kommuniziert, auf denen der kryptografische LSP nicht installiert ist.

Schließlich können LSP-Kategorien von anderen LSPs verwendet werden, um zu bestimmen, wo sie in der Winsock-Protokollkette selbst installiert werden sollen. Seit Jahren möchten verschiedene LSP-Entwickler wissen, wie sich ein LSP verhält. Ein LSP, der den Datenstrom überprüft, möchte sich beispielsweise über einem LSP-System mit Verschlüsselung der Daten besächen. Natürlich ist diese Methode der LSP-Kategorisierung kein Beweis dafür, da sie sich von Drittanbieter-LSPs abhängig macht, um sich selbst entsprechend zu kategorisieren.

Die LSP-Kategorisierung und andere Sicherheitsverbesserungen in Windows Vista und höher sollen verhindern, dass Benutzer versehentlich schädliche LSPs installieren.

## <a name="lsp-categories"></a>LSP-Kategorien

Auf Windows Vista und höher kann ein LSP basierend auf der Interaktion mit Windows Sockets-Aufrufen und -Daten klassifiziert werden. Eine LSP-Kategorie ist eine identifizierbare Gruppe von Verhaltensweisen für eine Teilmenge von Winsock SPI-Funktionen. Beispielsweise wird ein HTTP-Inhaltsfilter als Dateninspektor (LSP \_ INSPECTOR-Kategorie) kategorisiert. Die \_ LSP INSPECTOR-Kategorie überprüft (aber nicht ändert) Parameter für SPI-Datenübertragungsfunktionen. Eine Anwendung kann die Kategorie eines LSP abfragen und den LSP basierend auf der LSP-Kategorie und den zulässigen LSP-Kategorien der Anwendung nicht laden.

In der folgenden Tabelle sind die Kategorien aufgeführt, in die ein LSP klassifiziert werden kann.

| LSP-Kategorie              | Beschreibung                                                     |
|---------------------------|-----------------------------------------------------------------|
| **LSP \_ CRYPTO \_ COMPRESS** | Der LSP ist ein Kryptografie- oder Datenkomprimierungsanbieter.         |
| **\_LSP-FIREWALL**         | Der LSP ist ein Firewallanbieter.                                 |
| **LSP \_ LOCAL \_ CACHE**     | Der LSP ist ein lokaler Cacheanbieter.                              |
| **LSP \_ INBOUND \_ MODIFY**  | Der LSP ändert eingehende Daten.                                  |
| **LSP \_ INSPECTOR**        | Der LSP überprüft oder filtert Daten.                               |
| **LSP \_ OUTBOUND \_ MODIFY** | Der LSP ändert ausgehende Daten.                                 |
| **\_LSP-PROXY**            | Der LSP fungiert als Proxy und leitet Pakete um.                  |
| **\_LSP-REDIRECTOR**       | Der LSP ist ein Netzwerkumleitungsserver.                                |
| **LSP \_ SYSTEM**           | Der LSP ist für die Verwendung in Diensten und Systemprozessen akzeptabel. |



 

Ein LSP kann zu mehreren Kategorien gehören. Beispielsweise könnte ein Firewall-/Sicherheits-LSP sowohl zu den Kategorien inspector (**LSP \_ INSPECTOR**) als auch firewall (**LSP \_ FIREWALL**) gehören.

Wenn für einen LSP keine Kategorie festgelegt ist, wird er als in der Kategorie Alle anderen betrachtet. Diese LSP-Kategorie wird nicht in Dienste oder Systemprozesse geladen (z. B. lsass, winlogon und viele svchost-Prozesse).

## <a name="categorizing-lsps"></a>Kategorisieren von LSPs

Auf Windows Vista und höher sind mehrere neue Funktionen zum Kategorisieren eines LSP verfügbar:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Um einen LSP zu kategorisieren, wird die [**Funktion WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) oder [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) mit einer GUID aufgerufen, um den ausgeblendeten LSP-Eintrag, die Für diesen LSP-Protokolleintrag festzulegende Informationsklasse und einen Satz von Flags zum Ändern des Verhaltens der Funktion zu identifizieren.

Die [**WSCGetProviderInfo-**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) oder [**WSCGetProviderInfo32-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) wird auf ähnliche Weise verwendet, um die Daten abzurufen, die einer Informationsklasse für einen LSP zugeordnet sind.

## <a name="categorizing-applications"></a>Kategorisieren von Anwendungen

Für Windows Vista und höher stehen mehrere neue Funktionen zum Kategorisieren einer Anwendung zur Verfügung:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Um eine Anwendung zu kategorisieren, wird die [**WSCSetApplicationCategory-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) mit dem Ladepfad zum ausführbaren Image aufgerufen, um die Anwendung, die beim Starten der Anwendung verwendeten Befehlszeilenargumente und die LSP-Kategorien zu identifizieren, die für alle Instanzen dieser Anwendung zulässig sind.

Die [**WSCGetApplicationCategory-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) wird auf ähnliche Weise zum Abrufen der LSP-Kategorien (Layered Service Provider) verwendet, die einer Anwendung zugeordnet sind.

## <a name="determining-which-lsps-get-loaded"></a>Bestimmen, welche LSPs geladen werden

Der letzte Teil der LSP-Kategorisierung besteht darin, zu bestimmen, welche LSPs in welche Prozesse geladen werden. Wenn ein Prozess Winsock lädt, werden die folgenden Vergleiche der Anwendungskategorie und der LSP-Kategorien für alle installierten LSPs durchgeführt:

-   Wenn die Anwendung nicht kategorisiert ist, lassen Sie zu, dass alle LSPs in den Prozess geladen werden.
-   Wenn sowohl die Anwendung als auch der LSP Kategorien zugewiesen haben, muss Folgendes zutreffen: <dl> Mindestens eine der LSP-Kategorien ist in den angegebenen Kategorien der Anwendung vorhanden.  
    In den LSPs-Kategorien werden nur Kategorien angegeben, die in den angegebenen Kategorien der Anwendung angegeben sind. Wenn die Anwendung beispielsweise eine Kategorie angibt, muss sie in der Kategorie des LSP liegen.  
    Wenn die \_ LSP-Systemkategorie in der Kategorie der Anwendung vorhanden ist, muss sie in den Kategorien des LSP vorhanden sein.  
    </dl>

> [!Note]  
> Wenn ein LSP nicht kategorisiert ist, ist seine Kategorie effektiv 0 (null). Damit eine Übereinstimmung auftritt, müssen alle angegebenen LSP-Kategorien in den Kategorien der Anwendung vorhanden sein (die Kategorien der Anwendung müssen eine Obermenge der LSP-Kategorien sein), wobei der Nachteil besteht, dass LSP SYSTEM auch in der Kategorie des LSP vorhanden sein muss, wenn LSP \_ SYSTEM in der Kategorie der Anwendung vorhanden ist.

 

Betrachten Sie das folgenden Beispiel:

Die *Foo.exe* Anwendung wird als LSP \_ SYSTEM + LSP FIREWALL + LSP CRYPTO COMPRESS kategorisiert. \_ \_ \_ Die Anwendung *Bar.exe* wird als LSP \_ FIREWALL + LSP CRYPTO COMPRESS kategorisiert. \_ \_ Auf dem System sind vier LSPs installiert:

-   LSP1 hat eine Kategorie von LSP \_ SYSTEM festgelegt.
-   LSP2 ist kein Kategoriensatz, sodass die Kategorie 0 (null) ist.
-   LSP3 hat eine Kategorie von LSP \_ FIREWALL festgelegt.
-   LSP4 verfügt über festgelegte Kategorien von LSP \_ SYSTEM + LSP \_ FIREWALL + LSP CRYPTO COMPRESS \_ + \_ LSP \_ INSPECTOR

In diesem Beispiel würde die *Foo.exe* Anwendung nur LSP1 laden, während die *Bar.exe* Anwendung LSP3 laden würde.

## <a name="determining-winsock-providers-installed"></a>Bestimmen der installierten Winsock-Anbieter

Das Microsoft Windows Software Development Kit (SDK) enthält ein Winsock-Beispielprogramm, mit dem die auf einem lokalen Computer installierten Winsock-Transportanbieter bestimmt werden können. Standardmäßig wird der Quellcode für dieses Winsock-Beispiel im folgenden Verzeichnis des Windows SDK für Windows 7 installiert:

*C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock \\ LSP*

Dieses Beispiel ist ein Hilfsprogramm zum Installieren und Testen von mehrschichtigen Dienstanbietern. Sie kann jedoch auch verwendet werden, um programmgesteuert detaillierte Informationen aus dem Winsock-Katalog auf einem lokalen Computer zu sammeln. Erstellen Sie dieses Winsock-Beispiel, und führen Sie den folgenden Konsolenbefehl aus, um alle aktuellen Winsock-Anbieter, einschließlich Basisanbieter und Layer-Dienstanbieter, auflisten zu können:

**instlsp -p**

Die Ausgabe ist eine Liste der winsock-Anbieter, die auf dem lokalen Computer installiert sind, einschließlich mehrschichtiger Dienstanbieter. In der Ausgabe werden die Katalog-ID und der Zeichenfolgenname für den Winsock-Anbieter aufgeführt.

Führen Sie den folgenden Konsolenbefehl aus, um ausführlichere Informationen zu allen Winsock-Anbietern zu sammeln:

**instlsp -p -v**

Die Ausgabe ist eine Liste der [**WSAPROTOCOL \_ INFO-Strukturen,**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) die auf dem lokalen Computer unterstützt werden.

Führen Sie den folgenden Konsolenbefehl aus, um eine Liste mit nur mehrschichtigen Dienstanbietern auf dem lokalen Computer zu erhalten:

**instlsp -l**

Führen Sie zum Zuordnen der LSP-Struktur den folgenden Konsolenbefehl aus:

**instlsp -m**

> [!Note]  
> Das TDI-Feature ist veraltet und wird in zukünftigen Versionen von Microsoft Windows. Verwenden Sie je nach Verwendung von TDI entweder den Winsock Kernel (WSK) oder Windows Filtering Platform (WFP). Weitere Informationen zu WFP und WSK finden Sie unter Windows [Filtering Platform](../fwp/windows-filtering-platform-start-page.md) und [Winsock Kernel](/windows-hardware/drivers/ddi/_netvista/). Einen Blogeintrag Windows Core Networking zu WSK und TDI finden Sie unter [Introduction to Winsock Kernel (WSK) (Einführung in Winsock Kernel (WSK)).](/archive/blogs/wndp/)

 

 

 
