---
title: IPsec-Konfiguration
description: Windows Die Filterplattform (WFP) ist die zugrunde liegende Plattform für Windows Firewall mit erweiterter Sicherheit.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cf20fc8c95aafe3c387195b02468cec3ce884cc97287adde44a594305ee189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069014"
---
# <a name="ipsec-configuration"></a>IPsec-Konfiguration

Windows Die Filterplattform (WFP) ist die zugrunde liegende Plattform für Windows Firewall mit erweiterter Sicherheit. WFP wird verwendet, um Netzwerkfilterregeln zu konfigurieren, die Regeln zum Sichern des Netzwerkdatenverkehrs mit IPsec enthalten. Anwendungsentwickler können IPsec direkt mithilfe der WFP-API konfigurieren, um von einem präziseren Filtermodell für Netzwerkdatenverkehr zu profitieren, als das Modell, das über das MMC-Snap-In (Microsoft Management Console) für Windows Firewall mit erweiterter Sicherheit verfügbar gemacht wird.

## <a name="what-is-ipsec"></a>Was ist IPsec?

Internetprotokollsicherheit (Internet Protocol Security, IPsec) ist eine Reihe von Sicherheitsprotokollen, die zum vertraulichen Übertragen von IP-Paketen über das Internet verwendet werden. IPsec ist für alle IPv6-Implementierungen obligatorisch und optional für IPv4.

Geschützter IP-Datenverkehr verfügt über zwei optionale IPsec-Header, die die Typen des kryptografischen Schutzes identifizieren, die auf das IP-Paket angewendet werden, und Informationen zum Decodieren des geschützten Pakets enthalten.

Der ESP-Header (Encapsulating Security Payload) wird zum Schutz vor schädlichen Änderungen durch Authentifizierung und optionale Verschlüsselung verwendet. Sie kann für Datenverkehr verwendet werden, der NAT-Router (Network Address Translation) durchläuft.

Der Authentifizierungsheader (Authentication Header, AH) wird nur zum Schutz vor böswilligen Änderungen durch Ausführen der Authentifizierung verwendet. Sie kann nicht für Datenverkehr verwendet werden, der NAT-Router durchläuft.

Weitere Informationen zu IPsec finden Sie unter:

<dl>

[Technische Referenz zu IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>Was ist IKE?

Internet Key Exchange (IKE) ist ein Schlüsselaustauschprotokoll, das Teil des IPsec-Protokollsatzes ist. IKE wird beim Einrichten einer sicheren Verbindung verwendet und führt den sicheren Austausch geheimer Schlüssel und anderer schutzbezogener Parameter ohne Eingreifen des Benutzers durch.

Weitere Informationen zu IKE finden Sie unter:

<dl>

[Internetschlüssel-Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>Was ist AuthIP?

Authentifiziertes Internetprotokoll (AuthIP) ist ein neues Schlüsselaustauschprotokoll, das IKE wie folgt erweitert.

<dl> Während IKE nur Anmeldeinformationen für die Computerauthentifizierung unterstützt, unterstützt AuthIP auch:

-   Benutzeranmeldeinformationen: NTLM, Kerberos, Zertifikate.
-   NAP-Integritätszertifikate (Network Access Protection).
-   Anonyme Anmeldeinformationen, die für die optionale Authentifizierung verwendet werden.
-   Kombination von Anmeldeinformationen; Beispielsweise eine Kombination aus Computer- und Benutzer-Kerberos-Anmeldeinformationen.

  
AuthIP verfügt über einen Authentifizierungswiederholungsmechanismus, der alle konfigurierten Authentifizierungsmethoden überprüft, bevor die Verbindung unterbrochen wird.  
AuthIP kann mit sicheren Sockets verwendet werden, um anwendungsbasierten IPsec-geschützten Datenverkehr zu implementieren. Sie bietet:

-   Socketbasierte Authentifizierung und Verschlüsselung. Weitere Informationen finden Sie unter [**WSASetSocketSecurity.**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)
-   Clientidentitätswechsel. (IPsec nimmt die Identität des Sicherheitskontexts an, unter dem der Socket erstellt wird.)
-   Eingehende und ausgehende Peernamenüberprüfung. Weitere Informationen finden Sie unter [**WSASetSocketPeerTargetName.**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)

  
</dl>

Weitere Informationen zu AuthIP finden Sie unter:

<dl>

[AuthIP in Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>Was ist eine IPsec-Richtlinie?

Eine IPsec-Richtlinie ist ein Satz von Regeln, die bestimmen, welche Art von IP-Datenverkehr mithilfe von IPsec geschützt werden muss und wie dieser Datenverkehr geschützt werden soll. Auf einem Computer ist jeweils nur eine IPsec-Richtlinie aktiv.

Um mehr über das Implementieren von IPsec-Richtlinien zu erfahren, öffnen Sie das MMC-Snap-In lokale Sicherheitsrichtlinie (secpol.msc), drücken Sie F1, um die Hilfe anzuzeigen, und wählen Sie dann im Inhaltsverzeichnis Erstellen und Verwenden von IPsec-Richtlinien aus.

Weitere Informationen zu IPsec-Richtlinien finden Sie unter:

<dl>

[Übersicht über IPsec-Richtlinienkonzepte](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Beschreibung einer IPsec-Richtlinie](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Verwenden von WFP zum Konfigurieren von IPsec-Richtlinien

Die Microsoft-Implementierung von IPsec verwendet Windows Filterplattform, um IPsec-Richtlinien einzurichten. IPsec-Richtlinien werden wie folgt implementiert, indem Filter auf verschiedenen WFP-Ebenen hinzugefügt werden.

-   Fügen Sie auf den Ebenen FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} Filter hinzu, die die von den Schlüsselerstellungsmodulen (IKE/AuthIP) während des Mm-Austauschs (Main Mode) verwendeten Aushandlungsrichtlinien angeben. Authentifizierungsmethoden und kryptografische Algorithmen werden auf diesen Ebenen angegeben.
-   Fügen Sie auf der Ebene FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} Filter hinzu, die die von den Schlüsselerstellungsmodulen während des Austauschs von Quick Mode (QM) und Extended Mode (EM) verwendeten Aushandlungsrichtlinien angeben. IPsec-Header (AH/ESP) und kryptografische Algorithmen werden auf diesen Ebenen angegeben.

    Eine Aushandlungsrichtlinie wird als Richtlinienanbieterkontext angegeben, der dem Filter zugeordnet ist. Das Schlüsselmodul listet die Richtlinienanbieterkontexte basierend auf den Datenverkehrsmerkmalen auf und ruft die Richtlinie ab, die für die Sicherheitsaushandlung verwendet werden soll.

    > [!Note]  
    > Die WFP-API kann verwendet werden, um die Sicherheitszuordnungen (Security Associations, SAs) direkt anzugeben und daher die Aushandlungsrichtlinie des Schlüsselmoduls zu ignorieren.

     

-   Fügen Sie auf den Ebenen FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} und FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} Filter hinzu, die Aufrufe aufrufen und bestimmen, welcher Datenverkehrsfluss geschützt werden soll.
-   Fügen Sie auf den Ebenen FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} Filter hinzu, die Identitätsfilterung und anwendungsspezifische Richtlinien implementieren.

Das folgende Diagramm veranschaulicht die Interaktion der verschiedenen WFP-Komponenten in Bezug auf den IPsec-Vorgang.![ipsec-Konfiguration mithilfe der Windows-Filterplattform](images/ipsec-configuration.jpg)

Sobald IPsec konfiguriert ist, wird es in WFP integriert und erweitert die WFP-Filterfunktionen, indem Informationen zur Verwendung als Filterbedingungen auf den ALE-Autorisierungsebenen (Application Layer Enforcement) zur Verfügung gestellt werden. Beispielsweise stellt IPsec die Remotebenutzer- und Remotecomputeridentität bereit, die WFP auf der ALE Connect-Ebene verfügbar macht und Autorisierungsebenen akzeptiert. Diese Informationen können für eine differenzierte Remoteidentitätsautorisierung durch eine WFP-basierte Firewallimplementierungen verwendet werden.

Im Folgenden finden Sie eine Beispielisolationsrichtlinie, die mit IPsec implementiert werden kann:

-   FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6}-Ebenen – Kerberos-Authentifizierung.
-   FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6}-Ebenen – AH/SHA-1.
-   Ebenen FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} und FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} – Ermittlung der Aushandlung für den gesamten Netzwerkdatenverkehr.
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}-Ebenen: IPsec ist für den gesamten Netzwerkdatenverkehr erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**WFP-Ebenen**
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

**Mit der WFP-API implementierte IPsec-Richtlinienszenarien:**
</dt> <dt>

[Transportmodus](regular-transport-mode.md)
</dt> <dt>

[Transportmodus der Aushandlungsermittlung](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Transportmodus der Aushandlungsermittlung im Begrenzungsmodus](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel Modus](tunnel-mode.md)
</dt> <dt>

[Garantierte Verschlüsselung](guaranteed-encryption.md)
</dt> <dt>

[Remoteidentitätsautorisierung](remote-identity-authorization.md)
</dt> <dt>

[Manuelle IPsec-SAs](manual-ipsec-sas.md)
</dt> <dt>

[IKE/AuthIP-Ausnahmen](ike-exemptions.md)
</dt> <dt>

**IPsec-Lösungen:**
</dt> <dt>

[Server- und Domänenisolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 