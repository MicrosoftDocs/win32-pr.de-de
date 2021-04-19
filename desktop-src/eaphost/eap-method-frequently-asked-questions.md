---
title: Häufig gestellte Fragen zur EAP-Methode
description: Bietet Antworten auf häufig gestellte Programmier Fragen zum Erstellen von EAP-Methoden.
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106342171"
---
# <a name="eap-method-frequently-asked-questions"></a>Häufig gestellte Fragen zur EAP-Methode

Dieses Thema enthält Antworten auf häufig gestellte Programmier Fragen zum Erstellen von EAP-Methoden.

## <a name="eap-method-frequently-asked-questions"></a>Häufig gestellte Fragen zur EAP-Methode



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
<td>Was sind &quot; Konfigurationsdaten &quot; ?</td>
<td>Die Begriffe &quot; Konfigurationsdaten &quot; und &quot; Verbindungsdaten &quot; sind synonym.</td>
</tr>
<tr class="even">
<td>Was sind &quot; Verbindungsdaten &quot; ?</td>
<td>&quot;Verbindungsdaten &quot; sind ein Methoden spezifisches EAP-BLOB, das Konfigurationsinformationen für die-Methode enthält. Diese Verbindungsdaten werden von der-Methode erstellt, wenn Sie erstmalig konfiguriert wird. Sie werden nie von einer anderen Komponente als der EAP-Methode selbst interpretiert oder geändert.</td>
</tr>
<tr class="odd">
<td>Was sind &quot; Anmelde Informationen &quot; ?</td>
<td>Die Nutzungs &quot; Bedingungen &quot; und die &quot; Benutzer &quot; Daten sind synonym.</td>
</tr>
<tr class="even">
<td>Was sind &quot; Benutzerdaten &quot; ?</td>
<td>&quot;Benutzerdaten &quot; sind ein Methoden spezifisches EAP-BLOB, das Benutzer Anmelde Informationen enthält, z. b. einen Benutzernamen und ein Kennwort. Die Benutzerdaten werden nie von einer anderen Komponente als der EAP-Methode selbst interpretiert oder geändert. Die Begriffe " &quot; Benutzerdaten" und "Anmelde Informationen" &quot; &quot; &quot; sind synonym.</td>
</tr>
<tr class="odd">
<td>Was ist ein &quot; EAP-Attribut &quot; ?</td>
<td>Bei einem &quot; EAP-Attribut &quot; handelt es sich um eine Datenstruktur, die einen vordefinierten Datentyp enthält. Attribute werden verwendet, um Informationen zwischen EAP-Methoden und Supplicants oder zwischen EAP-Methoden und Authentifikatoren zu übermitteln. Peer-und Authenticator-Implementierungen einer EAP-Methode können diese Attribute über ein Netzwerk austauschen.</td>
</tr>
<tr class="even">
<td>Können die Konfigurations-API und die Lauf Zeit-API in der gleichen Methoden-dll angezeigt werden?</td>
<td>Ja. Achten Sie darauf, dass Sie die Unterscheidung beim Konfigurieren der Registrierungseinträge für die EAP-Methode selbst angeben. Der Konfigurations Pfad und der peerpfad müssen identisch sein.</td>
</tr>
<tr class="odd">
<td>Können die Konfigurations-API und die Lauf Zeit-API in separaten Methoden-DLLs angezeigt werden?</td>
<td>Ja. Achten Sie darauf, dass Sie die Unterscheidung beim Konfigurieren der Registrierungseinträge für die EAP-Methode selbst angeben. Die Konfigurations-und Peer Pfade müssen auf die richtigen DLLs zeigen.</td>
</tr>
<tr class="even">
<td>Gewusst wie eine EAP-Methode installieren?</td>
<td>Zum Installieren einer EAP-Methode müssen Sie zuerst [<strong>DllRegisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DllRegisterServer) und [<strong>DllUnregisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DllUnregisterServer) in der EAP-Methoden-DLL selbst implementieren. Verwenden Sie anschließend <strong>regsvr32.exe</strong> , um die-Methode zu installieren und zu deinstallieren. Die entsprechenden Registrierungsschlüssel müssen ebenfalls festgelegt werden. Weitere Informationen finden Sie unter [Installieren einer EAP-Methode](installing-an-eap-method.md).<br/></td>
</tr>
<tr class="odd">
<td>Was ist der in-Band- [Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP)?</td>
<td>Wenn die in-Band-NAP-Unterstützung aktiviert ist, werden NAP-Pakete in EAP-Methoden Paketen transportiert. Wenn die Out-of-Band-NAP-Unterstützung aktiviert ist, wird der SoH-Austausch (NAP [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) ) im Gegensatz zu internen EAP-Methoden Paketen durchgeführt, und NAP-generierte Zertifikate werden in der EAP-Methoden Authentifizierung verwendet.</td>
</tr>
<tr class="even">
<td>Kann ich die in-Band-NAP-Unterstützung für meine EAP-Methode aktivieren?</td>
<td>Ja, die in-Band-NAP-Unterstützung für die EAP-Methode kann aktiviert werden. Weitere Informationen finden Sie [unter Aktivieren von In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md).</td>
</tr>
<tr class="odd">
<td>Wie funktioniert die flexible EAP-Authentifizierung über Secure Tunneling(EAP-fast)?</td>
<td>Das EAP-fast-Szenario funktioniert wie folgt. <br/>
<ul>
<li>Die-Methode verarbeitet eine Kenn Wort Änderung bei einmaligem Anmelden (Single-Sign-on, SSO) mit der-Methoden Benutzeroberfläche.</li>
<li>Die-Methode gibt das [<strong>eatkredentialschangi]</strong>(/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type)-Attribut zurück.</li>
<li>Der Supplicant zeigt dem Benutzer an, dass die Anmelde Informationen geändert wurden, und fordert den Benutzer auf, seine Anmelde Informationen erneut einzugeben.</li>
<li>Der Supplicant gibt die Benutzer Anmelde Informationen erneut ein und sendet diese Anmelde Informationen an die-Methode.</li>
</ul>
Weitere Informationen zu EAP-fast finden Sie unter [EAP-flexible Authentifizierung über sicheres Tunnelingverfahren](https://go.microsoft.com/fwlink/p/?linkid=84010) (EAP-fast).</td>
</tr>
<tr class="even">
<td>Was ist der vorinstallierte Schlüssel (Pre-Shared Key, PSK)?</td>
<td>Eine Methode zum übertragen und empfangen digitaler Signale, in der die Phase eines übertragenen Signals zum vermitteln von Informationen variiert. Das Eingabefeld [<strong>eapconfiginputpsk</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_config_input_field_type) enthält den EAP-fast-PSK des Benutzers.</td>
</tr>
<tr class="odd">
<td>Was ist wow, und wie ist es wichtig für EAPHost?</td>
<td>Microsoft Windows-32-Bit-on-Windows-64-Bit (WOW) ist eine Betriebssystem Komponente in 64-Bit-Windows, die die x86-Platt Form Anwendung 32-Bit unterstützt. Normalerweise würde ein EAP-Methoden Autor eine Form der C/C++-Struktur definieren, um Konfigurationsdaten, Anmeldedaten und interaktive Benutzeroberflächen Daten zu kapseln. Um Inkompatibilitäten in WoW und anderen Szenarien zu vermeiden, müssen Sie sicherstellen, dass die Datenstrukturen in verschiedenen Prozessorarchitekturen (32-Bit-und 64-Bit-Prozessoren) ähnlich ausgerichtet werden. In der Regel werden die Felder mit der Pseudo Auffüll Fläche so ausgerichtet, dass die Konfigurations-, Anmelde-und interaktiven UI-Daten sowohl auf 32-als auch 64-Bit-Prozessoren identisch sind.</td>
</tr>
<tr class="even">
<td>Was sind &quot; Aktionscodes, &quot; und unter welchen Bedingungen werden diese Aktionscodes zurückgegeben?</td>
<td>&quot;Aktionscodes &quot; ermöglichen es Methoden, den Authentifizierungs Fluss zu steuern, und sind für den Zustands Automaten ganzzahlig. Sie sind Werte, die von einer EAP-Methode zurückgegeben werden, um die nächste Aktion anzugeben, die der EAPHost ausführen sollte. Beispielsweise könnte ein Aktions Code EAPHost anzeigen, dass die EAP-Methode ein Paket für die Übertragung bereit hat. Der Supplicant hält alle Aktionscodes an, die von einer EAP-Methode zurückgegeben werden, gibt jedoch nie Aktionscodes aus. Weitere Informationen finden Sie unter [EAP-Peer-Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).<br/></td>
</tr>
<tr class="odd">
<td>Wann gibt eine Methode [<strong>eappeermethodresponseaction Discard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) zurück, und was bedeutet dieser Aktions Code für EAPHost?</td>
<td>[<strong>Eappeermethodresponeraktionverwerfen</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) wird von einer EAP-Methode zurückgegeben, um dem EAPHost mitzuteilen, dass er das Paket verwerfen muss, das er für die Methode bereitgestellt hat. Insbesondere hat die-Methode festgestellt, dass das Paket ungültig ist. EAPHost wartet dann auf das nächste Paket.</td>
</tr>
<tr class="even">
<td>Wann gibt eine Methode [<strong>eappeermethodresponseaction Send</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) zurück, und was bedeutet dieser Aktions Code für EAPHost?</td>
<td>[<strong>Eappeermethodresponabaktionsend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) wird von einer EAP-Methode zurückgegeben, um für EAPHost anzugeben, dass das nächste von EAPHost empfangene Paket an den Netzwerk Zugriffs Server (NAS) gesendet werden muss.</td>
</tr>
<tr class="odd">
<td>Wann gibt eine Methode [<strong>eappeermethodresponseaction result</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) zurück, und was bedeutet dieser Aktions Code für EAPHost?</td>
<td>[<strong>Eappeermethodresponseaktionresult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) wird von einer EAP-Methode zurückgegeben, um dem EAPHost mitzuteilen, dass die Authentifizierungs Sitzung abgeschlossen wurde und dass die Ergebnisse dieser Sitzung verfügbar sind.</td>
</tr>
<tr class="even">
<td>Wann gibt eine Methode [<strong>eappeermethodresponseaction invokeui</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) zurück, und was bedeutet dieser Aktions Code für EAPHost?</td>
<td>[<strong>Eappeermethodresponabaktioninvokeui</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) wird von einer EAP-Methode zurückgegeben, die besagt, dass für EAPHost eine Benutzereingabe erforderlich ist, um die Authentifizierung fortzusetzen, und dass ein Dialogfeld für die Benutzeroberfläche angezeigt werden muss, um diese Eingabe zu erhalten. Nachdem die Benutzereingabe Daten abgerufen wurden, kann EAPHost die EAP-Methode erneut mit den aktualisierten UI-Kontext Daten aufrufen.</td>
</tr>
<tr class="odd">
<td>Wann gibt eine Methode [<strong>eappeermethodresponseaction</strong>Response] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) zurück, und was bedeutet dieser Aktions Code für EAPHost?</td>
<td>[<strong>Eappeermethodresponse-Aktions Antwort</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) wird von einer EAP-Methode zurückgegeben, um EAPHost anzugeben, dass die EAP-Methode über Attribute verfügt, die für die Verwendung während der Authentifizierung für EAPHost verfügbar sind. EAPHost Ruft die Attribute durch Aufrufen der [<strong>eappeergetresponlattribute</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeergetresponseattributes)-Methode ab, gefolgt von einem Aufruf der [<strong>eappeersettresponlattributs</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetresponseattributes)-Methode.</td>
</tr>
<tr class="even">
<td>Wann gibt eine Methode [<strong>eappeermethodresponseaction None</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) zurück, und was bedeutet dieser Aktions Code für EAPHost?</td>
<td>[<strong>Eappeermethodresponeraktionnone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) wird von einer EAP-Methode zurückgegeben, um für EAPHost anzugeben, dass zurzeit keine Aktion erforderlich ist.</td>
</tr>
<tr class="odd">
<td>Kann ich die Ablauf Verfolgung auf der Authenticator-Seite aktivieren?</td>
<td>Ja. Weitere Informationen finden Sie unter [aktivieren](enabling-tracing.md)der Ablauf Verfolgung.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Referenz für die EAPHost-Peer Methode](eap-host-peer-method-api-reference.md)
</dt> <dt>

[Allgemeine FAQs zu EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[FAQ zu EAPHost-Supplicant](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[EAPHost-Entwicklungs FAQs](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

