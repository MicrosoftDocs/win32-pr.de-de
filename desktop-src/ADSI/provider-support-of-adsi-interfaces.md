---
title: Anbieterunterstützung von ADSI-Schnittstellen
description: Die folgende Tabelle enthält eine kurze Beschreibung der Schnittstellen, die von den anbietern unterstützt werden, die in ADSI für Windows 2000 und DS-Client enthalten sind.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Anbieterunterstützung von ADSI-Schnittstellen ADSI
- ADSI ADSI , Dienstanbieter, Schnittstellen, die von den einzelnen Anbietern unterstützt werden
- Anbieterunterstützung für IADsUser
- Anbieterunterstützung für IADsComputer
- Anbieterunterstützung für IADsComputerOperations
- Anbieterunterstützung für IADsDomain
- Anbieterunterstützung für IADsFileService
- Anbieterunterstützung für IADsGroup
- Anbieterunterstützung für IADsClass
- Anbieterunterstützung für IADsProperty
- Anbieterunterstützung für IADsSyntax
- Anbieterunterstützung für IADsContainer
- Anbieterunterstützung für IADsNamespaces
- Anbieterunterstützung für IADsAccessControlEntry
- Anbieterunterstützung für IADsAccessControlList
- Anbieterunterstützung für IADsSecurityDescriptor
- Anbieterunterstützung für IADsObjectOptions
- Anbieterunterstützung für IADsCollection
- Anbieterunterstützung für IADsMembers
- Anbieterunterstützung für IADsPathname
- Anbieterunterstützung für IADsPrintQueue
- Anbieterunterstützung für IADsPrintQueueOperations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c393cb8476830617a300f33eac741bd27b3cacbd686442dd4def5bf6c35526e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178829"
---
# <a name="provider-support-of-adsi-interfaces"></a>Anbieterunterstützung von ADSI-Schnittstellen

Die folgende Tabelle enthält eine kurze Beschreibung der Schnittstellen, die von den anbietern unterstützt werden, die in ADSI für Windows 2000 und DS-Client enthalten sind. Ein mit "Ja" markierter Eintrag gibt an, dass mindestens ein ADSI-Objekt des angegebenen Anbieters die zugeordnete Schnittstelle unterstützt. "Nein" gibt an, dass kein Objekt des Anbieters die -Schnittstelle in dieser Version unterstützt. In Zukunft können derzeit nicht unterstützte Schnittstellen von den vom System bereitgestellten Anbietern unterstützt werden.

Weitere Informationen zu den spezifischen Implementierungsdetails des ADSI-Anbieters finden Sie unter:

-   [ADSI-LDAP-Anbieter](adsi-ldap-provider.md)
-   [ADSI WinNT-Anbieter](adsi-winnt-provider.md)
-   [ADSI-ROUTER](adsi-router.md)

Um weitere Informationen darüber zu erhalten, welche Eigenschaft oder Methode für jede Schnittstelle unterstützt wird, klicken Sie in der ersten Spalte der Tabelle auf den entsprechenden Schnittstellennamen.



| Schnittstellenname                                                 | LDAP | Winnt |
|----------------------------------------------------------------|------|-------|
| [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Ja  | Ja   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Ja  | Nein    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Ja  | Nein    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | Nein   | Nein    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | Nein   | Nein    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | Nein   | Nein    |
| [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Ja  | Ja   |
| [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | Nein   | Ja   |
| [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | Nein   | Ja   |
| [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | Nein   | Ja   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Ja  | Ja   |
| [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Ja  | Nein    |
| [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | Nein   | Ja   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | Nein   | Nein    |
| [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Ja  | Ja   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | Nein   | Nein    |
| [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | Nein   | Ja   |
| [**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | Nein   | Ja   |
| [**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | Nein   | Ja   |
| [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Ja  | Ja   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | Nein   | Nein    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Ja  | Nein    |
| [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Ja  | Nein    |
| [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Ja  | Ja   |
| [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Ja  | Ja   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | Nein   | Nein    |
| [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Ja  | Nein    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Ja  | Nein    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | Nein   | Nein    |
| [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Ja  | Ja   |
| [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Ja  | Nein    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | Nein   | Nein    |
| [**IADsPathName**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Ja  | Ja   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | Nein   | Nein    |
| [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | Nein   | Ja   |
| [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | Nein   | Ja   |
| [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Ja  | Ja   |
| [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Ja  | Ja   |
| [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Ja  | Ja   |
| [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Ja  | Ja   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Ja  | Ja   |
| [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Ja  | Ja   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Ja  | Ja   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | Nein   | Nein    |
| [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | Nein   | Ja   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Ja  | Nein    |
| [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | Nein   | Ja   |
| [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | Nein   | Ja   |
| [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | Nein   | Ja   |
| [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Ja  | Ja   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | Nein   | Nein    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | Nein   | Nein    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Ja  | Ja   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Ja  | Nein    |
| [**Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Ja  | Nein    |



 

## <a name="provider-support-for-iadsuser"></a>Anbieterunterstützung für IADsUser



| Eigenschaft                                                    | LDAP          | Winnt         |
|-------------------------------------------------------------|---------------|---------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | Unterstützt     | Unterstützt     |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | Unterstützt     | Unterstützt     |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Nicht unterstützt   | Nicht unterstützt |
| [**BadLoginCount**](iadsuser-property-methods.md)          | Unterstützt     | Unterstützt     |
| [**Department**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**Beschreibung**](iadsuser-property-methods.md)            | Unterstützt     | Unterstützt     |
| [**Division**](iadsuser-property-methods.md)               | Unterstützt     | Nicht unterstützt   |
| [**Emailaddress**](iadsuser-property-methods.md)           | Unterstützt     | Nicht unterstützt   |
| [**Employeeid**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**FaxNumber**](iadsuser-property-methods.md)              | Unterstützt     | Nicht unterstützt   |
| [**Firstname**](iadsuser-property-methods.md)              | Unterstützt     | Nicht unterstützt   |
| [**FullName**](iadsuser-property-methods.md)               | Unterstützt     | Unterstützt     |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Nicht unterstützt | Nicht unterstützt   |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Nicht unterstützt | Nicht unterstützt   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Unterstützt     | Unterstützt     |
| [**Homepage**](iadsuser-property-methods.md)               | Unterstützt     | Nicht unterstützt   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | Unterstützt     | Unterstützt     |
| [**Sprachen**](iadsuser-property-methods.md)              | Nicht unterstützt | Nicht unterstützt   |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**LastLogin**](iadsuser-property-methods.md)              | Unterstützt     | Unterstützt     |
| [**LastLogoff**](iadsuser-property-methods.md)             | Unterstützt     | Unterstützt     |
| [**Lastname**](iadsuser-property-methods.md)               | Unterstützt     | Nicht unterstützt   |
| [**LoginHours**](iadsuser-property-methods.md)             | Unterstützt     | Unterstützt     |
| [**LoginScript**](iadsuser-property-methods.md)            | Unterstützt     | Unterstützt     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | Unterstützt     | Unterstützt     |
| [**Manager**](iadsuser-property-methods.md)                | Unterstützt     | Nicht unterstützt   |
| [**MaxLogins**](iadsuser-property-methods.md)              | Nicht unterstützt   | Nicht unterstützt   |
| [**MaxStorage**](iadsuser-property-methods.md)             | Unterstützt     | Unterstützt     |
| [**NamePrefix**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**NameSuffix**](iadsuser-property-methods.md)             | Unterstützt     | Nicht unterstützt   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**OtherName**](iadsuser-property-methods.md)              | Unterstützt     | Nicht unterstützt   |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Nicht unterstützt   | Unterstützt     |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | Unterstützt     | Nicht unterstützt   |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Nicht unterstützt   | Unterstützt     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | Unterstützt     | Unterstützt     |
| [**Bild**](iadsuser-property-methods.md)                | Unterstützt     | Nicht unterstützt   |
| [**PostalAddresses**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**PostalCodes**](iadsuser-property-methods.md)            | Unterstützt     | Nicht unterstützt   |
| [**Profil**](iadsuser-property-methods.md)                | Unterstützt     | Unterstützt     |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Nicht unterstützt   | Nicht unterstützt   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Unterstützt     | Nicht unterstützt   |
| [**TelefonStart**](iadsuser-property-methods.md)          | Unterstützt     | Nicht unterstützt   |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Unterstützt     | Nicht unterstützt   |
| [**TelephonePager**](iadsuser-property-methods.md)         | Unterstützt     | Nicht unterstützt   |
| [**Titel**](iadsuser-property-methods.md)                  | Unterstützt     | Nicht unterstützt   |



 

## <a name="provider-support-for-iadscomputer"></a>Anbieterunterstützung für IADsComputer



| Eigenschaften                                     | LDAP                    | Winnt       |
|------------------------------------------------|-------------------------|-------------|
| [**ComputerID**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Department**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Division**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**Location**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Modell**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Operatingsystem**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**OperatingSystemVersion**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**Besitzer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Prozessor**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**Funktion**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**Website**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**StorageCapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Schnittstelle wird nicht unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Anbieterunterstützung für IADsComputerOperations



| Eigenschaft                                   | LDAP                    | Winnt           |
|--------------------------------------------|-------------------------|-----------------|
| [**Herunterfahren**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | Schnittstelle wird nicht unterstützt | Nicht implementiert |
| [**Status**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | Schnittstelle wird nicht unterstützt | Nicht implementiert |



 

## <a name="provider-support-for-iadsdomain"></a>Anbieterunterstützung für IADsDomain



| Eigenschaft                                         | LDAP                    | Winnt           |
|--------------------------------------------------|-------------------------|-----------------|
| [**IsWorkgroup**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | Schnittstelle wird nicht unterstützt | Nicht implementiert |
| [**MinPasswordLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | Schnittstelle wird nicht unterstützt | Unterstützt       |
| [**MinPasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Schnittstelle wird nicht unterstützt | Unterstützt       |
| [**MaxpasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Schnittstelle wird nicht unterstützt | Unterstützt       |
| [**MaxBadPasswordsAllowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | Schnittstelle wird nicht unterstützt | Unterstützt       |
| [**PasswordHistoryLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | Schnittstelle wird nicht unterstützt | Unterstützt       |
| [**PasswordAttributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Schnittstelle wird nicht unterstützt | Nicht unterstützt     |
| [**AutoUnlockInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Schnittstelle wird nicht unterstützt | Unterstützt       |
| [**LockoutObservationInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | Schnittstelle wird nicht unterstützt | Unterstützt       |



 

## <a name="provider-support-for-iadsfileservice"></a>Anbieterunterstützung für IADsFileService



| Eigenschaft                                | LDAP                    | Winnt     |
|-----------------------------------------|-------------------------|-----------|
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | Schnittstelle wird nicht unterstützt | Unterstützt |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | Schnittstelle wird nicht unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadsgroup"></a>Anbieterunterstützung für IADsGroup



| Eigenschaft                         | LDAP      | Winnt     |
|----------------------------------|-----------|-----------|
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadsclass"></a>Anbieterunterstützung für IADsClass



| Eigenschaft                                   | LDAP               | Winnt           |
|--------------------------------------------|--------------------|-----------------|
| [**PrimaryInterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Unterstützt          | Unterstützt       |
| [**Clsid**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Unterstützt          | Unterstützt       |
| [**Oid**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Unterstützt          | Unterstützt       |
| [**Abstrakt**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Unterstützt          | Unterstützt       |
| [**Hilfs**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Unterstützt          | Unterstützt       |
| [**MandatoryProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Unterstützt          | Unterstützt       |
| [**Optionale Eigenschaften**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Unterstützt          | Unterstützt       |
| [**NamingProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Unterstützt          | Nicht implementiert |
| [**DerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Unterstützt          | Nicht unterstützt     |
| [**AuxDerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Unterstützt          | Nicht unterstützt     |
| [**PossibleSuperiors**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Unterstützt          | Unterstützt       |
| [**Containment**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Für Lesedauer unterstützt | Unterstützt       |
| [**Container**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Für Lese-/Lese-Unterstützung unterstützt | Unterstützt       |
| [**HelpFileName**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Unterstützt          | Unterstützt       |
| [**HelpFileContext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Unterstützt          | Unterstützt       |
| Methode                                     | LDAP               | Winnt           |
| [**Qualifikation**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | Nicht implementiert    | Nicht implementiert |



 

## <a name="provider-support-for-iadsproperty"></a>Anbieterunterstützung für IADsProperty



| Eigenschaft                            | LDAP      | Winnt     |
|-------------------------------------|-----------|-----------|
| [**Oid**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Unterstützt | Unterstützt |
| [**Syntax**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Unterstützt | Unterstützt |
| [**MaxRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Unterstützt | Unterstützt |
| [**MinRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Unterstützt | Unterstützt |
| [**Mehrwertigen**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadssyntax"></a>Anbieterunterstützung für IADsSyntax



| Eigenschaft                              | LDAP      | Winnt     |
|---------------------------------------|-----------|-----------|
| [**OleAutoDataType**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadscontainer"></a>Anbieterunterstützung für IADsContainer



| Eigenschaft                        | LDAP            | Winnt           |
|---------------------------------|-----------------|-----------------|
| [**Count**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Nicht implementiert | Nicht implementiert |
| [**Hinweise**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Unterstützt       | Nicht implementiert |
| [**Filter**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Unterstützt       | Unterstützt       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Anbieterunterstützung für IADsNamespaces



| Eigenschaft                                   | LDAP      | Winnt     |
|--------------------------------------------|-----------|-----------|
| [**defaultContainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Unterstützt | Unterstützt |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Anbieterunterstützung für IADsAccessControlEntry



| Eigenschaft                                              | LDAP      | Winnt       |
|-------------------------------------------------------|-----------|-------------|
| [**Accessmask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Unterstützt | Nicht unterstützt |
| [**AccessType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Unterstützt | Nicht unterstützt |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Unterstützt | Nicht unterstützt |
| [**Flaggen**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Unterstützt | Nicht unterstützt |
| [**ObjektType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Unterstützt | Nicht unterstützt |
| [**Inheritedobjecttype**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Unterstützt | Nicht unterstützt |
| [**Treuhänder**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Anbieterunterstützung für IADsAccessControlList



| Eigenschaft                                                       | LDAP      | Winnt       |
|----------------------------------------------------------------|-----------|-------------|
| [**AceCount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Unterstützt | Nicht unterstützt |
| [**AceRevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Unterstützt | Nicht unterstützt |
| Methode                                                         | LDAP      | Winnt       |
| [**AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Unterstützt | Nicht unterstützt |
| [**CopyAccessList**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Unterstützt | Nicht unterstützt |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Unterstützt | Nicht unterstützt |
| [**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Anbieterunterstützung für IADsSecurityDescriptor



| Eigenschaft                                                                        | LDAP      | Winnt       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Control**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Unterstützt | Nicht unterstützt |
| [**DaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Unterstützt | Nicht unterstützt |
| [**Discretionaryacl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Unterstützt | Nicht unterstützt |
| [**Gruppe**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Unterstützt | Nicht unterstützt |
| [**GroupDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Unterstützt | Nicht unterstützt |
| [**Besitzer**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Unterstützt | Nicht unterstützt |
| [**OwnerDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Unterstützt | Nicht unterstützt |
| [**SaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Unterstützt | Nicht unterstützt |
| [**Systemacl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Unterstützt | Nicht unterstützt |
| Methode                                                                          | LDAP      | Winnt       |
| [**CopySecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Anbieterunterstützung für IADsObjectOptions



| Methode                                           | LDAP      | Winnt                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Unterstützt | Schnittstelle wird nicht unterstützt |
| [**Setoption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Unterstützt | Schnittstelle wird nicht unterstützt |



 

## <a name="provider-support-for-iadscollection"></a>Anbieterunterstützung für IADsCollection



| Methode                                                | LDAP                    | Winnt       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Add (Hinzufügen)**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Schnittstelle wird nicht unterstützt | Nicht unterstützt |
| [**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**Getobject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Schnittstelle wird nicht unterstützt | Unterstützt   |
| [**Entfernen**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Schnittstelle wird nicht unterstützt | Unterstützt   |



 

## <a name="provider-support-for-iadsmembers"></a>Anbieterunterstützung für IADsMembers



| Eigenschaft                                           | LDAP                                                      | Winnt       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Count**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Unterstützt für GroupCollection, aber nicht für UserCollection | Nicht unterstützt |
| [**Filter**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Unterstützt                                                 | Unterstützt   |
| Methode                                             | LDAP                                                      | Winnt       |
| [**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Unterstützt                                                 | Unterstützt   |



 

## <a name="provider-support-for-iadspathname"></a>Anbieterunterstützung für IADsPathname



| Eigenschaft                                                    | LDAP      | Winnt       |
|-------------------------------------------------------------|-----------|-------------|
| [**EscapedMode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Unterstützt | Unterstützt   |
| Methode                                                      | LDAP      | Winnt       |
| [**Festgelegt**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Unterstützt | Unterstützt   |
| [**SetDisplayType**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Unterstützt | Unterstützt   |
| [**Gerätehandle**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Unterstützt | Unterstützt   |
| [**GetNumElements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Unterstützt | Unterstützt   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Unterstützt | Unterstützt   |
| [**GetEscapedElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Unterstützt | Nicht unterstützt |
| [**RemoveLeafElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Unterstützt | Unterstützt   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Unterstützt | Unterstützt   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Anbieterunterstützung für IADsPrintQueue



| Eigenschaft                                     | LDAP        | Winnt       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Unterstützt   | Nicht unterstützt |
| [**Modell**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Unterstützt   | Unterstützt.  |
| [**Datatype**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Nicht unterstützt | Unterstützt   |
| [**Printprocessor**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | Nicht unterstützt | Unterstützt   |
| [**Beschreibung**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Unterstützt   | Unterstützt   |
| [**Location**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Unterstützt   | Unterstützt   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Unterstützt   | Unterstützt   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Unterstützt   | Unterstützt   |
| [**DefaultJobPriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | Nicht unterstützt | Unterstützt   |
| [**Priorität**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Unterstützt   | Unterstützt   |
| [**BannerPage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Unterstützt   | Unterstützt   |
| [**PrintDevices**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Unterstützt   | Unterstützt   |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Nicht unterstützt | Nicht unterstützt |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Anbieterunterstützung für IADsPrintQueueOperations



| Eigenschaft                                                | LDAP      | Winnt      |
|---------------------------------------------------------|-----------|------------|
| [**Status**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Unterstützt | Unterstützt  |
| Methode                                                  | LDAP      | Winnt      |
| [**Anhalten**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Unterstützt | Unterstützt. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Unterstützt | Unterstützt  |
| [**Bereinigen**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Unterstützt | Unterstützt  |
| [**Fortsetzen**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Unterstützt | Unterstützt  |



 

 

 




