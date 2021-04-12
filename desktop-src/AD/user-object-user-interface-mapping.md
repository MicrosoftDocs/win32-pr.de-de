---
title: Zuordnung von Benutzerobjekten und Benutzeroberflächen
description: In den folgenden Tabellen sind die Eigenschaften Seiten aufgeführt, die vom Snap-in "Active Directory Benutzer und Computer" bereitgestellt werden.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- Benutzerobjekt-Benutzeroberflächen Zuordnung AD
- Zuordnung von Benutzeroberflächen Zuordnung, Benutzerobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc797be7c53ba7759051016ddd0548c8c7124cd2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472485"
---
# <a name="user-object-user-interface-mapping"></a>Zuordnung von Benutzerobjekten und Benutzeroberflächen

In den folgenden Tabellen sind die Eigenschaften Seiten aufgeführt, die vom Snap-in "Active Directory Benutzer und Computer" bereitgestellt werden. Jede Tabelle identifiziert die Benutzeroberflächen Elemente der Eigenschaften Seite und das Attribut, das diesem Benutzeroberflächen Element zugeordnet ist. Da die Eigenschaften Seiten, die vom Active Directory Benutzer-und Computer-Snap-in angezeigt werden, erweitert werden können, ist es nicht möglich, diese Daten für alle Seiten bereitzustellen, die in einem Eigenschaften Blatt angezeigt werden.

## <a name="general-property-page"></a>Eigenschaften Seite "Allgemein"

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen der Eigenschaften Seite **Allgemein** aufgeführt.



| UI-Bezeichnung         | Attribut in Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| First Name (Vorname)       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Last Name (Nachname)        | [**SN**](/windows/desktop/ADSchema/a-sn)                                                 |
| Initialen         | [**Initialen**](/windows/desktop/ADSchema/a-initials)                                     |
| Anzeigename     | [**Display Name**](/windows/desktop/ADSchema/a-displayname)                               |
| BESCHREIBUNG      | [**Beschreibung**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Telefonnummer | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Telefon: Sonstige | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| E-Mail           | [**E-Mail-Adressen**](/windows/desktop/ADSchema/a-mail)                                 |
| Webseite         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Webseite: Sonstige  | [**Urne**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Eigenschaften Seite "Konto"

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen der Eigenschaften Seite für das **Konto** aufgeführt.



| UI-Bezeichnung                                | Attribut in Active Directory Domain Services                                                   | Kommentar                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Benutzer Anmelde Name                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Dieses Feld stammt von allen Elementen im [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) -Attribut, das dem letzten @-Zeichen vorangestellt ist. Das letzte Zeichen "@" und alles nach dem Zeichen wird in das Suffix-Kombinations Feld eingefügt.                                                                                                                                                      |
| Benutzer Anmelde Name (Pre-Windows 2000)      | [**sAMAccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Anmeldezeiten                             | [**LogonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Anmelden an                               | [**logonworkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Konto ist gesperrt                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) und [ **LockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Wenn das [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) -Attribut nicht NULL ist, wird das [**LockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) -Attribut zu **lockoutTime** hinzugefügt und mit dem aktuellen Datum und der aktuellen Uhrzeit verglichen, um zu bestimmen, ob das Konto gesperrt ist.                                                                                                                                |
| Benutzer muss Kennwort bei der nächsten Anmeldung ändern | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Kein Kommentar.                                                                                                                                                                                                                                                                                                                                                                             |
| Benutzer kann Kennwort nicht ändern             | –                                                                                             | Dies ist das Steuerelement für das Ändern von Kenn Wörtern in der ACL.                                                                                                                                                                                                                                                                                                                                         |
| Weitere Konto Optionen                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Die verbleibenden Elemente in den Konto Optionen wechseln Bits in das [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) -Attribut Bitmaske (Flags in einem DWORD).                                                                                                                                                                                                                                 |
| Konto läuft ab                         | [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | Mit dem Steuerelement " **Konto läuft** ab" wird das Datum angezeigt, an dem das Konto am Ende von abläuft. Das [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires) -Attribut wird als Datum gespeichert, an dem das Konto abläuft. Aus diesem Grund wird das im **Konto** angezeigte Datum als ein Tag vor dem Datum angezeigt, das im **AccountExpires** -Attribut enthalten ist. |



 

## <a name="address-property-page"></a>Address-Eigenschaften Seite

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen der Eigenschaften Seite " **Address** " aufgeführt.



| UI-Bezeichnung        | Attribut in Active Directory Domain Services                                                 | Kommentar                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Street          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Kein Kommentar.                                               |
| P. O. Box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Kein Kommentar.                                               |
| City            | [**l**](/windows/desktop/ADSchema/a-l)                                                                         | Der Name des **l** -Attributs ist ein Kleinbuchstabe "l", wie im Gebiets Schema. |
| Bundesland/Kanton  | [**St**](/windows/desktop/ADSchema/a-st)                                                                       | Kein Kommentar.                                               |
| Zip/Postleitzahl | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Kein Kommentar.                                               |
| Land/Region  | [**c**](/windows/desktop/ADSchema/a-c), [**Co**](/windows/desktop/ADSchema/a-co)und [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) | Kein Kommentar.                                               |



 

## <a name="member-of-property-page"></a>Mitglied der Eigenschaften Seite

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen des Members **der** Eigenschaften Seite aufgeführt.



| UI-Bezeichnung          | Attribut in Active Directory Domain Services   | Kommentar                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mitglied von         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Schließt alle Gruppen in der UI-Liste ein, mit Ausnahme der primären Gruppe, die in der AD durch das [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) -Attribut dargestellt wird. |
| Primäre Gruppe festlegen | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: an [**primarygrouptoken**](/windows/desktop/ADSchema/a-primarygrouptoken) der primären Gruppe gebunden.                                                                                  |



 

## <a name="organization-property-page"></a>Eigenschaften Seite "Organisation"

In der folgenden Tabelle werden die Benutzeroberflächen Bezeichnungen der Eigenschaften Seite für die **Organisation** angezeigt.



| UI-Bezeichnung       | Attribut in Active Directory Domain Services | Kommentar     |
|----------------|-----------------------------------------------|-------------|
| Titel          | [**title**](/windows/desktop/ADSchema/a-title)                 | Kein Kommentar. |
| Department     | [**department**](/windows/desktop/ADSchema/a-department)       | Kein Kommentar. |
| Company        | [**Geschäfts**](/windows/desktop/ADSchema/a-company)             | Kein Kommentar. |
| Manager: Name   | [**manager**](/windows/desktop/ADSchema/a-manager)             | Kein Kommentar. |
| Direktberichte | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Kein Kommentar. |



 

## <a name="profile-property-page"></a>Profil Eigenschaften Seite

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen der **Profil** Eigenschaften Seite aufgeführt.



| UI-Bezeichnung                | Attribut in Active Directory Domain Services | Kommentar                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Profilpfad            | [**Profilpfad**](/windows/desktop/ADSchema/a-profilepath)     | Kein Kommentar.                                                                                                             |
| Anmelde Skript            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Kein Kommentar.                                                                                                             |
| Basisordner: lokaler Pfad | [**homedirectory**](/windows/desktop/ADSchema/a-homedirectory) | Wenn **lokaler Pfad** ausgewählt ist, wird der lokale Pfad im [**Homedirectory**](/windows/desktop/ADSchema/a-homedirectory) -Attribut gespeichert. |
| Basisordner: verbinden    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Wenn **Connect** ausgewählt ist, wird das zugeordnete Laufwerk im [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) -Attribut gespeichert.          |
| Basisordner:         | [**homedirectory**](/windows/desktop/ADSchema/a-homedirectory) | Wenn **Connect** ausgewählt ist, wird der Pfad im [**Homedirectory**](/windows/desktop/ADSchema/a-homedirectory) -Attribut gespeichert.          |



 

## <a name="telephones-property-page"></a>Eigenschaften Seite "Telefone"

In der folgenden Tabelle werden die Benutzeroberflächen Elemente der Eigenschaften Seite für **Telefone** und ihre entsprechenden Active Directory Attribute aufgelistet.



| UI-Bezeichnung        | Attribut in Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Startseite            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Startseite: Sonstige     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Pager           | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                 |
| Pager: Sonstige    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Mobile          | [**Funk**](/windows/desktop/ADSchema/a-mobile)                                               |
| Mobil: Sonstige   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: Sonstige      | [**otherfaksimiletelefonienumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| IP-Telefon        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| IP-Telefon: Sonstige | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Notizen           | [**Opo**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Eigenschaften Seiten für Umgebung, Sitzungen, Remote Steuerung und Terminal Dienste-Profil

Die Seiten **Umgebung**, **Sitzungen**, **Remote Steuerung** und **Terminaldienste-Profil** werden für ein Benutzerobjekt zur Unterstützung von Terminal Diensten bereitgestellt. Die Benutzeroberflächen Elemente für diese Seiten entsprechen nicht den einzelnen Attributen. Stattdessen werden die Einstellungen in privaten Daten in Active Directory Domain Services gespeichert. Der Zugriff auf die Terminaldiensteeinstellungen ist mit der [**iadstsuserex**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) -Schnittstelle möglich.

 

 