---
description: Ein Namespace bezieht sich auf eine Funktion zum Zuordnen (mindestens) des Protokolls und der Adressierungsattribute eines Netzwerkdiensts zu mindestens einem Benutzernamen.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Namensauflösungsmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23395cc6db5a93ec572f59e0d5ac6aaa7890c5c42a7966b86601eb190a54796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822781"
---
# <a name="name-resolution-model"></a>Namensauflösungsmodell

Ein *Namespace* bezieht sich auf eine Funktion zum Zuordnen (mindestens) des Protokolls und der Adressierungsattribute eines Netzwerkdiensts zu mindestens einem Benutzernamen. Viele Namespaces werden derzeit verwendet, z.B. das [Domain Name System](../dns/dns-start-page.md) (DNS), [Active Directory Domain Services,](../ad/active-directory-domain-services.md)die Bindery, NetWare-Verzeichnisdienste (NDS) von und X.500. Diese Namespaces unterscheiden sich stark in ihrer Organisation und Ihrer Umsetzung. Einige ihrer Eigenschaften sind aus Sicht der Winsock-Namensauflösung besonders wichtig zu verstehen.

## <a name="types-of-namespaces"></a>Namespacetypen

Es gibt drei verschiedene Arten von Namespaces, in denen ein Dienst registriert werden kann:

-   Dynamisch
-   statischen
-   Beständig

Dynamische Namespaces ermöglichen es Diensten, sich dynamisch beim Namespace zu registrieren und clients zur Laufzeit die verfügbaren Dienste zu entdecken. Dynamische Namespaces basieren häufig auf Broadcasts, um die weitere Verfügbarkeit eines Netzwerkdiensts anzugeben. Ältere Beispiele für dynamische Namespaces sind der SAP-Namespace (Service Advertising Protocol), der in einer NetWare-Umgebung verwendet wird, und der Namespace des Namensbindungsprotokolls (Name Binding Protocol, NBP), der von AppleTalk verwendet wird. Der PNRP-Namespace (Peer Name Resolution Protocol), der für Windows verwendet wird, ist ein aktuelleres Beispiel für einen dynamischen Namespace.

Statische Namespaces erfordern, dass alle Dienste im Voraus registriert werden, d.&a; wenn der Namespace erstellt wird. Ein Beispiel für einen statischen Namespace  sind die *Host-,* Protokoll- und Dienstdateien, die von den meisten TCP/IP-Implementierungen verwendet werden. Auf Windows befinden sich diese Dateien in der Regel im Ordner *C: \\ Windows \\ System32-Treiber \\ \\ usw.*

Persistente Namespaces ermöglichen es Diensten, sich während der Zeit beim Namespace zu registrieren. Im Gegensatz zu dynamischen Namespaces behalten persistente Namespaces die Registrierungsinformationen jedoch in einem nicht permanenten Speicher bei, in dem sie so lange beibehalten werden, bis der Dienst anfing, sie zu entfernen. Persistente Namespaces werden von Verzeichnisdiensten wie X.500 und dem NDS (NetWare Directory Service) typisiert. Diese Umgebungen ermöglichen das Hinzufügen, Löschen und Ändern von Diensteigenschaften. Darüber hinaus kann das Dienstobjekt, das den Dienst innerhalb des Verzeichnisdiensts darstellt, über eine Vielzahl von Attributen verfügen, die dem Dienst zugeordnet sind. Das wichtigste Attribut für Clientanwendungen sind die Adressierungsinformationen des Diensts. DNS ist ein weiteres Beispiel für einen persistenten Namespace. Obwohl es eine programmgesteuerte Möglichkeit gibt, DNS-Namen mithilfe von Windows Sockets aufzulösen, unterstützt der DNS-Namespaceanbieter in Windows die Registrierung neuer DNS-Namen mit Winsock nicht. Sie müssen die DNS-Funktionen direkt verwenden, um DNS-Namen zu registrieren. Weitere Informationen finden Sie in der [DNS-Referenz.](../dns/dns-reference.md)

## <a name="namespace-organization"></a>Namespaceorganisation

Viele Namespaces sind hierarchisch angeordnet. Einige, z. B. X.500 und NDS, ermöglichen eine unbegrenzte Schachtelung. Andere ermöglichen die Kombination von Diensten in einer einzelnen Hierarchie- oder Gruppenebene. Dies wird in der Regel als Arbeitsgruppe *bezeichnet.* Beim Erstellen einer Abfrage ist es häufig erforderlich, einen Kontextpunkt innerhalb einer Namespacehierarchie zu erstellen, ab der die Suche beginnt.

## <a name="namespace-provider-architecture"></a>Architektur des Namespaceanbieters

Natürlich unterscheiden sich die programmgesteuerten Schnittstellen, die zum Abfragen der verschiedenen Namespacetypen und zum Registrieren von Informationen innerhalb eines Namespace (sofern unterstützt) verwendet werden, stark. Ein *Namespaceanbieter* ist eine lokal gespeicherte Software, die weiß, wie zwischen der Winsock-Namespace-SPI und einem vorhandenen Namespace (der lokal implementiert werden oder über das Netzwerk darauf zugegriffen werden kann) zuordnen kann. Die Architektur des Namespaceanbieters wird wie folgt veranschaulicht:

![Architektur des Namespaceanbieters](images/ovrvw3-1.png)

Beachten Sie, dass für einen bestimmten Namespace, z. B. DNS, mehrere Namespaceanbieter auf einem bestimmten Computer installiert sein können.

Wie bereits erwähnt, bezieht sich der generische Begriff *Dienst* auf die Serverhälfte einer Client-/Serveranwendung. In Winsock ist ein Dienst einer Dienstklasse zugeordnet, und jede  Instanz eines bestimmten Diensts hat einen Dienstnamen, der innerhalb der Dienstklasse eindeutig sein muss. Beispiele für Dienstklassen sind FTP-Server, SQL Server, XYZ Corp. Employee Info Server usw. Wie im Beispiel veranschaulicht wird, sind einige Dienstklassen bekannt, während andere eindeutig und spezifisch für eine bestimmte vertikale Anwendung sind. In beiden Fällen wird jede Dienstklasse sowohl durch einen Klassennamen als auch durch einen Klassenbezeichner dargestellt. Der Klassenname muss nicht unbedingt eindeutig sein, aber der Klassenbezeichner muss sein. Globally Unique Identifiers (GUIDs) werden verwendet, um Dienstklassenbezeichner zu darstellen. Für bekannte Dienste wurden Klassennamen und Klassenbezeichner (GUIDs) vorab zugewiesen, und Makros können z. B. zwischen TCP-Portnummern (in Host-Byte-Reihenfolge) und den entsprechenden Klassenbezeichner-GUIDs konvertiert werden. Bei anderen Diensten wählt der Entwickler den Klassennamen aus und verwendet das Hilfsprogramm Uuidgen.exe, um eine GUID für den Klassenbezeichner zu generieren.

Das Konzept einer Dienstklasse ist vorhanden, um die Einrichtung einer Gruppe von Attributen zu ermöglichen, die von allen Instanzen eines bestimmten Diensts gemeinsam verwendet werden. Dieser Attributsatz wird zum Zeitpunkt der Definition der Dienstklasse für Winsock bereitgestellt und als Schemainformationen der Dienstklasse bezeichnet. Wenn ein Dienst auf einem Hostcomputer installiert und verfügbar gemacht wird, wird dieser Dienst als *instanziiert* betrachtet, und sein Dienstname wird verwendet, um eine bestimmte Instanz des Diensts von anderen Instanzen zu unterscheiden, die dem Namespace bekannt sein können.

Beachten Sie, dass die Installation einer Dienstklasse nur auf Computern erfolgen muss, auf denen der Dienst ausgeführt wird, nicht auf allen Clients, die den Dienst möglicherweise nutzen. Nach Möglichkeit stellt die Ws2-32.dll Dienstklassenschemainformationen für einen Namespaceanbieter zur Verfügung, wenn eine Instanziierung eines Diensts registriert oder eine Dienstabfrage \_ initiiert wird. Der Ws232.dll speichert diese Informationen natürlich nicht selbst, sondern versucht, sie von einem Namespaceanbieter abzurufen, der seine Fähigkeit zur Bereitstellung dieser \_ Daten angegeben hat. Da es keine Garantie gibt, dass die Ws2-32.dll das Dienstklassenschema angeben kann, müssen Namespaceanbieter, die diese Informationen benötigen, über einen Fallbackmechanismus verfügen, um sie mit namespacespezifischen Mittel \_ zu erhalten.

Wie bereits erwähnt, hat das Internet ein sogenanntes hostzentriertes Dienstmodell übernommen. Anwendungen, die die Transportadresse eines Diensts suchen müssen, müssen in der Regel zuerst die Adresse eines bestimmten Hosts auflösen, der als Host für den Dienst bekannt ist. Zu dieser Adresse fügen sie die bekannte Portnummer hinzu und erstellen daher eine vollständige Transportadresse. Um die Auflösung von Hostnamen zu vereinfachen, wurde ein spezieller Dienstklassenbezeichner vorab zugewiesen (**SVCID \_ HOSTNAME**). Eine Abfrage, die **SVCID \_ HOSTNAME** als Dienstklasse und einen Hostnamen für den Dienstinstanznamen angibt, gibt Hostadresseninformationen zurück, wenn die Abfrage erfolgreich ist.

In Windows Sockets 2 sollten protokollunabhängige Anwendungen vermeiden, die internen Details einer Transportadresse zu verstehen. Daher ist es problematisch, zuerst eine Hostadresse zu erhalten und dann im Port hinzuzufügen. Um dies zu vermeiden, können Abfragen auch den bekannten Namen eines bestimmten Diensts und das Protokoll enthalten, über das der Dienst ausgeführt wird, z. B. FTP über TCP. In diesem Fall gibt eine erfolgreiche Abfrage eine vollständige Transportadresse für den angegebenen Dienst auf dem angegebenen Host zurück, und die Anwendung muss die Internen einer [**Sockaddr-Struktur nicht**](sockaddr-2.md) überprüfen.

Die Internet-Domain Name System verfügt nicht über eine klar definierte Möglichkeit zum Speichern von Dienstklassenschemainformationen. Daher können DNS-Namespaceanbieter für Winsock nur bekannte TCP/IP-Dienste aufnehmen, für die eine Dienstklassen-GUID vorab zugewiesen wurde.

In der Praxis ist dies keine schwerwiegende Einschränkung, da Dienstklassen-GUIDs für den gesamten Satz von TCP- und UDP-Ports vorab zugeordnet wurden und Makros verfügbar sind, um die GUID abzurufen, die jedem TCP- oder UDP-Port mit dem Port zugeordnet ist, der in der Host-Byte-Reihenfolge ausgedrückt wird. Daher werden alle vertrauten Dienste wie HTTP, FTP, Telnet, Whois usw. gut unterstützt.

Wenn Sie mit unserem Dienstklassenbeispiel fortfahren, können Instanznamen des FTP-Diensts "alder.intel.com" oder "ftp.microsoft.com" sein, während eine Instanz des XYZ Corp. Employee Info Server den Namen "XYZ Corp. Employee Info Server Version 3.5" erhalten kann.

In den ersten beiden Fällen wird der gewünschte Dienst durch die Kombination aus der Dienstklassen-GUID für FTP und dem Computernamen (angegeben als Dienstinstanzname) eindeutig identifiziert. Im dritten Fall kann der Hostname, in dem sich der Dienst befindet, zum Zeitpunkt der Dienstabfrage gefunden werden, sodass der Dienstinstanzname keinen Hostnamen enthalten muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DNS-Referenz](../dns/dns-reference.md)
</dt> <dt>

[Namensauflösungsdatenstrukturen](name-resolution-data-structures-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Zusammenfassung der Namensauflösungsfunktionen](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
