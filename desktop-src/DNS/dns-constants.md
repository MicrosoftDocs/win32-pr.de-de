---
title: DNS-Konstanten
description: Die folgenden Konstanten werden für DNS in Der Host-Byte-Reihenfolge definiert.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61da11c9d8f5af28e2152bad5fe9c7b5eb6eb7d83fdb7f94c11e8c2f3c04d9f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164156"
---
# <a name="dns-constants"></a>DNS-Konstanten

Die folgenden Konstanten werden für DNS in Der Host-Byte-Reihenfolge definiert.

## <a name="dns-record-types"></a>DNS-Eintragstypen



| Konstante           | Wert            |
|--------------------|------------------|
| \_DNS-TYP \_ A       | 0x0001           |
| \_ \_ DNS-TYP-NS      | 0x0002           |
| \_DNS-TYP \_ MD      | 0x0003           |
| \_ \_ DNS-TYP MF      | 0x0004           |
| \_DNS-TYP \_ CNAME   | 0x0005           |
| \_ \_ DNS-TYP-SOA     | 0x0006           |
| \_DNS-TYP \_ MB      | 0x0007           |
| \_DNS-TYP \_ MG      | 0x0008           |
| \_DNS-TYP \_ MR      | 0x0009           |
| \_DNS-TYP \_ NULL    | 0x000a           |
| \_DNS-TYP \_ WKS     | 0x000b           |
| \_ \_ DNS-TYP PTR     | 0x000c           |
| \_DNS-TYP \_ HINFO   | 0x000d           |
| \_DNS-TYP \_ MINFO   | 0x000e           |
| \_DNS-TYP \_ MX      | 0x000f           |
| \_ \_ DNS-TYPTEXT    | 0x0010           |
| \_DNS-TYP \_ RP      | 0x0011           |
| \_DNS-TYP \_ AFSDB   | 0x0012           |
| \_DNS-TYP \_ X25     | 0x0013           |
| \_ \_ DNS-TYP ISDN    | 0x0014           |
| \_DNS-TYP \_ RT      | 0x0015           |
| \_DNS-TYP \_ NSAP    | 0x0016           |
| \_DNS-TYP \_ NSAPPTR | 0x0017           |
| \_DNS-TYP \_ SIG     | 0x0018           |
| \_ \_ DNS-TYPSCHLÜSSEL     | 0x0019           |
| \_DNS-TYP \_ PX      | 0x001a           |
| \_ \_ DNS-TYP-GPOS    | 0x001b           |
| \_DNS-TYP \_ AAAA    | 0x001c           |
| \_DNS-TYP \_ LOC     | 0x001d           |
| \_DNS-TYP \_ NXT     | 0x001e           |
| \_ \_ DNS-TYP EID     | 0x001f           |
| \_DNS-TYP \_ NIMLOC  | 0x0020           |
| \_DNS-TYP \_ SRV     | 0x0021           |
| \_DNS-TYP \_ ATMA    | 0x0022           |
| \_DNS-TYP \_ NAPTR   | 0x0023           |
| \_ \_ DNS-TYP KX      | 0x0024           |
| \_ \_ DNS-TYPZERTIFIKAT    | 0x0025           |
| \_DNS-TYP \_ A6      | 0x0026           |
| \_DNS-TYP \_ DNAME   | 0x0027           |
| \_ \_ DNS-TYPSENKE    | 0x0028           |
| DNS \_ TYPE \_ OPT     | 0x0029           |
| \_DNS-TYP \_ DS      | 0x002B           |
| \_DNS-TYP \_ RRSIG   | 0x002E           |
| \_ \_ DNS-TYP NSEC    | 0x002F           |
| \_DNS-TYP \_ DNSKEY  | 0x0030           |
| \_DNS-TYP \_ DHCID   | 0x0031           |
| \_DNS-TYP \_ UINFO   | 0x0064           |
| \_ \_ DNS-TYP-UID     | 0x0065           |
| \_DNS-TYP \_ GID     | 0x0066           |
| \_DNS-TYP \_ UNSPEC  | 0x0067           |
| \_ \_ DNS-TYP-ADDRS   | 0x00f8           |
| \_DNS-TYP \_ TKEY    | 0x00f9           |
| \_DNS-TYP \_ TSIG    | 0x00fa           |
| \_DNS-TYP \_ IXFR    | 0x00fb           |
| \_DNS-TYP \_ AXFR    | 0x00fc           |
| \_DNS-TYP \_ MAILB   | 0x00fd           |
| \_DNS-TYP \_ MAILA   | 0x00fe           |
| DNS \_ TYPE \_ ALL     | 0x00ff           |
| DNS \_ TYPE \_ ANY     | 0x00ff           |
| \_DNS-TYP \_ WINS    | 0xff01           |
| \_DNS-TYP \_ WINSR   | 0xff02           |
| \_DNS-TYP \_ NBSTAT  | \_DNS-TYP \_ WINSR |



 

## <a name="dns-class-types"></a>DNS-Klassentypen



| Konstante             | Wert  |
|----------------------|--------|
| \_DNS-KLASSE \_ INTERNET | 0x0001 |
| \_DNS-KLASSE \_ CSNET    | 0x0002 |
| \_DNS-KLASSE \_ CHAOS    | 0x0003 |
| \_DNS-KLASSE \_ HESIOD   | 0x0004 |
| \_DNS-KLASSE \_ NONE     | 0x00fe |
| \_DNS-KLASSE \_ ALL      | 0x00ff |
| \_DNS-KLASSE \_ ANY      | 0x00ff |



 

## <a name="dns-query-types"></a>DNS-Abfragetypen



| Konstante                    | Wert  |
|-----------------------------|--------|
| DNS \_ OPCODE \_ QUERY          | 0x0000 |
| DNS \_ OPCODE \_ IQUERY         | 0x0001 |
| DNS \_ OPCODE \_ SERVER \_ STATUS | 0x0002 |
| DNS \_ OPCODE \_ UNKNOWN        | 0x0003 |
| DNS \_ OPCODE \_ NOTIFY         | 0x0004 |
| DNS \_ OPCODE \_ UPDATE         | 0x0005 |



 

## <a name="dns-record-flags"></a>DNS-Eintragsflags

Die folgenden Flags beziehen sich auf den Abschnitt eines Ressourceneintrags (RR) innerhalb einer DNS-Nachricht:



| Konstante           | Wert      | Bedeutung                         |
|--------------------|------------|---------------------------------|
| \_DNSREC-FRAGE   | 0x00000000 | RR befindet sich im Frageabschnitt.   |
| DNSREC \_ ANSWER     | 0x00000001 | RR befindet sich im Antwortabschnitt.     |
| DNSREC \_ AUTHORITY  | 0x00000002 | RR befindet sich im Abschnitt "Autorität".  |
| DNSREC \_ ADDITIONAL | 0x00000003 | RR befindet sich im zusätzlichen Abschnitt. |



 

Die folgenden Flags beziehen sich auf den Abschnitt einer RR innerhalb einer DNS-Updatemeldung gemäß [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt):



| Konstante       | Wert      | Bedeutung                           |
|----------------|------------|-----------------------------------|
| DNSREC \_ ZONE   | 0x00000000 | RR befindet sich im Abschnitt "Zone".         |
| DNSREC \_ PREREQ | 0x00000001 | RR befindet sich im Abschnitt "Voraussetzungen". |
| DNSREC \_ UPDATE | 0x00000002 | RR befindet sich im Abschnitt "Update".       |



 

Die folgenden Flags schließen sich gegenseitig aus:



| Konstante        | Wert      | Bedeutung                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ DELETE  | 0x00000004 | Löscht eine RR. Wird in Verbindung mit DNSREC \_ UPDATE verwendet.       |
| DNSREC \_ NOEXIST | 0x00000004 | RR ist nicht vorhanden. Wird in Verbindung mit DNSREC \_ PREREQ verwendet. |



 

## <a name="dns-query-options"></a>DNS-Abfrageoptionen



| Konstante                                | Wert      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS \_ QUERY \_ STANDARD                    | 0x00000000 | Standardabfrage.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS \_ QUERY \_ ACCEPT TRUNCATED RESPONSE (DNS-ABFRAGE \_ AKZEPTIERT ABGESCHNITTENE \_ ANTWORT) | 0x00000001 | Gibt abgeschnittene Ergebnisse zurück. Unter TCP wird kein Wiederholungsversuch ausgeführt.                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_DNS-ABFRAGE \_ VERWENDET NUR \_ TCP \_              | 0x00000002 | Verwendet TCP nur für die Abfrage.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_ \_ DNS-ABFRAGE KEINE \_ REKURSION               | 0x00000004 | Leitet den DNS-Server an, eine iterative Abfrage auszuführen (insbesondere wird der DNS-Server dazu versingt, keine rekursive Auflösung auszuführen, um die Abfrage aufzulösen).                                                                                                                                                                                                                                                                                                   |
| \_ \_ DNS-ABFRAGEUMGEHUNGSCACHE \_               | 0x00000008 | Umgeht den [*Konfliktlösercache*](r-gly.md) bei der Suche.                                                                                                                                                                                                                                                                                                                                                                            |
| \_DNS-ABFRAGE \_ KEINE \_ \_ WIRE-ABFRAGE             | 0x00000010 | Leitet DNS an, eine Abfrage nur für den lokalen Cache auszuführen. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt. Verwenden Sie für ähnliche Funktionen **NUR DNS \_ QUERY \_ CACHE \_**.<br/>                                                                                                                                                                                                                                      |
| \_DNS-ABFRAGE \_ KEIN LOKALER \_ \_ NAME             | 0x00000020 | Leitet DNS an, den lokalen Namen zu ignorieren. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                    |
| DNS \_ QUERY \_ NO \_ HOSTS \_ FILE             | 0x00000040 | Verhindert, dass die DNS-Abfrage die HOSTS-Datei abfragt. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                   |
| DNS \_ QUERY \_ NO \_ NETBT                   | 0x00000080 | Verhindert, dass die DNS-Abfrage NetBT für die Auflösung verwendet. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                  |
| NUR \_ \_ DNS-ABFRAGEVERKABELUNG \_                  | 0x00000100 | Leitet DNS an, eine Abfrage nur über das Netzwerk auszuführen, und umgeht dabei lokale Informationen. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                      |
| DNS \_ QUERY \_ RETURN \_ MESSAGE             | 0x00000200 | Leitet DNS an, die gesamte DNS-Antwortnachricht zurück zu geben. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                   |
| NUR \_ \_ DNS-ABFRAGE -MULTICAST \_             | 0x00000400 | Verhindert, dass die Abfrage DNS verwendet, und verwendet nur die Multicastnamensauflösung (Local Link Multicast Name Resolution, LLMNR). **Windows Vista und Windows Server 2008 oder höher:** Dieser Wert wird unterstützt.<br/>                                                                                                                                                                                                                                                                  |
| DNS \_ QUERY \_ NO MULTICAST (DNS-ABFRAGE \_ OHNE MULTICAST)               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS \_ QUERY TREAT AS \_ \_ \_ FQDN (DNS-ABFRAGE ALS FQDN BEHANDELN)             | 0x00001000 | Verhindert, dass die DNS-Antwort Suffixe an den übermittelten Namen in einem Namensauflösungsprozess anfügen kann.                                                                                                                                                                                                                                                                                                                                                  |
| DNS \_ QUERY \_ ADDRCONFIG                  | 0x00002000 | Windows 7: Senden Sie [](/windows/win32/api/windns/ns-windns-dns_a_data) keine A-Typabfragen, wenn IPv4-Adressen auf einer Schnittstelle nicht verfügbar sind, und senden Sie keine Abfragen vom [**Typ AAAA,**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) wenn keine IPv6-Adressen verfügbar sind.                                                                                                                                                                                                                                   |
| DNS \_ QUERY \_ DUAL \_ ADDR                  | 0x00004000 | Windows 7: Abfragen von [**AAAA-**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) und A-Typdatensätzen und Zurückgeben von Ergebnissen für jede. [](/windows/win32/api/windns/ns-windns-dns_a_data) Ergebnisse  für A-Typdatensätze werden dem **AAAA-Typ** zugeordnet.                                                                                                                                                                                                                                                           |
| DNS \_ QUERY \_ MULTICAST \_ WAIT             | 0x00020000 | Wartet auf ein vollständiges Timeout, um alle Antworten vom lokalen Link zu erfassen. Wenn nicht festgelegt, ist das Standardverhalten, mit der ersten Antwort zurück zu geben. **Windows Vista und Windows Server 2008 oder höher:** Dieser Wert wird unterstützt.<br/>                                                                                                                                                                                                              |
| DNS \_ QUERY \_ MULTICAST \_ VERIFY           | 0x00040000 | Leitet einen Test mithilfe des Hostnamens des lokalen Computers an, um die Eindeutigkeit des Namens auf demselben lokalen Link zu überprüfen. Erfasst alle Antworten, auch wenn das normale LLMNR-Absenderverhalten nicht aktiviert ist. **Windows Vista und Windows Server 2008 oder höher:** Dieser Wert wird unterstützt.<br/>                                                                                                                                                                                  |
| \_ \_ DNS-ABFRAGE: \_ \_ TTL-WERTE NICHT \_ ZURÜCKSETZEN    | 0x00100000 | Wenn festgelegt und die Antwort mehrere Datensätze enthält, werden Datensätze mit der Tl gespeichert, die dem Mindestwert TTL aus allen Datensätzen entspricht. Wenn diese Option festgelegt ist, wird "TTL einzelner Datensätze nicht ändern" im zurückgegebenen Datensatz nicht geändert.                                                                                                                                                                               |
| \_DNS-ABFRAGE \_ DEAKTIVIEREN DER \_ IDN-CODIERUNG \_      | 0x00200000 | Deaktiviert die Unterstützung der IDN-Codierung (International Domain Name) in den [**APIs DnsQuery,**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) [**DnsQueryEx,**](/windows/desktop/api/Windns/nf-windns-dnsqueryex) [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)und [**DnsReplaceRecordSet.**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) Alle Punycodenamen werden als ASCII behandelt und im Kabel ASCII codiert. Alle Nicht-ASCII-Namen werden in UTF8 codiert. **Windows 8 oder höher:** Dieser Wert wird unterstützt.<br/> |
| DNS \_ QUERY \_ APPEND \_ MULTILABEL          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| RESERVIERTE \_ \_ DNS-ABFRAGE                    | 0xf0000000 | Reserviert.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>DNS-Updateoptionen



| Konstante                                 | Wert      | Bedeutung                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS \_ UPDATE \_ SECURITY \_ USE \_ DEFAULT      | 0x00000000 | Verwendet das Standardverhalten, das in der Registrierung angegeben ist, für sichere dynamische DNS-Updates.                                                                |
| DNS \_ UPDATE \_ SECURITY \_ OFF               | 0x00000010 | Versucht nicht, dynamische Updates zu sichern.                                                                                                                      |
| DNS \_ UPDATE \_ SECURITY \_ ON                | 0x00000020 | Versucht ein nicht sicheres dynamisches Update; Wenn dies abgelehnt wird, wird versucht, ein sicheres dynamisches Update zu erhalten.                                                                               |
| NUR \_ \_ DNS-UPDATESICHERHEIT \_              | 0x00000100 | Versucht nur, dynamische Updates zu sichern.                                                                                                                         |
| SICHERHEITSKONTEXT \_ DES \_ \_ DNS-UPDATECACHES \_    | 0x00000200 | Speichert den Sicherheitskontext für die Verwendung in zukünftigen Transaktionen zwischen.                                                                                                   |
| DNS \_ UPDATE TEST USE LOCAL SYS ACCT (DNS-UPDATETEST: \_ \_ \_ \_ LOKALES SYS \_ ACCT VERWENDEN) | 0x00000400 | Verwendet Anmeldeinformationen des lokalen Computerkontos.                                                                                                               |
| DNS \_ UPDATE \_ FORCE \_ SECURITY \_ NEGO       | 0x00000800 | Verwendet keinen zwischengespeicherten Sicherheitskontext.                                                                                                                         |
| \_DNS-UPDATE \_ ALLE \_ \_ MASTERSERVER \_ AUSPROBIEREN   | 0x00001000 | Sendet DNS-Updates an alle Multimaster-DNS-Server.                                                                                                            |
| DNS \_ UPDATE SKIP NO UPDATE \_ ADAPTERS (KEINE \_ \_ \_ UPDATEADAPTER ÜBERSPRINGEN)  | 0x00002000 | Aktualisieren Sie keine Adapter, bei denen dynamische DNS-Updates deaktiviert sind. **Windows 2000 Server mit SP2 oder höher:** Dieser Wert wird unterstützt.<br/>                 |
| DNS \_ UPDATE \_ REMOTE \_ SERVER              | 0x00004000 | Registrieren Sie CNAME-Einträge auf einem Remoteserver zusätzlich zum lokalen DNS-Server. **Windows 2000 Server mit SP2 oder höher:** Dieser Wert wird unterstützt.<br/> |
| \_DNS-UPDATE \_ RESERVIERT                    | 0xffff0000 | Für die zukünftige Verwendung reserviert.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>DNS-Antwortcodes



| Fehler                | Bedeutung                                        |
|----------------------|------------------------------------------------|
| DNS \_ RCODE \_ NOERROR  | Kein Fehler                                       |
| DNS \_ RCODE \_ FORMERR  | Formatfehler                                   |
| DNS \_ RCODE \_ SERVFAIL | Serverfehler                                 |
| DNS \_ RCODE \_ NXDOMAIN | Name error (Namesfehler)                                     |
| DNS \_ RCODE \_ NOTIMPL  | Nicht implementiert                                |
| DNS \_ RCODE \_ ABGELEHNT  | Verbindung verweigert                             |
| DNS \_ RCODE \_ YXDOMAIN | Domänenname darf nicht vorhanden sein                   |
| DNS \_ RCODE \_ YXRRSET  | Ressourcendatensatz (RR) darf nicht vorhanden sein      |
| DNS \_ RCODE \_ NXRRSET  | RR-Satz ist nicht vorhanden                          |
| DNS \_ RCODE \_ NOTAUTH  | Nicht autoritativ für Zone                     |
| DNS \_ RCODE \_ NOTZONE  | Name nicht in Zone                               |
| DNS \_ RCODE \_ BADVERS  | Fehlerhafter Erweiterungsmechanismus für DIE DNS-Version (EDNS) |
| DNS \_ RCODE \_ BADSIG   | Fehlerhafte Signatur                                  |
| DNS \_ RCODE \_ BADKEY   | Fehlerhafter Schlüssel                                        |
| DNS \_ RCODE \_ BADTIME  | Fehlerhafter Zeitstempel                                  |



 

 

 





