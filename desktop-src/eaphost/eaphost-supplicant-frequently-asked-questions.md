---
title: Häufig gestellte Fragen zu EAPHost-Supplicant
description: Dieses Thema enthält Antworten auf häufig gestellte Fragen zur EAPHost-Supplicant-API.
ms.assetid: bf8db711-386e-47c2-be47-4cfd6c4d8d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38e75220b186ef58f2b9f264f8f5fc0550a4119
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "103735297"
---
# <a name="eaphost-supplicant-frequently-asked-questions"></a>Häufig gestellte Fragen zu EAPHost-Supplicant

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur EAPHost-Supplicant-API.

### <a name="eaphost-supplicant-frequently-asked-questions"></a>Häufig gestellte Fragen zu EAPHost-Supplicant



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
<td>Warum muss ich [<strong>eaphostpeer Initialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) und [<strong>eaphostpeer. Initialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) anrufen?</td>
<td>[<strong>Eaphostpeer Initialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) und [<strong>eaphostpeer-initialisieren</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) initialisieren Sie die für die prozessübergreifende Kommunikation (prozessübergreifende Communication, IPC) verwendete com-Umgebung zwischen einem Supplicant und EAPHost, und entfernen Sie die Initialisierung.</td>
</tr>
<tr class="even">
<td>Welche Funktionen müssen für Threads aufgerufen werden, die com für [Single Thread-Apartment](/previous-versions/ms810413(v=msdn.10)) (STA) initialisieren?</td>
<td>[<strong>Eaphostpeerinvokeconfigui</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), [<strong>eaphostpeerinvokeinteractiveui</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) und [<strong>eaphostauthentipeorinvokeconfigui</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodauthenticatorapis/NF-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui) müssen für Threads aufgerufen werden, die com für STA initialisieren. Dies kann durch Aufrufen der com-API [<strong>CoInitialize</strong>] (/Windows/Win32/API/objbase/NF-objbase-CoInitialize) erreicht werden. Wenn die Supplicant mit dem STA-Thread beendet wurde, muss der STA-Thread [<strong>zählinitialize</strong>] (/Windows/Win32/API/combaseapi/NF-combaseapi-CoUninitialize) vor dem Beenden aufgerufen werden.</td>
</tr>
<tr class="odd">
<td>Wie exportiert EAPHost das Schlüsselmaterial?</td>
<td>EAPHost-EAP-Methoden exportieren Master Sitzungsschlüssel (Master Session Keys, msks) in Form von Microsoft Point-to-Point Encryption (MPPE)-Schlüsseln an die Supplicants. Zusätzliches Schlüsselmaterial, wie z. b. paar Weise Hauptschlüssel (PMKS), kann vom Supplicant mithilfe des MSK generiert werden. Damit die-Methoden während der Authentifizierung andere Schlüssel generieren können, können die Methoden diese Schlüssel als anbieterspezifische Attribute für die Supplicants bereitstellen.</td>
</tr>
<tr class="even">
<td>Was ist ein erweiterter Master Sitzungsschlüssel (emsk)?</td>
<td>Emsk ist zusätzliches Schlüsselmaterial, das von der EAP-Methode exportiert wird. Emsk ist mindestens 64 Oktette. Emsk wird für den EAP-Client und-Server freigegeben, aber nicht für den Authentifikator oder einen anderen Drittanbieter. Derzeit ist emsk für die zukünftige Verwendung reserviert. Weitere Informationen finden Sie unter " [Extensible Authentication Protocol EAP"-Methoden Anforderungen für drahtlose LANs](https://go.microsoft.com/fwlink/p/?linkid=84064).<br/></td>
</tr>
<tr class="odd">
<td>Wann verwendet oder generiert eine Methode ein Attribut?</td>
<td>Wenn eine EAP-Methode Attribute oder emsk generiert, werden vom Supplicant Attribute verwendet. In der Regel sind Attribute, die von Supplicants genutzt werden, Schlüssel. Die verbrauchten Attribute sind " <strong>eateterid</strong>", " <strong>eatserverid</strong>", " <strong>eatmethodid</strong>", " <strong>eatemsk</strong>" und " <strong>eatkredentialschge</strong>". Weitere Informationen finden Sie unter [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type). Mit einer EAP-Methode können zusätzliche anwendungsspezifische emsk-Materialien exportiert werden, z.b.:
<ul>
<li>Sitzungs-ID</li>
<li>[Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Welche Attribute verbrauchen [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) ?</td>
<td>Der Native Wireless [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Supplicant verwendet die folgenden EAPHost-Authentifizierungs Attribute:
<ul>
<li>Kenn Wort Benachrichtigung ändern</li>
<li>Sende-/empfangsschlüssel für Microsoft Point-to-Point-Verschlüsselung (MPPE). VendorID/vendortype = 331/16 und 311/1</li>
</ul>
Bei MPPE-Schlüsseln handelt es sich um Schlüssel, die am Ende der erfolgreichen Authentifizierung von Peer und Authenticator generiert werden. Diese Schlüssel werden von [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) und dem Netzwerk Zugriffs Server (Network Access Server, NAS) zum Verschlüsseln und Entschlüsseln von gesendeten und empfangenen Paketen verwendet.<br/></td>
</tr>
<tr class="odd">
<td>Was ist der Zweck des EAP_PEER_FLAG_GUEST_ACCESS-Flags in EAPHost?</td>
<td>Wenn dieses Flag in [<strong>eaphostpeerbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) festgelegt ist, interpretiert EAPHost dies als Anforderung für die Gast Autorisierung und gibt eine <strong>null</strong> -Identitäts Antwort zurück, die dann an den Supplicant weitergeleitet und an den EAP-Server zurückgegeben wird.</td>
</tr>
<tr class="even">
<td>Wie fordert das Supplicant eine Computer Authentifizierung an?</td>
<td>Die Computer Authentifizierung wird angefordert, indem das Flag [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) festgelegt wird.</td>
</tr>
<tr class="odd">
<td>Wie fordert die Supplicant die Benutzerauthentifizierung an?</td>
<td>Die Benutzerauthentifizierung wird angefordert, indem das Flag [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) nicht festgelegt wird.</td>
</tr>
<tr class="even">
<td>Wann verwende ich [<strong>eaphostpeerfreerrormemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) anstelle der [<strong>eaphostfreeaperror</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror)-Funktion?</td>
<td>Die [<strong>eaphostpeer Memory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory)-Funktion wird nur für die Freigabe von [<strong>EAP_ERROR</strong>] (/Windows/Desktop/API/eaptypes/NS-eaptypes-eap_error)-Strukturen verwendet, die von EAPHost-Konfigurations-APIs zurückgegeben werden. EAPHost-Konfigurations-APIs sind in eaphostpeer. h definiert. Im Gegensatz dazu wird die [<strong>eaphostpeerfreeaperror</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror)-Funktion zum Freigeben von <strong>EAP_ERROR</strong> Strukturen verwendet, die von EAPHost-Lauf Zeit-APIs zurückgegeben werden. EAPHost-Lauf Zeit-APIs werden in eappapis. h definiert. Verwenden Sie niemals die Laufzeitversion der API mit der Konfigurations Version der APIs. Dies kann zu unerwarteten Ergebnissen führen.<br/></td>
</tr>
<tr class="odd">
<td>Ich habe meine Benutzeroberfläche in demselben Thread implementiert, den ich zum Verarbeiten einer EAP-Authentifizierungs Sitzung auf dem Supplicant verwende. Nachdem ich eine interaktive Benutzeroberfläche zum Abrufen von Anmelde Informationen oder anderen Benutzereingabe Daten ausgelöst habe, schlägt der nächste von EAPHost zu einer EAP-Peer Methode angegebene Vorgang mit <strong>ERROR_OBJECT_DISCONNECTED</strong>fehl. Warum ist das passiert, und wie kann ich es beheben?</td>
<td>Obwohl es sich bei den Client seitigen EAPHost-APIs um APIs im c-Stil handelt, handelt es sich bei diesen C-APIs lediglich um Wrapper entsprechender com-APIs. Die C-Stil-APIs werden in einer Multithread-COM-Umgebung ausgeführt. Der UI-Code wird in der Regel im Apartment Thread Modell ausgeführt. Da die beiden Thread Modelle miteinander in Konflikt stehen, führen Sie den UI-Code nicht im gleichen Thread aus, der EAP-Authentifizierungen verarbeitet.</td>
</tr>
<tr class="even">
<td>Warum nimmt die [<strong>eaphosteterbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession)-API einen [<em>notificationhandler</em>] (/Previous-Versions/Windows/Desktop/API)-Rückruf Funktionszeiger als Parameter an?</td>
<td>[<em>Notificationhandler</em>] (/Previous-Versions/Windows/Desktop/API) ist der Mechanismus, mit dem ein Supplicant benachrichtigt wird, dass er sich erneut authentifizieren muss. Es gibt verschiedene Szenarien, in denen der Supplicant zur erneuten Authentifizierung erforderlich ist, einschließlich der Authentifizierung mit dem [Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP).</td>
</tr>
<tr class="odd">
<td>Was ist der Zweck des Parameters " <em>pconnectionid</em> " in der API [<strong>eaphosteterbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession)?</td>
<td><em>pconnectionid</em> ist ein Zeiger auf einen Supplicant definierten GUID-Wert, der verwendet wird, um eine Netzwerkverbindung zu identifizieren, die zu dem Supplicant gehört. Wenn die Rückruffunktion [<em>notificationhandler</em>] (/Previous-Versions/Windows/Desktop/API) aufgerufen wird, wird diese GUID übergeben, um die Netzwerkverbindung zu identifizieren, die vom Supplicant für Authentifizierungsanforderungen verwendet wird.</td>
</tr>
<tr class="even">
<td>Gewusst wie wissen, ob es eine Änderung des Quarantäne Zustands gibt?</td>
<td>Der Benutzer erhält nur dann eine visuelle Benachrichtigung über eine Änderung des Quarantäne Zustands, wenn im System mindestens eine Schnittstelle für den Netzwerk Zugriffsschutz (Network Access Protection, QEC) registriert ist. Wenn dies der Fall ist, wird der Benutzer bei einer erneuten Authentifizierung über ein Popup Fenster über eine Quarantäne Zustandsänderung benachrichtigt.</td>
</tr>
<tr class="odd">
<td>Gewusst wie wissen, ob im System eine NAP-QEC-registrierte Schnittstelle vorhanden ist?</td>
<td>Öffnen Sie ein Fenster mit erhöhten Rechten, und führen Sie den folgenden Netsh-Befehl aus: &quot; netsh NAP Client Show State &quot; . Weitere Informationen finden Sie unter [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Welche Verbindungs-ID sollte der QEC bei der erneuten Authentifizierung verwenden, wenn sich der Supplicant erneut authentifiziert?</td>
<td>Der QEC muss dieselbe Verbindungs-ID verwenden, die für die vorherige Sitzung verwendet wurde.</td>
</tr>
<tr class="odd">
<td>Es ist nur eine EAPHost-Supplicant-Methode zum Anzeigen von Dialogfeldern für die Benutzeroberfläche (UI) verfügbar, EAP-Methoden weisen jedoch verschiedene Typen von UI-spezifischen aufrufen auf. Welche Methode sollte der Supplicant aufrufen, wenn er den Aktions Code " <strong>eaphosteterresponseinvokeui</strong> " erhält, der anzeigt, dass der Supplicant ein UI-Dialogfeld anzeigen muss?</td>
<td>Für den Benutzer ist keine Aktion erforderlich, da EAPHost weiß, welche Methoden Funktion aufgerufen werden soll. Wenn beispielsweise der Aktions Code <strong>eaphosteterresponseinvokeui</strong> zurückgegeben wird, ruft die Supplicant diese drei Funktionen in der folgenden Reihenfolge auf: [<strong>eaphostpeer ergetuicontext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeergetuicontext), [<strong>eaphostpeer erinvokeinteractiveui</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) und [<strong>eaphostetersetuicontext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeersetuicontext)</td>
</tr>
<tr class="even">
<td>Worin besteht der Unterschied zwischen einem Anmelde Informations-BLOB und einem konfigurationsblob?</td>
<td>Das BLOB für die Anmelde Informationen enthält nur Benutzerdaten, z. b. Benutzername, Kennwort und PIN. Das konfigurationsblob enthält die Einstellungen, die das Verhalten der-Methode steuern.</td>
</tr>
<tr class="odd">
<td>Kann ich die Ablauf Verfolgung auf der EAPHost-Clientseite aktivieren?</td>
<td>Ja. Weitere Informationen finden Sie unter [aktivieren](enabling-tracing.md)der Ablauf Verfolgung.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Supplicant-API-Referenz](eap-host-supplicant-api-reference.md)
</dt> <dt>

[Allgemeine FAQs zu EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[FAQ zu EAPHost-Methoden](eap-method-frequently-asked-questions.md)
</dt> <dt>

[EAPHost-Entwicklungs FAQs](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

