---
description: Enthält ein-Objekt für jede nicht konfigurierte Komponente in der Anwendungs Auflistung. Nicht konfigurierte Komponenten können die com+-Dienste nicht verwenden. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, halten Einstellungen auf Komponentenebene.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Legacycomponents-Sammlung
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
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748176"
---
# <a name="legacycomponents-collection"></a>Legacycomponents-Sammlung

Enthält ein-Objekt für jede nicht konfigurierte Komponente in der Anwendungs Auflistung. Nicht konfigurierte Komponenten können die com+-Dienste nicht verwenden. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, halten Einstellungen auf Komponentenebene.

Diese Auflistung unterstützt die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, jedoch nicht die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode. Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren oder zu importieren.

## <a name="members"></a>Member

Die **legacycomponents** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [AccessPermissions](#accesspermissions)
-   [Activateatstorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [Bitness](#bitness)
-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [Dllersatz](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [InprocServer32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [Launchberechtigungen](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService](#localservice)
-   [Kennwort](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [RunAs](#runas)
-   [Service Parameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>AccessPermissions



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die Benutzerkonten an, denen der Zugriff auf die Komponente gestattet oder verweigert wird. |
| Access         | ReadWrite                                                                       |
| type           | String                                                                          |
| Standard        | –                                                                             |
| Minimalsystem | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>Activateatstorage



| Eingabe | Wert |
|----------------|------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob der Server auf dem Datenspeicher Computer ausgeführt werden soll. |
| Access         | ReadWrite                                                        |
| type           | Mögliche Zeichen folgen Werte: "N" "Y"                                    |
| Standard        | "N"                                                              |
| Minimalsystem | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Eingabe | Wert |
|----------------|---------------------|
| BESCHREIBUNG    | Die Anwendungs-ID. |
| Access         | ReadOnly            |
| type           | String              |
| Standard        | –                 |
| Minimalsystem | Windows XP          |



 

### <a name="appname"></a>AppName



| Eingabe | Wert |
|----------------|------------------------------|
| BESCHREIBUNG    | Der Namen der Anwendung. |
| Access         | ReadOnly                     |
| type           | String                       |
| Standard        | –                          |
| Minimalsystem | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt die Authentifizierungs Ebene für Aufrufe fest, wobei die Werte den RPC-Authentifizierungs Einstellungen (Remote Procedure Calls) entsprechen. Wenn comadminauthenticationdefault ausgewählt wird, wird die Einstellung in der DefaultAuthenticationLevel-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung verwendet. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| type           | Lange mögliche Werte: comadminauthenticationdefault (0) comadminauthenticationnone (1) comadminauthenticationconnect (2) comadminauthentication-Aufruf (3) comadminauthenticationpacket (4) comadminauthenticationintegrity (5) comadminauthenticationprivacy (6)                                              |
| Standard        | Comadminauthenticationdefault (0)                                                                                                                                                                                                                                                                     |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="bitness"></a>Bitness



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Stellt den binären bikretness-Typ der Komponente dar. Auf Systemen, die 64-Bit-Windows verwenden, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten. |
| Access         | ReadOnly                                                                                                                                                              |
| type           | Lange mögliche Werte: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                         |
| Standard        | –                                                                                                                                                                   |
| Minimalsystem | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Eingabe | Wert |
|----------------|------------------------|
| BESCHREIBUNG    | Der Name der Klasse. |
| Access         | ReadOnly               |
| type           | String                 |
| Standard        | –                    |
| Minimalsystem | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID für die Komponente. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | –                                                                                                                                                       |
| Minimalsystem | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>Dllersatz



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zu einer surragate-Serveranwendung an. |
| Access         | ReadWrite                                                  |
| type           | String                                                     |
| Standard        | –                                                        |
| Minimalsystem | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zu einer benutzerdefinierten benutzerdefinierten Handler-dll von 32 Bit an. |
| Access         | ReadWrite                                                          |
| type           | String                                                             |
| Standard        | –                                                                |
| Minimalsystem | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zu einer 32-Bit-Prozess internen Server-DLL an. |
| Access         | ReadWrite                                                  |
| type           | String                                                     |
| Standard        | –                                                        |
| Minimalsystem | Windows XP                                                 |



 

### <a name="isenabled"></a>isEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Wenn die COM+-Anwendung oder-Komponente deaktiviert ist, ist isaktivierter Wert false. Wenn die COM+-Anwendung oder-Komponente aktiviert ist, ist isaktivierte "true". |
| Access         | ReadWrite                                                                                                                                 |
| type           | Bool                                                                                                                                      |
| Standard        | Richtig                                                                                                                                      |
| Minimalsystem | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>Launchberechtigungen



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt Benutzerkonten an, denen die Berechtigung zum Starten dieser Komponente gestattet oder verweigert wird. |
| Access         | ReadWrite                                                                              |
| type           | String                                                                                 |
| Standard        | –                                                                                    |
| Minimalsystem | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an. Um die Systemsicherheit zu schützen, verwenden Sie Zeichen folgen in Anführungszeichen im Pfad, um anzugeben, wo der ausführbare Dateiname endet und die Argumente beginnen. Beispiel: " \\ C: \\ Program Files \\ Company Files \\Application.exe\\ " Param1 Param2 ". |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                                                                                                      |
| Standard        | –                                                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService



| Eingabe | Wert |
|----------------|-----------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zur Dienst Anwendung an. |
| Access         | ReadWrite                                           |
| type           | String                                              |
| Standard        | –                                                 |
| Minimalsystem | Windows XP                                          |



 

### <a name="password"></a>Kennwort



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt das Kennwort fest, das vom Server Prozess zum Anmelden unter der angegebenen runas-Identität verwendet wird. Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die runas-Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht synchron sind, kann die Komponente erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden. |
| Access         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Standard        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Name, der die Komponente identifiziert. Diese Eigenschaft wird zurückgegeben, wenn die Name-Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                             |
| type           | String                                                                                                                               |
| Standard        | –                                                                                                                                  |
| Minimalsystem | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Eingabe | Wert |
|----------------|---------------------------------------|
| BESCHREIBUNG    | Gibt den Remote Server Computer an. |
| Access         | ReadWrite                             |
| type           | String                                |
| Standard        | –                                   |
| Minimalsystem | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den Benutzer an, unter dessen Identität die Komponente ausgeführt wird. Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die runas-Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht synchron sind, kann die Komponente erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Standard        | –                                                                                                                                                                                                                                                                                                                                                                                               |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>Service Parameter



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die Parameter an, die an die Anwendung bei Aufruf als Dienst Anwendung übermittelt werden. |
| Access         | ReadWrite                                                                                 |
| type           | String                                                                                    |
| Standard        | –                                                                                       |
| Minimalsystem | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) der Komponente an. Die SRP-Vertrauens Ebene bezieht sich auf die Vertrauens Ebene, die Sie einer Komponente bereitstellen möchten. Eine uneingeschränkte SRP-Vertrauens Ebene entspricht dem \_ fulllytrusted-Enumerationswert der sichereren levelid \_ , während eine unzulässige SRP-Vertrauens Ebene dem sichereren \_ levelid-Enumerationswert entspricht \_ . Die Enumeration für die Vertrauens Ebenen ist in winsafer. h definiert. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| type           | Lange mögliche Werte: sicherere \_ levelid nicht \_ zulässig (0x0) sicherere \_ levelid \_ fullytrusted (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Standard        | sicherere \_ levelid \_ fullytrusted                                                                                                                                                                                                                                                                                                                                                                                                        |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Eine Komponente, der Sie den uneingeschränkten Zugriff als vertrauenswürdig einstufen möchten, sollte mit der strengsten Sicherheit verbunden sein. Anwendungen, die uneingeschränkt sind, können nur unbeschränkte Komponenten laden, während unzulässige Anwendungen nicht ausgeführt werden dürfen und somit keine Komponenten laden können.

### <a name="threadingmodel"></a>ThreadingModel



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, wie Instanzen der Komponente Threads zur Methoden Ausführung zugewiesen werden. Werte entsprechen com-Threading Modellen.                                                  |
| Access         | ReadOnly                                                                                                                                                                            |
| type           | Lange mögliche Werte: comadminthreadingmodelapartment (0) comadminthreadingmodelfree (1) comadminthreadingmodelmain (2) comadminthreadingmodelboth (3) comadminthreadingmodelneutral (4) |
| Standard        | –                                                                                                                                                                                 |
| Minimalsystem | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
