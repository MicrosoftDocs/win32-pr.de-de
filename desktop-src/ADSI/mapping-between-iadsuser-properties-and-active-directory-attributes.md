---
title: Zuordnung zwischen IADsUser-Eigenschaften und Active Directory Attributen
description: Wenn zutreffend, wird eine Eigenschaft des ADSI-Benutzer Objekts einem entsprechenden Active Directory Attribut zugeordnet. Die Eigenschaften von ADSI-Benutzer Objekten werden den IADsUser-Eigenschafts Methoden zugeordnet.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Zuordnung zwischen IADsUser-Eigenschaften und Active Directory Attributen ADSI
- LDAP-Anbieter-ADSI, Benutzerobjekt, Zuordnung zwischen IADsUser-Eigenschaften und Active Directory Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b817a8c56e2c74c846e1343e0ed7803427f4a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391014"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Zuordnung zwischen IADsUser-Eigenschaften und Active Directory Attributen

Wenn zutreffend, wird eine Eigenschaft des ADSI-Benutzer Objekts einem entsprechenden Active Directory Attribut zugeordnet. Die Eigenschaften von ADSI-Benutzer Objekten werden den [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Eigenschafts Methoden zugeordnet.

In der folgenden Tabelle wird die Zuordnung zwischen den [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Eigenschaften für den LDAP-Anbieter und dem entsprechenden Active Directory-Attribut aufgelistet.



| IADsUser (Eigenschaft)                                           | Active Directory-Attribut                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Accountdeaktiviert**](iadsuser-property-methods.md)        | **Anzeigen \_ Das Konto "UF \_ accountdeaktivieren** " im Attribut " [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) ".  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**Badloginaddress**](iadsuser-property-methods.md)        | Nicht unterstützt.                                                                                              |
| [**Badlogincount**](iadsuser-property-methods.md)          | [**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Klinik**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Beschreibung**](iadsuser-property-methods.md)            | [**Beschreibung**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Division**](iadsuser-property-methods.md)               | [**Division**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**EmployeeID**](iadsuser-property-methods.md)             | [**EmployeeID**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**Faxnummer**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**Display Name**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**Graceloginsallowed**](iadsuser-property-methods.md)     | Nicht unterstützt.                                                                                              |
| [**Graceloginsrestdauer**](iadsuser-property-methods.md)   | Nicht unterstützt.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homedirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Seite**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**Isaccountlocked**](iadsuser-property-methods.md)        | [**Lockout Time**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Sprachen**](iadsuser-property-methods.md)              | Nicht unterstützt.                                                                                              |
| [**Lastfailedlogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**Lastlogoff**](iadsuser-property-methods.md)             | [**lastlogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**SN**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**Loginhours**](iadsuser-property-methods.md)             | [**LogonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**Loginscript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**Loginworkstations**](iadsuser-property-methods.md)      | [**Benutzer Arbeitsstationen**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Dienst**](iadsuser-property-methods.md)                | [**manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**Maxlogins**](iadsuser-property-methods.md)              | Nicht unterstützt.                                                                                              |
| [**Maxstorage**](iadsuser-property-methods.md)             | [**maxstorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix Name**](iadsuser-property-methods.md)             | [**Personal Titel**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**Wird**](iadsuser-property-methods.md)             | [**generationqualifizierer**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**Officelocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**Passwordexpirationdate**](iadsuser-property-methods.md) | Mit Gruppenrichtlinie Editor festlegen                                                                               |
| [**Passwordlastchanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**Passwordminimumlength**](iadsuser-property-methods.md)  | Mit Gruppenrichtlinie Editor festlegen                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **Anzeigen \_ Das Flag "UF \_ passwd \_ notreqd** " im Attribut " [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) ". |
| [**Picture**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**Postaladressen**](iadsuser-property-methods.md)        | [**PostalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**Postalcodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Profil**](iadsuser-property-methods.md)                | [**Profilpfad**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**Requirements-Wort**](iadsuser-property-methods.md)  | Mit Gruppenrichtlinie Editor festlegen                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**Telefoniehome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**Telefoniemobile**](iadsuser-property-methods.md)        | [**Funk**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**Telefoniepager**](iadsuser-property-methods.md)         | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Titel**](iadsuser-property-methods.md)                  | [**Tel**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 