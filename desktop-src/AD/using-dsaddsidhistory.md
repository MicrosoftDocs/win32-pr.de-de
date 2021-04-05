---
title: Verwenden von dsaddsidhistory
description: In diesem Thema wird beschrieben, wie Sie die dsaddsidhistory-Funktion verwenden.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Verwenden von dsaddsidhistory Active Directory
- Active Directory Active Directory mithilfe von dsaddsidhistory
- Dsaddsidhistory Active Directory mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d45792dbd8c7a2bfa2dd047111a3ed165a2011e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707511"
---
# <a name="using-dsaddsidhistory"></a>Verwenden von dsaddsidhistory

Die [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) -Funktion Ruft die primäre Konto Sicherheits-ID (SID) eines Sicherheits Prinzipals aus einer Domäne (der Quell Domäne) ab und fügt Sie dem **SIDHistory** -Attribut eines Sicherheits Prinzipals in einer anderen (Ziel-) Domäne in einer anderen Gesamtstruktur hinzu. Wenn sich die Quell Domäne im einheitlichen Modus von Windows 2000 befindet, ruft diese Funktion auch die **SIDHistory** -Werte des Quell Prinzipals ab und fügt Sie dem **SIDHistory** des Ziel Prinzipals hinzu.

Das Hinzufügen von SIDs zum **SIDHistory** eines Sicherheits Prinzipals ist ein Sicherheits abhängiger Vorgang, der dem Ziel Prinzipal Zugriff auf alle Ressourcen gewährt, auf die der Quell Prinzipal Zugriff hat, vorausgesetzt, dass Vertrauens Stellungen von anwendbaren Ressourcen Domänen zur Zieldomäne vorhanden sind.

In einer Windows 2000-Domäne im einheitlichen Modus erstellt eine Benutzeranmeldung ein Zugriffs Token, das die primäre Konto-SID und die Gruppen-SIDs des Benutzers sowie den Benutzer **SIDHistory** und den **SIDHistory** der Gruppen enthält, in denen der Benutzer Mitglied ist. Wenn diese früheren SIDs (**SIDHistory** -Werte) im Token des Benutzers vorhanden sind, erhält der Benutzer Zugriff auf Ressourcen, die durch Zugriffs Steuerungs Listen (ACLs) geschützt sind, die die früheren SIDs enthalten.

Mit diesem Vorgang werden bestimmte Windows 2000-Bereitstellungs Szenarien vereinfacht. Insbesondere wird ein Szenario unterstützt, in dem Konten in einer neuen Windows 2000-Gesamtstruktur für Benutzer und Gruppen erstellt werden, die bereits in einer Windows NT 4,0-Produktionsumgebung vorhanden sind. Wenn Sie die Windows NT 4,0-Konto-SID im Windows 2000-Konto **SIDHistory** platzieren, wird der Zugriff auf Netzwerkressourcen beibehalten, damit sich der Benutzer bei seinem neuen Windows 2000-Konto anmeldet.

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) unterstützt auch die Migration von BDCs-Ressourcen Servern (Windows NT 4,0 Backup Domain Controllers) (oder DCS und Mitglieds Server in einer Windows 2000-Domäne im einheitlichen Modus) zu einer Windows 2000-Domäne als Mitglieds Server. Diese Migration erfordert die Erstellung in der Windows 2000-Zieldomäne von lokalen Domänen Gruppen, die in Ihrem **SIDHistory**-Element die primären SIDs der lokalen Gruppen, die auf dem BDC definiert sind (oder lokale Domänen Gruppen, auf die in ACLs auf den Windows 2000-Servern verwiesen wird) in der Quell Domäne. Durch Erstellen einer lokalen Zielgruppe, die den **SIDHistory** und alle Mitglieder der lokalen Quell Gruppe enthält, wird der Zugriff auf die migrierten Server Ressourcen, die durch ACLs geschützt sind, die auf die lokale Quell Gruppe verweisen, für alle Mitglieder beibehalten.

> [!Note]  
> Die Verwendung von [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert ein Verständnis der umfassenderen administrativen und Sicherheits Implikationen in diesen und anderen Szenarien. Weitere Informationen finden Sie im Whitepaper "Planen der Migration von Windows NT zu Microsoft Windows 2000", das als Dommig.doc in den Windows 2000-Support Tools bereitgestellt wird. Diese Dokumentation finden Sie auch auf der Produkt-CD unter \\ Support \\ Tools.

 

## <a name="authorization-requirements"></a>Autorisierungs Anforderungen

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert Administratorrechte in den Quell-und Zieldomänen. Insbesondere muss der Aufrufer dieser API Mitglied der Gruppe "Domänen Administratoren" in der Zieldomäne sein. Für diese Mitgliedschaft wird eine hart codierte Überprüfung durchgeführt. Außerdem muss der Aufrufer oder das im *srcdomaincreds* -Parameter bereitgestellte Konto, wenn er nicht **null** ist, Mitglied der Gruppe "Administratoren" oder "Domänen Administratoren" in der Quell Domäne sein.

## <a name="domain-and-trust-requirements"></a>Domänen-und Vertrauens Anforderungen

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert, dass die Zieldomäne im einheitlichen Modus von Windows 2000 oder höher ist, da nur dieser Domänentyp das **SIDHistory** -Attribut unterstützt. Die Quell Domäne kann entweder Windows NT 4,0 oder Windows 2000, gemischter oder einheitlicher Modus sein. Die Quell-und Zieldomänen dürfen sich nicht in derselben Gesamtstruktur befinden. Windows NT 4,0-Domänen sind definitionsgemäß nicht in einer Gesamtstruktur vorhanden. Diese Gesamtstruktur übergreifende Einschränkung stellt sicher, dass doppelte SIDs, unabhängig davon, ob Sie als primäre SIDs-oder **SIDHistory** -Werte angezeigt werden, nicht in derselben Gesamtstruktur erstellt werden.

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert in den in der folgenden Tabelle aufgeführten Fällen eine externe Vertrauensstellung von der Quell Domäne zur Zieldomäne.



| Fall                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Quell Domäne ist Windows 2000.<br/>                                    | Das Quell- **SIDHistory** -Attribut, das nur in Windows 2000-Quell Domänen verfügbar ist, ist möglicherweise nur mit LDAP lesbar, das diese Vertrauensstellung für den Integritätsschutz erfordert.<br/>                                                                                             |
| Die Quell Domäne ist Windows NT 4,0, und *srcdomaincreds* ist **null**.<br/> | Der Identitätswechsel, der zur Unterstützung der Quell Domänen Vorgänge mithilfe der Anmelde Informationen des Aufrufers erforderlich ist, hängt von dieser Vertrauensstellung Der Identitätswechsel erfordert auch, dass der Zieldomänen Controller auf Domänen Controllern standardmäßig "vertrauenswürdig für Delegierung" aktiviert ist.<br/> |



 

Es ist jedoch keine Vertrauensstellung zwischen den Quell-und Zieldomänen erforderlich, wenn es sich bei der Quell Domäne um Windows NT 4,0 und *srcdomaincreds* nicht um **null** handelt.

## <a name="source-domain-controller-requirements"></a>Anforderungen an den Quell Domänen Controller

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert, dass der Domänen Controller, der als Ziel für Vorgänge in der Quell Domäne ausgewählt ist, der PDC in Windows NT 4,0-Domänen oder der PDC-Emulator in Windows 2000-Domänen ist. Die Überwachung der Quell Domäne wird mithilfe von Schreibvorgängen generiert. der PDC ist daher in Windows NT 4,0-Quell Domänen erforderlich, und die Einschränkung "PDC-only" stellt sicher, dass **dsaddsidhistory** -Überwachungen auf einem einzelnen Computer generiert werden. Dies verringert die Notwendigkeit, die Überwachungs Protokolle aller DCS zu überprüfen, um die Verwendung dieses Vorgangs zu überwachen.

> [!Note]  
> In Windows NT 4,0-Quell Domänen muss auf dem PDC (Ziel der Vorgänge in der Quell Domäne) Service Pack 4 (SP4) und höher ausgeführt werden, um eine ordnungsgemäße Unterstützung der Überwachung sicherzustellen.

 

Der folgende Registrierungs Wert muss als reg \_ DWORD-Wert erstellt und auf dem Quell Domänen Controller für Windows NT 4,0-und Windows 2000-Quell Domänen Controller auf 1 festgelegt werden.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

Durch Festlegen dieses Werts werden RPC-Aufrufe über den TCP-Transport ermöglicht. Dies ist erforderlich, da samrpc-Schnittstellen standardmäßig nur auf Named Pipes Remote fähig sind. Die Verwendung von Named Pipes führt zu einem System für die Verwaltung von Anmelde Informationen, das sich für interaktiv angemeldete Benutzer eignet, die vernetzte Aufrufe durchführen, aber für einen System Prozess, der Netzwerk Aufrufe durch benutzerdefinierte Anmelde Informationen ausführt, nicht flexibel ist. RPC über TCP ist für diesen Zweck besser geeignet. Wenn dieser Wert festgelegt wird, wird die Systemsicherheit nicht verringert. Wenn dieser Wert erstellt oder geändert wird, muss der Quell Domänen Controller neu gestartet werden, damit diese Einstellung wirksam wird.

Die neue lokale Gruppe " <SrcDomainName> $ $ $" muss zu Überprüfungszwecken in der Quell Domäne erstellt werden.

## <a name="auditing"></a>Überwachung

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) -Vorgänge werden überwacht, um sicherzustellen, dass sowohl Quell-als auch Zieldomänen Administratoren erkennen können, wann diese Funktion ausgeführt wurde. Die Überwachung ist sowohl in der Quell-als auch in der Zieldomäne obligatorisch. **Dsaddsidhistory** überprüft, ob der Überwachungsmodus in jeder Domäne on ist, und dass die Konto Verwaltungs Überwachung für Erfolgs-/Fehlerereignisse ausgeführt wird. In der Zieldomäne wird für jeden erfolgreichen oder fehlgeschlagenen **dsaddsidhistory** -Vorgang ein eindeutiges Überwachungs Ereignis vom Typ "SID-Verlauf hinzufügen" generiert.

Eindeutige Überwachungs Ereignisse für "SID-Verlauf hinzufügen" sind auf Windows NT 4,0-Systemen nicht verfügbar. Um Überwachungs Ereignisse zu generieren, die die Verwendung von [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) für die Quell Domäne eindeutig widerspiegeln, werden Vorgänge für eine spezielle Gruppe durchführt, deren Name der eindeutige Bezeichner im Überwachungs Protokoll ist. Die lokale Gruppe " <SrcDomainName> $ $ $", deren Name aus dem NetBIOS-Namen der Quell Domäne besteht, der mit drei Dollarzeichen ($) (ASCII-Code = 0x24 und Unicode = U + 0024) angehängt ist, muss vor dem Aufrufen von **dsaddsidhistory** auf dem Quell Domänen Controller erstellt werden. Jeder Quell Benutzer und jede globale Gruppe, die Ziel dieses Vorgangs ist, wird der Mitgliedschaft in dieser Gruppe hinzugefügt und daraus entfernt. Dadurch werden die Überwachungs Ereignisse Add Member und DELETE Member in der Quell Domäne generiert, die Durchsuchen nach Ereignissen überwacht werden können, die auf den Gruppennamen verweisen.

> [!Note]  
> [**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) -Vorgänge in lokalen Gruppen in einer Windows NT 4,0-oder Windows 2000-Quell Domäne im gemischten Modus können nicht überwacht werden, da lokale Gruppen nicht zu Mitgliedern einer anderen lokalen Gruppe gemacht werden können und daher nicht zur speziellen <SrcDomainName> lokalen Gruppe "$ $ $" hinzugefügt werden können. Diese fehlende Überwachung stellt kein Sicherheitsproblem für die Quell Domäne dar, da der Zugriff auf die Quell Domänen Ressource von diesem Vorgang nicht beeinträchtigt wird. Das Hinzufügen der SID einer lokalen Quell Gruppe zu einer lokalen Zielgruppe gewährt keinen Zugriff auf die Quell Ressourcen, die von dieser lokalen Gruppe geschützt werden, auf zusätzliche Benutzer. Durch das Hinzufügen von Mitgliedern zur lokalen Zielgruppe erhalten Sie keinen Zugriff auf Quell Ressourcen. Hinzugefügten Mitgliedern wird nur der Zugriff auf Server in der Zieldomäne gewährt, die aus der Quell Domäne migriert wurden, die möglicherweise von der lokalen SID der Quell Gruppe geschützte Ressourcen besitzt.

 

## <a name="data-transmission-security"></a>Daten Übertragungssicherheit

[**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erzwingt die folgenden Sicherheitsmaßnahmen:

-   Wird von einer Windows 2000-Arbeitsstation aufgerufen, werden die Anmelde Informationen des Aufrufers verwendet, um den RPC-Aufruf an den Zieldomänen Controller zu authentifizieren und zu schützen. Wenn *srcdomaincreds* nicht **null** ist, müssen sowohl die Arbeitsstation als auch der Ziel-DC die 128-Bit-Verschlüsselung unterstützen, um die Anmelde Informationen zu schützen. Wenn die 128-Bit-Verschlüsselung nicht verfügbar ist und *srcdomaincreds* bereitgestellt werden, muss der-Befehl auf dem Ziel-DC erfolgen.
-   Der Zieldomänen Controller kommuniziert mit dem Quell Domänen Controller entweder mithilfe von *srcdomaincreds* oder mithilfe der Anmelde Informationen des Aufrufers, um sich gegenseitig zu authentifizieren und den Integritätsschutz für den Lesevorgang der SID des Quell Kontos (mit einem Sam-Lookup) und **SIDHistory** (mit einem LDAP-Lesevorgang

## <a name="threat-models"></a>Bedrohungs Modelle

In der folgenden Tabelle sind die potenziellen Bedrohungen im Zusammenhang mit dem [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) -Befehl aufgelistet, und es werden die Sicherheitsmaßnahmen für die jeweilige Bedrohung behandelt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Potenzielle Bedrohung</th>
<th>Sicherheitsmeasure</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Man im mittleren Angriff<br/> Ein nicht autorisierter Benutzer fängt die Such-SID des Rückgabe Aufrufens <em>des Quell Objekts</em> ab und ersetzt dabei die Quell Objekt-SID durch eine beliebige sid für das Einfügen in ein SIDHistory-Zielobjekt.<br/></td>
<td>Die <em>Such-SID des Quell Objekts</em> ist eine authentifizierte RPC-Nachricht, die die Administrator Anmelde Informationen des Aufrufers mit dem paketintegritäts-Nachrichten Schutz verwendet. Dadurch wird sichergestellt, dass der Rückgabe Befehl ohne Erkennung nicht geändert werden kann. Vom Zieldomänen Controller wird ein eindeutiges Ereignis zum Hinzufügen einer SID-Verlaufs Überwachung erstellt &quot; &quot; , das die dem Ziel Konto- <strong>SIDHistory</strong>hinzugefügte sid<br/></td>
</tr>
<tr class="even">
<td>Trojaner-Quell Domäne<br/> Ein nicht autorisierter Benutzer erstellt eine &quot; Trojaner &quot; -Quell Domäne in einem privaten Netzwerk mit derselben Domänen-SID und einigen der gleichen Konto-SIDs wie die berechtigte Quell Domäne. Der nicht autorisierte Benutzer versucht dann, <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>dsaddsidhistory</strong></a> in einer Zieldomäne auszuführen, um die SID eines Quell Kontos zu erhalten. Dies geschieht, ohne dass die echten Quell Domänen Administrator-Anmelde Informationen erforderlich sind und keine Überwachungs Pfade in der realen Quell Domäne belassen werden. Die Methode des nicht autorisierten Benutzers zum Erstellen der Trojaner-Quell Domäne kann eines der folgenden sein:
<ul>
<li>Erwerben Sie eine Kopie (BDC-Sicherung) der Quell Domäne Sam.</li>
<li>Erstellen Sie eine neue Domäne, ändern Sie die Domänen-SID auf dem Datenträger entsprechend der berechtigten SID der Quell Domäne, und erstellen Sie dann ausreichend Benutzer, um ein Konto mit der gewünschten sid zu instanziieren.</li>
<li>Erstellen Sie ein BDC-Replikat. Hierfür sind Anmelde Informationen des Quell Domänen Administrators erforderlich. Dann nimmt der nicht autorisierte Benutzer das Replikat in ein privates Netzwerk, um den Angriff zu implementieren.</li>
</ul>
<br/></td>
<td>Es gibt zwar viele Möglichkeiten, wie ein nicht autorisierter Benutzer eine gewünschte Quell Objekt-SID abrufen oder erstellen kann, aber der nicht autorisierte Benutzer kann ihn nicht zum Aktualisieren des <strong>SIDHistory</strong> eines Kontos verwenden, ohne Mitglied der Gruppe der Zieldomänen Administratoren zu sein. Da die Überprüfung auf dem Zieldomänen Controller für die Mitgliedschaft von Domänen Administratoren hart codiert ist, gibt es auf dem Ziel-DC keine Methode zum Ändern der Zugriffs Steuerungsdaten, die diese Funktion schützen. Der Versuch, ein Trojaner-Quell Konto zu klonen, wird in der Zieldomäne überwacht. Dieser Angriff wird durch das Reservieren der Mitgliedschaft in der Gruppe der Domänen Administratoren für nur sehr vertrauenswürdige Personen verhindert.<br/></td>
</tr>
<tr class="odd">
<td>Änderung des SID-Verlaufs auf dem Datenträger<br/> Ein hoch entwickelter nicht autorisierter Benutzer mit Anmelde Informationen des Domänen Administrators und mit physischem Zugriff auf einen Domänen Controller in der Zieldomäne könnte einen Konto- <strong>SIDHistory</strong> -Wert auf dem Datenträger ändern<br/></td>
<td>Dieser Versuch wird nicht durch die Verwendung von <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>dsaddsidhistory</strong></a>aktiviert. Dieser Angriff wird verringert, indem der physische Zugriff auf Domänen Controller mit Ausnahme von sehr vertrauenswürdigen Administratoren verhindert wird.<br/></td>
</tr>
<tr class="even">
<td>Nicht autorisierter Code zum Entfernen von Schutzmaßnahmen<br/> Ein nicht autorisierter Benutzer oder nicht autorisierter Administrator mit physischem Zugriff auf den Verzeichnisdienst Code könnte nicht autorisierten Code erstellen, der Folgendes:
<ol>
<li>Entfernt die Überprüfung der Mitgliedschaft in der Gruppe "Domänen Administratoren" im Code.</li>
<li>Ändert die Aufrufe auf dem Quell Domänen Controller, der die SID auf einen nicht überwachten lookupsidfromname zeigt.</li>
<li>Entfernt Überwachungs Protokoll Aufrufe.</li>
</ol>
<br/></td>
<td>Ein Benutzer mit physischem Zugriff auf den DS-Code und ausreichend wissen, um nicht autorisierten Code zu erstellen, ist in der Lage, das <strong>SIDHistory</strong> -Attribut eines Kontos willkürlich zu ändern. Die <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>dsaddsidhistory</strong></a> -API erhöht dieses Sicherheitsrisiko nicht.<br/></td>
</tr>
<tr class="odd">
<td>Ressourcen anfällig für gestohlene SIDs<br/> Wenn ein nicht autorisierter Benutzer eine der hier beschriebenen Methoden zum Ändern eines Konto- <strong>SIDHistory</strong>verwendet hat und die Ressourcen Domänen von Interesse der nicht autorisierten Benutzerkonto Domäne vertrauen, kann der nicht autorisierte Benutzer nicht autorisierten Zugriff auf die Ressourcen der gestohlenen sid erhalten. Dies ist möglicherweise nicht möglich, ohne einen Überwachungs Pfad in der Konto Domäne zu verlassen, von der die SID gestohlen wurde.<br/></td>
<td>Ressourcen Domänen Administratoren schützen Ihre Ressourcen, indem Sie nur Vertrauens Stellungen einrichten, die aus Sicht der Sicherheit sinnvoll sind. Die Verwendung von <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>dsaddsidhistory</strong></a> ist in der vertrauenswürdigen Zieldomäne auf Mitglieder der Gruppe der Domänen Administratoren beschränkt, die bereits über umfassende Berechtigungen innerhalb des Umfangs ihrer Zuständigkeiten verfügen.<br/></td>
</tr>
<tr class="even">
<td>Nicht autorisierte Zieldomäne<br/> Ein nicht autorisierter Benutzer erstellt eine Windows 2000-Domäne mit einem Konto, dessen <strong>SIDHistory</strong> eine sid enthält, die aus einer Quell Domäne gestohlen wurde. Der nicht autorisierte Benutzer verwendet dieses Konto, um nicht autorisierten Zugriff auf Ressourcen zu erhalten.<br/></td>
<td>Der nicht autorisierte Benutzer benötigt Administrator Anmelde Informationen für die Quell Domäne, damit <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>dsaddsidhistory</strong></a>verwendet werden kann, und verlässt einen Überwachungs Pfad auf dem Quell Domänen Controller. Die nicht autorisierte Zieldomäne erhält nicht autorisierten Zugriff nur in anderen Domänen, die der nicht autorisierten Domäne vertrauen, die Administrator Rechte in diesen Ressourcen Domänen benötigt.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="operational-constraints"></a>Betriebliche Einschränkungen

In diesem Abschnitt werden die operativen Einschränkungen der Verwendung der [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) -Funktion beschrieben.

Die SID von *srcprincipal* darf nicht bereits in der Ziel Gesamtstruktur vorhanden sein, entweder als primäre Konto-SID oder als **SIDHistory** eines Kontos. Die Ausnahme besteht darin, dass [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) keinen Fehler generiert, wenn versucht wird, eine SID zu einem **SIDHistory** -Wert hinzuzufügen, der eine identische sid enthält. Durch dieses Verhalten kann **dsaddsidhistory** mehrmals mit identischer Eingabe ausgeführt werden, was Erfolg und einen konsistenten Endzustand für die Benutzerfreundlichkeit des Tool Entwicklers zur Folge hat.

> [!Note]  
> Die Replikations Latenz des globalen Katalogs kann ein Fenster bereitstellen, in dem doppelte SIDs erstellt werden können. Doppelte SIDs können jedoch problemlos von einem Administrator gelöscht werden.

 

*Srcprincipal* und *dstprincipal* müssen einen der folgenden Typen aufweisen:

-   Benutzer
-   Sicherheits aktivierte Gruppe, einschließlich:

    <dl> Lokale Gruppe  
    Globale Gruppe  
    Lokale Domänen Gruppe (nur Windows 2000 einheitlicher Modus)  
    Universelle Gruppe (nur Windows 2000 einheitlicher Modus)  
    </dl>

Die Objekttypen von *srcprincipal* und *dstprincipal* müssen mit identisch sein.

-   Wenn *srcprincipal* ein Benutzer ist, muss *dstprincipal* ein Benutzer sein.
-   Wenn *srcprincipal* eine lokale Gruppe oder eine lokale Gruppe der Domäne ist, muss *dstprincipal* eine lokale Gruppe der Domäne sein.
-   Wenn *srcprincipal* eine globale oder universelle Gruppe ist, muss *dstprincipal* eine globale oder universelle Gruppe sein.

*Srcprincipal* und *dstprincipal* dürfen keinen der folgenden Typen aufweisen: ([**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) schlägt in diesen Fällen mit einem Fehler fehl)

-   Computer (Arbeitsstation oder Domänen Controller)
-   Vertrauensstellung zwischen Domänen
-   Temporäres doppeltes Konto (praktisch nicht verwendetes Feature, Legacy von LanMan)
-   Konten mit bekannten SIDs. Bekannte SIDs sind in jeder Domäne identisch. das Hinzufügen zu einem **SIDHistory** würde also die SID-Eindeutigkeits Anforderung einer Windows 2000-Gesamtstruktur verletzen. Konten mit bekannten SIDs enthalten die folgenden lokalen Gruppen:

    <dl> Konto-Operatoren  
    Administratoren  
    Sicherungs Operatoren  
    Gäste  
    Druck Operatoren  
    Replicator  
    Server-Operatoren  
    Benutzer  
    </dl>

Wenn *srcprincipal* über eine bekannte relative Kennung (RID) und ein Domänen spezifisches Präfix verfügt, d. h. Domänen Administratoren, Domänen Benutzer und Domänen Computer, muss *dstprincipal* dieselbe bekannte Rid aufweisen, damit [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfolgreich ausgeführt werden kann. Konten mit bekannten RIDs enthalten folgende Benutzer und globale Gruppen:

-   Administrator
-   Gast
-   Domänen Administratoren
-   Domänen Gäste
-   Domänenbenutzer

## <a name="setting-the-registry-value"></a>Festlegen des Registrierungs Werts

Im folgenden Verfahren wird gezeigt, wie der Registrierungs Wert TcpipClientSupport festgelegt wird.

**So legen Sie den Registrierungs Wert "TcpipClientSupport" fest**

1.  Erstellen Sie den folgenden Registrierungs Wert als reg \_ DWORD-Wert auf dem Quell Domänen Controller, und legen Sie seinen Wert auf 1 fest.

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ LSA \\ TcpipClientSupport**

2.  Starten Sie dann den Quell Domänen Controller neu. Dieser Registrierungs Wert bewirkt, dass Sam an TCP/IP lauscht. [**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) schlägt fehl, wenn dieser Wert nicht auf dem Quell Domänen Controller festgelegt ist.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Aktivieren der Überwachung von Ereignissen zur Benutzer-/Gruppenverwaltung

Das folgende Verfahren zeigt, wie Sie die Überwachung von Ereignissen für die Benutzer-/Gruppenverwaltung in einer Windows 2000-oder Windows Server 2003-Quell-oder-Zieldomäne aktivieren.

**So aktivieren Sie die Überwachung von Benutzer-/gruppenverwaltungsereignissen in einer Windows 2000-oder Windows Server 2003-Quell-oder-Zieldomäne**

1.  Wählen Sie im MMC-Snap-in Active Directory-Benutzer und-Computer den Container Domänen Controller der Zieldomäne aus.
2.  Klicken **Sie mit** der rechten Maustaste auf **Domänen Controller** .
3.  Klicken Sie auf die Registerkarte **Gruppenrichtlinie** .
4.  Wählen Sie die **Standard Domänen Controller Richtlinie** aus, und klicken Sie auf **Bearbeiten**
5.  Doppelklicken Sie unter **Computer Konfiguration \\ Windows-Einstellungen \\ Sicherheitseinstellungen \\ lokale Richtlinien Überwachungs \\ Richtlinie** auf **Kontoverwaltung** überwachen.
6.  Wählen Sie im Fenster Überwachungs **Kontoverwaltung** sowohl **erfolgreiche** als auch **Fehler** hafte Überwachung aus. Richtlinien Updates werden nach einem Neustart oder nach einer Aktualisierung wirksam.
7.  Überprüfen Sie, ob die Überwachung aktiviert ist, indem Sie die effektive Überwachungsrichtlinie im Gruppenrichtlinie MMC-Snap-in anzeigen.

Das folgende Verfahren zeigt, wie Sie die Überwachung von Ereignissen für die Benutzer-/Gruppenverwaltung in einer Windows NT 4,0-Domäne aktivieren.

**So aktivieren Sie die Überwachung von Benutzer-/gruppenverwaltungsereignissen in einer Windows NT 4,0-Domäne**

1.  Klicken Sie im **Benutzer-Manager für Domänen** auf das Menü **Richtlinien** , **und wählen Sie** überwachen
2.  Wählen Sie **diese Ereignisse** überwachen aus.
3.  Überprüfen Sie für die **Benutzer-und Gruppenverwaltung** den **Erfolg und den Fehler**.

Das folgende Verfahren zeigt, wie Sie die Überwachung von Benutzer-/gruppenverwaltungsereignissen in einer Windows NT 4,0-, Windows 2000-oder Windows Server 2003-Quell Domäne aktivieren.

**So aktivieren Sie die Überwachung von Benutzer-/gruppenverwaltungsereignissen in einer Windows NT 4,0-, Windows 2000-oder Windows Server 2003-Quell Domäne**

1.  Klicken Sie im **Benutzer-Manager für Domänen** auf das **Benutzer** Menü, und wählen Sie **neue lokale Gruppe** aus.
2.  Geben Sie einen Gruppennamen ein, der aus dem NetBIOS-Namen der Quell Domäne besteht, der mit drei Dollarzeichen ($) angehängt wird, z. b. fabrikam $ $ $. Das Beschreibungsfeld sollte angeben, dass diese Gruppe verwendet wird, um die Verwendung von [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) oder Klon Vorgängen zu überwachen. Stellen Sie sicher, dass in der Gruppe keine Mitglieder vorhanden sind. Klicken Sie auf **OK**.

Der [**dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) -Vorgang schlägt fehl, wenn die Quell-und Ziel Überwachung nicht aktiviert ist, wie hier beschrieben.

## <a name="set-up-trust-if-required"></a>Einrichten von Vertrauens Stellungen bei Bedarf

Wenn einer der folgenden Punkte zutrifft, muss eine Vertrauensstellung von der Quell Domäne zur Zieldomäne eingerichtet werden (Dies muss in einer anderen Gesamtstruktur Vorkommen):

-   Die Quell Domäne ist Windows Server 2003.
-   Die Quell Domäne ist Windows NT 4,0, und *srcdomaincreds* ist **null**.

 

 





