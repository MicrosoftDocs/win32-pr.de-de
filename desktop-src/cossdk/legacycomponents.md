---
description: Enthält ein -Objekt für jede nicht konfigurierte Komponente in der Applications-Auflistung. Nicht konfigurierte Komponenten können com+-Dienste nicht verwenden. Die eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten Einstellungen, die auf Komponentenebene vorgenommen wurden.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: LegacyComponents-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0815c9124020ff08e7033f7d1f18f8d9c5b6736763d401a3564bbdd8c6ffdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120400"
---
# <a name="legacycomponents-collection"></a>LegacyComponents-Sammlung

Enthält ein -Objekt für jede nicht konfigurierte Komponente in der Applications-Auflistung. Nicht konfigurierte Komponenten können com+-Dienste nicht verwenden. Die eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten Einstellungen, die auf Komponentenebene vorgenommen wurden.

Diese Auflistung unterstützt die [**Remove-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts,**](comadmincatalogcollection.md) jedoch nicht die [**Add-Methode.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) Verwenden Sie zum Installieren oder Importieren von Komponenten in eine Anwendung Methoden für das [**COMAdminCatalog-Objekt.**](comadmincatalog.md)

## <a name="members"></a>Member

Die **LegacyComponents-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [AccessPermissions](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [Authenticationlevel](#authenticationlevel)
-   [Bitness](#bitness)
-   [Classname](#classname)
-   [Clsid](#clsid)
-   [DllSurrogate](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [Inprocserver32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [LaunchPermissions](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService](#localservice)
-   [Kennwort](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [RunAs](#runas)
-   [ServiceParameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>AccessPermissions



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------|
| Beschreibung    | Gibt die Benutzerkonten an, denen der Zugriff auf die Komponente gewährt oder verweigert wird. |
| Zugriff         | ReadWrite                                                                       |
| type           | String                                                                          |
| Standard        | Nicht zutreffend                                                                             |
| Mindestsystem | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| Eingabe | Wert |
|----------------|------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob der Server auf dem Datenspeichercomputer ausgeführt werden soll. |
| Zugriff         | ReadWrite                                                        |
| type           | Zeichenfolge Mögliche Werte:"N""Y"                                    |
| Standard        | "N"                                                              |
| Mindestsystem | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Eingabe | Wert |
|----------------|---------------------|
| Beschreibung    | Die Anwendungs-ID. |
| Zugriff         | ReadOnly            |
| type           | String              |
| Standard        | Nicht zutreffend                 |
| Mindestsystem | Windows XP          |



 

### <a name="appname"></a>AppName



| Eingabe | Wert |
|----------------|------------------------------|
| Beschreibung    | Der Namen der Anwendung. |
| Zugriff         | ReadOnly                     |
| type           | String                       |
| Standard        | Nicht zutreffend                          |
| Mindestsystem | Windows XP                   |



 

### <a name="authenticationlevel"></a>Authenticationlevel



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt die Authentifizierungsebene für Aufrufe mit Werten fest, die den RPC-Authentifizierungseinstellungen (Remote Procedure Call) entsprechen. Wenn COMAdminAuthenticationDefault ausgewählt wird, wird die Einstellung in der DefaultAuthenticationLevel-Eigenschaft in der [**LocalComputer-Sammlung**](localcomputer.md) verwendet. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                             |
| type           | Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)                                              |
| Standard        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                     |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Es wird empfohlen, die Konstanten in der Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="bitness"></a>Bitness



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Stellt den binären Bitzahltyp der Komponente dar. Auf Systemen, die 64-Bit-Windows, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten. |
| Zugriff         | ReadOnly                                                                                                                                                              |
| type           | Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)                                                                                         |
| Standard        | Nicht zutreffend                                                                                                                                                                   |
| Mindestsystem | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Eingabe | Wert |
|----------------|------------------------|
| Beschreibung    | Der Name der Klasse. |
| Zugriff         | ReadOnly               |
| type           | String                 |
| Standard        | Nicht zutreffend                    |
| Mindestsystem | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine GUID für die Komponente. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | Nicht zutreffend                                                                                                                                                       |
| Mindestsystem | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| Beschreibung    | Gibt den vollständigen Pfad zu einer Ersatzserveranwendung an. |
| Zugriff         | ReadWrite                                                  |
| type           | String                                                     |
| Standard        | Nicht zutreffend                                                        |
| Mindestsystem | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------|
| Beschreibung    | Gibt den vollständigen Pfad zu einer benutzerdefinierten 32-Bit-In-Process-Handler-DLL an. |
| Zugriff         | ReadWrite                                                          |
| type           | String                                                             |
| Standard        | Nicht zutreffend                                                                |
| Mindestsystem | Windows XP                                                         |



 

### <a name="inprocserver32"></a>Inprocserver32



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| Beschreibung    | Gibt den vollständigen Pfad zu einer 32-Bit-In-Process-Server-DLL an. |
| Zugriff         | ReadWrite                                                  |
| type           | String                                                     |
| Standard        | Nicht zutreffend                                                        |
| Mindestsystem | Windows XP                                                 |



 

### <a name="isenabled"></a>isEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Wenn die COM+-Anwendung oder -Komponente deaktiviert ist, ist IsEnabled false. Wenn die COM+-Anwendung oder -Komponente aktiviert ist, ist IsEnabled true. |
| Zugriff         | ReadWrite                                                                                                                                 |
| type           | Bool                                                                                                                                      |
| Standard        | Richtig                                                                                                                                      |
| Mindestsystem | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------|
| Beschreibung    | Gibt Benutzerkonten an, denen die Berechtigung zum Starten dieser Komponente gewährt oder verweigert wird. |
| Zugriff         | ReadWrite                                                                              |
| type           | String                                                                                 |
| Standard        | Nicht zutreffend                                                                                    |
| Mindestsystem | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an. Verwenden Sie zum Schutz der Systemsicherheit Zeichenfolgen in Anführungszeichen im Pfad, um anzugeben, wo der name der ausführbaren Datei endet und die Argumente beginnen. Beispiel: \\ "C: \\ Programme \\ Company Files \\Application.exe\\ " param1 param2". |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                                                                                                      |
| Standard        | Nicht zutreffend                                                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService



| Eingabe | Wert |
|----------------|-----------------------------------------------------|
| Beschreibung    | Gibt den vollständigen Pfad zur Dienstanwendung an. |
| Zugriff         | ReadWrite                                           |
| type           | String                                              |
| Standard        | Nicht zutreffend                                                 |
| Mindestsystem | Windows XP                                          |



 

### <a name="password"></a>Kennwort



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt das Kennwort fest, das vom Serverprozess für die Anmeldung unter der angegebenen RunAs-Identität verwendet wird. Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die RunAs-Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht mehr synchron sind, kann die Komponente erst gestartet werden, wenn sie von einem Administrator zurückgesetzt wurden. |
| Zugriff         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Standard        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Ein Name, der die Komponente identifiziert. Diese Eigenschaft wird zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                             |
| type           | String                                                                                                                               |
| Standard        | Nicht zutreffend                                                                                                                                  |
| Mindestsystem | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Eingabe | Wert |
|----------------|---------------------------------------|
| Beschreibung    | Gibt den Remoteservercomputer an. |
| Zugriff         | ReadWrite                             |
| type           | String                                |
| Standard        | Nicht zutreffend                                   |
| Mindestsystem | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt den Benutzer an, unter dessen Identität die Komponente ausgeführt wird. Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die RunAs-Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht mehr synchron sind, kann die Komponente erst gestartet werden, wenn sie von einem Administrator zurückgesetzt wurden. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Standard        | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                               |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die Parameter an, die an die Anwendung übergeben werden, wenn sie als Dienstanwendung aufgerufen wird. |
| Zugriff         | ReadWrite                                                                                 |
| type           | String                                                                                    |
| Standard        | Nicht zutreffend                                                                                       |
| Mindestsystem | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die Vertrauensebene der Komponente für die Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) an. Die SRP-Vertrauensebene bezieht sich auf die Vertrauensebene, die Sie einer Komponente zu geben bereit sind. Eine uneingeschränkte SRP-Vertrauensebene entspricht dem SAFER \_ LEVELID \_ FULLYTRUSTED-Enum-Wert, während eine Disallowed SRP-Vertrauensebene dem SAFER \_ LEVELID \_ DISALLOWED-Aufzählwert entspricht. Die Enumeration für die Vertrauensebenen wird in Winsafer.h definiert. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| type           | Long Possible values:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Standard        | SAFER \_ LEVELID \_ FULLYTRUSTED                                                                                                                                                                                                                                                                                                                                                                                                        |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Einer Komponente, der Sie mit uneingeschränktem Zugriff vertrauen möchten, sollte die strengste Sicherheit angefügt sein. Anwendungen, die uneingeschränkt sind, können nur uneingeschränkte Komponenten laden, während nicht zugelassene Anwendungen nicht ausgeführt werden dürfen und daher keine Komponenten laden können.

### <a name="threadingmodel"></a>ThreadingModel



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, wie Instanzen der Komponente Threads für die Methodenausführung zugewiesen werden. Werte entsprechen COM-Threadingmodellen.                                                  |
| Zugriff         | ReadOnly                                                                                                                                                                            |
| type           | Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4) |
| Standard        | Nicht zutreffend                                                                                                                                                                                 |
| Mindestsystem | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
