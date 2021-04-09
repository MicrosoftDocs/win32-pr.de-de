---
description: Mit dieser Konfiguration wird eine IPSec-Sicherheits Zuordnung (SA) zwischen zwei Hosts im gleichen Subnetz erstellt, um die Authentifizierung mit dem Authentifizierungs Header (AH) und dem MD5-Hash Algorithmus (Message Digest 5) auszuführen.
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Konfiguration 3: Verwenden von IPSec zwischen zwei local-Link-Hosts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129216"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Konfiguration 3: Verwenden von IPSec zwischen zwei local-Link-Hosts

Mit dieser Konfiguration wird eine IPSec-Sicherheits Zuordnung (SA) zwischen zwei Hosts im gleichen Subnetz erstellt, um die Authentifizierung mit dem Authentifizierungs Header (AH) und dem MD5-Hash Algorithmus (Message Digest 5) auszuführen. In diesem Beispiel sichert die angezeigte Konfiguration den gesamten Datenverkehr zwischen zwei benachbarten Hosts: Host 1 mit der Link-Local-Adresse FE80:: 2AA: FF: FE53: A92C und Host 2 mit der Link-Local-Adresse FE80:: 2AA: FF: FE92: D0F1.

**So verwenden Sie IPSec zwischen zwei local-Link-Hosts**

1.  Erstellen Sie auf Host 1 mithilfe des Befehls dem ipsec6 c leere Sicherheits Zuordnungs Dateien (Sad) und Security Policy (SPD). In diesem Beispiel ist der Befehl Ipsec6.exe dem ipsec6 c Test. Dadurch werden zwei Dateien erstellt, um Sicherheits Zuordnungen (Test. Sad) und Sicherheitsrichtlinien (Test. SPD) manuell zu konfigurieren.
2.  Bearbeiten Sie auf Host 1 die SPD-Datei, um eine Sicherheitsrichtlinie hinzuzufügen, die den gesamten Datenverkehr zwischen Host 1 und Host 2 sichert.

    Die folgende Tabelle zeigt die Sicherheitsrichtlinie, die der Datei "Test. SPD" vor dem ersten Eintrag für dieses Beispiel hinzugefügt wurde (der erste Eintrag in der Datei "Test. SPD" wurde nicht geändert).

    | SPD-Datei Feldname | Beispielwert              |
    |---------------------|----------------------------|
    | **Richtlinie**          | 2                          |
    | **Remoteipaddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **Lokalpaddr**     | \*                         |
    | **Remoteport**      | \*                         |
    | **Protokoll**        | \*                         |
    | **LocalPort**       | \*                         |
    | **Ipsecprotocol**   | **Ada**                     |
    | **Ipsecmode**       | **Personen**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **Sabundleindex**   | **NONE**                   |
    | **Richtung**       | **Bidirect**               |
    | **Aktion**          | **Apply**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Platzieren Sie am Ende der Zeile ein Semikolon, das diese Sicherheitsrichtlinie konfiguriert. Die Richtlinien Einträge müssen in absteigender numerischer Reihenfolge abgelegt werden.

3.  Bearbeiten Sie auf Host 1 die Datei "Sad", und fügen Sie den gesamten Datenverkehr zwischen Host 1 und Host 2 SA-Einträge hinzu. Es müssen zwei Sicherheits Zuordnungen erstellt werden: eine für den Datenverkehr zu Host 2 und eine für den Datenverkehr von Host 2.

    In der folgenden Tabelle wird der erste SA-Eintrag angezeigt, der der Datei "Test. Sad" für dieses Beispiel hinzugefügt wurde (für Datenverkehr zu Host 2).

    | Trauriger Datei Feldname | Beispielwert              |
    |---------------------|----------------------------|
    | **Saentry**         | 2                          |
    | **SPI**             | 3001                       |
    | **Savon paddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **"-Paddr"**      | **RICHTLINIE**                 |
    | **Srcipaddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **Srcport**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Richtung**       | **Ausgehende**               |
    | **Secpolicyindex**  | 2                          |

    

     

    Platzieren Sie am Ende der Zeile ein Semikolon, das diese SA konfiguriert.

    In der folgenden Tabelle wird der zweite SA-Eintrag angezeigt, der der Datei "Test. Sad" für dieses Beispiel hinzugefügt wurde (für Datenverkehr von Host 2).

    | Trauriger Datei Feldname | Beispielwert              |
    |---------------------|----------------------------|
    | **Saentry**         | 1                          |
    | **SPI**             | 3000                       |
    | **Savon paddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **"-Paddr"**      | **RICHTLINIE**                 |
    | **Srcipaddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **Srcport**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Richtung**       | **Einheimische**                |
    | **Secpolicyindex**  | 2                          |

    

     

    Platzieren Sie am Ende der Zeile ein Semikolon, das diese SA konfiguriert. Die SA-Einträge müssen in absteigender numerischer Reihenfolge abgelegt werden.

4.  Erstellen Sie auf Host 1 eine Textdatei, die eine Text Zeichenfolge enthält, die zum Authentifizieren der mit Host 2 erstellten SAS verwendet wird. In diesem Beispiel wird die Datei "Test. Key" mit dem Inhalt "This is a Test" erstellt. Sie müssen die Schlüssel Zeichenfolge in doppelte Anführungszeichen einschließen, damit der Schlüssel vom dem ipsec6-Tool gelesen werden konnte.

    Die Microsoft IPv6-Technologievorschau unterstützt nur manuell konfigurierte Schlüssel für die Authentifizierung von IPSec-SAS. Die manuellen Schlüssel werden konfiguriert, indem Textdateien erstellt werden, die die Text Zeichenfolge des manuellen Schlüssels enthalten. In diesem Beispiel wird der gleiche Schlüssel für die SAS in beide Richtungen verwendet. Sie können verschiedene Schlüssel für eingehende und ausgehende SAS verwenden, indem Sie unterschiedliche Schlüsseldateien erstellen und mit dem keyfile-Feld in der SAD-Datei auf Sie verweisen.

5.  Erstellen Sie auf Host 2 leere Sicherheits Zuordnungs Dateien (Sad) und Security Policy (SPD) mit dem Befehl dem ipsec6 c. In diesem Beispiel ist der Befehl Ipsec6.exe dem ipsec6 c Test. Dadurch werden zwei Dateien mit leeren Einträgen zum manuellen Konfigurieren von Sicherheits Zuordnungen (Test. Sad) und Sicherheitsrichtlinien (Test. SPD) erstellt.

    Um das Beispiel zu vereinfachen, werden die gleichen Dateinamen für die Sad-und SPD-Dateien auf Host 2 verwendet. Sie können auswählen, dass auf jedem Host unterschiedliche Dateinamen verwendet werden sollen.

6.  Bearbeiten Sie auf Host 2 die SPD-Datei, um eine Sicherheitsrichtlinie hinzuzufügen, die den gesamten Datenverkehr zwischen Host 2 und Host 1 sichert.

    In der folgenden Tabelle wird der Sicherheitsrichtlinien Eintrag angezeigt, der vor dem ersten Eintrag der Datei "Test. SPD" für dieses Beispiel hinzugefügt wurde (der erste Eintrag in der Datei "Test. SPD" wurde nicht geändert).

    | SPD-Datei Feldname | Beispielwert              |
    |---------------------|----------------------------|
    | **Richtlinie**          | 2                          |
    | **Remoteipaddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **Lokalpaddr**     | \*                         |
    | **Remoteport**      | \*                         |
    | **Protokoll**        | \*                         |
    | **LocalPort**       | \*                         |
    | **Ipsecprotocol**   | **Ada**                     |
    | **Ipsecmode**       | **Personen**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **Sabundleindex**   | **NONE**                   |
    | **Richtung**       | **Bidirect**               |
    | **Aktion**          | **Apply**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Platzieren Sie am Ende der Zeile ein Semikolon, das diese Sicherheitsrichtlinie konfiguriert. Die Richtlinien Einträge müssen in absteigender numerischer Reihenfolge abgelegt werden.

7.  Bearbeiten Sie auf Host 2 die traurige Datei, und fügen Sie SA-Einträge hinzu, um den gesamten Datenverkehr zwischen Host 2 und Host 1 zu sichern. Es müssen zwei Sicherheits Zuordnungen erstellt werden: eine für den Datenverkehr zu Host 1 und eine für den Datenverkehr von Host 1.

    In der folgenden Tabelle werden die ersten SA angezeigt, die der Datei "Test. Sad" für dieses Beispiel hinzugefügt wurden (für Datenverkehr von Host 1).

    | Trauriger Datei Feldname | Beispielwert              |
    |---------------------|----------------------------|
    | **Saentry**         | 2                          |
    | **SPI**             | 3001                       |
    | **Savon paddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **"-Paddr"**      | **RICHTLINIE**                 |
    | **Srcipaddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **Srcport**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Richtung**       | **Einheimische**                |
    | **Secpolicyindex**  | 2                          |

    

     

    Platzieren Sie am Ende der Zeile ein Semikolon, das diese SA konfiguriert.

    In der folgenden Tabelle wird der zweite SA-Eintrag angezeigt, der der Datei "Test. Sad" für dieses Beispiel hinzugefügt wurde (für Datenverkehr zu Host 1).

    | Trauriger Datei Feldname | Beispielwert              |
    |---------------------|----------------------------|
    | **Saentry**         | 1                          |
    | **SPI**             | 3000                       |
    | **Savon paddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **"-Paddr"**      | **RICHTLINIE**                 |
    | **Srcipaddr**       | **RICHTLINIE**                 |
    | **Protokoll**        | **RICHTLINIE**                 |
    | **DestPort**        | **RICHTLINIE**                 |
    | **Srcport**         | **RICHTLINIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Richtung**       | **Ausgehende**               |
    | **Secpolicyindex**  | 2                          |

    

     

    Platzieren Sie am Ende der Zeile ein Semikolon, das diese SA konfiguriert. Die SA-Einträge müssen in absteigender numerischer Reihenfolge abgelegt werden.

8.  Erstellen Sie auf Host 2 eine Textdatei, die eine Text Zeichenfolge enthält, die zum Authentifizieren der mit Host 1 erstellten SAS verwendet wird. In diesem Beispiel wird die Datei "Test. Key" mit dem Inhalt "This is a Test" erstellt. Sie müssen die Schlüssel Zeichenfolge in doppelte Anführungszeichen einschließen, damit der Schlüssel vom dem ipsec6-Tool gelesen werden konnte.
9.  Fügen Sie auf Host 1 mithilfe des Befehls "dem ipsec6 a" die konfigurierten Sicherheitsrichtlinien und SAS aus den SPD-und Sad-Dateien hinzu. In diesem Beispiel wird der Befehl dem ipsec6 a Test auf Host 1 ausgeführt.
10. Fügen Sie auf Host 2 die konfigurierten Sicherheitsrichtlinien und die SAS aus den SPD-und Sad-Dateien hinzu, indem Sie den dem ipsec6 a-Befehl verwenden. In diesem Beispiel wird der Befehl dem ipsec6 a Test auf Host 2 ausgeführt.
11. Ping Host 1 von Host 2 mit dem ping6-Befehl.

    Wenn Sie den Datenverkehr mit Microsoft-Netzwerkmonitor oder einem anderen Paketsniffer erfassen, sollte der Austausch der ICMPv6-Echo Anforderungs-und Echo Antwort Nachrichten mit einem Authentifizierungs Header zwischen dem IPv6-Header und dem ICMPv6-Header angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene Konfigurationen für IPv6](recommended-configurations-2.md)
</dt> <dt>

[Einzelnes Subnetz mit Link-Local-Adressen](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[IPv6-Datenverkehr zwischen Knoten in unterschiedlichen Subnetzen eines IPv4-Netzwerks (IPv6-zu-IPv4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



