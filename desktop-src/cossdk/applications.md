---
description: Enthält ein -Objekt für jede COM+-Anwendung, die auf dem lokalen Computer installiert ist. Die eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten alle Einstellungen, die auf Anwendungsebene vorgenommen wurden.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Applications-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 23ce8d7dc343e9cbca9aab642aee99424c5fffdde8ef0f15a52d2959bf492095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549424"
---
# <a name="applications-collection"></a>Applications-Sammlung

Enthält ein -Objekt für jede COM+-Anwendung, die auf dem lokalen Computer installiert ist. Die eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten alle Einstellungen, die auf Anwendungsebene vorgenommen wurden.

Sie legen Eigenschaften für Komponenten innerhalb einer Anwendung mithilfe der zugehörigen [**Components-Auflistung**](components.md) fest. Sie weisen einer Anwendung Rollen mithilfe der zugehörigen [**Rollensammlung**](roles.md) zu.

Um Komponenten in einer Anwendung zu installieren, verwenden Sie Methoden für das [**COMAdminCatalog-Objekt.**](comadmincatalog.md) Um eine Anwendung aus einer Datei zu installieren oder eine Anwendung herunterzufahren oder zu exportieren, verwenden Sie auch Methoden für das **COMAdminCatalog-Objekt.** Andernfalls können Sie der **Applications-Sammlung** ein Objekt hinzufügen, um eine neue Anwendung zu erstellen.

Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **Applications-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Komponenten**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Rollen**](roles.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Partitionen**](partitions.md)
-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Aktivierung](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [Applicationdirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [Authentifizierung](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Änderbar](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Löschbar](#deleteable)
-   [Beschreibung](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [ID](#applications-collection)
-   [Identität](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [Name](#applicationproxyservername)
-   [Kennwort](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [Replizierbar](#replicable)
-   [RunForever](#runforever)
-   [Servicename](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendung 3 GB Arbeitsspeicher in ihrem Prozess verwenden kann. Wenn dies nicht aktiviert ist, kann die Anwendung nur 2 GB Arbeitsspeicher verwenden. |
| Zugriff         | ReadWrite                                                                                                                                     |
| Typ           | Bool                                                                                                                                          |
| Standard        | Falsch                                                                                                                                         |
| Mindestsystem | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob Zugriffsüberprüfungen nur auf Prozessebene oder sowohl auf Prozess- als auch auf Komponentenebene ausgeführt werden. Es wird empfohlen, die Konstanten in der Enumeration und nicht die numerischen Werte zu verwenden. |
| Zugriff         | ReadWrite                                                                                                                                                                                                       |
| Typ           | Lange mögliche Werte: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Standard        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Mindestsystem | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Aktivierung



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Die lokale Aktivierung gibt an, dass Objekte innerhalb der Anwendung innerhalb eines dedizierten lokalen Serverprozesses (Serveranwendung) ausgeführt werden. Die In-Process-Aktivierung gibt an, dass Objekte im Prozess ihres Erstellers (Bibliotheksanwendung) ausgeführt werden. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                           |
| Typ           | Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)                                                                                                                                                        |
| Standard        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob Zugriffsüberprüfungen für die Anwendung ausgeführt werden, wenn Clients aufruft. |
| Zugriff         | ReadWrite                                                                                          |
| Typ           | Bool                                                                                               |
| Standard        | Richtig                                                                                               |
| Mindestsystem | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>Applicationdirectory



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der vollständige Pfad zur Anwendung. Diese Informationen werden benötigt, wenn Sie SxS-Assemblys (Side-by-Side) konfigurieren. Mit SxS-Assemblys (Side-by-Side) können ASP-Anwendungen angeben, welche Version einer von SxS unterstützten System-DLL verwendet werden soll, z. B. MSVCRT, MSXML, COMCTL, GDIPLUS usw. Wenn Ihre ASP-Anwendung beispielsweise MSVCRT Version 2.0 verwendet, können Sie sicherstellen, dass Ihre Anwendung weiterhin MSVCRT Version 2.0 verwendet, auch nachdem Service Packs auf den Server angewendet wurden. Jede neue Version von MSVCRT wird weiterhin auf dem Computer installiert, version 2.0 bleibt jedoch bestehen und wird von Ihrer Anwendung verwendet. Von SxS unterstützte DLLs werden in %WINDIR% \\ WinSxS gespeichert. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Standard        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> In jedem Anwendungspool kann nur eine Version einer System-DLL verwendet werden, obwohl dieses Feature auf Anwendungsebene konfiguriert werden kann. Wenn die Anwendung App1 beispielsweise MSVCRT, Version 2.5 und die Anwendung App2 MSVCRT, Version 2.4, verwendet, sollten sich App1 und App2 nicht im selben Anwendungspool befinden. Wenn dies der Lage ist, wird die Version von MSVCRT für die zuerst geladene Anwendung geladen, und die andere Anwendung wird gezwungen, sie zu verwenden, bis die Anwendungen entladen werden.

 

Weitere Informationen finden Sie unter "Parallele Assemblys" unter [Änderungen in COM+-Diensten in IIS 6.0.](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90))

### <a name="applicationproxy"></a>ApplicationProxy



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendung ein Anwendungsproxy ist. |
| Zugriff         | ReadOnly                                                   |
| Typ           | Bool                                                       |
| Standard        | Falsch                                                      |
| Mindestsystem | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Ein Remoteservername, der beim Exportieren des Anwendungsproxys verwendet wird. Auf diesen Servernamen verweist der Anwendungsproxy, wenn er auf einem Clientcomputer installiert ist. |
| Zugriff         | ReadWrite                                                                                                                                                              |
| type           | String                                                                                                                                                                 |
| Standard        | ""                                                                                                                                                                     |
| Mindestsystem | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Eingabe | Wert |
|----------------|---------------------------------------------------|
| Beschreibung    | Eine GUID, die die Anwendungspartitions-ID darstellt. |
| Zugriff         | ReadOnly                                          |
| type           | String                                            |
| Standard        | <Generated>                                 |
| Mindestsystem | Windows Server 2003                               |



 

### <a name="authentication"></a>Authentifizierung



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt die Authentifizierungsebene für Aufrufe mit Werten fest, die den RPC-Authentifizierungseinstellungen (Remote Procedure Call) entsprechen. Wenn COMAdminAuthenticationDefault ausgewählt wird, wird die Einstellung in der DefaultAuthenticationLevel-Eigenschaft in der [**LocalComputer-Auflistung**](localcomputer.md) verwendet. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Typ           | Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)                                              |
| Standard        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Für Bibliotheksanwendungen (in Bearbeitung) sind comAdminAuthenticationDefault und COMAdminAuthenticationNone die einzigen gültigen Einstellungen. Es wird empfohlen, die Konstanten in der Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, welche Identität beim Identitätswechsel von Aufrufen dargestellt wird.                                                                                                                                                                      |
| Zugriff         | ReadWrite                                                                                                                                                                                                                               |
| Typ           | Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Standard        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Änderbar



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, ob Änderungen an den Anwendungseinstellungen oder deren Komponenten entweder programmgesteuert oder über das Verwaltungstool komponentendienste zulässig sind. |
| Zugriff         | ReadWrite                                                                                                                                                                     |
| Typ           | Bool                                                                                                                                                                          |
| Standard        | Richtig                                                                                                                                                                          |
| Mindestsystem | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine Befehlszeilenzeichenfolge für die Verwendung beim Debuggen. Die Anwendung kann in einem Debugger mit der angegebenen Befehlszeile gestartet werden. |
| Zugriff         | ReadWrite                                                                                                                  |
| type           | String                                                                                                                     |
| Standard        | ""                                                                                                                         |
| Mindestsystem | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Anzahl von Poolanwendungen an, die gleichzeitig ausgeführt werden können. |
| Zugriff         | ReadWrite                                                                        |
| Typ           | Long (1-1048576)                                                                 |
| Standard        | 1                                                                                |
| Mindestsystem | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Eingabe | Wert |
|----------------|---------------------------------------------------------------|
| Beschreibung    | Informationszeichenfolge, um zu beschreiben, wer die Anwendung erstellt hat. |
| Zugriff         | ReadWrite                                                     |
| type           | String                                                        |
| Standard        | ""                                                            |
| Mindestsystem | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Eingabe | Wert |
|----------------|------------------------------------------------------------------|
| Beschreibung    | Bestimmt, ob die ausgleichende Resource Manager aktiviert ist. |
| Zugriff         | ReadWrite                                                        |
| Typ           | Bool                                                             |
| Standard        | Falsch                                                            |
| Mindestsystem | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------|
| Beschreibung    | Name und Pfad der Datei zum Speichern des Protokolls für den kompensierenden Ressourcen-Manager (CRM). |
| Zugriff         | ReadWrite                                                                              |
| type           | String                                                                                 |
| Standard        | ""                                                                                     |
| Mindestsystem | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Deleteable



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt fest, ob die Anwendung entweder programmgesteuert oder über das Verwaltungstool komponentendienste gelöscht werden kann. |
| Zugriff         | ReadWrite                                                                                                                   |
| Typ           | Bool                                                                                                                        |
| Standard        | Richtig                                                                                                                        |
| Mindestsystem | Windows 2000                                                                                                                |



 

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|----------------------------|
| Beschreibung    | Beschreibt die Anwendung. |
| Zugriff         | ReadWrite                  |
| type           | String                     |
| Standard        | ""                         |
| Mindestsystem | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------|
| Beschreibung    | Aktiviert das Speicherabbild des Zustands einer COM+-Anwendung zum Zeitpunkt des Fehlers in einem bestimmten Verzeichnis. |
| Zugriff         | ReadWrite                                                                                             |
| Typ           | Bool                                                                                                  |
| Standard        | Falsch                                                                                                 |
| Mindestsystem | Windows XP                                                                                            |



 

> [!Note]  
> Ab Windows Server 2003 verfügen nur Administratoren über Lesezugriffsberechtigungen für die COM+-Dumpdateien.

 

### <a name="dumponexception"></a>DumpOnException



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Aktiviert das Speicherabbild des Zustands einer COM+-Anwendung, wenn die Anwendung eine nicht behandelte Ausnahme verursacht und von der COM+-Runtime beendet wird. |
| Zugriff         | ReadWrite                                                                                                                                     |
| Typ           | Bool                                                                                                                                          |
| Standard        | Falsch                                                                                                                                         |
| Mindestsystem | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------|
| Beschreibung    | Aktiviert das Speicherabbild des Zustands einer COM+-Anwendung, wenn die Anwendung fehlschlägt. |
| Zugriff         | ReadWrite                                                                       |
| Typ           | Bool                                                                            |
| Standard        | Falsch                                                                           |
| Mindestsystem | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Eingabe | Wert |
|----------------|--------------------------------------------------------------|
| Beschreibung    | Der Pfad des Verzeichnisses, in dem die Dumpdateien gespeichert werden. |
| Zugriff         | ReadWrite                                                    |
| type           | String                                                       |
| Standard        | "%systemroot% \\ system32 \\ com \\ dmp"                           |
| Mindestsystem | Windows XP                                                   |



 

> [!Note]  
> Ab Windows Server 2003 verfügen nur Administratoren über Lesezugriffsberechtigungen für die COM+-Dumpdateien.

 

### <a name="eventsenabled"></a>EventsEnabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------|
| Beschreibung    | Gibt an, ob Ereignisse für die Anwendung aktiviert sind. |
| Zugriff         | ReadWrite                                                 |
| Typ           | Bool                                                      |
| Standard        | Richtig                                                      |
| Mindestsystem | Windows 2000                                              |



 

### <a name="id"></a>ID



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine GUID, die die Anwendung darstellt. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                            |
| type           | String                                                                                                                                                               |
| Standard        | <Generated>                                                                                                                                                    |
| Mindestsystem | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identity



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt die Serverprozessidentität für die Anwendung fest. Geben Sie ein gültiges Benutzerkonto oder einen "interaktiven Benutzer" an, damit die Anwendung die Identität des aktuellen angemeldeten Benutzers an nimmt. Sie können auch die Zeichenfolgen "nt authority \\ localservice", "nt authority \\ networkservice" und "nt authority \\ system" angeben. Das Standardkennwort für diese drei Konten ist "" (leere Zeichenfolge). |
| Zugriff         |                                                                                                                                                                                                                                                                                                                                                                                    |
| type           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Standard        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

Die Identity-Eigenschaft ist für Bibliotheksanwendungen, die im Clientprozess ausgeführt werden, nicht aktiviert.

Die Password-Eigenschaft sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie Identity festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht mehr synchron sind, kann die Anwendung erst gestartet werden, wenn sie von einem Administrator zurückgesetzt werden.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt die Identitätswechselebene fest, die für Aufrufe an andere Anwendungen verwendet wird.                                                                                           |
| Zugriff         | ReadWrite                                                                                                                                                     |
| Typ           | Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Standard        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Mindestsystem | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>isEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Wenn die COM+-Anwendung oder -Komponente deaktiviert ist, ist IsEnabled false. Wenn die COM+-Anwendung oder -Komponente aktiviert ist, ist IsEnabled true. |
| Zugriff         | ReadWrite                                                                                                                                 |
| Typ           | Bool                                                                                                                                      |
| Standard        | Richtig                                                                                                                                      |
| Mindestsystem | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Eingabe | Wert |
|----------------|--------------------------------------|
| Beschreibung    | Identifiziert COM+-Systemanwendungen. |
| Zugriff         | ReadOnly                             |
| Typ           | Bool                                 |
| Standard        | Falsch                                |
| Mindestsystem | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Anzahl von Dateien an, die vor dem Überschreiben generiert werden sollen. |
| Zugriff         | ReadWrite                                                                        |
| Typ           | Long (1-200)                                                                     |
| Standard        | 5                                                                                |
| Mindestsystem | Windows XP                                                                       |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Namen der Anwendung. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                            |
| type           | String                                                                                                                                                                                                                               |
| Standard        | "Neue Anwendung"                                                                                                                                                                                                                    |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> Für Anwendungen sollten eindeutige Namen ausgewählt werden. Wenn mehrere Anwendungen mit demselben Namen erstellt werden, kann dies den Verweise auf die Anwendungen nach Namen beeinträchtigen, was zu unvorhersehbarem Verhalten führt.

 

### <a name="password"></a>Kennwort



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------|
| Beschreibung    | Legt das Kennwort fest, das vom Serverprozess für die Anmeldung unter der Identität verwendet wird. |
| Zugriff         | WriteOnly                                                                  |
| type           | String                                                                     |
| Standard        | ""                                                                         |
| Mindestsystem | Windows 2000                                                               |



 

Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie identity festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht mehr synchron sind, kann die Anwendung erst gestartet werden, wenn sie von einem Administrator zurückgesetzt werden.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, unter welchen Umständen Anforderungen in der Warteschlange an eine Anwendung authentifiziert werden.                                                 |
| Zugriff         | ReadWrite                                                                                                                               |
| Typ           | Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2) |
| Standard        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Mindestsystem | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Anzahl gleichzeitiger Listenerthreads an. Der gültige Bereich für diese Eigenschaft ist 0 bis 1000. Bei einer neu erstellten Anwendung wird die Einstellung von dem Algorithmus abgeleitet, der derzeit zum Bestimmen der Standardanzahl von Listenerthreads verwendet wird: das 16-fache der Anzahl von CPUs auf dem Server. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| Typ           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Standard        | 0                                                                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Diese Eigenschaft ist auch mit Lese-/Schreibfunktionen auf der Registerkarte **Queuing** des Verwaltungtools für Komponentendienste verfügbar.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob der Listener für komponenten in der Warteschlange für die Anwendung aktiviert ist. Wenn diese Option aktiviert ist, wird der Listener gestartet, wenn die Anwendung gestartet wird. Diese Eigenschaft wird nur wirksam, wenn QueuingEnabled auf True festgelegt ist. |
| Zugriff         | ReadWrite                                                                                                                                                                                                            |
| Typ           | Bool                                                                                                                                                                                                                 |
| Standard        | Falsch                                                                                                                                                                                                                |
| Mindestsystem | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob der COM+ Queued Components-Dienst für die Anwendung aktiviert ist. |
| Zugriff         | ReadWrite                                                                            |
| Typ           | Bool                                                                                 |
| Standard        | Falsch                                                                                |
| Mindestsystem | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Anzahl von Aktivierungen konfigurierter Objekte in der Anwendung an, die vor dem Wiederverwerten des Prozesses akzeptiert werden. Die Standardanzahl der Aktivierungen ist 0. |
| Zugriff         | ReadWrite                                                                                                                                                            |
| Typ           | Long (0-1048576)                                                                                                                                                     |
| Standard        | 0                                                                                                                                                                    |
| Mindestsystem | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Anzahl von Aufrufen an, mit denen konfigurierte Objekte in der Anwendung akzeptiert werden können, bevor der Prozess wiederverwertet wird. Die Standardanzahl der Aufrufe ist 0. |
| Zugriff         | ReadWrite                                                                                                                                                      |
| Typ           | Long (0-1048576)                                                                                                                                               |
| Standard        | 0                                                                                                                                                              |
| Mindestsystem | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, wie lange (in Minuten) ein wiederverwendeter Prozess ausgeführt werden kann, bevor er heruntergefahren wird. Der Countdown beginnt unmittelbar nach dem Recyceln des Prozesses. Das maximale Ablaufdatum beträgt 1.440 Minuten (24 Stunden), und der Standardwert beträgt 15 Minuten. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                        |
| Typ           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Standard        | 15                                                                                                                                                                                                                                                               |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Anzahl von Minuten an, die ein Prozess ausgeführt werden kann, bevor er wiederverwendet wird. Die maximale Lebensdauer beträgt 3.0240 Minuten (21 Tage), und der Standardwert ist 0 Minuten. |
| Zugriff         | ReadWrite                                                                                                                                                                   |
| Typ           | Long (0-30240)                                                                                                                                                              |
| Standard        | 0                                                                                                                                                                           |
| Mindestsystem | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die maximale Speicherauslastung (in Kilobyte) an, die ein Prozess vor der Wiederverwendung zulässig ist. Wenn die Arbeitsspeicherauslastung des Prozesses die angegebene Anzahl für einen längeren Zeitraum als eine Minute überschreitet, wird der Prozess wiederverwendet. Die Standardspeicherauslastung beträgt 0 KB. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                              |
| Typ           | Long (0-1048576)                                                                                                                                                                                                                                                       |
| Standard        | 0                                                                                                                                                                                                                                                                      |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replizierbar



| Eingabe | Wert |
|----------------|------------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendung repliziert werden kann. |
| Zugriff         | ReadWrite                                            |
| Typ           | Bool                                                 |
| Standard        | Richtig                                                 |
| Mindestsystem | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Aktiviert, dass ein Serverprozess fortgesetzt wird, wenn sich eine Anwendung im Leerlauf befindet. Wenn true festgelegt ist, wird der Serverprozess nicht heruntergefahren, wenn er im Leerlauf bleibt. Wenn false festgelegt ist, wird der Prozess entsprechend dem Wert heruntergefahren, der von der ShutdownAfter-Eigenschaft festgelegt wird. RunForever ist nicht für Bibliotheksanwendungen (in-process) aktiviert. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                |
| Typ           | Bool                                                                                                                                                                                                                                                                                                     |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                    |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>Dienstname



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Dienstname, der der Anwendung entspricht, die für die Ausführung als Dienstanwendung konfiguriert ist. Wenn dieser Wert **NULL** ist, ist die Anwendung nicht für die Ausführung als Dienst konfiguriert. Andernfalls können die Konfigurationsinformationen für den Dienst mithilfe des Dienstnamens gefunden werden. |
| Zugriff         | ReadOnly                                                                                                                                                                                                                                                                         |
| type           | String                                                                                                                                                                                                                                                                           |
| Standard        | ""                                                                                                                                                                                                                                                                               |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legt die Verzögerung fest, bevor ein Serverprozess heruntergefahren wird, nachdem er sich im Leerlauf befindet. Die Wartezeit beim Herunterfahren liegt zwischen 0 und 1440 Minuten (24 Stunden). Wenn RunForever auf True festgelegt ist, wird diese Eigenschaft ignoriert. ShutdownAfter ist für Bibliotheksanwendungen (in Bearbeitung) nicht aktiviert. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                          |
| Typ           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Standard        | 3                                                                                                                                                                                                                                                                  |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob diese Anwendung für die Verwendung über das SOAP-Protokoll verfügbar gemacht wird. |
| Zugriff         | ReadWrite                                                                            |
| Typ           | Bool                                                                                 |
| Standard        | Falsch                                                                                |
| Mindestsystem | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------|
| Beschreibung    | Der URL-Endpunkt, an dem diese Anwendung über das SOAP-Protokoll verfügbar gemacht wird. |
| Zugriff         | ReadWrite                                                                    |
| type           | String                                                                       |
| Standard        | ""                                                                           |
| Mindestsystem | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------|
| Beschreibung    | Die E-Mail-Adresse, unter der diese Anwendung über das SOAP-Protokoll verfügbar gemacht wird. |
| Zugriff         | ReadWrite                                                                     |
| type           | String                                                                        |
| Standard        | ""                                                                            |
| Mindestsystem | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Das virtuelle IIS-Stammverzeichnis, in dem sich die Zugriffsskripts befinden, die die Anwendung über das SOAP-Protokoll verfügbar machen. |
| Zugriff         | ReadWrite                                                                                                            |
| type           | String                                                                                                               |
| Standard        | ""                                                                                                                   |
| Mindestsystem | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt die Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) für die Anwendung. Wenn true festgelegt ist, wird die SRPTrustLevel-Eigenschaft für die Anwendung verwendet. Wenn diese Einstellung auf FALSE festgelegt ist, werden die Richtlinien für Softwareeinschränkungen aus den lokalen Sicherheitseinstellungen verwendet. Die lokalen Sicherheitseinstellungen werden über das Snap-In Lokale Sicherheitsrichtlinie des Microsoft Management Console gesteuert. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| Typ           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                                 |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt die Vertrauensebene der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) der Anwendung an. Diese Eigenschaft wird nur verwendet, wenn die SRPEnabled-Eigenschaft auf True festgelegt ist. Die SRP-Vertrauensebene bezieht sich auf die Vertrauensebene, die Sie einer Anwendung erteilen möchten. Eine uneingeschränkte SRP-Vertrauensebene entspricht dem SAFER \_ LEVELID \_ FULLYTRUSTED-Enumerationswert, während eine Nicht zugelassene SRP-Vertrauensebene dem SAFER \_ LEVELID \_ DISALLOWED-Enumerationswert entspricht. Die Enumeration für die Vertrauensebenen wird in Winsafer.h definiert. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Typ           | Lange mögliche Werte:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Standard        | SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

An eine Anwendung, der Sie mit uneingeschränktem Zugriff vertrauen möchten, sollte die strengste Sicherheit angefügt sein. Anwendungen, die unrestricted sind, können nur uneingeschränkte Komponenten laden, während Unzulässige Anwendungen nicht ausgeführt werden dürfen und daher keine Komponenten laden können.

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
