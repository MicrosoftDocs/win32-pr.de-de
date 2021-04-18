---
title: Allgemeine häufig gestellte Fragen
description: Lesen Sie Antworten auf häufig gestellte Fragen zu den EAPHost-APIs, z. b. "wie lautet die Lebensdauer einer Authentifizierung?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106339105"
---
# <a name="general-frequently-asked-questions"></a>Allgemeine häufig gestellte Fragen

Im folgenden Thema finden Sie Antworten auf häufig gestellte Fragen zu den EAPHost-APIs.

### <a name="general-frequently-asked-questions"></a>Allgemeine häufig gestellte Fragen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Frage</th>
<th>Antwort</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Was ist ein Supplicant?</td>
<td>Der Supplicant ist die Entität, die mithilfe von EAPHost authentifiziert werden soll. Typische Supplicants sind [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Clients, 802,3-Clients und RRAS (Routing-und RAS-Dienst), Punkt-zu-Punkt-Clients (PPP).</td>
</tr>
<tr class="even">
<td>Was ist ein Peer?</td>
<td>Der Peer ist die Clientseite einer EAP-Authentifizierung.</td>
</tr>
<tr class="odd">
<td>Wie unterscheidet sich ein Peer von einem Supplicant?</td>
<td>Der Supplicant transportiert Pakete, während ein Peer dies nicht tut. Dennoch sind die Begriffe "Peer", "Supplicant" und "Client" größtenteils Synonym.</td>
</tr>
<tr class="even">
<td>Was ist ein Authentifikator?</td>
<td>Der Authentifikator ist der drahtlos Zugriffspunkt, der Netzwerk Zugriffs Server (Network Access Server, NAS) oder das Netzwerk Zugriffsgerät (nad), das den Supplicant authentifiziert. Der Authentifikator wird auch als EAP-Server bezeichnet.</td>
</tr>
<tr class="odd">
<td>Was ist die Lebensdauer einer Authentifizierung?</td>
<td>Die Lebensdauer einer einzelnen Authentifizierungs Sitzung auf der Clientseite ist alles, was zwischen den aufgerufenen Funktionen [<strong>eaphostpeer erbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) und [<strong>eaphostpeer erendsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) auftritt. Die Lebensdauer auf der Authenticator-Seite ist alles, was zwischen den Funktionen [<strong>eappeerbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) und [<strong>eappeerendsession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession) auftritt.</td>
</tr>
<tr class="even">
<td>Was ist ein BLOB? Warum würde ich ein Konfigurations-BLOB (Binary) in XML konvertieren?</td>
<td>Ein BLOB ist eine Binary Large Object. XML hat mehrere Vorteile gegenüber einem binären konfigurationsblob. Konfigurationsdaten, die in XML gespeichert werden, sind lesbarer, Benutzer bearbeitbarer und plattformübergreifender.</td>
</tr>
<tr class="odd">
<td>Wann kann ich ein gespeichertes XML-BLOB in ein binäres Blob konvertieren?</td>
<td>Es ist möglich, ein binäres Blob oder ein XML-BLOB zu speichern, aber Sie müssen das XML-BLOB immer wieder in ein binäres Blob konvertieren, bevor es mit Lauf Zeit-APIs verwendet werden kann. die Lauf Zeit-APIs können ein XML-Verzeichnis nicht akzeptieren.</td>
</tr>
<tr class="even">
<td>Was sind native Methoden?</td>
<td>Native EAP-Methoden verwenden die neue EAPHost-API.</td>
</tr>
<tr class="odd">
<td>Was sind Legacy Methoden?</td>
<td>Ältere EAP-Methoden werden in der [Extensible Authentication-Protokoll Referenz](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference)definiert. Die Legacy-EAP-Methoden stehen für die Verwendung in Windows Vista und Windows Server 2008 zur Verfügung. Diese Methoden sind möglicherweise nicht für die Verwendung in nachfolgenden Versionen des Betriebssystems verfügbar.</td>
</tr>
<tr class="even">
<td>Worin besteht der Unterschied zwischen Legacy-und systemeigenen Methoden?</td>
<td>Die nativen APIs sind einfacher und verfügen über weniger Features. Alle neuen EAP-Methoden sollten mithilfe der EAPHost-API geschrieben werden.</td>
</tr>
<tr class="odd">
<td>Was ist eine &quot; Gruppenrichtlinie &quot; ?</td>
<td>Eine Beschreibung der Gruppenrichtlinie finden Sie unter [Gruppenrichtlinie Sammlung](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Können EAPHost-Funktionen die von der Gruppenrichtlinie angegebene Konfigurationsrichtlinie außer Kraft setzen?</td>
<td>Nein, niemals. Wenn die Gruppenrichtlinie verwendet wird, werden die EAPHost-Konfigurationseinstellungen von Gruppenrichtlinien Einstellungen immer überschrieben.</td>
</tr>
<tr class="odd">
<td>Was ist einmaliges Anmelden (Single-Sign-on, SSO)?</td>
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) ist ein Mechanismus für die Layer-2-Authentifizierung. Abhängig von der SSO-Konfiguration ermöglicht SSO Benutzern, sich vor oder unmittelbar nach der Anmeldung bei Windows bei dem Netzwerk mithilfe der [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Authentifizierung zu authentifizieren. SSO kann so konfiguriert werden, dass Windows-Anmelde Informationen für die Netzwerk Authentifizierung verwendet werden (in diesem Fall geben die Benutzer ihre Anmelde Informationen nur einmal ein) oder verwenden andere Anmelde Informationen für Windows-und Netzwerk Authentifizierung. Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).<br/></td>
</tr>
<tr class="even">
<td>Was ist der Zugriffs Anbieter für die Vorab Anmeldung (PLAP)</td>
<td>Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).</td>
</tr>
<tr class="odd">
<td>Was ist das Protected Extensible Authentication Protocol (Peer)?</td>
<td>Weitere Informationen finden Sie unter [Peer-App](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) und Informationen [zum Extensible Authentication-Protokoll](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</td>
</tr>
<tr class="even">
<td>Wie geht es mit der Sitzungs Wiederaufnahme und der erneuten Authentifizierung durch.</td>
<td>Die Wiederaufnahme der Sitzung und die erneute Authentifizierung treten in der Regel beim Roaming in einem Drahtlos Netzwerk auf. Die Windows-Datenschutz-API (DPAPI) bietet eine Möglichkeit, Daten zu schützen und an einen Benutzer und optional an die Anmelde Sitzung zu binden. Der Aufrufer gibt [<strong>cryptprotectmemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) einen unverschlüsselten Puffer an, und DPAPI verschlüsselt den Speicher an Ort und Stelle. Später kann der Aufrufer den verschlüsselten Puffer an [<strong>cryptunprotectmemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) übergeben, und DPAPI entschlüsselt den Speicher wieder. Weitere Informationen finden Sie unter [TLS-interne Anwendungs Erweiterung (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) und [Peer-App](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).<br/></td>
</tr>
<tr class="odd">
<td>Was ist EAP-Transport Level Security (EAP-TLS)?</td>
<td>EAP-TLS ist ein Client/Server-Protokoll, bei dem unterschiedliche Zertifikat Profile in der Regel für den Client und den Server verwendet werden. Weitere Informationen finden Sie unter [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/></td>
</tr>
<tr class="even">
<td>Gewusst wie eine Kenn Wort Änderung mithilfe der API der lokalen Sicherheits Autorität (Local Security Authority, LSA) implementieren?</td>
<td>Verwenden Sie die [<strong>lsacallauthenticationpackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage)-Funktion, um eine Kenn Wort Änderung zu implementieren.</td>
</tr>
<tr class="odd">
<td>Warum soll die Ablauf Verfolgung in EAPHost aktiviert werden?</td>
<td>Die Ablauf Verfolgungs Protokolle enthalten Debuginformationen (nur in englischer Sprache), die Microsoft-Entwicklern und-Partnern dabei helfen können, die Hauptursachen von Problemen zu ermitteln, die mit dem Authentifizierungsprozess auftreten. Weitere Informationen finden Sie unter [aktivieren](enabling-tracing.md)der Ablauf Verfolgung.<br/></td>
</tr>
<tr class="even">
<td>Warum erhalte ich den Fehlercode NTE_BAD_KEY_STATE (0x8009000bl), wenn ich die [Kryptografie](/windows/desktop/SecCrypto/cryptography-portal) -API zum Anmelden beim EAP-TLS-Austausch verwende?</td>
<td>In WinError. h wird NTE_BAD_KEY_STATE (0x8009000bl) als Schlüssel definiert, &quot; der nicht für die Verwendung im angegebenen Zustand gültig ist &quot; . Dieser Fehler wird in der Regel in den folgenden Szenarien zurückgegeben.
<ul>
<li>Beim Versuch, ein nicht exportier bares privates Schlüssel-BLOB zu exportieren</li>
<li>Bei einem erfolglosen Versuch, ein Pseudo zufälliges Funktions-Hash handle (PRF) mithilfe von [<strong>cryptkreatehash</strong>] (/Windows/Desktop/API/wincrypt/NF-wincrypt-cryptcreatehash) zu generieren.</li>
</ul>
Weitere Informationen finden Sie unter [Beenden von Nachrichten im TLS 1,0-Protokoll](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</td>
</tr>
<tr class="odd">
<td>Was ist eine pseudo zufällige Funktion (PRF)?</td>
<td>Eine Funktion, die einen Schlüssel, eine Bezeichnung und einen Ausgangswert als Eingabe annimmt und dann eine Ausgabe beliebiger Länge erzeugt. Weitere Informationen finden Sie unter [Beenden von Nachrichten im TLS 1,0-Protokoll](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).<br/></td>
</tr>
<tr class="even">
<td>Wie wird EAPHost an Netzwerkadapter gebunden?</td>
<td>EAPHost ermöglicht das gleichzeitige Betreiben mehrerer Supplicants, und jede Supplicant kann an mehrere Netzwerkadapter gebunden werden. EAPHost-Supplicants stellen eine Bindung an die Netzwerk Ebenen bereit und Steuern den Authentifizierungsprozess. Supplicants enthalten die Authentifizierungs Konfiguration. Supplicants speichert auch den Zustand und stellt nachfolgende Verbindungssicherheit bereit. Da EAPHost nicht direkt an einen Netzwerk Mechanismus gebunden wird, ist die Erweiterbarkeit möglich.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[FAQ zu EAPHost-Supplicant](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[FAQ zu EAPHost-Methoden](eap-method-frequently-asked-questions.md)
</dt> <dt>

[EAPHost-Entwicklungs FAQs](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

