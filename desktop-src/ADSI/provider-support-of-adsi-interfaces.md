---
title: Anbieter Unterstützung von ADSI-Schnittstellen
description: Die folgende Tabelle enthält eine kurze Beschreibung der Schnittstellen, die von den Anbietern unterstützt werden, die in ADSI für Windows 2000 und dem DS-Client enthalten sind.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Anbieter Unterstützung von ADSI-Schnittstellen ADSI
- ADSI ADSI, Dienstanbieter, Schnittstellen, die von jedem Anbieter unterstützt werden
- Anbieter Unterstützung für IADsUser
- Anbieter Unterstützung für iadscomputer
- Anbieter Unterstützung für iadscomputeroperations
- Anbieter Unterstützung für iadsdomain
- Anbieter Unterstützung für iadsfileservice
- Anbieter Unterstützung für IADsGroup
- Anbieter Unterstützung für iadsclass
- Anbieter Unterstützung für iadsproperty
- Anbieter Unterstützung für iadssyntax
- Anbieter Unterstützung für IADsContainer
- Anbieter Unterstützung für iadsnamespaces
- Anbieter Unterstützung für IADsAccessControlEntry
- Anbieter Unterstützung für IADsAccessControlList
- Anbieter Unterstützung für IADsSecurityDescriptor
- Anbieter Unterstützung für iadsobjectoptions
- Anbieter Unterstützung für iadscollection
- Anbieter Unterstützung für iadsmembers
- Anbieter Unterstützung für iadspathname
- Anbieter Unterstützung für iadsprintqueue
- Anbieter Unterstützung für iadsprintqueueoperations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12803929d96a61aac6603be2c528084c91693c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309236"
---
# <a name="provider-support-of-adsi-interfaces"></a>Anbieter Unterstützung von ADSI-Schnittstellen

Die folgende Tabelle enthält eine kurze Beschreibung der Schnittstellen, die von den Anbietern unterstützt werden, die in ADSI für Windows 2000 und dem DS-Client enthalten sind. Ein mit "yes" markierter Eintrag gibt an, dass mindestens ein ADSI-Objekt des angegebenen Anbieters die zugeordnete Schnittstelle unterstützt. "No" gibt an, dass kein Objekt des Anbieters die-Schnittstelle in dieser Version unterstützt. In Zukunft können derzeit nicht unterstützte Schnittstellen von den vom System bereitgestellten Anbietern unterstützt werden.

Weitere Informationen zu den ADSI-anbieterspezifischen Implementierungsdetails finden Sie unter:

-   [ADSI-LDAP-Anbieter](adsi-ldap-provider.md)
-   [ADSI WinNT-Anbieter](adsi-winnt-provider.md)
-   [ADSI-Router](adsi-router.md)

Klicken Sie in der ersten Spalte der Tabelle auf den entsprechenden Schnittstellennamen, um weitere Informationen dazu zu erhalten, welche Eigenschaft oder Methode für die einzelnen Schnittstellen unterstützt wird.



| Schnittstellenname                                                 | LDAP | WinNT |
|----------------------------------------------------------------|------|-------|
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Ja  | Ja   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Ja  | Nein    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Ja  | Nein    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | Nein   | Nein    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | Nein   | Nein    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | Nein   | Nein    |
| [**Iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Ja  | Ja   |
| [**Iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | Nein   | Ja   |
| [**Iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | Nein   | Ja   |
| [**Iadscomputeroperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | Nein   | Ja   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Ja  | Ja   |
| [**Iadsdeleteops**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Ja  | Nein    |
| [**Iadsdomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | Nein   | Ja   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | Nein   | Nein    |
| [**Iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Ja  | Ja   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | Nein   | Nein    |
| [**Iadsfileservice**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | Nein   | Ja   |
| [**Iadsfileserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | Nein   | Ja   |
| [**Iadsfileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | Nein   | Ja   |
| [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Ja  | Ja   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | Nein   | Nein    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Ja  | Nein    |
| [**Iadsloalität**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Ja  | Nein    |
| [**Iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Ja  | Ja   |
| [**Iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Ja  | Ja   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | Nein   | Nein    |
| [**Iadso**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Ja  | Nein    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Ja  | Nein    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | Nein   | Nein    |
| [**Iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Ja  | Ja   |
| [**Iadsou**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Ja  | Nein    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | Nein   | Nein    |
| [**Iadspathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Ja  | Ja   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | Nein   | Nein    |
| [**Iadsprintjob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | Nein   | Ja   |
| [**Iadsprintjoboperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | Nein   | Ja   |
| [**Iadsprintqueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Ja  | Ja   |
| [**Iadsprintqueueoperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Ja  | Ja   |
| [**Iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Ja  | Ja   |
| [**Iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Ja  | Ja   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Ja  | Ja   |
| [**Iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Ja  | Ja   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Ja  | Ja   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | Nein   | Nein    |
| [**Iadsresource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | Nein   | Ja   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Ja  | Nein    |
| [**Iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | Nein   | Ja   |
| [**Iadsserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | Nein   | Ja   |
| [**Iadssession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | Nein   | Ja   |
| [**Iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Ja  | Ja   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | Nein   | Nein    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | Nein   | Nein    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Ja  | Ja   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Ja  | Nein    |
| [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Ja  | Nein    |



 

## <a name="provider-support-for-iadsuser"></a>Anbieter Unterstützung für IADsUser



| Eigenschaft                                                    | LDAP          | WinNT         |
|-------------------------------------------------------------|---------------|---------------|
| [**Accountdeaktiviert**](iadsuser-property-methods.md)        | Unterstützt     | Unterstützt     |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | Unterstützt     | Unterstützt     |
| [**Badloginaddress**](iadsuser-property-methods.md)        | Nicht unterstützt   | Nicht unterstützt |
| [**Badlogincount**](iadsuser-property-methods.md)          | Unterstützt     | Unterstützt     |
| [**Klinik**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**Beschreibung**](iadsuser-property-methods.md)            | Unterstützt     | Unterstützt     |
| [**Division**](iadsuser-property-methods.md)               | Unterstützt     | Nicht unterstützt   |
| [**EmailAddress**](iadsuser-property-methods.md)           | Unterstützt     | Nicht unterstützt   |
| [**EmployeeID**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**Faxnummer**](iadsuser-property-methods.md)              | Unterstützt     | Nicht unterstützt   |
| [**FirstName**](iadsuser-property-methods.md)              | Unterstützt     | Nicht unterstützt   |
| [**FullName**](iadsuser-property-methods.md)               | Unterstützt     | Unterstützt     |
| [**Graceloginsallowed**](iadsuser-property-methods.md)     | Nicht unterstützt | Nicht unterstützt   |
| [**Graceloginsrestdauer**](iadsuser-property-methods.md)   | Nicht unterstützt | Nicht unterstützt   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Unterstützt     | Unterstützt     |
| [**Seite**](iadsuser-property-methods.md)               | Unterstützt     | Nicht unterstützt   |
| [**Isaccountlocked**](iadsuser-property-methods.md)        | Unterstützt     | Unterstützt     |
| [**Sprachen**](iadsuser-property-methods.md)              | Nicht unterstützt | Nicht unterstützt   |
| [**Lastfailedlogin**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**LastLogin**](iadsuser-property-methods.md)              | Unterstützt     | Unterstützt     |
| [**Lastlogoff**](iadsuser-property-methods.md)             | Unterstützt     | Unterstützt     |
| [**LastName**](iadsuser-property-methods.md)               | Unterstützt     | Nicht unterstützt   |
| [**Loginhours**](iadsuser-property-methods.md)             | Unterstützt     | Unterstützt     |
| [**Loginscript**](iadsuser-property-methods.md)            | Unterstützt     | Unterstützt     |
| [**Loginworkstations**](iadsuser-property-methods.md)      | Unterstützt     | Unterstützt     |
| [**Dienst**](iadsuser-property-methods.md)                | Unterstützt     | Nicht unterstützt   |
| [**Maxlogins**](iadsuser-property-methods.md)              | Nicht unterstützt   | Nicht unterstützt   |
| [**Maxstorage**](iadsuser-property-methods.md)             | Unterstützt     | Unterstützt     |
| [**NamePrefix Name**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**Wird**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**Officelocations**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**OtherName**](iadsuser-property-methods.md)              | Unterstützt     | Nicht unterstützt   |
| [**Passwordexpirationdate**](iadsuser-property-methods.md) | Nicht unterstützt   | Unterstützt     |
| [**Passwordlastchanged**](iadsuser-property-methods.md)    | Unterstützt     | Nicht unterstützt   |
| [**Passwordminimumlength**](iadsuser-property-methods.md)  | Nicht unterstützt   | Unterstützt     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | Unterstützt     | Unterstützt     |
| [**Picture**](iadsuser-property-methods.md)                | Unterstützt     | Nicht unterstützt   |
| [**Postaladressen**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**Postalcodes**](iadsuser-property-methods.md)            | Unterstützt     | Nicht unterstützt   |
| [**Profil**](iadsuser-property-methods.md)                | Unterstützt     | Unterstützt     |
| [**Requirements-Wort**](iadsuser-property-methods.md)  | Nicht unterstützt   | Nicht unterstützt   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Unterstützt     | Nicht unterstützt   |
| [**Telefoniehome**](iadsuser-property-methods.md)          | Unterstützt     | Nicht unterstützt   |
| [**Telefoniemobile**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**Telefoniepager**](iadsuser-property-methods.md)         | Unterstützt     | Nicht unterstützt   |
| [**Titel**](iadsuser-property-methods.md)                  | Unterstützt     | Nicht unterstützt   |



 

## <a name="provider-support-for-iadscomputer"></a>Anbieter Unterstützung für iadscomputer



| Eigenschaften                                     | LDAP                    | WinNT       |
|------------------------------------------------|-------------------------|-------------|
| [**Computer-ID**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Klinik**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Division**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Schnittstelle nicht unterstützt | Unterstützt   |
| [**Hotels**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Modell**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Netzwerkadressen**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**OperatingSystem**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Schnittstelle nicht unterstützt | Unterstützt   |
| [**OperatingSystemVersion**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Schnittstelle nicht unterstützt | Unterstützt   |
| [**Besitzer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Schnittstelle nicht unterstützt | Unterstützt   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Prozessor**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Schnittstelle nicht unterstützt | Unterstützt   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Schnittstelle nicht unterstützt | Unterstützt   |
| [**Funktion**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Website**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**Storagecapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Schnittstelle nicht unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Anbieter Unterstützung für iadscomputeroperations



| Eigenschaft                                   | LDAP                    | WinNT           |
|--------------------------------------------|-------------------------|-----------------|
| [**Abschlusses**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | Schnittstelle nicht unterstützt | Nicht implementiert |
| [**Status**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | Schnittstelle nicht unterstützt | Nicht implementiert |



 

## <a name="provider-support-for-iadsdomain"></a>Anbieter Unterstützung für iadsdomain



| Eigenschaft                                         | LDAP                    | WinNT           |
|--------------------------------------------------|-------------------------|-----------------|
| [**Isworkgroup**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | Schnittstelle nicht unterstützt | Nicht implementiert |
| [**Minpasswordlength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | Schnittstelle nicht unterstützt | Unterstützt       |
| [**Minpasswordage**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Schnittstelle nicht unterstützt | Unterstützt       |
| [**Maxpasswordage**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Schnittstelle nicht unterstützt | Unterstützt       |
| [**Maxbadpasswordsallowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | Schnittstelle nicht unterstützt | Unterstützt       |
| [**PasswordHistoryLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | Schnittstelle nicht unterstützt | Unterstützt       |
| [**Passwordattributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Schnittstelle nicht unterstützt | Nicht unterstützt     |
| [**Autounlockinterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Schnittstelle nicht unterstützt | Unterstützt       |
| [**Lockoutobservationinterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | Schnittstelle nicht unterstützt | Unterstützt       |



 

## <a name="provider-support-for-iadsfileservice"></a>Anbieter Unterstützung für iadsfileservice



| Eigenschaft                                | LDAP                    | WinNT     |
|-----------------------------------------|-------------------------|-----------|
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | Schnittstelle nicht unterstützt | Unterstützt |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | Schnittstelle nicht unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadsgroup"></a>Anbieter Unterstützung für IADsGroup



| Eigenschaft                         | LDAP      | WinNT     |
|----------------------------------|-----------|-----------|
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadsclass"></a>Anbieter Unterstützung für iadsclass



| Eigenschaft                                   | LDAP               | WinNT           |
|--------------------------------------------|--------------------|-----------------|
| [**Primaryinterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Unterstützt          | Unterstützt       |
| [**CLSID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Unterstützt          | Unterstützt       |
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Unterstützt          | Unterstützt       |
| [**Kter**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Unterstützt          | Unterstützt       |
| [**Sten**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Unterstützt          | Unterstützt       |
| [**MandatoryProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Unterstützt          | Unterstützt       |
| [**OptionalProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Unterstützt          | Unterstützt       |
| [**Namingproperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Unterstützt          | Nicht implementiert |
| [**Derivedfrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Unterstützt          | Nicht unterstützt     |
| [**"Auxderivedfrom"**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Unterstützt          | Nicht unterstützt     |
| [**Possiblevorgesetzten**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Unterstützt          | Unterstützt       |
| [**Containment**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Unterstützt für Lesevorgänge | Unterstützt       |
| [**Container**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Unterstützt für Lesevorgänge | Unterstützt       |
| [**Helpfilename**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Unterstützt          | Unterstützt       |
| [**Helpfilecontext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Unterstützt          | Unterstützt       |
| Methode                                     | LDAP               | WinNT           |
| [**Qualifikation**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | Nicht implementiert    | Nicht implementiert |



 

## <a name="provider-support-for-iadsproperty"></a>Anbieter Unterstützung für iadsproperty



| Eigenschaft                            | LDAP      | WinNT     |
|-------------------------------------|-----------|-----------|
| [**OID**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Unterstützt | Unterstützt |
| [**Syntax**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Unterstützt | Unterstützt |
| [**Maxrange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Unterstützt | Unterstützt |
| [**Minrange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Unterstützt | Unterstützt |
| [**Mehrwertigen**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadssyntax"></a>Anbieter Unterstützung für iadssyntax



| Eigenschaft                              | LDAP      | WinNT     |
|---------------------------------------|-----------|-----------|
| [**Oleautodatatype**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadscontainer"></a>Anbieter Unterstützung für IADsContainer



| Eigenschaft                        | LDAP            | WinNT           |
|---------------------------------|-----------------|-----------------|
| [**Countdown**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Nicht implementiert | Nicht implementiert |
| [**Hinweise**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Unterstützt       | Nicht implementiert |
| [**Filter**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Unterstützt       | Unterstützt       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Anbieter Unterstützung für iadsnamespaces



| Eigenschaft                                   | LDAP      | WinNT     |
|--------------------------------------------|-----------|-----------|
| [**defaultcontainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Anbieter Unterstützung für IADsAccessControlEntry



| Eigenschaft                                              | LDAP      | WinNT       |
|-------------------------------------------------------|-----------|-------------|
| [**AccessMask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Unterstützt | Nicht unterstützt |
| [**Access Type**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Unterstützt | Nicht unterstützt |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Unterstützt | Nicht unterstützt |
| [**Fahren**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Unterstützt | Nicht unterstützt |
| [**ObjektType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Unterstützt | Nicht unterstützt |
| [**Ereritedobjecttype**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Unterstützt | Nicht unterstützt |
| [**Stiftungs**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Anbieter Unterstützung für IADsAccessControlList



| Eigenschaft                                                       | LDAP      | WinNT       |
|----------------------------------------------------------------|-----------|-------------|
| [**Acecount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Unterstützt | Nicht unterstützt |
| [**Acerevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Unterstützt | Nicht unterstützt |
| Methode                                                         | LDAP      | WinNT       |
| [**Addace**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Unterstützt | Nicht unterstützt |
| [**Copyaccesslist**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Unterstützt | Nicht unterstützt |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Unterstützt | Nicht unterstützt |
| [**" \_ \_ netwenum"**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Anbieter Unterstützung für IADsSecurityDescriptor



| Eigenschaft                                                                        | LDAP      | WinNT       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Control**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Unterstützt | Nicht unterstützt |
| [**Dacldefdefault**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Unterstützt | Nicht unterstützt |
| [**Diskretionaryacl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Unterstützt | Nicht unterstützt |
| [**Gruppe**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Unterstützt | Nicht unterstützt |
| [**Gruppen Standard**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Unterstützt | Nicht unterstützt |
| [**Besitzer**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Unterstützt | Nicht unterstützt |
| [**Besitzer Standard**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Unterstützt | Nicht unterstützt |
| [**Sacldefault**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Unterstützt | Nicht unterstützt |
| [**SystemAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Unterstützt | Nicht unterstützt |
| Methode                                                                          | LDAP      | WinNT       |
| [**Copysecuritydescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Anbieter Unterstützung für iadsobjectoptions



| Methode                                           | LDAP      | WinNT                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Unterstützt | Schnittstelle nicht unterstützt |
| [**SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Unterstützt | Schnittstelle nicht unterstützt |



 

## <a name="provider-support-for-iadscollection"></a>Anbieter Unterstützung für iadscollection



| Methode                                                | LDAP                    | WinNT       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Hinzufügen**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Schnittstelle nicht unterstützt | Nicht unterstützt |
| [**" \_ \_ netwenum"**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Schnittstelle nicht unterstützt | Unterstützt   |
| [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Schnittstelle nicht unterstützt | Unterstützt   |
| [**Aufgeh**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Schnittstelle nicht unterstützt | Unterstützt   |



 

## <a name="provider-support-for-iadsmembers"></a>Anbieter Unterstützung für iadsmembers



| Eigenschaft                                           | LDAP                                                      | WinNT       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Countdown**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Wird für GroupCollection, aber nicht für UserCollection unterstützt. | Nicht unterstützt |
| [**Filter**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Unterstützt                                                 | Unterstützt   |
| Methode                                             | LDAP                                                      | WinNT       |
| [**" \_ \_ netwenum"**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Unterstützt                                                 | Unterstützt   |



 

## <a name="provider-support-for-iadspathname"></a>Anbieter Unterstützung für iadspathname



| Eigenschaft                                                    | LDAP      | WinNT       |
|-------------------------------------------------------------|-----------|-------------|
| [**Escapedmode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Unterstützt | Unterstützt   |
| Methode                                                      | LDAP      | WinNT       |
| [**Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Unterstützt | Unterstützt   |
| [**Setdisplaytype**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Unterstützt | Unterstützt   |
| [**Gerätehandle**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Unterstützt | Unterstützt   |
| [**Getnumelements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Unterstützt | Unterstützt   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Unterstützt | Unterstützt   |
| [**Getescapedelements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Unterstützt | Nicht unterstützt |
| [**Removeleafelement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Unterstützt | Unterstützt   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Unterstützt | Unterstützt   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Anbieter Unterstützung für iadsprintqueue



| Eigenschaft                                     | LDAP        | WinNT       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Unterstützt   | Nicht unterstützt |
| [**Modell**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Unterstützt   | Unterstützt.  |
| [**Datentyp**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Nicht unterstützt | Unterstützt   |
| [**PrintProcessor**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | Nicht unterstützt | Unterstützt   |
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Unterstützt   | Unterstützt   |
| [**Hotels**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Unterstützt   | Unterstützt   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Unterstützt   | Unterstützt   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Unterstützt   | Unterstützt   |
| [**Defaultjobpriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | Nicht unterstützt | Unterstützt   |
| [**Priorität**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Unterstützt   | Unterstützt   |
| [**Bannerpage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Unterstützt   | Unterstützt   |
| [**Printdevices**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Unterstützt   | Unterstützt   |
| [**Netzwerkadressen**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Nicht unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Anbieter Unterstützung für iadsprintqueueoperations



| Eigenschaft                                                | LDAP      | WinNT      |
|---------------------------------------------------------|-----------|------------|
| [**Status**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Unterstützt | Unterstützt  |
| Methode                                                  | LDAP      | WinNT      |
| [**Anhalten**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Unterstützt | Unterstützt. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Unterstützt | Unterstützt  |
| [**Bereinigen**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Unterstützt | Unterstützt  |
| [**Fortsetzen**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Unterstützt | Unterstützt  |



 

 

 




