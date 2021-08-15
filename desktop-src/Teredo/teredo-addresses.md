---
title: Teredo-Adressen
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Weitere Informationen zu: Teredo-Adressen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a8b283d2bab6c9ba091ecc3b37c6218fadb0face78e04b807be03d68b814d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354136"
---
# <a name="teredo-addresses"></a>Teredo-Adressen

Eine Teredo-Adresse besteht aus folgendem Code:

-   **Teredo-Präfix**

    Die ersten 32 Bits gelten für das Teredo-Präfix, das für alle Teredo-Adressen identisch ist. Windows XP und Windows Server 2003 verwendeten zunächst das Teredo-Präfix 3FFE:831F::/32. Das für Teredo in RFC 4380 definierte Präfix ist 2001::/32 und ist das Präfix, das von Teredo in Windows Vista und Windows Server 2008 verwendet wird. Computer mit Windows XP und Windows Server 2003 verwenden das Teredo-Präfix 2001::/32, wenn sie mit dem Microsoft-Sicherheitsbulletin MS06-064 aktualisiert werden.

-   **IPv4-Adresse des Teredo-Servers**

    Die nächsten 32 Bits enthalten die öffentliche IPv4-Adresse des Teredo-Servers, der bei der Konfiguration dieser Teredo-Adresse mitgeholfen hat. Weitere Informationen finden Sie unter "Erstkonfiguration für Teredo-Clients" in diesem Artikel.

-   **Flags**

    Die nächsten 16 Bits für sind für Teredo-Flags reserviert. Bei Windows XP-basierten Teredo-Clients ist das einzige definierte Flag das obere Bit, das als Cone-Flag bezeichnet wird. Das Cone-Flag wird festgelegt, wenn sich der Teredo-Client hinter einer Kegel-NAT befindet. Die Ermittlung, ob die mit dem Internet verbundene NAT eine Cone NAT ist, erfolgt während der Erstkonfiguration des Teredo-Clients. Weitere Informationen finden Sie unter "Erstkonfiguration für Teredo-Clients" in diesem Artikel.

    Für Windows Vista- und Windows Server 2008-basierte Teredo-Clients bieten nicht verwendete Bits im Feld Flags einen Schutz vor Adressscans durch böswillige Benutzer. Die 16 Bits im Feld Flags für Windows Vista- und Windows Server 2008-basierte Teredo-Clients bestehen aus folgenden: CRAAAAUG AAAAAAAA. Das C-Bit ist für das Cone-Flag. Das R-Bit ist für die zukünftige Verwendung reserviert. Das U-Bit ist für das Flag Universal/Local (auf 0 festgelegt). Das G-Bit ist das Flag Individual/Group (auf 0 festgelegt). Die A-Bits werden auf eine zufällig generierte 12-Bit-Zahl festgelegt. Bei Verwendung einer Zufallszahl für die A-Bits muss ein böswilliger Benutzer, der den Rest der Teredo-Adresse ermittelt hat, indem er den anfänglichen Konfigurationsaustausch von Paketen zwischen dem Teredo-Client und dem Teredo-Server erfasst hat, bis zu 4.096 (212) verschiedene Adressen versuchen, um die Adresse eines Teredo-Clients während einer Adressprüfung zu bestimmen.

-   **Verdeckter externer Port**

    Die nächsten 16 Bits speichern eine verdeckte Version des externen UDP-Ports, die dem teredo-Datenverkehr für diesen Teredo-Client entspricht. Wenn der Teredo-Client sein erstes Paket an einen Teredo-Server sendet, wird der UDP-Quellport des Pakets von der NAT einem anderen externen UDP-Port zugeordnet. Der Teredo-Client verwaltet diese Portzuordnung, sodass sie in der Nat-Übersetzungstabelle verbleibt. Daher verwendet der teredo-Datenverkehr für den Host den gleichen externen, zugeordneten UDP-Port. Der externe UDP-Port wird vom Teredo-Server vom UDP-Quellport des eingehenden anfänglichen Pakets bestimmt, das vom Teredo-Client gesendet und an den Teredo-Client zurücksandt wird.

    Der externe Port wird durch XORing the external port with 0xFFFF. Die verdeckte Version des externen Ports 5000 im Hexadezimalformat ist beispielsweise EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). Das Verschleieren des externen Ports verhindert, dass NATs den externen Port innerhalb der Nutzlast der Pakete übersetzen, die sie weiterleiten.

-   **Verdeckte externe Adresse**

    Die letzten 32 Bits speichern eine verdeckte Version der externen IPv4-Adresse, die dem teredo-Datenverkehr für diesen Teredo-Client entspricht. Wenn der Teredo-Client wie der externe Port sein erstes Paket an einen Teredo-Server sendet, wird die Quell-IP-Adresse des Pakets von der NAT einer anderen externen (öffentlichen) Adresse zugeordnet. Der Teredo-Client verwaltet diese Adresszuordnung, sodass sie in der Nat-Übersetzungstabelle verbleibt. Daher verwendet der teredo-Datenverkehr für den Host dieselbe externe, zugeordnete, öffentliche IPv4-Adresse. Die externe IPv4-Adresse wird vom Teredo-Server von der IPv4-Quelladresse des eingehenden anfänglichen Pakets bestimmt, das vom Teredo-Client gesendet und an den Teredo-Client zurücksandt wird.

    Die externe Adresse wird durch XORinging the external address with 0xFFFFFFFF. Die verdeckte Version der öffentlichen IPv4-Adresse 131.107.0.1 im Doppelpunkt-Hexadezimalformat ist beispielsweise 7C94:FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). Das Verschleieren der externen Adresse verhindert, dass NATs die externe Adresse innerhalb der Nutzlast der Pakete übersetzen, die sie weiterleiten.

 

 




