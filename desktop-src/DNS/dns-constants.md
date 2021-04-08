---
title: DNS-Konstanten
description: Die folgenden Konstanten werden für DNS in der Host-Byte Reihenfolge definiert.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64497e14d6c4ae11f4a6ed68200614aa4f602270
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038612"
---
# <a name="dns-constants"></a>DNS-Konstanten

Die folgenden Konstanten werden für DNS in der Host-Byte Reihenfolge definiert.

## <a name="dns-record-types"></a>DNS-Daten Satz Typen



| Konstante           | Wert            |
|--------------------|------------------|
| DNS- \_ Typ \_ A       | 0x0001           |
| DNS- \_ Typ- \_ NS      | 0x0002           |
| DNS- \_ Typ \_ MD      | 0x0003           |
| DNS- \_ Typ- \_ MF      | 0x0004           |
| DNS- \_ Typ \_ CNAME   | 0x0005           |
| DNS- \_ Typ \_ SOA     | 0x0006           |
| DNS- \_ Typ \_ MB      | 0x0007           |
| DNS- \_ Typ- \_ mg      | 0x0008           |
| DNS- \_ Typ \_ Mr      | 0x0009           |
| DNS- \_ Typ \_ null    | 0x000a           |
| DNS- \_ Typ- \_ Wert     | 0x000b           |
| DNS- \_ Typ \_ ptr     | 0x000c           |
| DNS- \_ Typ \_ hinfo   | 0x000d           |
| DNS- \_ Typ \_ MINFO   | 0x000e           |
| DNS- \_ Typ \_ MX      | 0x000f           |
| DNS \_ - \_ Typtext    | 0x0010           |
| DNS- \_ Typ- \_ RP      | 0x0011           |
| DNS- \_ Typ \_ AFSDB   | 0x0012           |
| DNS- \_ Typ \_ x25     | 0x0013           |
| DNS- \_ Typ \_ ISDN    | 0x0014           |
| DNS- \_ Typ \_ RT      | 0x0015           |
| DNS- \_ Typ \_ NSAP    | 0x0016           |
| DNS- \_ Typ \_ nsapptr | 0x0017           |
| DNS- \_ Typ \_ sig     | 0x0018           |
| DNS \_ - \_ Typschlüssel     | 0x0019           |
| DNS- \_ Typ \_ px      | 0x001a           |
| DNS-Typ-Gruppenrichtlinien Objekte \_ \_    | 0x001b           |
| DNS- \_ Typ \_ AAAA    | 0x001c           |
| DNS- \_ Typ \_ Loc     | 0x001d           |
| DNS- \_ Typ \_ NXT     | 0x001e           |
| DNS- \_ Typ- \_ Eid     | 0x001F           |
| DNS- \_ Typ " \_ nimloc"  | 0x0020           |
| DNS- \_ Typ \_ SRV     | 0x0021           |
| DNS- \_ Typ \_ Atma    | 0x0022           |
| DNS- \_ Typ ( \_ NAPTR)   | 0x0023           |
| DNS- \_ Typ \_ Kx      | 0x0024           |
| DNS \_ - \_ typzertifikat    | 0x0,025           |
| DNS- \_ Typ \_ a6      | 0x0026           |
| DNS- \_ Typ \_ DName   | 0x0027           |
| DNS \_ - \_ typsenke    | 0x0028           |
| DNS \_ - \_ typopt     | 0x0000           |
| DNS- \_ Typ- \_ DS      | 0x002b           |
| DNS- \_ Typ \_ RRSIG   | 0x002e           |
| DNS- \_ Typ \_ nsec    | 0x002f           |
| DNS- \_ Typ \_ DNSKEY  | 0x0030           |
| DNS- \_ Typ \_ DHCID   | 0x0031           |
| DNS- \_ Typ- \_ uinfo   | 0x0064           |
| DNS- \_ Typ- \_ UID     | 0x0065           |
| DNS- \_ Typ- \_ gid     | 0x0066           |
| DNS- \_ Typ \_ nicht Spezifikation  | 0x0067           |
| DNS- \_ Typ- \_ addrs   | 0x00f 8           |
| DNS- \_ Typ \_ TKey    | 0x00f 9           |
| DNS- \_ Typ \_ TSIG    | 0x00fa           |
| DNS- \_ Typ \_ IXFR    | 0x00fb           |
| DNS- \_ Typ \_ AXFR    | 0x00fc           |
| DNS- \_ Typ \_ mailb   | 0x00fd           |
| DNS- \_ Typ \_ Maila   | 0x00fe           |
| DNS- \_ Typ \_ alle     | 0x00FF           |
| DNS- \_ Typ \_ beliebig     | 0x00FF           |
| DNS- \_ Typ \_ WINS    | 0xff01           |
| DNS- \_ Typ \_ WINSR   | 0xff02           |
| DNS- \_ Typ \_ nbstat  | DNS- \_ Typ \_ WINSR |



 

## <a name="dns-class-types"></a>DNS-Klassentypen



| Konstante             | Wert  |
|----------------------|--------|
| DNS- \_ Klasse \_ Internet | 0x0001 |
| DNS- \_ Klasse ( \_ CSNET)    | 0x0002 |
| DNS- \_ Klassen \_ Chaos    | 0x0003 |
| DNS- \_ Klasse \_ hesiod   | 0x0004 |
| DNS- \_ Klasse \_ None     | 0x00fe |
| Alle DNS- \_ Klasse \_      | 0x00FF |
| DNS- \_ Klasse \_ Any      | 0x00FF |



 

## <a name="dns-query-types"></a>DNS-Abfragetypen



| Konstante                    | Wert  |
|-----------------------------|--------|
| DNS- \_ Opcode- \_ Abfrage          | 0x0000 |
| DNS- \_ Opcode ( \_ IQUERY)         | 0x0001 |
| DNS- \_ Opcode- \_ Server \_ Status | 0x0002 |
| Unbekannter DNS- \_ Opcode. \_        | 0x0003 |
| DNS- \_ Opcode \_ Benachrichtigen         | 0x0004 |
| DNS- \_ Opcode- \_ Update         | 0x0005 |



 

## <a name="dns-record-flags"></a>DNS-Datensatz-Flags

Die folgenden Flags verweisen auf den Abschnitt (RR) eines Ressourceneinsatzes innerhalb einer DNS-Nachricht:



| Konstante           | Wert      | Bedeutung                         |
|--------------------|------------|---------------------------------|
| dnsrec- \_ Frage   | 0x00000000 | RR befindet sich im Abschnitt "Frage"   |
| dnsrec- \_ Antwort     | 0x00000001 | RR befindet sich im Abschnitt "Antwort".     |
| dnsrec- \_ Autorität  | 0x00000002 | RR befindet sich im Abschnitt "Authority".  |
| dnsrec \_ zusätzlich | 0x00000003 | RR befindet sich im zusätzlichen Abschnitt |



 

Die folgenden Flags verweisen auf einen RR-Abschnitt innerhalb einer DNS-Update Nachricht pro [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt):



| Konstante       | Wert      | Bedeutung                           |
|----------------|------------|-----------------------------------|
| dnsrec- \_ Zone   | 0x00000000 | RR befindet sich im Abschnitt "Zone".         |
| dnsrec \_ Prereq | 0x00000001 | RR befindet sich im Abschnitt "Voraussetzung" |
| dnsrec- \_ Update | 0x00000002 | RR befindet sich im Abschnitt "Update".       |



 

Die folgenden Flags schließen sich gegenseitig aus:



| Konstante        | Wert      | Bedeutung                                                    |
|-----------------|------------|------------------------------------------------------------|
| dnsrec \_ Löschen  | 0x00000004 | Löschen eines RR-. Wird in Verbindung mit der dnsrec-Aktualisierung verwendet. \_       |
| dnsrec- \_ Knoten | 0x00000004 | RR ist nicht vorhanden. Wird in Verbindung mit dnsrec \_ Prereq verwendet. |



 

## <a name="dns-query-options"></a>DNS-Abfrage Optionen



| Konstante                                | Wert      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS- \_ Abfrage \_ Standard                    | 0x00000000 | Standard Abfrage.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS- \_ Abfrage \_ Accept \_ truncated \_ Response | 0x00000001 | Gibt abgeschnittene Ergebnisse zurück. Der Versuch unter TCP wird nicht wiederholt.                                                                                                                                                                                                                                                                                                                                                                                                   |
| DNS \_ - \_ Abfrage \_ nur TCP verwenden \_              | 0x00000002 | Verwendet TCP nur für die Abfrage.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| DNS- \_ Abfrage \_ keine \_ Rekursion               | 0x00000004 | Weist den DNS-Server an, eine iterative Abfrage auszuführen (weist den DNS-Server insbesondere an, keine rekursive Auflösung zum Auflösen der Abfrage auszuführen).                                                                                                                                                                                                                                                                                                   |
| DNS- \_ Abfrage \_ Umgehungs \_ Cache               | 0x00000008 | Umgeht den Konflikt [*Löser Cache für die Suche*](r-gly.md) .                                                                                                                                                                                                                                                                                                                                                                            |
| DNS- \_ Abfrage \_ keine Wire- \_ \_ Abfrage             | 0x00000010 | Weist DNS an, nur eine Abfrage im lokalen Cache auszuführen. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt. Verwenden Sie für eine ähnliche Funktionalität **nur den DNS- \_ Abfrage \_ Cache \_**.<br/>                                                                                                                                                                                                                                      |
| DNS- \_ Abfrage \_ kein \_ lokaler \_ Name             | 0x00000020 | Weist DNS an, den lokalen Namen zu ignorieren. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                    |
| DNS \_ - \_ Abfrage \_ keine \_ Hostdatei             | 0x00000040 | Verhindert, dass die DNS-Abfrage die Hostdatei konsultiert. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                   |
| DNS- \_ Abfrage \_ nicht \_ NetBT                   | 0x00000080 | Verhindert, dass die DNS-Abfrage NetBT zur Auflösung verwendet. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                  |
| nur DNS- \_ Abfrage Netzwerk \_ \_                  | 0x00000100 | Weist DNS an, eine Abfrage nur mit dem Netzwerk auszuführen, wobei lokale Informationen umgangen werden. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                      |
| DNS- \_ Abfrage \_ Rückgabe \_ Meldung             | 0x00000200 | Weist DNS an, die gesamte DNS-Antwortnachricht zurückzugeben. **Windows 2000 Server und Windows 2000 Professional:** Dieser Wert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                   |
| \_ \_ nur Multicast für DNS-Abfragen \_             | 0x00000400 | Verhindert, dass die Abfrage DNS verwendet und nur eine lokale Link-Multicast-Namensauflösung (LLMNR) verwendet wird. **Windows Vista und Windows Server 2008 oder höher:** Dieser Wert wird unterstützt.<br/>                                                                                                                                                                                                                                                                  |
| DNS- \_ Abfrage \_ kein \_ Multicast               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DNS \_ - \_ Abfrage \_ als voll qualifizierten Namen behandeln \_             | 0x00001000 | Verhindert, dass die DNS-Antwort Suffixe an den übermittelten Namen in einem namens Auflösungsprozess anfügt.                                                                                                                                                                                                                                                                                                                                                  |
| DNS- \_ Abfrage \_ addrconfig                  | 0x00002000 | Nur Windows 7: senden Sie keine [**typabfragen**](/windows/win32/api/windns/ns-windns-dns_a_data) , wenn keine IPv4-Adressen für eine Schnittstelle verfügbar sind, und senden Sie keine [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) -typabfragen, wenn keine IPv6-Adressen verfügbar sind.                                                                                                                                                                                                                                   |
| \_Dual- \_ \_ addr für DNS-Abfrage                  | 0x00004000 | Nur Windows 7: Fragen Sie sowohl [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) [**-als auch Typdaten**](/windows/win32/api/windns/ns-windns-dns_a_data) Sätze ab, und geben Sie jeweils Ergebnisse zurück. Die Ergebnisse für einen Typ-Daten Satz werden **dem** **AAAA** -Typ zugeordnet.                                                                                                                                                                                                                                                           |
| \_ \_ Multicast Wartezeit für DNS-Abfragen \_             | 0x00020000 | Wartet auf ein vollständiges Timeout, um alle Antworten von der lokalen Verknüpfung zu erfassen. Wenn nicht festgelegt, besteht das Standardverhalten darin, mit der ersten Antwort zurückzugeben. **Windows Vista und Windows Server 2008 oder höher:** Dieser Wert wird unterstützt.<br/>                                                                                                                                                                                                              |
| DNS- \_ Abfrage \_ Multicast- \_ Überprüfung           | 0x00040000 | Leitet einen Test mithilfe des Hostnamens des lokalen Computers um, um die namens Eindeutigkeit für die gleiche lokale Verknüpfung zu überprüfen. Sammelt alle Antworten, auch wenn normales LLMNR-Absender Verhalten nicht aktiviert ist. **Windows Vista und Windows Server 2008 oder höher:** Dieser Wert wird unterstützt.<br/>                                                                                                                                                                                  |
| DNS- \_ Abfrage nicht \_ \_ Zurücksetzen von TTL- \_ \_ Werten    | 0x00100000 | Wenn diese Einstellung festgelegt ist und die Antwort mehrere Datensätze enthält, werden die Datensätze mit der Gültigkeitsdauer der Gültigkeitsdauer (TTL) für alle Datensätze gespeichert. Wenn diese Option festgelegt ist, wird "die Gültigkeitsdauer einzelner Datensätze nicht ändern" im zurückgegebenen Daten Satz Satz nicht geändert.                                                                                                                                                                               |
| DNS- \_ Abfrage \_ deaktivierte \_ IDN- \_ Codierung      | 0x00200000 | Deaktiviert die Unterstützung der Unterstützung für internationale Domänen Namen (IDN) in den APIs [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a), [**dnsqueryex**](/windows/desktop/api/Windns/nf-windns-dnsqueryex), [**dnsmodifyrecordsinset**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)und [**dnsreplacerecordset**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) . Alle Punycode-Namen werden als ASCII behandelt und werden bei der Übertragung ASCII-codiert. Alle nicht-ASCII-Namen werden bei der Übertragung in UTF8 codiert. **Windows 8 oder höher:** Dieser Wert wird unterstützt.<br/> |
| DNS-Abfrage-anfügende \_ \_ \_ mehrfach Bezeichnung          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_reservierte DNS-Abfrage \_                    | "0xF0000000" | Reserviert.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>DNS-Aktualisierungs Optionen



| Konstante                                 | Wert      | Bedeutung                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standardeinstellung für die DNS- \_ Update \_ Sicherheit \_ \_      | 0x00000000 | Verwendet das in der Registrierung angegebene Standardverhalten für sichere dynamische DNS-Updates.                                                                |
| DNS- \_ Update \_ Sicherheit deaktiviert \_               | 0x00000010 | Versucht nicht, dynamische Updates zu sichern.                                                                                                                      |
| DNS- \_ Update \_ Sicherheit \_ für                | 0x00000020 | Versucht ein nicht sicheres dynamisches Update; Wenn Sie abgelehnt wird, versucht, das dynamische Update zu sichern                                                                               |
| nur DNS- \_ Update \_ Sicherheit \_              | 0x00000100 | Versucht nur, dynamische Updates zu sichern.                                                                                                                         |
| DNS- \_ Update \_ Cache- \_ Sicherheits \_ Kontext    | 0x00000200 | Speichert den Sicherheitskontext für die Verwendung in zukünftigen Transaktionen zwischen.                                                                                                   |
| DNS- \_ Update \_ Test \_ use \_ local \_ sys \_ Acct | 0x00000400 | Verwendet die Anmelde Informationen des lokalen Computer Kontos.                                                                                                               |
| DNS- \_ Update \_ Force-Sicherheit ( \_ \_ NGO)       | 0x00000800 | Verwendet keinen zwischengespeicherten Sicherheitskontext.                                                                                                                         |
| DNS \_ - \_ Update \_ alle \_ Master \_ Server testen   | 0x00001000 | Sendet DNS-Updates an alle DNS-Server mit mehreren Mastern.                                                                                                            |
| DNS- \_ Update- \_ \_ keine \_ Update \_ Adapter überspringen  | 0x00002000 | Aktualisieren Sie keine Adapter, bei denen dynamische DNS-Updates deaktiviert sind. **Windows 2000 Server mit SP2 oder höher:** Dieser Wert wird unterstützt.<br/>                 |
| DNS- \_ Update- \_ Remote \_ Server              | 0x00004000 | Registrieren Sie CNAME-Einträge auf einem Remote Server zusätzlich zum lokalen DNS-Server. **Windows 2000 Server mit SP2 oder höher:** Dieser Wert wird unterstützt.<br/> |
| DNS- \_ Update \_ reserviert                    | 0xFFFF0000 | Für die zukünftige Verwendung reserviert.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>DNS-Antwort Codes



| Fehler                | Bedeutung                                        |
|----------------------|------------------------------------------------|
| DNS- \_ RCODE \_ noError  | Kein Fehler                                       |
| DNS- \_ RCODE- \_ FORMERR  | Formatierungs Fehler                                   |
| DNS- \_ RCODE- \_ SERVFAIL | Server Fehler                                 |
| DNS- \_ RCODE- \_ nxdomäne | Namensfehler                                     |
| DNS- \_ RCODE- \_ Benachrichtigung  | Nicht implementiert                                |
| DNS- \_ RCODE wurde \_ verweigert.  | Verbindung verweigert                             |
| DNS- \_ RCODE- \_ jdomäne | Der Domänen Name darf nicht vorhanden sein                   |
| DNS- \_ RCODE- \_ yxrrset  | Der Ressourcen Daten Satz Satz (RR) darf nicht vorhanden sein.      |
| DNS- \_ RCODE- \_ nxrrset  | Der RR-Satz ist nicht vorhanden.                          |
| DNS- \_ RCODE- \_ notauth  | Für Zone nicht autorisierend                     |
| DNS- \_ RCODE- \_ notzone  | Name nicht in Zone                               |
| DNS- \_ RCODE- \_ badvers  | Ungültiger Erweiterungsmechanismus für die DNS-Version (EDNS) |
| DNS- \_ RCODE \_ BadSig   | Ungültige Signatur.                                  |
| DNS- \_ RCODE- \_ badkey   | Ungültige Taste                                        |
| DNS- \_ RCODE- \_ badtime  | Ungültiger Zeitstempel                                  |



 

 

 





