---
title: Teredo-Adressen
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Weitere Informationen: Teredo-Adressen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc08a53da2f710423d948e9479df2aeb08f20178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349648"
---
# <a name="teredo-addresses"></a>Teredo-Adressen

Eine Teredo-Adresse besteht aus den folgenden Elementen:

-   **Teredo-Präfix**

    Die ersten 32 Bits gelten für das Teredo-Präfix, das für alle Teredo-Adressen gleich ist. Windows XP und Windows Server 2003 verwendeten zunächst das Teredo-Präfix 3FFE: 831F::/32. Das für Teredo in RFC 4380 definierte Präfix ist 2001::/32 und ist das Präfix, das von Teredo in Windows Vista und Windows Server 2008 verwendet wird. Bei Computern unter Windows XP und Windows Server 2003 wird das 2001::/32 Teredo-Präfix verwendet, wenn dieses mit dem Microsoft-Sicherheits Bulletin MS06-064 aktualisiert wird.

-   **IPv4-Adresse des Teredo-Servers**

    Die nächsten 32 Bits enthalten die öffentliche IPv4-Adresse des Teredo-Servers, der die Konfiguration dieser Teredo-Adresse unterstützt. Weitere Informationen finden Sie unter "Erstkonfiguration für Teredo-Clients" in diesem Artikel.

-   **Flags**

    Die nächsten 16 Bits für sind für Teredo-Flags reserviert. Bei Windows XP-basierten Teredo-Clients ist das einzige definierte Flag das hohe Bestell Bit, das als Cone-Flag bezeichnet wird. Das Cone-Flag wird festgelegt, wenn der Teredo-Client hinter einer Kegel-NAT liegt. Die Bestimmung, ob es sich bei der mit dem Internet verbundenen NAT um eine Kegel-NAT handelt, tritt während der Erstkonfiguration des Teredo-Clients auf. Weitere Informationen finden Sie unter "Erstkonfiguration für Teredo-Clients" in diesem Artikel.

    Bei Windows Vista-und Windows Server 2008-basierten Teredo-Clients bieten nicht verwendete Bits innerhalb des Flags-Felds eine Schutz Ebene vor Adress Scans durch böswillige Benutzer. Die 16 Bits innerhalb des Flags-Felds für Windows Vista-und Windows Server 2008-basierte Teredo-Clients bestehen aus folgendem: craaaaug aaaaaaaa. Das C-Bit ist für das Cone-Flag. Das R-Bit ist für die zukünftige Verwendung reserviert. Das U-Bit ist für das Universal/local-Flag (auf 0 festgelegt). Das G-Bit ist ein Einzel-/gruppenflag (auf 0 festgelegt). Die Bits werden auf eine nach dem Zufallsprinzip generierte 12-Bit-Zahl festgelegt. Durch die Verwendung einer Zufallszahl für eine Bits muss ein böswilliger Benutzer, der den Rest der Teredo-Adresse ermittelt hat, indem er den anfänglichen Konfigurations Austausch von Paketen zwischen dem Teredo-Client und dem Teredo-Server erfasst, bis zu 4.096 (212) verschiedene Adressen testen, um die Adresse eines Teredo-Clients während eines Adress Scans zu ermitteln.

-   **Verschlüsselter externer Port**

    Die nächsten 16 Bits speichern eine verdeckte Version des externen UDP-Ports, die dem gesamten Teredo-Datenverkehr für diesen Teredo-Client entspricht. Wenn der Teredo-Client sein erstes Paket an einen Teredo-Server sendet, wird der UDP-Quellport des Pakets durch die NAT einem anderen, externen UDP-Port zugeordnet. Der Teredo-Client verwaltet diese Port Zuordnung, sodass er in der Übersetzungstabelle der NAT verbleibt. Daher verwendet sämtlicher Teredo-Datenverkehr für den Host denselben externen, zugeordneten UDP-Port. Der externe UDP-Port wird vom Teredo-Server vom UDP-Quell Port des eingehenden anfänglichen Pakets bestimmt, das vom Teredo-Client gesendet und zurück an den Teredo-Client gesendet wurde.

    Der externe Port wird durch das XORing des externen Ports mit 0xFFFF verdeckt. Die verdeckte Version des externen Ports 5000 im hexadezimalen Format lautet beispielsweise EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xec77). Das verdecken des externen Ports verhindert, dass NATs den externen Port in der Nutzlast der weitergeleiteten Pakete übersetzen.

-   **Verdeckte externe Adresse**

    Die letzten 32 Bits speichern eine verdeckte Version der externen IPv4-Adresse, die dem gesamten Teredo-Datenverkehr für diesen Teredo-Client entspricht. Ebenso wie der externe Port, wenn der Teredo-Client sein erstes Paket an einen Teredo-Server sendet, wird die Quell-IP-Adresse des Pakets durch den NAT einer anderen externen (öffentlichen) Adresse zugeordnet. Der Teredo-Client verwaltet diese Adress Zuordnung, sodass er in der Übersetzungstabelle der NAT verbleibt. Daher wird für den gesamten Teredo-Datenverkehr für den Host dieselbe externe, zugeordnete öffentliche IPv4-Adresse verwendet. Die externe IPv4-Adresse wird durch den Teredo-Server von der IPv4-Quelladresse des eingehenden anfänglichen Pakets bestimmt, das vom Teredo-Client gesendet und an den Teredo-Client zurückgesendet wird.

    Die externe Adresse wird durch das XORing der externen Adresse mit 0xFFFFFFFF verdeckt. Beispielsweise ist die verdeckte Version der öffentlichen IPv4-Adresse 131.107.0.1 im Doppelpunkt-Hexadezimal Format 7c94: FFFE (131.107.0.1 = 0x836b0001, 0x836b0001 XOR 0xFFFFFFFF = 0x7c94fffe). Durch das Verschleiern der externen Adresse können NATs die externe Adresse in der Nutzlast der weitergeleiteten Pakete übersetzen.

 

 




