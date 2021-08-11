---
title: Verwenden von DsAddSidHistory
description: In diesem Thema wird die Verwendung der DsAddSidHistory-Funktion beschrieben.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Verwenden von DsAddSidHistory Active Directory
- Active Directory Active Directory , using, Using DsAddSidHistory
- DsAddSidHistory Active Directory mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb37e09d5c7b337717f27b0e68ad17331ee27270da9e7b79a0d6bba791d2e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182524"
---
# <a name="using-dsaddsidhistory"></a>Verwenden von DsAddSidHistory

Die [**DsAddSidHistory-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ruft die primäre Kontosicherheits-ID (SID) eines Sicherheitsprinzipals aus einer Domäne (der Quelldomäne) ab und fügt sie dem **sIDHistory-Attribut** eines Sicherheitsprinzipals in einer anderen (Ziel-)Domäne in einer anderen Gesamtstruktur hinzu. Wenn sich die Quelldomäne im einheitlichen Modus Windows 2000 befindet, ruft diese Funktion auch die **sIDHistory-Werte** des Quellprinzipals ab und fügt sie der **sIDHistory** des Zielprinzipals hinzu.

Das Hinzufügen von SIDs zur **sIDHistory** eines Sicherheitsprinzipals ist ein sicherheitsrelevanter Vorgang, der dem Zielprinzipal effektiv Zugriff auf alle Ressourcen gewährt, auf die der Quellprinzipal zugreifen kann, vorausgesetzt, dass Vertrauensstellungen von den entsprechenden Ressourcendomänen zur Zieldomäne vorhanden sind.

In einem einheitlichen Modus Windows 2000-Domäne erstellt ein Benutzeranmeldung ein Zugriffstoken, das die SID des primären Benutzerkontos und die Gruppen-SIDs sowie den Benutzer **sIDHistory** und **die sIDHistory** der Gruppen enthält, denen der Benutzer angehört. Wenn diese früheren SIDs (**sIDHistory-Werte)** im Token des Benutzers enthalten sind, erhält der Benutzer Zugriff auf Ressourcen, die durch Zugriffssteuerungslisten (Access Control Lists, ACLs) geschützt sind, die die früheren SIDs enthalten.

Dieser Vorgang erleichtert bestimmte Windows 2000-Bereitstellungsszenarien. Insbesondere wird ein Szenario unterstützt, in dem Konten in einer neuen Windows 2000-Gesamtstruktur für Benutzer und Gruppen erstellt werden, die bereits in einer Windows NT 4.0-Produktionsumgebung vorhanden sind. Indem die WINDOWS NT 4.0-Konto-SID im Windows 2000-Konto **sIDHistory** platziert wird, bleibt der Zugriff auf Netzwerkressourcen für den Benutzer erhalten, der sich bei seinem neuen Windows 2000-Konto anmeldet.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) unterstützt auch die Migration von Windows NT 4.0-Sicherungsdomänencontrollern (BDCs) (oder DCs und Mitgliedsservern in einem einheitlichen Modus Windows 2000-Domäne) zu einer Windows 2000-Domäne als Mitgliedsserver. Diese Migration erfordert die Erstellung von lokalen Domänengruppen in der Zieldomäne Windows 2000, die in ihrer **sIDHistory** die primären SIDs der lokalen Gruppen enthalten, die auf dem BDC definiert sind (oder lokale Domänengruppen, auf die in ACLs auf den Windows 2000 Servern verwiesen wird) in der Quelldomäne. Durch das Erstellen einer lokalen Zielgruppe, die **sIDHistory** und alle Mitglieder der lokalen Quellgruppe enthält, wird der Zugriff auf die migrierten Serverressourcen, die durch ACLs geschützt werden, die auf die lokale Quellgruppe verweisen, für alle Mitglieder verwaltet.

> [!Note]  
> Die Verwendung von [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert ein Verständnis der umfassenderen Administrativen und Sicherheitsauswirkungen in diesen und anderen Szenarien. Weitere Informationen finden Sie im Whitepaper "Planning Migration from Windows NT to Microsoft Windows 2000" (Planen der Migration von Windows NT zu Microsoft Windows 2000), das als Dommig.doc in den Windows 2000-Supporttools bereitgestellt wird. Diese Dokumentation finden Sie auch auf der Produkt-CD unter \\ \\ Supporttools.

 

## <a name="authorization-requirements"></a>Autorisierungsanforderungen

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert Administratorrechte in der Quell- und Zieldomäne. Insbesondere muss der Aufrufer dieser API Mitglied der Gruppe Domänenadministratoren in der Zieldomäne sein. Eine hart codierte Überprüfung für diese Mitgliedschaft wird ausgeführt. Außerdem muss der Aufrufer oder das im *SrcDomainCreds-Parameter* bereitgestellte Konto, falls nicht **NULL,** Mitglied der Gruppe Administratoren oder Domänenadministratoren in der Quelldomäne sein.

## <a name="domain-and-trust-requirements"></a>Domänen- und Vertrauensstellungsanforderungen

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert, dass sich die Zieldomäne im einheitlichen Modus Windows 2000 oder höher befindet, da nur dieser Domänentyp das **Attribut sIDHistory** unterstützt. Die Quelldomäne kann entweder Windows NT 4.0 oder Windows 2000, gemischter oder systemeigener Modus sein. Die Quell- und Zieldomänen dürfen sich nicht in derselben Gesamtstruktur befinden. Windows NT 4.0-Domänen befinden sich definitionsgemäß nicht in einer Gesamtstruktur. Diese Gesamtstrukturübergreifende Einschränkung stellt sicher, dass doppelte SIDs, die als primäre SIDs oder **sIDHistory-Werte** angezeigt werden, nicht in derselben Gesamtstruktur erstellt werden.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert in den in der folgenden Tabelle aufgeführten Fällen eine externe Vertrauensstellung von der Quelldomäne zur Zieldomäne.



| Fall                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Quelldomäne ist Windows 2000.<br/>                                    | Das **sIDHistory-Quellattribut,** das nur in Windows 2000 Quelldomänen verfügbar ist, kann nur über LDAP gelesen werden, was diese Vertrauensstellung für den Integritätsschutz erfordert.<br/>                                                                                             |
| Die Quelldomäne ist Windows NT 4.0 und *SrcDomainCreds* **ist NULL.**<br/> | Der Identitätswechsel, der zur Unterstützung von Quelldomänenvorgängen mit den Anmeldeinformationen des Aufrufers erforderlich ist, hängt von dieser Vertrauensstellung ab. Der Identitätswechsel erfordert auch, dass auf dem Zieldomänencontroller "Vertrauenswürdig für delegierung" standardmäßig auf Domänencontrollern aktiviert ist.<br/> |



 

Es ist jedoch keine Vertrauensstellung zwischen der Quell- und der Zieldomäne erforderlich, wenn die Quelldomäne Windows NT 4.0 und *SrcDomainCreds* nicht **NULL** ist.

## <a name="source-domain-controller-requirements"></a>Anforderungen an den Quelldomänencontroller

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfordert, dass der Domänencontroller, der als Ziel für Vorgänge in der Quelldomäne ausgewählt wurde, der PDC in Windows NT 4.0-Domänen oder der PDC-Emulator in Windows 2000 Domänen ist. Die Überwachung von Quelldomänen wird über Schreibvorgänge generiert. Daher ist der PDC in Windows NT 4.0-Quelldomänen erforderlich, und die ausschließliche PDC-Einschränkung stellt sicher, dass **DsAddSidHistory-Überwachungen** auf einem einzelnen Computer generiert werden. Dies reduziert die Notwendigkeit, die Überwachungsprotokolle aller Dcs zu überprüfen, um die Verwendung dieses Vorgangs zu überwachen.

> [!Note]  
> In Windows NT 4.0-Quelldomänen muss auf dem PDC (Ziel von Vorgängen in der Quelldomäne) Service Pack 4 (SP4) und höher ausgeführt werden, um eine ordnungsgemäße Überwachungsunterstützung sicherzustellen.

 

Der folgende Registrierungswert muss als REG \_ DWORD-Wert erstellt und sowohl für Windows NT 4.0- als auch für Windows 2000-Quelldomänencontroller auf dem Quelldomänencontroller auf 1 festgelegt werden.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

Wenn Sie diesen Wert festlegen, werden RPC-Aufrufe über den TCP-Transport aktiviert. Dies ist erforderlich, da SAMRPC-Schnittstellen standardmäßig nur für Named Pipes remotable sind. Die Verwendung von Named Pipes führt zu einem Anmeldeinformationsverwaltungssystem, das für interaktiv angemeldete Benutzer geeignet ist, die Netzwerkaufrufe tätigen, ist aber nicht flexibel für einen Systemprozess, der Netzwerkaufrufe mit vom Benutzer bereitgestellten Anmeldeinformationen vornimmt. RPC über TCP ist für diesen Zweck besser geeignet. Wenn Sie diesen Wert festlegen, wird die Systemsicherheit nicht beeinträchtigt. Wenn dieser Wert erstellt oder geändert wird, muss der Quelldomänencontroller neu gestartet werden, damit diese Einstellung wirksam wird.

Die neue lokale Gruppe <SrcDomainName> "$$$" muss zu Überwachungszwecken in der Quelldomäne erstellt werden.

## <a name="auditing"></a>Überwachung

[**DsAddSidHistory-Vorgänge**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) werden überwacht, um sicherzustellen, dass sowohl Quell- als auch Zieldomänenadministratoren erkennen können, wann diese Funktion ausgeführt wurde. Die Überwachung ist sowohl in der Quell- als auch in der Zieldomäne obligatorisch. **DsAddSidHistory** überprüft, ob der Überwachungsmodus in jeder Domäne aktiviert ist und dass die Kontoverwaltungsüberwachung von Erfolgs-/Fehlerereignissen aktiviert ist. In der Zieldomäne wird für jeden erfolgreichen oder **fehlgeschlagenen DsAddSidHistory-Vorgang** ein eindeutiges Überwachungsereignis "Sid-Verlauf hinzufügen" generiert.

Eindeutige Überwachungsereignisse "Sid-Verlauf hinzufügen" sind auf Windows NT 4.0-Systemen nicht verfügbar. Um Überwachungsereignisse zu generieren, die eindeutig die Verwendung von [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) für die Quelldomäne widerspiegeln, führt sie Vorgänge für eine spezielle Gruppe aus, deren Name der eindeutige Bezeichner im Überwachungsprotokoll ist. Auf <SrcDomainName> dem Quelldomänencontroller muss vor dem Aufrufen von **DsAddSidHistory** eine lokale Gruppe namens "$$$" erstellt werden, deren Name aus dem NetBIOS-Quelldomänennamen besteht, der mit drei Dollarzeichen ($) (ASCII-Code = 0x24 und Unicode = U+0024) angefügt ist. Jeder Quellbenutzer und jede globale Gruppe, die ein Ziel dieses Vorgangs ist, wird hinzugefügt und dann aus der Mitgliedschaft dieser Gruppe entfernt. Dadurch werden Überwachungsereignisse "Mitglied hinzufügen" und "Mitglied löschen" in der Quelldomäne generiert, die überwacht werden können, indem nach Ereignissen gesucht wird, die auf den Gruppennamen verweisen.

> [!Note]  
> [**DsAddSidHistory-Vorgänge**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) für lokale Gruppen in einer Windows NT 4.0 oder Windows 2000-Quelldomäne im gemischten Modus können nicht überwacht werden, da lokale Gruppen nicht zu Mitgliedern einer anderen lokalen Gruppe werden können und daher nicht der speziellen <SrcDomainName> lokalen Gruppe "$$$" hinzugefügt werden können. Diese fehlende Überwachung stellt kein Sicherheitsproblem für die Quelldomäne dar, da der Ressourcenzugriff auf die Quelldomäne von diesem Vorgang nicht betroffen ist. Das Hinzufügen der SID einer lokalen Quellgruppe zu einer lokalen Zielgruppe gewährt keinen zusätzlichen Benutzern Zugriff auf Quellressourcen, die durch diese lokale Gruppe geschützt werden. Das Hinzufügen von Mitgliedern zur lokalen Zielgruppe gewährt ihnen keinen Zugriff auf Quellressourcen. Hinzugefügten Mitgliedern wird nur Zugriff auf Server in der Zieldomäne gewährt, die aus der Quelldomäne migriert wurden, die möglicherweise über Ressourcen verfügen, die durch die SID der lokalen Quellgruppe geschützt sind.

 

## <a name="data-transmission-security"></a>Sicherheit der Datenübertragung

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erzwingt die folgenden Sicherheitsmaßnahmen:

-   Von einer Windows 2000-Arbeitsstation aufgerufen, werden die Anmeldeinformationen des Aufrufers verwendet, um den RPC-Aufruf an den Zieldomänencontroller zu authentifizieren und den Datenschutz zu schützen. Wenn *SrcDomainCreds* nicht **NULL** ist, müssen sowohl die Arbeitsstation als auch der Zieldomänencontroller die 128-Bit-Verschlüsselung unterstützen, um die Anmeldeinformationen datenschutzlich zu schützen. Wenn die 128-Bit-Verschlüsselung nicht verfügbar ist und *SrcDomainCreds* bereitgestellt wird, muss der Aufruf auf dem Zieldomänencontroller erfolgen.
-   Der Zieldomänencontroller kommuniziert entweder mithilfe von *SrcDomainCreds* oder den Anmeldeinformationen des Aufrufers mit dem Quelldomänencontroller, um sich gegenseitig zu authentifizieren und die Integrität des Leseschutzes für die SID des Quellkontos (mithilfe einer SAM-Suche) und **sIDHistory** (mit ldap-Leseberechtigung) zu schützen.

## <a name="threat-models"></a>Bedrohungsmodelle

In der folgenden Tabelle sind die potenziellen Bedrohungen aufgeführt, die dem [**DsAddSidHistory-Aufruf**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) zugeordnet sind, und es werden die Sicherheitsmaßnahmen behandelt, die für die jeweilige Bedrohung relevant sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Potenzielle Bedrohung</th>
<th>Sicherheitsmaßnahme</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Man-in-the-Middle-Angriff<br/> Ein nicht autorisierter Benutzer fängt die Such-SID des Rückgabeaufrufs <em>des Quellobjekts</em> ab und ersetzt die Quellobjekt-SID durch eine beliebige SID für das Einfügen in ein ZIELobjekt SIDhistory.<br/></td>
<td>Die <em>Such-SID des Quellobjekts</em> ist ein authentifizierter RPC, der die Administratoranmeldeinformationen des Aufrufers mit Paketintegritätsnachrichtenschutz verwendet. Dadurch wird sichergestellt, dass der Rückgabeaufruf nicht ohne Erkennung geändert werden kann. Der Zieldomänencontroller erstellt ein &quot; eindeutiges Überwachungsereignis zum Hinzufügen des SID-Verlaufs, &quot; das die sid wiedergibt, die dem Zielkonto <strong>sIDHistory</strong>hinzugefügt wurde.<br/></td>
</tr>
<tr class="even">
<td>Domäne der Quelle "Trojaner"<br/> Ein nicht autorisierter Benutzer erstellt eine &quot; Trojaner-Quelldomäne in &quot; einem privaten Netzwerk, das über die gleiche Domänen-SID und einige der gleichen Konto-SIDs wie die legitime Quelldomäne verfügt. Der nicht autorisierte Benutzer versucht dann, <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> in einer Zieldomäne auszuführen, um die SID eines Quellkontos abzurufen. Dies geschieht ohne die Tatsächlichen Anmeldeinformationen des Quelldomänenadministrators und ohne einen Überwachungspfad in der echten Quelldomäne zu verlassen. Die Methode des nicht autorisierten Benutzers zum Erstellen der Quelldomäne "TrojanEr" könnte eine der folgenden Sein:
<ul>
<li>Rufen Sie eine Kopie (BDC-Sicherung) des SAM der Quelldomäne ab.</li>
<li>Erstellen Sie eine neue Domäne, ändern Sie die Domänen-SID auf dem Datenträger entsprechend der legitimen Quelldomänen-SID, und erstellen Sie dann genügend Benutzer, um ein Konto mit der gewünschten SID zu instanziieren.</li>
<li>Erstellen Sie ein BDC-Replikat. Hierfür sind Anmeldeinformationen des Quelldomänenadministrators erforderlich. Anschließend führt der nicht autorisierte Benutzer das Replikat in ein privates Netzwerk, um den Angriff zu implementieren.</li>
</ul>
<br/></td>
<td>Es gibt zwar viele Möglichkeiten für einen nicht autorisierten Benutzer, eine gewünschte Quellobjekt-SID abzurufen oder zu erstellen, aber der nicht autorisierte Benutzer kann sie nicht verwenden, um die <strong>IDHistory</strong> eines Kontos zu aktualisieren, ohne Mitglied der Gruppe "Zieldomänenadministratoren" zu sein. Da die Überprüfung auf dem Zieldomänencontroller für die Mitgliedschaft des Domänenadministrators hart codiert ist, gibt es auf dem Zieldomänencontroller keine Methode zum Ändern einer Datenträgeränderung, um die Zugriffssteuerungsdaten zu ändern, die diese Funktion schützen. In der Zieldomäne wird der Versuch überwacht, ein Quellkonto für einen Trojaner zu klonen. Dieser Angriff wird gemindert, indem die Mitgliedschaft in der Gruppe Domänenadministratoren nur für personen mit hoher Vertrauenswürdigschaft reserviert wird.<br/></td>
</tr>
<tr class="odd">
<td>Änderung des SID-Verlaufs auf dem Datenträger<br/> Ein komplexer, nicht autorisierter Benutzer mit Domänenadministratoranmeldeinformationen und physischem Zugriff auf einen Domänencontroller in der Zieldomäne kann einen <strong>sIDHistory-Wert</strong> des Kontos auf dem Datenträger ändern.<br/></td>
<td>Dieser Versuch wird nicht mithilfe von <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>aktiviert. Dieser Angriff wird gemindert, indem der physische Zugriff auf Domänencontroller für alle Außer-vertrauenswürdigen Administratoren verhindert wird.<br/></td>
</tr>
<tr class="even">
<td>Nicht autorisierter Code, der zum Entfernen von Schutzmaßnahmen verwendet wird<br/> Ein nicht autorisierter Benutzer oder ein nicht autorisierter Administrator mit physischem Zugriff auf den Verzeichnisdienstcode könnte nicht autorisierten Code erstellen, der Folgendes:
<ol>
<li>Entfernt die Überprüfung auf Mitgliedschaft in der Gruppe Domänenadministratoren im Code.</li>
<li>Ändert die Aufrufe auf dem Quelldomänencontroller, der die SID auf einen LookupSidFromName verweist, der nicht überwacht wird.</li>
<li>Entfernt Überwachungsprotokollaufrufe.</li>
</ol>
<br/></td>
<td>Jemand, der physischen Zugriff auf den DS-Code hat und über ausreichende Kenntnisse verfügt, um nicht autorisierten Code zu erstellen, kann das <strong>sIDHistory-Attribut</strong> eines Kontos beliebig ändern. Die <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory-API</strong></a> erhöht dieses Sicherheitsrisiko nicht.<br/></td>
</tr>
<tr class="odd">
<td>Ressourcen, die für gestohlene SIDs anfällig sind<br/> Wenn ein nicht autorisierter Benutzer erfolgreich eine der hier beschriebenen Methoden zum Ändern eines <strong>Kontos sIDHistory</strong>verwendet hat und die ressourcendomänen von Interesse der nicht autorisierten Benutzerkontodomäne vertrauen, kann der nicht autorisierte Benutzer nicht autorisierten Zugriff auf die Ressourcen der gestohlenen SID erhalten, möglicherweise ohne einen Überwachungspfad in der Kontodomäne zu hinterlassen, aus der die SID gestohlen wurde.<br/></td>
<td>Ressourcendomänenadministratoren schützen ihre Ressourcen, indem sie nur die Vertrauensstellungen einrichten, die aus Sicherheitssicht sinnvoll sind. Die Verwendung von <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> ist in der vertrauenswürdigen Zieldomäne auf Mitglieder der Gruppe Domänenadministratoren beschränkt, die bereits über umfassende Berechtigungen im Rahmen ihrer Zuständigkeiten verfügen.<br/></td>
</tr>
<tr class="even">
<td>Nicht autorisierte Zieldomäne<br/> Ein nicht autorisierter Benutzer erstellt eine Windows 2000-Domäne mit einem Konto, dessen <strong>sIDHistory</strong> eine SID enthält, die aus einer Quelldomäne gestohlen wurde. Der nicht autorisierte Benutzer verwendet dieses Konto für den nicht autorisierten Zugriff auf Ressourcen.<br/></td>
<td>Der nicht autorisierte Benutzer benötigt Administratoranmeldeinformationen für die Quelldomäne, um <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>zu verwenden, und verlässt einen Überwachungspfad auf dem Quelldomänencontroller. Die nicht autorisierte Zieldomäne erhält nicht autorisierten Zugriff nur in anderen Domänen, die der nicht autorisierten Domäne vertrauen, was Administratorrechte in diesen Ressourcendomänen erfordert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="operational-constraints"></a>Betriebseinschränkungen

In diesem Abschnitt werden die betriebsbedingten Einschränkungen der Verwendung der [**DsAddSidHistory-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) beschrieben.

Die SID von *SrcPrincipal* darf nicht bereits in der Zielstruktur vorhanden sein, entweder als primäre Konto-SID oder in der **sIDHistory** eines Kontos. Die Ausnahme ist, dass [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) beim Versuch, eine SID zu einer **sIDHistory** hinzuzufügen, die eine identische SID enthält, keinen Fehler generiert. Durch dieses Verhalten kann **DsAddSidHistory** mehrmals mit identischer Eingabe ausgeführt werden, was zu einem Erfolg und einem konsistenten Endzustand führt, um die Benutzerfreundlichkeit des Toolentwicklers zu erleichtern.

> [!Note]  
> Die Replikationslatenz des globalen Katalogs kann ein Fenster bereitstellen, in dem doppelte SIDs erstellt werden können. Doppelte SIDs können jedoch problemlos von einem Administrator gelöscht werden.

 

*SrcPrincipal* und *DstPrincipal* müssen einen der folgenden Typen aufweisen:

-   Benutzer
-   Sicherheitsfähige Gruppe, einschließlich:

    <dl> Lokale Gruppe  
    Globale Gruppe  
    Lokale Domänengruppe (nur Windows 2000 im einheitlichen Modus)  
    Universelle Gruppe (nur Windows 2000 im einheitlichen Modus)  
    </dl>

Die Objekttypen *von SrcPrincipal* und *DstPrincipal* müssen übereinstimmen.

-   Wenn *SrcPrincipal* ein Benutzer ist, muss *DstPrincipal* ein Benutzer sein.
-   Wenn *SrcPrincipal* eine lokale oder lokale Domänengruppe ist, muss *DstPrincipal* eine lokale Domänengruppe sein.
-   Wenn *SrcPrincipal* eine globale oder universelle Gruppe ist, muss *DstPrincipal* eine globale oder universelle Gruppe sein.

*SrcPrincipal* und *DstPrincipal* können keinen der folgenden Typen aufweisen: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) schlägt in diesen Fällen mit einem Fehler fehl)

-   Computer (Arbeitsstation oder Domänencontroller)
-   Domänenübergreifende Vertrauensstellung
-   Temporäres dupliziertes Konto (praktisch nicht verwendetes Feature, eine Vorgängerversion von LANman)
-   Konten mit bekannten SIDs. Bekannte SIDs sind in jeder Domäne identisch. daher würde das Hinzufügen zu einer **sIDHistory** die SID-Eindeutigkeitsanforderung einer Windows 2000-Gesamtstruktur verletzen. Konten mit bekannten SIDs umfassen die folgenden lokalen Gruppen:

    <dl> Kontooperatoren  
    Administratoren  
    Sicherungsoperatoren  
    Gäste  
    Druckoperatoren  
    Replicator  
    Serveroperatoren  
    Benutzer  
    </dl>

Wenn *SrcPrincipal* über einen bekannten relativen Bezeichner (RID) und ein domänenspezifisches Präfix verfügt, d. h. Domänenadministratoren, Domänenbenutzer und Domänencomputer, muss *DstPrincipal* über die gleiche bekannte RID verfügen, damit [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) erfolgreich ausgeführt werden kann. Konten mit bekannten RIDs umfassen die folgenden Benutzer und globalen Gruppen:

-   Administrator
-   Gast
-   Domänenadministratoren
-   Domänenbenutzer
-   Domänenbenutzer

## <a name="setting-the-registry-value"></a>Festlegen des Registrierungswerts

Das folgende Verfahren zeigt, wie Sie den TcpipClientSupport-Registrierungswert festlegen.

**So legen Sie den TcpipClientSupport-Registrierungswert fest**

1.  Erstellen Sie den folgenden Registrierungswert als REG \_ DWORD-Wert auf dem Quelldomänencontroller, und legen Sie seinen Wert auf 1 fest.

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ TcpipClientSupport**

2.  Starten Sie dann den Quelldomänencontroller neu. Dieser Registrierungswert bewirkt, dass der SAM TCP/IP überwacht. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) schlägt fehl, wenn dieser Wert auf dem Quelldomänencontroller nicht festgelegt ist.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Aktivieren der Überwachung von Benutzer-/Gruppenverwaltungsereignissen

Das folgende Verfahren zeigt, wie Sie die Überwachung von Benutzer-/Gruppenverwaltungsereignissen in einer Windows 2000- oder Windows Server 2003-Quell- oder -Zieldomäne aktivieren.

**So aktivieren Sie die Überwachung von Benutzer-/Gruppenverwaltungsereignissen in einer Windows 2000- oder Windows Server 2003-Quell- oder Zieldomäne**

1.  Wählen Sie im Active Directory-Benutzer und -Computer MMC-Snap-In den Zieldomänencontrollercontainer aus.
2.  Klicken Sie mit der rechten Maustaste auf **Domänencontroller,** und wählen Sie **Eigenschaften** aus.
3.  Klicken Sie auf die Registerkarte **Gruppenrichtlinie.**
4.  Wählen Sie die **Standarddomänencontrollerrichtlinie aus,** und klicken Sie auf **Bearbeiten.**
5.  Doppelklicken Sie **unter Computerkonfiguration \\ Windows Einstellungen \\ Sicherheits- Einstellungen \\ \\ Überwachungsrichtlinie für lokale Richtlinien** auf **Kontoverwaltung überwachen.**
6.  Wählen Sie im Fenster **Kontoverwaltung überwachen** die Beiden Überwachung **erfolgreich** und **Fehler** aus. Richtlinienupdates werden nach einem Neustart oder nach einer Aktualisierung wirksam.
7.  Überprüfen Sie, ob die Überwachung aktiviert ist, indem Sie die effektive Überwachungsrichtlinie im Gruppenrichtlinie MMC-Snap-In anzeigen.

Das folgende Verfahren zeigt, wie Sie die Überwachung von Benutzer-/Gruppenverwaltungsereignissen in einer Windows NT 4.0-Domäne aktivieren.

**So aktivieren Sie die Überwachung von Benutzer-/Gruppenverwaltungsereignissen in einer Windows NT 4.0-Domäne**

1.  Klicken Sie im **Benutzer-Manager für Domänen** auf das Menü **Richtlinien,** und wählen Sie **Überwachen** aus.
2.  Wählen Sie **Diese Ereignisse überwachen** aus.
3.  Aktivieren Sie für **Benutzer- und Gruppenverwaltung** die Informationen **erfolg und fehler.**

Das folgende Verfahren zeigt, wie Sie die Überwachung von Benutzer-/Gruppenverwaltungsereignissen in einer Windows NT 4.0-, Windows 2000- oder Windows Server 2003-Quelldomäne aktivieren.

**So aktivieren Sie die Überwachung von Benutzer-/Gruppenverwaltungsereignissen in einer Windows NT 4.0-, Windows 2000- oder Windows Server 2003-Quelldomäne**

1.  Klicken Sie im **Benutzer-Manager für Domänen** auf das Menü **Benutzer,** und wählen Sie **Neue lokale Gruppe** aus.
2.  Geben Sie einen Gruppennamen ein, der aus dem NetBIOS-Quelldomänennamen besteht, dem drei Dollarzeichen ($) angefügt sind, z.B. FABRIKAM$$$. Das Beschreibungsfeld sollte angeben, dass diese Gruppe verwendet wird, um die Verwendung von [**DsAddSidHistory-**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) oder Klonvorgängen zu überwachen. Stellen Sie sicher, dass keine Mitglieder in der Gruppe vorhanden sind. Klicken Sie auf **OK**.

Der [**DsAddSidHistory-Vorgang**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) schlägt fehl, wenn die Quell- und Zielüberwachung nicht wie hier beschrieben aktiviert ist.

## <a name="set-up-trust-if-required"></a>Einrichten der Vertrauensstellung bei Bedarf

Wenn einer der folgenden Punkte zutrifft, muss eine Vertrauensstellung von der Quelldomäne zur Zieldomäne eingerichtet werden (dies muss in einer anderen Gesamtstruktur auftreten):

-   Die Quelldomäne ist Windows Server 2003.
-   Die Quelldomäne ist Windows NT 4.0 und *SrcDomainCreds* **ist NULL.**

 

 





