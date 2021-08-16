---
title: Zuordnung zwischen IADsUser-Eigenschaften und Active Directory-Attributen
description: Falls zutreffend, wird eine Eigenschaft des ADSI-Benutzerobjekts einem entsprechenden Active Directory-Attribut zugeordnet. Die ADSI-Benutzerobjekteigenschaften sind den IADsUser-Eigenschaftenmethoden zugeordnet.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Zuordnung zwischen IADsUser-Eigenschaften und Active Directory-Attributen ADSI
- LDAP-Anbieter ADSI , Benutzerobjekt, Zuordnung zwischen IADsUser-Eigenschaften und Active Directory-Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e659c6325457b2654ad5cfeef964975949150232c4ae3376fac640c51c41aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839480"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Zuordnung zwischen IADsUser-Eigenschaften und Active Directory-Attributen

Falls zutreffend, wird eine Eigenschaft des ADSI-Benutzerobjekts einem entsprechenden Active Directory-Attribut zugeordnet. Die ADSI-Benutzerobjekteigenschaften sind den [**IADsUser-Eigenschaftenmethoden**](/windows/desktop/api/Iads/nn-iads-iadsuser) zugeordnet.

In der folgenden Tabelle wird die Zuordnung zwischen den [**IADsUser-Eigenschaften**](/windows/desktop/api/Iads/nn-iads-iadsuser) für den LDAP-Anbieter und dem entsprechenden Active Directory-Attribut aufgeführt.



| IADsUser(Eigenschaft)                                           | Active Directory-Attribut                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **ADS \_ UF \_ ACCOUNTDISABLE-Flag** im [**userAccountControl-Attribut.**](/windows/desktop/ADSchema/a-useraccountcontrol)  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Nicht unterstützt.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Department**](iadsuser-property-methods.md)             | [**Abteilung**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Beschreibung**](iadsuser-property-methods.md)            | [**Beschreibung**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Division**](iadsuser-property-methods.md)               | [**Aufteilung**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**Emailaddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**Employeeid**](iadsuser-property-methods.md)             | [**Employeeid**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**FaxNumber**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**Firstname**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**Displayname**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Nicht unterstützt.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Nicht unterstützt.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Homepage**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Sprachen**](iadsuser-property-methods.md)              | Nicht unterstützt.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**Lastname**](iadsuser-property-methods.md)               | [**Sn**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Manager**](iadsuser-property-methods.md)                | [**manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | Nicht unterstützt.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Festlegen mit Gruppenrichtlinie Editor                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Festlegen mit Gruppenrichtlinie Editor                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **ADS \_ UF \_ PASSWD \_ NOTREQD-Flag** im [**userAccountControl-Attribut.**](/windows/desktop/ADSchema/a-useraccountcontrol) |
| [**Bild**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**PostalCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Profil**](iadsuser-property-methods.md)                | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Festlegen mit Gruppenrichtlinie Editor                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**mobil**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Titel**](iadsuser-property-methods.md)                  | [**Titel**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 