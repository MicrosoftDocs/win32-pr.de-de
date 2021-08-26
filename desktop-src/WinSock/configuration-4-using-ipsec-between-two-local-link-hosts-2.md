---
description: Diese Konfiguration erstellt eine IPsec-Sicherheitszuordnung (SECURITY Association, SA) zwischen zwei Hosts im gleichen Subnetz, um die Authentifizierung mit dem Authentifizierungsheader (AH) und dem MD5-Hashalgorithmus (Message Digest 5) durchzuführen.
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Konfiguration 3: Verwenden von IPsec zwischen zwei Hosts mit lokaler Verknüpfung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b72485db34e8ff2c4e29a201df258dfb9d2ab9a00717ab515cda982e7ea867dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121430"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Konfiguration 3: Verwenden von IPsec zwischen zwei Hosts mit lokaler Verknüpfung

Diese Konfiguration erstellt eine IPsec-Sicherheitszuordnung (SECURITY Association, SA) zwischen zwei Hosts im gleichen Subnetz, um die Authentifizierung mit dem Authentifizierungsheader (AH) und dem MD5-Hashalgorithmus (Message Digest 5) durchzuführen. In diesem Beispiel schützt die gezeigte Konfiguration den gesamten Datenverkehr zwischen zwei benachbarten Hosts: Host 1 mit der linklokalen Adresse FE80::2AA:FF:FE53:A92C und Host 2 mit der linklokalen Adresse FE80::2AA:FF:FE92:D0F1.

**So verwenden Sie IPsec zwischen zwei Hosts mit lokaler Verknüpfung**

1.  Erstellen Sie auf Host 1 mithilfe des Befehls ipsec6 c leere DATEIEN für Sicherheitszuordnungen (SAD) und Sicherheitsrichtliniendateien (SECURITY Policy, PROTOKOLLDATEI). In diesem Beispiel lautet der Ipsec6.exe Befehl ipsec6 c test. Dadurch werden zwei Dateien erstellt, um Sicherheitszuordnungen (Test.sad) und Sicherheitsrichtlinien (Test.lauf) manuell zu konfigurieren.
2.  Bearbeiten Sie auf Host 1 die PROTOKOLLDATEI, um eine Sicherheitsrichtlinie hinzuzufügen, die den gesamten Datenverkehr zwischen Host 1 und Host 2 sichert.

    Die folgende Tabelle zeigt die Sicherheitsrichtlinie, die vor dem ersten Eintrag für dieses Beispiel der Datei "Test.sollen" hinzugefügt wurde (der erste Eintrag in der Datei "Test.protokolldatei" wurde nicht geändert).

    | DOMÄNENNAMEN des Dateifeldnamens | Beispielwert              |
    |---------------------|----------------------------|
    | **Richtlinie**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protokoll**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **Ah**                     |
    | **IPSecMode**       | **Transport**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Richtung**       | **BIDIRECT**               |
    | **Aktion**          | **Anwenden**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Platzieren Sie ein Semikolon am Ende der Zeile, die diese Sicherheitsrichtlinie konfiguriert. Die Richtlinieneinträge müssen in absteigender numerischer Reihenfolge platziert werden.

3.  Bearbeiten Sie auf Host 1 die SAD-Datei, und fügen Sie SA-Einträge hinzu, um den gesamten Datenverkehr zwischen Host 1 und Host 2 zu sichern. Es müssen zwei Sicherheitszuordnungen erstellt werden: eine für Datenverkehr zu Host 2 und eine für Datenverkehr von Host 2.

    Die folgende Tabelle zeigt den ersten SA-Eintrag, der der Datei Test.sad für dieses Beispiel hinzugefügt wurde (für Datenverkehr zu Host 2).

    | SAD-Dateifeldname | Beispielwert              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **RICHTLINIE**                 |
    | **SrcIPAddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **SrcPort**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Richtung**       | **Ausgehende**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Platzieren Sie ein Semikolon am Ende der Zeile, die diese SA konfiguriert.

    Die folgende Tabelle zeigt den zweiten SA-Eintrag, der der Datei Test.sad für dieses Beispiel (für Datenverkehr von Host 2) hinzugefügt wurde.

    | SAD-Dateifeldname | Beispielwert              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **RICHTLINIE**                 |
    | **SrcIPAddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **SrcPort**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Richtung**       | **Eingehende**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Platzieren Sie ein Semikolon am Ende der Zeile, die diese SA konfiguriert. Die SA-Einträge müssen in absteigender numerischer Reihenfolge platziert werden.

4.  Erstellen Sie auf Host 1 eine Textdatei, die eine Textzeichenfolge zum Authentifizieren der mit Host 2 erstellten SAs enthält. In diesem Beispiel wird die Datei Test.key mit dem Inhalt "This is a test" (Dies ist ein Test) erstellt. Sie müssen doppelte Anführungszeichen um die Schlüsselzeichenfolge einschließen, damit der Schlüssel vom ipsec6-Tool gelesen werden kann.

    Microsoft IPv6 Technology Preview unterstützt nur manuell konfigurierte Schlüssel für die Authentifizierung von IPsec-SAs. Die manuellen Schlüssel werden konfiguriert, indem Textdateien erstellt werden, die die Textzeichenfolge des manuellen Schlüssels enthalten. In diesem Beispiel wird der gleiche Schlüssel für die SAs in beide Richtungen verwendet. Sie können unterschiedliche Schlüssel für eingehende und ausgehende SAs verwenden, indem Sie verschiedene Schlüsseldateien erstellen und mit dem Feld KeyFile in der SAD-Datei darauf verweisen.

5.  Erstellen Sie auf Host 2 mithilfe des Befehls ipsec6 c leere DATEIEN für Sicherheitszuordnungen (SAD) und Sicherheitsrichtliniendateien (SECURITY Policy, PROTOKOLLDATEI). In diesem Beispiel lautet der Ipsec6.exe Befehl ipsec6 c test. Dadurch werden zwei Dateien mit leeren Einträgen zum manuellen Konfigurieren von Sicherheitszuordnungen (Test.sad) und Sicherheitsrichtlinien (Test.lauf) erstellt.

    Um das Beispiel zu vereinfachen, werden auf Host 2 die gleichen Dateinamen für die SAD- und PROTOKOLLDATEIen verwendet. Sie können auf jedem Host unterschiedliche Dateinamen verwenden.

6.  Bearbeiten Sie auf Host 2 die PROTOKOLLDATEI, um eine Sicherheitsrichtlinie hinzuzufügen, die den gesamten Datenverkehr zwischen Host 2 und Host 1 sichert.

    Die folgende Tabelle zeigt den Sicherheitsrichtlinieneintrag, der vor dem ersten Eintrag der Datei "Test.protokolldatei" für dieses Beispiel hinzugefügt wurde (der erste Eintrag in der Datei "Test.protokolldatei" wurde nicht geändert).

    | DOMÄNENNAMEN des Dateifeldnamens | Beispielwert              |
    |---------------------|----------------------------|
    | **Richtlinie**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protokoll**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **Ah**                     |
    | **IPSecMode**       | **Transport**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Richtung**       | **BIDIRECT**               |
    | **Aktion**          | **Anwenden**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Platzieren Sie ein Semikolon am Ende der Zeile, die diese Sicherheitsrichtlinie konfiguriert. Die Richtlinieneinträge müssen in absteigender numerischer Reihenfolge platziert werden.

7.  Bearbeiten Sie auf Host 2 die SAD-Datei, und fügen Sie SA-Einträge hinzu, um den gesamten Datenverkehr zwischen Host 2 und Host 1 zu sichern. Es müssen zwei Sicherheitszuordnungen erstellt werden: eine für Datenverkehr zu Host 1 und eine für Datenverkehr von Host 1.

    Die folgende Tabelle zeigt die erste SA, die der Datei Test.sad für dieses Beispiel (für Datenverkehr von Host 1) hinzugefügt wurde.

    | SAD-Dateifeldname | Beispielwert              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **RICHTLINIE**                 |
    | **SrcIPAddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **SrcPort**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Richtung**       | **Eingehende**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Platzieren Sie ein Semikolon am Ende der Zeile, die diese SA konfiguriert.

    Die folgende Tabelle zeigt den zweiten SA-Eintrag, der der Datei Test.sad für dieses Beispiel hinzugefügt wurde (für Datenverkehr zu Host 1).

    | SAD-Dateifeldname | Beispielwert              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **RICHTLINIE**                 |
    | **SrcIPAddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **SrcPort**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Richtung**       | **Ausgehende**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Platzieren Sie ein Semikolon am Ende der Zeile, die diese SA konfiguriert. Die SA-Einträge müssen in absteigender numerischer Reihenfolge platziert werden.

8.  Erstellen Sie auf Host 2 eine Textdatei, die eine Textzeichenfolge zum Authentifizieren der mit Host 1 erstellten SAs enthält. In diesem Beispiel wird die Datei Test.key mit dem Inhalt "This is a test" (Dies ist ein Test) erstellt. Sie müssen doppelte Anführungszeichen um die Schlüsselzeichenfolge einschließen, damit der Schlüssel vom ipsec6-Tool gelesen werden kann.
9.  Fügen Sie auf Host 1 mithilfe des Befehls ipsec6 a die konfigurierten Sicherheitsrichtlinien und Sicherheitszuordnungen aus den PROTOKOLLDATEIen und SAD-Dateien hinzu. In diesem Beispiel wird der Befehl ipsec6 a test auf Host 1 ausgeführt.
10. Fügen Sie auf Host 2 mithilfe des Befehls ipsec6 a die konfigurierten Sicherheitsrichtlinien und Sicherheitszuordnungen aus den PROTOKOLLDATEIen und SAD-Dateien hinzu. In diesem Beispiel wird der Befehl ipsec6 a test auf Host 2 ausgeführt.
11. Pingen Sie Host 1 von Host 2 mit dem Befehl ping6.

    Wenn Sie den Datenverkehr mit Microsoft-Netzwerkmonitor oder einem anderen Paketsniffer erfassen, sollte der Austausch von ICMPv6-Echoanforderungs- und EchoAntwortnachrichten mit einem Authentifizierungsheader zwischen dem IPv6-Header und dem ICMPv6-Header angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene Konfigurationen für IPv6](recommended-configurations-2.md)
</dt> <dt>

[Einzelnes Subnetz mit lokalen Linkadressen](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[IPv6-Datenverkehr zwischen Knoten in verschiedenen Subnetzen eines IPv4-Internetnetzwerks (6to4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



