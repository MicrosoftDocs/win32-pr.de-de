---
title: IPSec-Konfiguration
description: Windows-Filter Plattform (WFP) ist die zugrunde liegende Plattform für die Windows-Firewall mit erweiterter Sicherheit.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948683"
---
# <a name="ipsec-configuration"></a>IPSec-Konfiguration

Windows-Filter Plattform (WFP) ist die zugrunde liegende Plattform für die Windows-Firewall mit erweiterter Sicherheit. WFP wird zum Konfigurieren von Netzwerk Filterungs Regeln verwendet, die Regeln zum Sichern des Netzwerk Datenverkehrs mit IPSec einschließen. Anwendungsentwickler können IPSec direkt mithilfe der WFP-API konfigurieren, um ein präziseeres Modell zum Filtern von Netzwerk Datenverkehr zu nutzen, als das über das MMC-Snap-in (Microsoft Management Console) für die Windows-Firewall mit erweiterter Sicherheit verfügbar gemachte Modell.

## <a name="what-is-ipsec"></a>Was ist IPSec?

Internet Protokoll Sicherheit (Internet Protocol Security, IPSec) ist ein Satz von Sicherheitsprotokollen, die zum Übertragen von IP-Paketen über das Internet verwendet werden. IPSec ist für alle IPv6-Implementierungen obligatorisch und optional für IPv4.

Der gesicherte IP-Datenverkehr verfügt über zwei optionale IPSec-Header, die die Typen des kryptografischen Schutzes identifizieren, die auf das IP-Paket angewendet werden, und Informationen zum Decodieren des geschützten Pakets enthalten.

Der Header "kapselnde Sicherheits Nutzlast (ESP)" wird für Datenschutz und Schutz gegen böswillige Änderungen verwendet, indem Authentifizierung und optionale Verschlüsselung durchgeführt werden. Sie kann für Datenverkehr verwendet werden, der NAT-Router (Netzwerk Adressübersetzung) durchläuft.

Der Authentifizierungs Header (AH) wird nur zum Schutz gegen böswillige Änderungen verwendet, indem eine Authentifizierung durchgeführt wird. Sie kann nicht für Datenverkehr verwendet werden, der NAT-Router durchläuft.

Weitere Informationen zu IPSec finden Sie unter:

<dl>

[Technische Referenz zu IPSec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>Was ist IKE?

Internetschlüsselaustausch (IKE) ist ein Schlüsselaustausch Protokoll, das Teil des IPSec-Protokoll Satzes ist. IKE wird beim Einrichten einer sicheren Verbindung verwendet und erfüllt den sicheren Austausch von geheimen Schlüsseln und anderen Schutz bezogenen Parametern, ohne dass der Benutzer eingreifen muss.

Weitere Informationen zu IKE finden Sie unter:

<dl>

[Internetschlüsselaustausch](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>Was ist AuthIP?

Authentifiziertes Internetprotokoll (AuthIP) ist ein neues Schlüsselaustausch Protokoll, das IKE wie folgt erweitert.

<dl> Obwohl IKE nur Anmelde Informationen für die Computer Authentifizierung unterstützt, unterstützt auch AuthIP Folgendes:

-   Benutzer Anmelde Informationen: NTLM, Kerberos, Zertifikate.
-   NAP-Integritäts Zertifikate (Network Access Protection, Netzwerk Zugriffsschutz)
-   Anonyme Anmelde Informationen, die für die optionale Authentifizierung verwendet werden.
-   Kombination von Anmelde Informationen; beispielsweise eine Kombination aus Computer-und Benutzer-Kerberos-Anmelde Informationen.

  
AuthIP verfügt über einen Authentifizierungs-Wiederholungs Mechanismus, mit dem alle konfigurierten Authentifizierungsmethoden überprüft werden, bevor die Verbindung fehlschlägt.  
AuthIP kann mit Secure Sockets verwendet werden, um Anwendungs basierten IPSec-geschützten Datenverkehr zu implementieren. Sie bietet:

-   Pro-Socket-Authentifizierung und-Verschlüsselung. Weitere Informationen finden Sie unter [**wsasetsocketsecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .
-   Client Identitätswechsel. (IPSec nimmt die Identität des Sicherheits Kontexts an, unter dem der Socket erstellt wird.)
-   Überprüfung des eingehenden und ausgehenden Peer namens. Weitere Informationen finden Sie unter [**wsasetsocketetertargetname**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .

  
</dl>

Weitere Informationen zu AuthIP finden Sie unter:

<dl>

[AuthIP in Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>Was ist eine IPSec-Richtlinie?

Eine IPSec-Richtlinie ist ein Satz von Regeln, die bestimmen, welcher Typ von IP-Datenverkehr mit IPSec gesichert werden muss und wie dieser Datenverkehr gesichert werden soll. Auf einem Computer ist jeweils nur eine IPSec-Richtlinie aktiv.

Wenn Sie mehr über die Implementierung von IPSec-Richtlinien erfahren möchten, öffnen Sie das MMC-Snap-in "lokale Sicherheitsrichtlinie" (secpol. msc), drücken Sie F1, um die Hilfe anzuzeigen, und wählen Sie dann erstellen und Verwenden von IPSec-Richtlinien im Inhaltsverzeichnis

Weitere Informationen zu IPSec-Richtlinien finden Sie unter:

<dl>

[Übersicht über IPSec-Richtlinien Konzepte](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Beschreibung einer IPSec-Richtlinie](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Verwenden von WFP zum Konfigurieren von IPSec-Richtlinien

Die Microsoft-Implementierung von IPSec verwendet die Windows-Filter Plattform zum Einrichten von IPSec-Richtlinien. IPSec-Richtlinien werden implementiert, indem auf verschiedenen WFP-Ebenen Filter wie folgt hinzugefügt werden.

-   Fügen Sie auf der swpm \_ \_ -Schicht IKEEXT \_ V {4 \| 6}-Schichten Filter hinzu, mit denen die von den Schlüssel für die Schlüssel Erstellung (IKE/AuthIP) während des Hauptmodus (mm) verwendeten Aushandlungs Richtlinien angegeben werden. Authentifizierungsmethoden und Kryptografiealgorithmen werden auf diesen Ebenen angegeben.
-   Auf der \_ Ebene der \_ IPSec \_ V {4 6} auf der swpm-Ebene \| fügen Sie Filter hinzu, mit denen die von den Schlüssel für die Schlüssel Erstellung verwendeten Aushandlungs Richtlinien während des Schnellmodus (qm) und des Modus für erweiterte Modi (EM) angegeben IPSec-Header (AH/ESP) und kryptografische Algorithmen werden auf diesen Ebenen angegeben.

    Eine Aushandlungs Richtlinie wird als Richtlinien Anbieter Kontext angegeben, der dem Filter zugeordnet ist. Das Schlüssel Bindungs Modul listet die Richtlinien Anbieter Kontexte basierend auf den Datenverkehrs Merkmalen auf und ruft die Richtlinie ab, die für die Sicherheitsaus Handlung verwendet werden soll.

    > [!Note]  
    > Die WFP-API kann verwendet werden, um die Sicherheits Zuordnungen (SAS) direkt anzugeben und damit die Aushandlungs Richtlinie des Schlüssel Bindungs Moduls zu ignorieren.

     

-   Auf der fwpm \_ -Schicht für \_ eingehende \_ Transport \_ v {4 \| 6} und fwpm- \_ Schicht \_ ausgehende \_ Transport \_ v {4 \| 6} werden Filter hinzugefügt, die Legenden aufrufen und bestimmen, welcher Daten Verkehrsfluss gesichert werden soll.
-   Fügen Sie auf der Ebene des swpm \_ -Schicht-e \_ \_ \_ \_ -v \_ {4 \| 6} Filter hinzu, mit denen die Identitäts Filterung und die Richtlinie pro Anwendung implementiert werden.

Das folgende Diagramm veranschaulicht die Interaktion der verschiedenen WFP-Komponenten in Bezug auf den IPSec-Vorgang.![IPSec-Konfiguration mit Windows-Filter Plattform](images/ipsec-configuration.jpg)

Nachdem IPsec konfiguriert wurde, wird es in WFP integriert und erweitert die WFP-Filterfunktionen, indem Informationen bereitgestellt werden, die als Filterbedingungen auf der Ebene der Autorisierungs Ebenen der Anwendungsschicht verwendet werden. IPSec stellt z. b. die Identität des Remote Benutzers und des Remote Computers bereit, die WFP auf den Ebenen "ALE Connect" und "Accept Authorization" verfügbar macht. Diese Informationen können für eine differenzierte Remote Identitäts Autorisierung durch eine WFP-basierte Firewall-Implementierung verwendet werden.

Im folgenden finden Sie eine Beispiel-Isolations Richtlinie, die mithilfe von IPSec implementiert werden kann:

-   Die Ebene " \_ \_ IKEEXT V {4 6}" der Ebene "f" \_ \| – Kerberos-Authentifizierung.
-   \_Ebene der \_ IPSec \_ V {4 \| 6} Ebenen der WPM-Ebene – AH/SHA-1.
-   WPM \_ -Schicht \_ eingehender \_ Transport \_ v {4 \| 6} und ausgehender Transport der WPM- \_ Ebene \_ \_ \_ v {4 \| 6} Ebenen-Aushandlungs Ermittlung für den gesamten Netzwerk Datenverkehr.
-   Voll \_ \_ \_ \_ \_ \_ ständig authentifizierender v {4 \| 6}-Ebenen-IPSec für den gesamten Netzwerk Datenverkehr erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**WFP-Ebenen**
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

**Mit der WFP-API implementierte IPSec-Richtlinien Szenarien:**
</dt> <dt>

[Transportmodus](regular-transport-mode.md)
</dt> <dt>

[Transport Modus für Aushandlungs Ermittlung](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Transport Modus für die Aushandlung von Aushandlungen im Begrenzungs Modus](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel Modus](tunnel-mode.md)
</dt> <dt>

[Garantierte Verschlüsselung](guaranteed-encryption.md)
</dt> <dt>

[Remote Identitäts Autorisierung](remote-identity-authorization.md)
</dt> <dt>

[Manuelle IPSec-SAS](manual-ipsec-sas.md)
</dt> <dt>

[IKE-/AuthIP-Ausnahmen](ike-exemptions.md)
</dt> <dt>

**IPSec-Lösungen:**
</dt> <dt>

[Server-und Domänen Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 