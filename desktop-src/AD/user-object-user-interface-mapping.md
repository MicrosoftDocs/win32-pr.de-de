---
title: Zuordnung von Benutzerobjekten und Benutzeroberflächen
description: In den folgenden Tabellen werden die Eigenschaftenseiten identifiziert, die vom Active Directory-Benutzer und -Computer-Snap-In bereitgestellt werden.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- Benutzerobjekt Benutzeroberfläche Zuordnungs-AD
- Benutzeroberfläche Zuordnung von AD, Benutzerobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024499"
---
# <a name="user-object-user-interface-mapping"></a>Zuordnung von Benutzerobjekten und Benutzeroberflächen

In den folgenden Tabellen werden die Eigenschaftenseiten identifiziert, die vom Active Directory-Benutzer und -Computer-Snap-In bereitgestellt werden. Jede Tabelle identifiziert die Benutzeroberflächenelemente der Eigenschaftenseite und das attribut, das diesem Benutzeroberflächenelement zugeordnet ist. Da die Eigenschaftenseiten, die vom Active Directory-Benutzer und -Computer Snap-In angezeigt werden, erweitert werden können, ist es nicht möglich, diese Daten für alle Seiten bereitzustellen, die in einem Eigenschaftenblatt angezeigt werden.

## <a name="general-property-page"></a>Eigenschaftenseite "Allgemein"

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen der Eigenschaftenseite **Allgemein** aufgeführt.



| Bezeichnung der Benutzeroberfläche         | Attribut in Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| First Name (Vorname)       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Last Name (Nachname)        | [**Sn**](/windows/desktop/ADSchema/a-sn)                                                 |
| Initialen         | [**Initialen**](/windows/desktop/ADSchema/a-initials)                                     |
| Anzeigename     | [**Displayname**](/windows/desktop/ADSchema/a-displayname)                               |
| BESCHREIBUNG      | [**Beschreibung**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Telefonnummer | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Telefon: Sonstiges | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| E-Mail           | [**E-Mail-Adressen**](/windows/desktop/ADSchema/a-mail)                                 |
| Webseite         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Webseite: Andere  | [**Url**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Seite "Account Property" (Kontoeigenschaft)

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen der **Eigenschaftenseite Konto** aufgeführt.



| Bezeichnung der Benutzeroberfläche                                | Attribut in Active Directory Domain Services                                                   | Kommentar                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserLogon-Name                          | [**Userprincipalname**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Dieses Feld wird aus allen Im [**userPrincipalName-Attributen**](/windows/desktop/ADSchema/a-userprincipalname) entnommen, die dem letzten @-Zeichen vorangestellt sind. Das letzte @-Zeichen und alles, nachdem es im Suffix-Kombinationsfeld platziert wurde.                                                                                                                                                      |
| Benutzeranmeldungsname (vor Windows 2000)      | [**Samaccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Anmeldezeiten                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Anmelden an                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Konto ist gesperrt                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) und [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Wenn das [**lockoutTime-Attribut**](/windows/desktop/ADSchema/a-lockouttime) nicht 0 (null) ist, wird das [**lockoutDuration-Attribut**](/windows/desktop/ADSchema/a-lockoutduration) **lockoutTime** hinzugefügt und mit dem aktuellen Datum und der aktuellen Uhrzeit verglichen, um festzustellen, ob das Konto gesperrt ist.                                                                                                                                |
| Benutzer muss Kennwort bei der nächsten Anmeldung ändern | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Benutzer kann Kennwort nicht ändern             | Nicht zutreffend                                                                                             | Dies ist das Steuerelement Kennwort ändern in der ACL.                                                                                                                                                                                                                                                                                                                                         |
| Andere Kontooptionen                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Die verbleibenden Elemente in Kontooptionen schalten Bits in der [**UserAccountControl-Attributbitmaske**](/windows/desktop/ADSchema/a-useraccountcontrol) (Flags in einem DWORD) um.                                                                                                                                                                                                                                 |
| Konto läuft ab                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | Das **Steuerelement Konto läuft ab** zeigt das Datum an, an dem das Konto am Ende abläuft. Das [**accountExpires-Attribut**](/windows/desktop/ADSchema/a-accountexpires) wird als Datum gespeichert, an dem das Konto abläuft. Aus diesem Grund wird das im **Kontoablauf-Steuerelement** angezeigte Datum als ein Tag vor dem Im **accountExpires-Attribut enthaltenen** Datum angezeigt. |



 

## <a name="address-property-page"></a>Eigenschaftenseite "Address"

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen der Eigenschaftenseite **Address** aufgeführt.



| Bezeichnung der Benutzeroberfläche        | Attribut in Active Directory Domain Services                                                 | Kommentar                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Straße          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Kein Kommentar.                                               |
| P.o.box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Kein Kommentar.                                               |
| City            | [**L**](/windows/desktop/ADSchema/a-l)                                                                         | Der  l-Attributname ist ein "L" in Kleinbuchstaben wie im Gebietsschema. |
| Bundesland/Kanton  | [**St**](/windows/desktop/ADSchema/a-st)                                                                       | Kein Kommentar.                                               |
| Postleitzahl | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Kein Kommentar.                                               |
| Land/Region  | [**c,**](/windows/desktop/ADSchema/a-c) [**co**](/windows/desktop/ADSchema/a-co)und [**countryCode**](/windows/desktop/ADSchema/a-countrycode) | Kein Kommentar.                                               |



 

## <a name="member-of-property-page"></a>Member der Eigenschaftenseite

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen der Eigenschaftenseite **Member Of** aufgeführt.



| Bezeichnung der Benutzeroberfläche          | Attribut in Active Directory Domain Services   | Kommentar                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mitglied von         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Schließt alle Gruppen in die Ui-Liste ein, mit Ausnahme der primären Gruppe, die im AD durch das [**primaryGroupId-Attribut**](/windows/desktop/ADSchema/a-primarygroupid) dargestellt wird. |
| Festlegen der primären Gruppe | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: Ist an [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) der primären Gruppe gebunden.                                                                                  |



 

## <a name="organization-property-page"></a>Eigenschaftenseite der Organisation

Die folgende Tabelle zeigt die Benutzeroberflächenbezeichnungen der **Eigenschaftenseite** Organisation.



| Benutzeroberflächenbezeichnung       | Attribut in Active Directory Domain Services | Kommentar     |
|----------------|-----------------------------------------------|-------------|
| Titel          | [**Titel**](/windows/desktop/ADSchema/a-title)                 | Kein Kommentar. |
| Department     | [**Abteilung**](/windows/desktop/ADSchema/a-department)       | Kein Kommentar. |
| Company        | [**Unternehmen**](/windows/desktop/ADSchema/a-company)             | Kein Kommentar. |
| Manager:Name   | [**manager**](/windows/desktop/ADSchema/a-manager)             | Kein Kommentar. |
| Direkte Berichte | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Kein Kommentar. |



 

## <a name="profile-property-page"></a>Profileigenschaftsseite

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen der **Eigenschaftenseite Profil** aufgeführt.



| Benutzeroberflächenbezeichnung                | Attribut in Active Directory Domain Services | Kommentar                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Profilpfad            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | Kein Kommentar.                                                                                                             |
| Anmeldeskript            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Kein Kommentar.                                                                                                             |
| Startordner: Lokaler Pfad | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Wenn **Lokaler Pfad** ausgewählt ist, wird der lokale Pfad im [**homeDirectory-Attribut**](/windows/desktop/ADSchema/a-homedirectory) gespeichert. |
| Startordner: Verbinden    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Wenn **Verbinden** ist, wird das zugeordnete Laufwerk im [**homeDrive-Attribut**](/windows/desktop/ADSchema/a-homedrive) gespeichert.          |
| Startordner: In         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Wenn **Verbinden** ausgewählt ist, wird der Pfad im [**homeDirectory-Attribut**](/windows/desktop/ADSchema/a-homedirectory) gespeichert.          |



 

## <a name="telephones-property-page"></a>Eigenschaftenseite "Telefone"

In der folgenden Tabelle sind die Benutzeroberflächenelemente der **Eigenschaftenseite Telefone** und die entsprechenden Active Directory-Attribute aufgeführt.



| Benutzeroberflächenbezeichnung        | Attribut in Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Start            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Startseite: Sonstiges     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Pager           | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                 |
| Pager: Sonstiges    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Mobil          | [**mobil**](/windows/desktop/ADSchema/a-mobile)                                               |
| Mobil: Sonstiges   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: Sonstiges      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| IP-Telefon        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| IP-Telefon: Sonstiges | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Hinweise           | [**Informationen**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Eigenschaftenseiten für Umgebungs-, Sitzungs-, Remotesteuerungs- und Terminaldiensteprofil

Die **Seiten Umgebung,** **Sitzungen,** **Remotesteuerung** und **Terminaldiensteprofil** werden für ein Benutzerobjekt bereitgestellt, um Terminaldienste zu unterstützen. Die Benutzeroberflächenelemente für diese Seiten entsprechen nicht einzelnen Attributen. Stattdessen werden die Einstellungen in privaten Daten in Active Directory Domain Services. Auf die Einstellungen der Terminaldienste kann über die [**IADsTsUserEx-Schnittstelle zugegriffen**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) werden.

 

 