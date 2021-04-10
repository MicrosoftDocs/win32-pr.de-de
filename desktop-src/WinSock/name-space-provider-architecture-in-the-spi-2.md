---
description: Programmgesteuerte Schnittstellen, die verwendet werden, um die verschiedenen Typen von Namespaces abzufragen und Informationen in einem Namespace zu registrieren (falls unterstützt), unterscheiden sich
ms.assetid: 6a037e8d-49f3-4286-929a-8bb64ea0960f
title: Architektur von Namespace Anbietern in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb567933cae60f56137eba39845bf27ad8c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214587"
---
# <a name="namespace-provider-architecture-in-the-spi"></a>Architektur von Namespace Anbietern in SPI

Programmgesteuerte Schnittstellen, die verwendet werden, um die verschiedenen Typen von Namespaces abzufragen und Informationen in einem Namespace zu registrieren (falls unterstützt), unterscheiden sich Ein Namespace Anbieter ist eine lokal residente Anwendung, die zwischen dem Windows Sockets-Namespace SPI und einem vorhandenen Namespace, der lokal implementiert werden kann oder auf die über das Netzwerk zugegriffen werden kann, zugeordnet werden kann. Dies wird wie folgt veranschaulicht:

![Namespace-Anbieter Diagramm](images/ovrvw3-1.png)

> [!Note]  
> Es ist möglich, dass für einen bestimmten Namespace, z. b. DNS, mehr als ein Namespace Anbieter auf einem bestimmten Computer installiert ist.

 

Wie bereits erwähnt, verweist der generische Begriff "Service" auf den Server-die Hälfte einer Client/Server-Anwendung. In Windows Sockets ist ein Dienst einer Dienstklasse zugeordnet, und jede Instanz eines bestimmten Dienstanbieter verfügt über einen Dienstnamen, der innerhalb der Dienstklasse eindeutig sein muss. Beispiele für Dienst Klassen sind FTP-Server, SQL Server, XYZ Corp. Employee Info Server usw.

Wie das Beispiel veranschaulicht, sind einige Dienst Klassen bekannt, während andere für eine bestimmte vertikale Anwendung eindeutig und spezifisch sind. In beiden Fällen wird jede Dienstklasse durch einen Klassennamen und einen Klassen Bezeichner dargestellt. Der Klassenname muss nicht unbedingt eindeutig sein, aber der Klassen Bezeichner muss lauten. GUID (Global Unique Identifier) werden zur Darstellung von Dienst Klassen-IDs verwendet. Für bekannte Dienste, Klassennamen und Klassen Bezeichner (GUIDs) wurde die Zuordnung aufgehoben, und es stehen Makros für die Konvertierung zur Verfügung, z. b. TCP-Portnummern und die entsprechenden klassenbezeichnerguids. Für andere Dienste wählt der Entwickler den Klassennamen aus und verwendet das Uuidgen.exe Hilfsprogramm, um eine GUID für den Klassen Bezeichner zu generieren.

Das Konzept einer Dienstklasse besteht darin, dass es möglich ist, einen Satz von Attributen einzurichten, die von allen Instanzen eines bestimmten dienstanzen gemeinsam gehalten werden. Dieser Satz von Attributen wird an Windows Sockets zu dem Zeitpunkt bereitgestellt, an dem die Dienstklasse definiert ist, und wird als Dienst Klassen Schema-Informationen bezeichnet. Der Ws2- \_32.dll wiederum leitet diese Informationen an alle aktiven Namespace Anbieter weiter. Wenn eine Instanz eines Diensts auf einem Host Computer installiert und verfügbar gemacht wird, wird der zugehörige Dienst Name verwendet, um diese bestimmte Instanz von anderen zu unterscheiden, die dem Namespace bekannt sein könnten.

Beachten Sie, dass die Installation einer Dienstklasse nur auf Computern erfolgen muss, auf denen der Dienst ausgeführt wird, und nicht auf allen Clients, die den Dienst verwenden können. Wenn möglich, stellt das Ws2- \_32.dll zu dem Zeitpunkt, zu dem eine Instanz eines Dienstanbieters registriert oder eine Dienst Abfrage initiiert wird, Schema Informationen für Dienst Klassen für einen Namespace Anbieter bereit. Die Ws2- \_32.dll speichert diese Informationen natürlich nicht selbst, sondern versucht, Sie von einem Namespace Anbieter abzurufen, der die Möglichkeit zur Bereitstellung dieser Daten angegeben hat. Da es keine Garantie gibt, dass der Ws2- \_32.dll das Dienst Klassen Schema bereitstellen kann, müssen Namespace Anbieter, die diese Informationen benötigen, über einen Fall Back Mechanismus verfügen, um ihn über Namespace spezifische Mittel zu erhalten.

Der Internet Domain Name System verfügt nicht über ein klar definiertes Mittel zum Speichern von Schema Informationen für Dienst Klassen. Demzufolge können DNS-Namespace Anbieter nur bekannte TCP/IP-Dienste unterstützen, für die eine Dienst Klassen-GUID vorab zugeordnet wurde. In der Praxis ist dies keine ernsthafte Einschränkung, da Dienst Klassen-GUIDs für den gesamten Satz von TCP-und UDP-Ports vorab zugeordnet wurden und Makros verfügbar sind, um die GUID abzurufen, die einem beliebigen TCP-oder UDP-Port zugeordnet ist. Daher werden alle vertrauten Dienste wie FTP, Telnet, Whois usw. gut unterstützt. Bei der Abfrage dieser Dienste ist der Hostname des Ziel Computers gemäß der Konvention der Name der Dienst Instanz.

Wenn wir mit unserem Dienst Klassen Beispiel fortfahren, können Instanznamen des FTP-Dienes "Alder.Intel.com" oder "Rhino.Microsoft.com" lauten, während eine Instanz von "XYZ Corp. Employee Infoserver" den Namen "XYZ Corp. Employee Infoserver Version 3,5" hat. In den ersten beiden Fällen wird der gewünschte Dienst durch die Kombination der Dienst Klassen-GUID für FTP und des Computer namens (angegeben als dienstinstanzname) eindeutig identifiziert. Im dritten Fall kann der Hostname, in dem sich der Dienst befindet, zum Zeitpunkt der Dienst Abfrage ermittelt werden, sodass der Dienst Instanzname keinen Hostnamen enthalten muss.

 

 



