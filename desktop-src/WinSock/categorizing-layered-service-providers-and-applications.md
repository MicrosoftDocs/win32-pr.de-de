---
title: Kategorisierung von geschichteten Dienstanbietern und Apps
description: Winsock 2 bietet mehrstufige Protokolle.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a966d54da0be26f75a074de18abe1b9e080c0c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348391"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Kategorisierung von geschichteten Dienstanbietern und Apps

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Winsock 2 bietet mehrstufige Protokolle. Bei einem geschichteten Protokoll handelt es sich um einen, der nur Kommunikationsfunktionen auf höherer Ebene implementiert, während er sich auf einen zugrunde liegenden Transport Stapel für den eigentlichen Datenaustausch mit einem Remote Endpunkt stützt. Ein Beispiel für ein geschichtetes Protokoll oder einen überlappenden Dienstanbieter wäre eine Sicherheitsebene, die dem Verbindungs Einrichtungsprozess ein Protokoll hinzufügt, um die Authentifizierung durchzuführen und ein einvernehmlich vereinbartes Verschlüsselungsschema einzurichten. Ein solches Sicherheitsprotokoll erfordert im Allgemeinen die Dienste eines zugrunde liegenden zuverlässigen Transport Protokolls, z. b. TCP oder SPX. Der vom Basis Anbieter implementierte Begriff "Basisprotokoll" bezieht sich auf einen Winsock-Anbieter, der ein Protokoll wie TCP oder SPX implementiert, das die Datenkommunikation mit einem Remote Endpunkt durchführen kann. Der Begriff "geschichtetes Protokoll" wird verwendet, um ein Protokoll zu beschreiben, das nicht allein stehen kann. Diese geschichteten Protokolle werden als Windows-überlappende Dienstanbieter (LSPs) installiert.

Ein Beispiel für einen LSP ist der Microsoft Firewall-Client Dienstanbieter, der als Teil von Internet secutity and Authentication Server (ISA) auf Clients installiert ist. Der Microsoft Firewall-Client Dienstanbieter installiert über die Winsock-Basis Anbieter für TCP und UDP. Eine Dynamic Link Library (dll) in der ISA Firewall-Client Software wird zu einem von Winsock geschichteten Dienstanbieter, der von allen Winsock-Anwendungen transparent verwendet wird. Auf diese Weise kann der ISA Firewall-Client-LSP Winsock-Funktionsaufrufe von Client Anwendungen abfangen und dann eine Anforderung an den ursprünglichen zugrunde liegenden Basis Dienstanbieter weiterleiten, wenn das Ziel lokal ist, oder auf den Firewalldienst auf einem ISA Server-Computer, wenn das Ziel Remote ist. Ein ähnliches LSP wird als Teil des Microsoft Forefront Firewall-Diensts und des Threat Management Gateway (TMG)-Clients auf Clients installiert.

Während der LSP-Initialisierung muss der LSP Zeiger auf eine Reihe von Funktionen der Winsock-Dienstanbieter Schnittstelle (SPI) bereitstellen. Diese Funktionen werden während der normalen Verarbeitung durch die Ebene direkt oberhalb des LSP (entweder eine andere LSP-oder Ws2- \_32.DLL) aufgerufen.

Es ist möglich, LSP-Kategorien basierend auf der Teilmenge der von LSP implementierten SPI-Funktionen und der Art der zusätzlichen Verarbeitung für jede dieser Funktionen zu definieren. Durch die Klassifizierung von LSPs und die Klassifizierung von Anwendungen, die Winsock-Sockets verwenden, ist es möglich, selektiv festzustellen, ob ein LSP an einem bestimmten Prozess zur Laufzeit beteiligt sein soll.

Unter Windows Vista und höher wird eine neue Methode zum kategorialisieren von Windows-überlappenden Dienstanbietern und Anwendungen bereitgestellt, sodass nur bestimmte LSPs geladen werden. Es gibt mehrere Gründe für das Hinzufügen dieser Features.

Einer der Hauptgründe dafür ist, dass bestimmte kritische System Prozesse wie Winlogon und LSASS Sockets erstellen, diese jedoch nicht zum Senden von Datenverkehr im Netzwerk verwendet werden. Die meisten LSPs sollten daher nicht in diese Prozesse geladen werden. Eine Reihe von Fällen wurde auch dokumentiert, wenn fehlerhafte LSPs dazu führen können, dass *lsass.exe* abstürzen. Wenn LSASS abstürzt, erzwingt das System ein Herunterfahren. Eine Nebenwirkung dieser System Prozesse beim Laden von LSPs besteht darin, dass diese Prozesse nie beendet werden, wenn ein LSP installiert oder entfernt wird, ist ein Neustart erforderlich.

Ein sekundärer Grund ist, dass Anwendungen bestimmte LSPs möglicherweise nicht laden möchten. Beispielsweise möchten einige Anwendungen möglicherweise kryptografielsps nicht laden. Dies könnte verhindern, dass die Anwendung mit anderen Systemen kommuniziert, auf denen kein "Installat-LSP" installiert ist.

Schließlich können LSP-Kategorien von anderen LSPs verwendet werden, um zu bestimmen, an welcher Stelle in der Winsock-Protokoll Kette Sie selbst installiert werden sollen. Jahrelang wollten verschiedene LSP-Entwickler wissen, wie sich ein LSP verhält. Beispielsweise sollte ein LSP, der den Datenstrom überprüft, über einem LSP sein, der die Daten verschlüsselt. Diese Methode der LSP-Kategorisierung ist natürlich nicht trügerisch, da Sie von Drittanbieter-LSPs abhängig ist, um sich entsprechend zu kategorisieren.

Die LSP-Kategorisierung und andere Sicherheitsverbesserungen in Windows Vista und höher wurden entwickelt, um Benutzer daran zu hindern, böswillige LSPs versehentlich zu installieren.

## <a name="lsp-categories"></a>LSP-Kategorien

Unter Windows Vista und höher kann ein LSP basierend auf der Interaktion mit Windows Sockets-aufrufen und-Daten klassifiziert werden. Eine LSP-Kategorie ist eine identifizierbare Gruppe von Verhalten für eine Teilmenge der Winsock-SPI-Funktionen. Beispielsweise wird ein HTTP-Inhaltsfilter als Daten Inspektor kategorisiert (die Kategorie LSP \_ Inspector). Die Kategorie LSP \_ Inspector prüft (aber nicht ändern) Parameter für die SPI-Funktionen der Datenübertragung. Eine Anwendung kann die Kategorie eines LSP Abfragen und das LSP nicht auf der Grundlage der LSP-Kategorie und des Satzes zulässiger LSP-Kategorien der Anwendung laden.

In der folgenden Tabelle sind die Kategorien aufgeführt, in die ein LSP klassifiziert werden kann.

| LSP-Kategorie              | BESCHREIBUNG                                                     |
|---------------------------|-----------------------------------------------------------------|
| **LSP \_ - \_ kryptografiekomprimieren** | Der LSP ist ein Kryptografieanbieter oder Daten Komprimierungs Anbieter.         |
| **LSP- \_ Firewall**         | Der LSP ist ein Firewall-Anbieter.                                 |
| **lokaler LSP- \_ \_ Cache**     | Der LSP ist ein lokaler Cache Anbieter.                              |
| **eingehende LSP- \_ \_ Änderung**  | Der LSP ändert eingehende Daten.                                  |
| **LSP- \_ Inspektor**        | Der LSP überprüft oder filtert Daten.                               |
| **ausgehende LSP- \_ \_ Änderung** | Der LSP ändert ausgehende Daten.                                 |
| **LSP- \_ Proxy**            | Der LSP fungiert als Proxy und leitet Pakete um.                  |
| **LSP- \_ Redirector**       | Der LSP ist ein Netzwerkredirector.                                |
| **LSP- \_ System**           | Der LSP ist für die Verwendung in Diensten und System Prozessen zulässig. |



 

Ein LSP kann zu mehr als einer Kategorie gehören. Beispielsweise könnte eine Firewall/Sicherheit-LSP sowohl zur Inspektor (**LSP \_ Inspector**) als auch zur Firewall-Kategorie (**LSP- \_ Firewall**) gehören.

Wenn ein LSP keinen Kategoriesatz hat, gilt er als in der Kategorie alle anderen. Diese LSP-Kategorie wird nicht in Dienste oder System Prozesse geladen (z. b. LSASS, Winlogon und viele svchost-Prozesse).

## <a name="categorizing-lsps"></a>Kategorisierung von LSPs

Zum kategorialisieren eines LSP sind unter Windows Vista und höher mehrere neue Funktionen verfügbar:

-   [**Wscgetproviderinfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**Wscsetproviderinfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Zum Kategorisieren eines LSP wird die [**wscsetproviderinfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) -Funktion oder die [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) -Funktion mit einer GUID aufgerufen, um den ausgeblendeten LSP-Eintrag zu identifizieren, die Informations Klasse, die für diesen LSP-Protokolleintrag festgelegt werden soll, und einen Satz von Flags, die verwendet werden, um das Verhalten der Funktion zu ändern.

Die [**wscgetproviderinfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) -Funktion oder die [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) -Funktion wird auf ähnliche Weise verwendet, um die Daten abzurufen, die einer Informations Klasse für einen LSP zugeordnet sind.

## <a name="categorizing-applications"></a>Kategorisierung von Anwendungen

Zum kategorialisieren einer Anwendung sind unter Windows Vista und höher mehrere neue Funktionen verfügbar:

-   [**Wscgetapplicationcategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**Wscabtapplicationcategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Um eine Anwendung zu kategorisieren, wird die [**wscsetapplicationcategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) -Funktion mit dem Ladepfad zum ausführbaren Image aufgerufen, um die Anwendung, die Befehlszeilenargumente, die beim Starten der Anwendung verwendet werden, und die LSP-Kategorien, die für alle Instanzen dieser Anwendung zulässig sind, zu identifizieren.

Die [**wscgetapplicationcategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) -Funktion wird auf ähnliche Weise verwendet, um die einer Anwendung zugeordneten LSP-Kategorien (geschichteter Dienstanbieter) abzurufen.

## <a name="determining-which-lsps-get-loaded"></a>Bestimmen, welche LSPs geladen werden

Der letzte Teil der LSP-Kategorisierung ist die Festlegung, welche LSPs in welche Prozesse geladen werden. Wenn Winsock von einem Prozess geladen wird, werden die folgenden Vergleiche aus der Anwendungskategorie und den LSP-Kategorien für alle installierten LSPs vorgenommen:

-   Wenn die Anwendung nicht kategorisiert ist, lassen Sie alle LSPs in den Prozess laden.
-   Wenn sowohl die Anwendung als auch der LSP Kategorien zugewiesen haben, muss Folgendes erfüllt sein: <dl> Mindestens eine der LSP-Kategorien ist in den angegebenen Kategorien der Anwendung vorhanden.  
    In den LSPs-Kategorien werden nur Kategorien angegeben, die in den angegebenen Kategorien der Anwendung angegeben sind. Wenn die Anwendung z. b. eine Kategorie angibt, muss Sie in der Kategorie des LSP angegeben werden.  
    Wenn die LSP \_ -System Kategorie in der Kategorie der Anwendung vorhanden ist, muss Sie in den LSP-Kategorien vorhanden sein.  
    </dl>

> [!Note]  
> Wenn ein LSP nicht kategorisiert wird, ist die zugehörige Kategorie tatsächlich NULL. Damit eine Entsprechung vorliegt, müssen alle angegebenen LSP-Kategorien in den Kategorien der Anwendung vorhanden sein (die Kategorien der Anwendung müssen eine übergeordnete Kategorie der LSP-Kategorien sein), wobei der Nachteil ist, dass das LSP- \_ System in der Kategorie der Anwendung auch in der Kategorie des LSP vorhanden sein muss, wenn das LSP-System in der Kategorie der Anwendung vorhanden ist.

 

Betrachten Sie das folgenden Beispiel:

Die *Foo.exe* -Anwendung wird als LSP \_ System + LSP \_ Firewall + LSP \_ Crypto \_ Compress kategorisiert. Die Anwendungs *Bar.exe* wird als LSP- \_ Firewall und LSP \_ - \_ kryptografiekomprimierung kategorisiert. Auf dem System sind vier LSPs installiert:

-   LSP1 hat eine Kategorie LSP-System festgelegt \_ .
-   LSP2 ist nicht als Kategorien festgelegt, sodass die Kategorie 0 (null) ist.
-   LSP3 hat eine Kategorie der LSP- \_ Firewall festgelegt.
-   LSP4 hat festgelegte Kategorien LSP \_ System + LSP \_ Firewall + LSP \_ Crypto \_ Compress + LSP \_ Inspector

In diesem Beispiel würde die *Foo.exe* Anwendung nur LSP1 laden, während die *Bar.exe* Anwendung LSP3 laden würde.

## <a name="determining-winsock-providers-installed"></a>Ermitteln der installierten Winsock-Anbieter

Das Microsoft Windows Software Development Kit (SDK) enthält ein Winsock-Beispielprogramm, das verwendet werden kann, um die auf einem lokalen Computer installierten Winsock-Transportanbieter zu bestimmen. Standardmäßig wird der Quellcode für dieses Winsock-Beispiel im folgenden Verzeichnis der Windows SDK für Windows 7 installiert:

*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ Winsock \\ LSP*

Dieses Beispiel ist ein Hilfsprogramm zum Installieren und Testen von geschichteten Dienstanbietern. Sie kann jedoch auch verwendet werden, um detaillierte Informationen aus dem Winsock-Katalog auf einem lokalen Computerprogramm gesteuert zu erfassen. Um alle aktuellen Winsock-Anbieter einschließlich der Basis Anbieter und der ebenendienstanbieter aufzulisten, erstellen Sie dieses Winsock-Beispiel, und führen Sie den folgenden Konsolen Befehl aus:

**INSTLSP-p**

Bei der Ausgabe handelt es sich um eine Liste der auf dem lokalen Computer installierten Winsock-Anbieter, einschließlich der mehrstufigen Dienstanbieter. In der Ausgabe werden die Katalog-ID und der Zeichen folgen Name für den Winsock-Anbieter aufgelistet.

Um ausführlichere Informationen zu allen Winsock-Anbietern zu erfassen, führen Sie den folgenden Konsolen Befehl aus:

**INSTLSP-p-v**

Bei der Ausgabe handelt es sich um eine Liste der auf dem lokalen Computer unterstützten [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen.

Führen Sie den folgenden Konsolen Befehl aus, um eine Liste der nur auf dem lokalen Computer installierten Dienstanbieter aufzulisten:

**INSTLSP-l**

Um die LSP-Struktur zuzuordnen, führen Sie den folgenden Konsolen Befehl aus:

**INSTLSP-m**

> [!Note]  
> Das TDI-Feature ist veraltet und wird in zukünftigen Versionen von Microsoft Windows entfernt. Je nachdem, wie Sie TDI verwenden, verwenden Sie entweder den Winsock Kernel (WSK) oder die Windows-Filter Plattform (WFP). Weitere Informationen zu WFP und WSK finden Sie unter [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md) und [Winsock-Kernel](/windows-hardware/drivers/ddi/_netvista/). Einen Blogeintrag zu WSK und TDI in Windows Core Network finden [Sie unter Einführung in Winsock Kernel (WSK)](/archive/blogs/wndp/).

 

 

 
