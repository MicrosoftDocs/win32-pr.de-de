---
description: Ein Namespace bezieht sich auf eine Funktion, mit der (minimal) das Protokoll und die Adressierungs Attribute eines Netzwerk Dienstanbieter mit einem oder mehreren anzeigen Amen verknüpft werden können.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Namens Auflösungs Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb209254dcee2419e1ed92c017fc7d37dc9c0a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526150"
---
# <a name="name-resolution-model"></a>Namens Auflösungs Modell

Ein *Namespace* bezieht sich auf eine Funktion, mit der (minimal) das Protokoll und die Adressierungs Attribute eines Netzwerk Dienstanbieter mit einem oder mehreren anzeigen Amen verknüpft werden können. Viele Namespaces werden zurzeit verwendet, einschließlich der [Domain Name System](../dns/dns-start-page.md) des Internets (DNS), [Active Directory Domain Services](../ad/active-directory-domain-services.md), der Bindery, NetWare-Verzeichnisdienste (NDS) von Novell und X. 500. Diese Namespaces unterscheiden sich stark von der Organisation und Implementierung. Einige der Eigenschaften sind besonders wichtig, um aus Sicht der Winsock-Namensauflösung zu verstehen.

## <a name="types-of-namespaces"></a>Typen von Namespaces

Es gibt drei verschiedene Typen von Namespaces, in denen ein Dienst registriert werden kann:

-   Dynamisch
-   statischen
-   Beständig

Mithilfe dynamischer Namespaces können Dienste bei Bedarf beim Namespace registriert werden, und Clients können die verfügbaren Dienste zur Laufzeit ermitteln. Dynamische Namespaces basieren häufig auf Übertragungen, um die fortgesetzte Verfügbarkeit eines Netzwerk Dienstanbieter anzugeben. Zu den älteren Beispielen dynamischer Namespaces gehört der in einer NetWare-Umgebung verwendete Service Advertising Protocol (SAP)-Namespace und der von AppleTalk verwendete NBP-Namespace (Name Binding Protocol). Der PNRP-Namespace (Peer Name Resolution Protocol), der unter Windows verwendet wird, ist ein aktuelleres Beispiel für einen dynamischen Namespace.

Statische Namespaces erfordern, dass alle Dienste vorab registriert werden, d. h. wenn der Namespace erstellt wird. Ein Beispiel für einen statischen Namespace sind die *Hosts*, *Protokoll*-und *Dienst* Dateien, die von den meisten TCP/IP-Implementierungen verwendet werden. Unter Windows befinden sich diese Dateien in der Regel im Ordner *C: \\ Windows \\ system32 \\ Drivers \\ usw* .

Persistente Namespaces ermöglichen es Diensten, sich dynamisch bei dem Namespace zu registrieren. Im Gegensatz zu dynamischen Namespaces behalten persistente Namespaces jedoch die Registrierungsinformationen im nicht flüchtigen Speicher bei, wo Sie bis zu dem Zeitpunkt verbleibt, an dem der Dienst die Entfernung anfordert. Persistente Namespaces werden durch Verzeichnisdienste wie z. b. X. 500 und den NDS (NetWare-Verzeichnisdienst) typisierten. Diese Umgebungen ermöglichen das Hinzufügen, löschen und Ändern von Dienst Eigenschaften. Außerdem kann das Dienst Objekt, das den Dienst im Verzeichnisdienst darstellt, über eine Vielzahl von Attributen verfügen, die mit dem Dienst verknüpft sind. Das wichtigste Attribut für Client Anwendungen sind die Adressierungs Informationen des dienstanders. DNS ist ein weiteres Beispiel für einen persistenten Namespace. Obwohl es eine programmgesteuerte Methode zum Auflösen von DNS-Namen mithilfe von Windows Sockets gibt, unterstützt der DNS-Namespace Anbieter in Windows das Registrieren neuer DNS-Namen mit Winsock nicht. Sie müssen die DNS-Funktionen direkt verwenden, um DNS-Namen zu registrieren. Weitere Informationen finden Sie in der [DNS-Referenz](../dns/dns-reference.md).

## <a name="namespace-organization"></a>Namespace Organisation

Viele Namespaces sind hierarchisch angeordnet. Einige (z. b. X. 500 und NDS) ermöglichen eine unbegrenzte Schachtelung. Andere ermöglichen das Kombinieren von Diensten zu einer einzelnen Hierarchie-oder Gruppenebene. Dies wird in der Regel als *Arbeitsgruppe* bezeichnet. Beim Erstellen einer Abfrage ist es häufig erforderlich, einen Kontext Punkt innerhalb einer Namespace Hierarchie einzurichten, von der die Suche beginnt.

## <a name="namespace-provider-architecture"></a>Architektur von Namespace Anbietern

Natürlich unterscheiden sich die programmgesteuerten Schnittstellen, die verwendet werden, um die verschiedenen Typen von Namespaces abzufragen und um Informationen in einem Namespace zu registrieren (falls unterstützt). Bei einem *Namespace Anbieter* handelt es sich um eine lokal residente Software, die die Zuordnung zwischen dem Winsock-Namespace SPI und einigen vorhandenen Namespaces (die lokal implementiert werden können oder auf die über das Netzwerk zugegriffen werden kann). Die Architektur des Namespace Anbieters wird wie folgt veranschaulicht:

![Architektur von Namespace Anbietern](images/ovrvw3-1.png)

Beachten Sie, dass es für einen bestimmten Namespace, z. a. DNS, möglich ist, mehr als einen Namespace Anbieter auf einem bestimmten Computer zu installieren.

Wie bereits erwähnt, verweist der allgemeine Begriffs *Dienst* auf den Server-die Hälfte einer Client/Server-Anwendung. In Winsock ist ein Dienst einer *Dienstklasse* zugeordnet, und jede Instanz eines bestimmten Dienstanbieter verfügt über einen *Dienstnamen* , der innerhalb der Dienstklasse eindeutig sein muss. Beispiele für Dienst Klassen sind FTP-Server, SQL Server, XYZ Corp. Employee Info Server usw. Wie das Beispiel veranschaulicht, sind einige Dienst Klassen bekannt, während andere für eine bestimmte vertikale Anwendung eindeutig und spezifisch sind. In beiden Fällen wird jede Dienstklasse durch einen Klassennamen und einen Klassen Bezeichner dargestellt. Der Klassenname muss nicht unbedingt eindeutig sein, aber der Klassen Bezeichner muss lauten. GUID (Global Unique Identifier) werden zur Darstellung von Dienst Klassen bezeichnerbezeichnerverwendet. Für bekannte Dienste wurden Klassennamen und Klassen Bezeichner (GUIDs) vorab zugeordnet, und es stehen Makros für die Konvertierung zur Verfügung, z. b. TCP-Portnummern (in der Host-Byte-Reihenfolge) und die entsprechenden klassenbezeichnerguids. Für andere Dienste wählt der Entwickler den Klassennamen aus und verwendet das Uuidgen.exe Hilfsprogramm, um eine GUID für den Klassen Bezeichner zu generieren.

Der Begriff einer Dienstklasse gibt an, dass eine Gruppe von Attributen eingerichtet werden kann, die von allen Instanzen eines bestimmten dienstanzen gemeinsam gehalten werden. Dieser Satz von Attributen wird zu dem Zeitpunkt bereitgestellt, zu dem die Dienstklasse in Winsock definiert ist, und wird als Dienst Klassen Schema-Informationen bezeichnet. Wenn ein Dienst installiert und auf einem Host Computer verfügbar gemacht wird, wird dieser Dienst als *instanziiert* betrachtet, und der zugehörige Dienst Name wird verwendet, um eine bestimmte Instanz des Diensts von anderen Instanzen zu unterscheiden, die dem Namespace bekannt sein könnten.

Beachten Sie, dass die Installation einer Dienstklasse nur auf Computern erfolgen muss, auf denen der Dienst ausgeführt wird, und nicht auf allen Clients, die den Dienst verwenden können. Wenn möglich, stellt das Ws2- \_32.dll zu dem Zeitpunkt, zu dem eine Instanziierung eines Dienstanbieters registriert oder eine Dienst Abfrage initiiert wird, Schema Informationen für den Dienst dar. Die Ws2- \_32.dll speichert diese Informationen natürlich nicht selbst, sondern versucht, Sie von einem Namespace Anbieter abzurufen, der die Möglichkeit zur Bereitstellung dieser Daten angegeben hat. Da es keine Garantie gibt, dass der Ws2- \_32.dll das Dienst Klassen Schema bereitstellen kann, müssen Namespace Anbieter, die diese Informationen benötigen, über einen Fall Back Mechanismus verfügen, um ihn über Namespace spezifische Mittel zu erhalten.

Wie bereits erwähnt, hat das Internet das als Host zentrierte Dienstmodell zu bezeichnen. Anwendungen, die die Transport Adresse eines Diensts suchen müssen, müssen zunächst die Adresse eines bestimmten Hosts auflösen, der als Host für den Dienst bekannt ist. An diese Adresse fügen Sie die bekannte Portnummer hinzu und erstellen somit eine komplette Transport Adresse. Um die Auflösung von Hostnamen zu vereinfachen, wurde ein spezieller Dienst Klassen Bezeichner vorab zugeordnet (**svcid- \_ Hostname**). Eine Abfrage, die den **svcid- \_ Hostnamen** als Dienstklasse angibt und einen Hostnamen für den Dienst Instanznamen angibt, gibt die Host Adressinformationen zurück, wenn die Abfrage erfolgreich ist.

In Windows Sockets 2 müssen Anwendungen, die Protokoll unabhängig sind, die internen Details einer Transport Adresse nicht verstehen. Daher ist es problematisch, zuerst eine Host Adresse zu erhalten und dann den Port hinzuzufügen. Um dies zu vermeiden, können Abfragen auch den bekannten Namen eines bestimmten dienstanens und das Protokoll enthalten, über das der Dienst betrieben wird, z. b. FTP über TCP. In diesem Fall gibt eine erfolgreiche Abfrage eine komplette Transport Adresse für den angegebenen Dienst auf dem angegebenen Host zurück, und die Anwendung muss die internale einer [**sockaddr**](sockaddr-2.md) -Struktur nicht überprüfen.

Die Domain Name System des Internets verfügt nicht über ein klar definiertes Mittel zum Speichern von Schema Informationen für Dienst Klassen. Demzufolge können DNS-Namespace Anbieter für Winsock nur bekannte TCP/IP-Dienste unterstützen, für die eine Dienst Klassen-GUID vorab zugeordnet wurde.

In der Praxis ist dies keine ernsthafte Einschränkung, da Dienst Klassen-GUIDs für den gesamten Satz von TCP-und UDP-Ports vorab zugeordnet wurden und Makros verfügbar sind, um die GUID abzurufen, die einem beliebigen TCP-oder UDP-Port zugeordnet ist, wobei der Port in der Host-Byte-Reihenfolge ausgedrückt wird. Daher werden alle vertrauten Dienste wie http, FTP, Telnet, Whois usw. gut unterstützt.

Wenn wir mit unserem Dienst Klassen Beispiel fortfahren, können Instanznamen des FTP-Dienes "Alder.Intel.com" oder "FTP.Microsoft.com" lauten, während eine Instanz von "XYZ Corp. Employee Infoserver" den Namen "XYZ Corp. Employee Infoserver Version 3,5" hat.

In den ersten beiden Fällen wird der gewünschte Dienst durch die Kombination der Dienst Klassen-GUID für FTP und des Computer namens (angegeben als dienstinstanzname) eindeutig identifiziert. Im dritten Fall kann der Hostname, in dem sich der Dienst befindet, zum Zeitpunkt der Dienst Abfrage ermittelt werden, sodass der Dienst Instanzname keinen Hostnamen enthalten muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DNS-Verweis](../dns/dns-reference.md)
</dt> <dt>

[Datenstrukturen für die Namensauflösung](name-resolution-data-structures-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Zusammenfassung der namens Auflösungs Funktionen](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
