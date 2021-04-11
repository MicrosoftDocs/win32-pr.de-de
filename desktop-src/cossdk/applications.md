---
description: Enthält ein-Objekt für jede com+-Anwendung, die auf dem lokalen Computer installiert ist. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten alle Einstellungen auf Anwendungsebene.
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
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127172"
---
# <a name="applications-collection"></a>Applications-Sammlung

Enthält ein-Objekt für jede com+-Anwendung, die auf dem lokalen Computer installiert ist. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten alle Einstellungen auf Anwendungsebene.

Mithilfe der Auflistung verknüpfter [**Komponenten**](components.md) legen Sie Eigenschaften für Komponenten innerhalb einer Anwendung fest. Sie weisen einer Anwendung Rollen mithilfe der Auflistung verwandte [**Rollen**](roles.md) zu.

Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren. Wenn Sie eine Anwendung aus einer Datei installieren oder eine Anwendung Herunterfahren oder exportieren möchten, verwenden Sie auch Methoden für das **comadmincatalog** -Objekt. Andernfalls können Sie der **Anwendungs** Auflistung ein Objekt hinzufügen, um eine neue Anwendung zu erstellen.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **Anwendungs** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ApplicationInstance**](applicationinstances.md)
-   [**Komponenten**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**Legacycomponents**](legacycomponents.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Rollen**](roles.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Partitionen**](partitions.md)
-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [3gigsupportenabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Aktivierung](#recycleactivationlimit)
-   [Applicationaccesschecksenabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [Applicationproxy](#applicationproxyservername)
-   [Applicationproxyservername](#applicationproxyservername)
-   [Apppartitionid](#apppartitionid)
-   [Authentifizierung](#authenticationcapability)
-   [Authenticationcapability](#authenticationcapability)
-   [Austauschbar](#changeable)
-   [CommandLine](#commandline)
-   [Concurrentapps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [Crmenabled](#crmenabled)
-   [Crmlogfile](#crmlogfile)
-   [Gelöscht werden](#deleteable)
-   [Beschreibung](#description)
-   [Dumpfähig](#dumpenabled)
-   [Dumponexception](#dumponexception)
-   [Dumponfailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [ID](#applications-collection)
-   [Identität](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [Maxdumpcount](#maxdumpcount)
-   [Name](#applicationproxyservername)
-   [Kennwort](#password)
-   [Qcauthentikatemsgs](#qcauthenticatemsgs)
-   [QcListenerMaxThreads](#qclistenermaxthreads)
-   [Queuelisteneraktivierte](#queuelistenerenabled)
-   [Queuingenabled](#queuingenabled)
-   [Recycleactivationlimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [Recycleexpirationtimeout](#recycleexpirationtimeout)
-   [Recyclelifetimelimit](#recyclelifetimelimit)
-   [Recyclememorylimit](#recyclememorylimit)
-   [Replizierbare](#replicable)
-   [Runforever](#runforever)
-   [Service Name](#servicename)
-   [Shutdownafter](#shutdownafter)
-   [Soapaktivierte](#soapactivated)
-   [Soapbaseurl](#soapbaseurl)
-   [Soapmailto](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [Srpabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3gigsupportenabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendung im Prozess 3 GB Arbeitsspeicher verwenden kann. Wenn diese Option nicht aktiviert ist, kann die Anwendung nur 2 GB Arbeitsspeicher verwenden. |
| Access         | ReadWrite                                                                                                                                     |
| type           | Bool                                                                                                                                          |
| Standard        | Falsch                                                                                                                                         |
| Minimalsystem | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob Zugriffs Überprüfungen nur auf der Prozessebene oder auf Prozess-und Komponentenebene durchgeführt werden. Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden. |
| Access         | ReadWrite                                                                                                                                                                                                       |
| type           | Lange mögliche Werte: comadminaccesschecksapplicationlevel (0) comadminaccesschecksapplicationcomponentlevel (1)                                                                                                |
| Standard        | Comadminaccesschecksapplicationcomponentlevel (1)                                                                                                                                                               |
| Minimalsystem | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Aktivierung



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Lokale Aktivierung gibt an, dass Objekte innerhalb der Anwendung innerhalb eines dedizierten lokalen Server Prozesses (Serveranwendung) ausgeführt werden. Die Prozess interne Aktivierung gibt an, dass Objekte im Prozess des Erstellers (Bibliotheks Anwendung) ausgeführt werden. |
| Access         | ReadWrite                                                                                                                                                                                                                           |
| type           | Lange mögliche Werte: comadminactivationinproc (0) comadminactivationlocal (1)                                                                                                                                                        |
| Standard        | Comadminactivationlocal (1)                                                                                                                                                                                                         |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>Applicationaccesschecksenabled



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob Zugriffs Überprüfungen für die Anwendung ausgeführt werden, wenn Clients Aufrufe an die Anwendung durchführen. |
| Access         | ReadWrite                                                                                          |
| type           | Bool                                                                                               |
| Standard        | Richtig                                                                                               |
| Minimalsystem | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>ApplicationDirectory



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der vollständige Pfad zur Anwendung. Diese Informationen sind erforderlich, wenn Sie parallele Assemblys (SxS) konfigurieren. Parallele Assemblys (SxS) ermöglichen ASP-Anwendungen, anzugeben, welche Version einer SxS-unterstützten System-DLL verwendet werden soll, z. b. msvcrt, MSXML, COMCTL, gdiplus usw. Wenn Ihre ASP-Anwendung z. b. msvcrt Version 2,0 verwendet, können Sie sicherstellen, dass Ihre Anwendung weiterhin msvcrt Version 2,0 verwendet, auch nachdem Service Packs auf den Server angewendet wurden. Jede neue Version von msvcrt ist weiterhin auf dem Computer installiert, Version 2,0 bleibt jedoch erhalten und wird von Ihrer Anwendung verwendet. SxS-unterstützte DLLs werden in% windir% \\ WinSxS gespeichert. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Standard        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Nur eine Version einer System-DLL kann in einem Anwendungs Pool verwendet werden, auch wenn diese Funktion auf Anwendungsebene konfigurierbar ist. Wenn z. b. Application App1 msvcrt verwendet, Version 2,5 und Application App2 msvcrt, Version 2,4, verwendet wird, sollten App1 und App2 nicht im selben Anwendungs Pool sein. Wenn dies der Fall ist, wird die Version von msvcrt der Anwendung, die zuerst geladen wird, geladen, und die andere Anwendung wird gezwungen, Sie zu verwenden, bis die Anwendungen entladen werden.

 

Weitere Informationen finden Sie unter "parallele Assemblys" in [Änderungen in den COM+-Diensten in IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).

### <a name="applicationproxy"></a>Applicationproxy



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendung ein Anwendungs Proxy ist. |
| Access         | ReadOnly                                                   |
| type           | Bool                                                       |
| Standard        | Falsch                                                      |
| Minimalsystem | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>Applicationproxyservername



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Remote Servername, der beim Exportieren des Anwendungs Proxys verwendet wird. Dabei handelt es sich um den Servernamen, auf den der Anwendungs Proxy verweist, wenn er auf einem Client Computer installiert wird. |
| Access         | ReadWrite                                                                                                                                                              |
| type           | String                                                                                                                                                                 |
| Standard        | ""                                                                                                                                                                     |
| Minimalsystem | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>Apppartitionid



| Eingabe | Wert |
|----------------|---------------------------------------------------|
| BESCHREIBUNG    | Eine GUID, die die ID der Anwendungs Partition darstellt. |
| Access         | ReadOnly                                          |
| type           | String                                            |
| Standard        | <Generated>                                 |
| Minimalsystem | Windows Server 2003                               |



 

### <a name="authentication"></a>Authentifizierung



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt die Authentifizierungs Ebene für Aufrufe fest, wobei die Werte den RPC-Authentifizierungs Einstellungen (Remote Procedure Calls) entsprechen. Wenn comadminauthenticationdefault ausgewählt wird, wird die Einstellung in der DefaultAuthenticationLevel-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung verwendet. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| type           | Lange mögliche Werte: comadminauthenticationdefault (0) comadminauthenticationnone (1) comadminauthenticationconnect (2) comadminauthentication-Aufruf (3) comadminauthenticationpacket (4) comadminauthenticationintegrity (5) comadminauthenticationprivacy (6)                                              |
| Standard        | Comadminauthenticationpacket (4)                                                                                                                                                                                                                                                                      |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Für Bibliotheksanwendungen (in-Process) sind nur die folgenden gültigen Einstellungen für comadminauthenticationdefault und comadminauthenticationnone zulässig. Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="authenticationcapability"></a>Authenticationcapability



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, welche Identität bei Aufrufen von Aufrufen angezeigt wird.                                                                                                                                                                      |
| Access         | ReadWrite                                                                                                                                                                                                                               |
| type           | Lange mögliche Werte: comadminauthenticationcapabilitiesnone (0x0) comadminauthenticationcapabilitiessecurereferen(0x2) comadminauthenticationcapabilitiesstaticcloaking (0x20) comadminauthenticationcapabilitiesdynamiccloaking (0x40) |
| Standard        | Comadminauthenticationcapabilitiesdynamiccloaking (0x40)                                                                                                                                                                                |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Austauschbar



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob Änderungen an den Anwendungseinstellungen oder den zugehörigen Komponenten entweder Programm gesteuert oder über das Verwaltungs Tool "Komponenten Dienste" zulässig sind. |
| Access         | ReadWrite                                                                                                                                                                     |
| type           | Bool                                                                                                                                                                          |
| Standard        | Richtig                                                                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine Befehlszeilen Zeichenfolge für die Verwendung beim Debuggen. Die Anwendung kann in einem Debugger mit der angegebenen Befehlszeile gestartet werden. |
| Access         | ReadWrite                                                                                                                  |
| type           | String                                                                                                                     |
| Standard        | ""                                                                                                                         |
| Minimalsystem | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>Concurrentapps



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Anzahl von Pool fähigen Anwendungen an, die gleichzeitig ausgeführt werden können. |
| Access         | ReadWrite                                                                        |
| type           | Long (1-1048576)                                                                 |
| Standard        | 1                                                                                |
| Minimalsystem | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Eingabe | Wert |
|----------------|---------------------------------------------------------------|
| BESCHREIBUNG    | Informations Zeichenfolge, die beschreibt, wer die Anwendung erstellt hat. |
| Access         | ReadWrite                                                     |
| type           | String                                                        |
| Standard        | ""                                                            |
| Minimalsystem | Windows 2000                                                  |



 

### <a name="crmenabled"></a>Crmenabled



| Eingabe | Wert |
|----------------|------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob das kompensierende Ressourcen-Manager aktiviert ist. |
| Access         | ReadWrite                                                        |
| type           | Bool                                                             |
| Standard        | Falsch                                                            |
| Minimalsystem | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>Crmlogfile



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Name und Pfad der Datei, in der das Protokoll für den kompensierenden Ressourcen-Manager (CRM) aufbewahrt wird. |
| Access         | ReadWrite                                                                              |
| type           | String                                                                                 |
| Standard        | ""                                                                                     |
| Minimalsystem | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Gelöscht werden



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt fest, ob die Anwendung entweder Programm gesteuert oder über das Verwaltungs Tool Komponenten Dienste gelöscht werden kann. |
| Access         | ReadWrite                                                                                                                   |
| type           | Bool                                                                                                                        |
| Standard        | Richtig                                                                                                                        |
| Minimalsystem | Windows 2000                                                                                                                |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|----------------------------|
| BESCHREIBUNG    | Beschreibt die Anwendung. |
| Access         | ReadWrite                  |
| type           | String                     |
| Standard        | ""                         |
| Minimalsystem | Windows 2000               |



 

### <a name="dumpenabled"></a>Dumpfähig



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht das Sichern des Status einer COM+-Anwendung zum Zeitpunkt des Fehlers in einem bestimmten Verzeichnis. |
| Access         | ReadWrite                                                                                             |
| type           | Bool                                                                                                  |
| Standard        | Falsch                                                                                                 |
| Minimalsystem | Windows XP                                                                                            |



 

> [!Note]  
> Ab Windows Server 2003 verfügen nur Administratoren über Lese Zugriffsberechtigungen für die com+-Dumpdateien.

 

### <a name="dumponexception"></a>Dumponexception



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht das Sichern des Status einer COM+-Anwendung, wenn die Anwendung eine nicht behandelte Ausnahme verursacht und von der com+-Laufzeit beendet wird. |
| Access         | ReadWrite                                                                                                                                     |
| type           | Bool                                                                                                                                          |
| Standard        | Falsch                                                                                                                                         |
| Minimalsystem | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>Dumponfailfast



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht das Sichern des Zustands einer COM+-Anwendung, wenn die Anwendung fehlschlägt. |
| Access         | ReadWrite                                                                       |
| type           | Bool                                                                            |
| Standard        | Falsch                                                                           |
| Minimalsystem | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Eingabe | Wert |
|----------------|--------------------------------------------------------------|
| BESCHREIBUNG    | Der Pfad des Verzeichnisses, in dem die Dumpdateien gespeichert werden. |
| Access         | ReadWrite                                                    |
| type           | String                                                       |
| Standard        | "% SystemRoot% \\ system32 \\ com \\ DMP"                           |
| Minimalsystem | Windows XP                                                   |



 

> [!Note]  
> Ab Windows Server 2003 verfügen nur Administratoren über Lese Zugriffsberechtigungen für die com+-Dumpdateien.

 

### <a name="eventsenabled"></a>EventsEnabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob Ereignisse für die Anwendung aktiviert sind. |
| Access         | ReadWrite                                                 |
| type           | Bool                                                      |
| Standard        | Richtig                                                      |
| Minimalsystem | Windows 2000                                              |



 

### <a name="id"></a>id



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID, die die Anwendung darstellt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                            |
| type           | String                                                                                                                                                               |
| Standard        | <Generated>                                                                                                                                                    |
| Minimalsystem | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identity



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt die Server Prozess Identität für die Anwendung fest. Geben Sie ein gültiges Benutzerkonto oder einen interaktiven Benutzer an, damit die Anwendung die Identität des aktuell angemeldeten Benutzers annimmt. Sie können auch die Zeichen folgen "NT Authority \\ LocalService", "NT Authority \\ Network Service" und "NT Authority \\ System" angeben. Das Standard Kennwort für diese drei Konten ist "" (leere Zeichenfolge). |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| type           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Standard        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

Die Identity-Eigenschaft ist nicht für Bibliotheksanwendungen aktiviert, die im Client Prozess ausgeführt werden.

Die Password-Eigenschaft sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht synchron sind, kann die Anwendung erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt die Identitätswechsel Ebene fest, die für Aufrufe an andere Anwendungen verwendet wird.                                                                                           |
| Access         | ReadWrite                                                                                                                                                     |
| type           | Lange mögliche Werte: comadminimpersonationanonymous (1) comadminimpersonationidentifiout (2) comadminimpersonationidentität (3) comadminimpersonationdelegat (4) |
| Standard        | Comadminimpersonationimitation (3)                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>isEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Wenn die COM+-Anwendung oder-Komponente deaktiviert ist, ist isaktivierter Wert false. Wenn die COM+-Anwendung oder-Komponente aktiviert ist, ist isaktivierte "true". |
| Access         | ReadWrite                                                                                                                                 |
| type           | Bool                                                                                                                                      |
| Standard        | Richtig                                                                                                                                      |
| Minimalsystem | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Eingabe | Wert |
|----------------|--------------------------------------|
| BESCHREIBUNG    | Identifiziert com+-Systemanwendungen. |
| Access         | ReadOnly                             |
| type           | Bool                                 |
| Standard        | Falsch                                |
| Minimalsystem | Windows 2000                         |



 

### <a name="maxdumpcount"></a>Maxdumpcount



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Anzahl der Dateien an, die vor dem Überschreiben generiert werden sollen. |
| Access         | ReadWrite                                                                        |
| type           | Long (1-200)                                                                     |
| Standard        | 5                                                                                |
| Minimalsystem | Windows XP                                                                       |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Namen der Anwendung. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadWrite                                                                                                                                                                                                                            |
| type           | String                                                                                                                                                                                                                               |
| Standard        | "Neue Anwendung"                                                                                                                                                                                                                    |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> Eindeutige Namen sollten für Anwendungen ausgewählt werden. Wenn mehrere Anwendungen mit demselben Namen erstellt werden, kann das verweisen auf die Anwendungen nach Name beeinträchtigt werden, was zu unvorhersehbarem Verhalten führt.

 

### <a name="password"></a>Kennwort



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt das Kennwort fest, das vom Server Prozess verwendet wird, um sich unter der Identität anzumelden. |
| Access         | WriteOnly                                                                  |
| type           | String                                                                     |
| Standard        | ""                                                                         |
| Minimalsystem | Windows 2000                                                               |



 

Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden. Wenn das Kennwort und die Identität nicht synchron sind, kann die Anwendung erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden.

### <a name="qcauthenticatemsgs"></a>Qcauthentikatemsgs



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, unter welchen Umständen Anforderungen in der Warteschlange an eine Anwendung authentifiziert werden.                                                 |
| Access         | ReadWrite                                                                                                                               |
| type           | Lange mögliche Werte: comadminqcmessageauthenticatesecureapps (0) comadminqcmessageauthenticateoff (1) comadminqcmessageauthenticateon (2) |
| Standard        | Comadminqcmessageauthentipeesecureapps (0)                                                                                             |
| Minimalsystem | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QcListenerMaxThreads



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Anzahl gleichzeitiger Listenerthreads an. Der gültige Bereich für diese Eigenschaft ist 0 bis 1000. Bei einer neu erstellten Anwendung wird die Einstellung von dem Algorithmus abgeleitet, der derzeit zum Bestimmen der Standard Anzahl von Listenerthreads verwendet wird: das 16-fache der Anzahl der CPUs auf dem Server. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| type           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Standard        | 0                                                                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Diese Eigenschaft ist auch mit Lese-/Schreibzugriff auf der Registerkarte **Warteschlange** des Verwaltungs Programms Komponenten Dienste verfügbar.

 

### <a name="queuelistenerenabled"></a>Queuelisteneraktivierte



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob der in der Warteschlange befindliche Komponenten Listener für die Anwendung aktiviert ist. Wenn diese Option aktiviert ist, wird der Listener beim Starten der Anwendung gestartet. Diese Eigenschaft wird nur wirksam, wenn queuingenabled auf true festgelegt ist. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| type           | Bool                                                                                                                                                                                                                 |
| Standard        | Falsch                                                                                                                                                                                                                |
| Minimalsystem | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>Queuingenabled



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob der com+-Dienst in der Warteschlange für die Anwendung aktiviert ist. |
| Access         | ReadWrite                                                                            |
| type           | Bool                                                                                 |
| Standard        | Falsch                                                                                |
| Minimalsystem | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>Recycleactivationlimit



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Anzahl von Aktivierungen von konfigurierten Objekten in der Anwendung an, die vor der Wiederverwendung des Prozesses akzeptiert werden sollen. Die Standard Anzahl von Aktivierungen ist 0 (null). |
| Access         | ReadWrite                                                                                                                                                            |
| type           | Long (0-1048576)                                                                                                                                                     |
| Standard        | 0                                                                                                                                                                    |
| Minimalsystem | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Anzahl von Aufrufen an, mit der konfigurierte Objekte in der Anwendung akzeptiert werden können, bevor der Prozess wieder verwendet wird. Die Standard Anzahl von Aufrufen ist 0 (null). |
| Access         | ReadWrite                                                                                                                                                      |
| type           | Long (0-1048576)                                                                                                                                               |
| Standard        | 0                                                                                                                                                              |
| Minimalsystem | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>Recycleexpirationtimeout



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die Zeitspanne (in Minuten) an, mit der ein wieder Verwender Prozess vor dem Herunterfahren ausgeführt werden kann. Der Countdown beginnt sofort, nachdem der Prozess wieder verwendet wurde. Der maximale Ablauf Timeout beträgt 1440 Minuten (24 Stunden), und der Standardwert beträgt 15 Minuten. |
| Access         | ReadWrite                                                                                                                                                                                                                                                        |
| type           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Standard        | 15                                                                                                                                                                                                                                                               |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>Recyclelifetimelimit



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Anzahl von Minuten an, die ein Prozess vor der Wiederverwendung ausgeführt werden darf. Die maximale Lebensdauer Beschränkung beträgt 30240 Minuten (21 Tage), und der Standardwert beträgt 0 Minuten. |
| Access         | ReadWrite                                                                                                                                                                   |
| type           | Long (0-30240)                                                                                                                                                              |
| Standard        | 0                                                                                                                                                                           |
| Minimalsystem | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>Recyclememorylimit



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die maximale Menge an Arbeitsspeicher Auslastung (in Kilobytes) an, die ein Prozess vor der Wiederverwendung zulässt. Wenn die Prozess Speicherauslastung für einen Zeitraum von mehr als einer Minute die angegebene Anzahl überschreitet, wird der Prozess wieder verwendet. Der Standardwert für die Speicherauslastung beträgt 0 KB. |
| Access         | ReadWrite                                                                                                                                                                                                                                                              |
| type           | Long (0-1048576)                                                                                                                                                                                                                                                       |
| Standard        | 0                                                                                                                                                                                                                                                                      |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replizierbare



| Eingabe | Wert |
|----------------|------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendung repliziert werden kann. |
| Access         | ReadWrite                                            |
| type           | Bool                                                 |
| Standard        | Richtig                                                 |
| Minimalsystem | Windows XP                                           |



 

### <a name="runforever"></a>Runforever



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht, dass ein Server Prozess fortgesetzt wird, wenn sich eine Anwendung im Leerlauf befindet. Wenn dieser Wert auf true festgelegt ist, wird der Server Prozess nicht heruntergefahren, wenn er im Leerlauf ist. Wenn der Wert auf false festgelegt ist, wird der Prozess gemäß dem Wert heruntergefahren, der von der Eigenschaft shutdownafter festgelegt wurde. Runforever ist für Anwendungen (in-Process) nicht aktiviert. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                |
| type           | Bool                                                                                                                                                                                                                                                                                                     |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                    |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>Dienstname



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Dienst Name, der der Anwendung entspricht, die zum Ausführen als Dienst Anwendung konfiguriert ist. Wenn dieser Wert **null** ist, ist die Anwendung nicht für die Verwendung als Dienst konfiguriert. Andernfalls können die Konfigurationsinformationen für den Dienst mithilfe des Dienst namens gefunden werden. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| type           | String                                                                                                                                                                                                                                                                           |
| Standard        | ""                                                                                                                                                                                                                                                                               |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>Shutdownafter



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legt die Verzögerung fest, bevor ein Server Prozess heruntergefahren wird, nachdem er in den Leerlauf wechselt. Die Wartezeit für das Herunterfahren liegt zwischen 0 und 1440 Minuten (24 Stunden). Wenn runforever auf true festgelegt ist, wird diese Eigenschaft ignoriert. Shutdownafter ist nicht für die Bibliothek (in-Process)-Anwendungen aktiviert. |
| Access         | ReadWrite                                                                                                                                                                                                                                                          |
| type           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Standard        | 3                                                                                                                                                                                                                                                                  |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>Soapaktivierte



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob diese Anwendung für die Nutzung über das SOAP-Protokoll verfügbar gemacht wird. |
| Access         | ReadWrite                                                                            |
| type           | Bool                                                                                 |
| Standard        | Falsch                                                                                |
| Minimalsystem | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>Soapbaseurl



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der URL-Endpunkt, an dem diese Anwendung über das SOAP-Protokoll verfügbar gemacht wird. |
| Access         | ReadWrite                                                                    |
| type           | String                                                                       |
| Standard        | ""                                                                           |
| Minimalsystem | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>Soapmailto



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------|
| BESCHREIBUNG    | Die e-Mail-Adresse, an der diese Anwendung über das SOAP-Protokoll verfügbar gemacht wird. |
| Access         | ReadWrite                                                                     |
| type           | String                                                                        |
| Standard        | ""                                                                            |
| Minimalsystem | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Das virtuelle IIS-Stammverzeichnis, in dem sich die Zugriffs Skripts befinden, die die Anwendung über das SOAP-Protokoll verfügbar machen. |
| Access         | ReadWrite                                                                                                            |
| type           | String                                                                                                               |
| Standard        | ""                                                                                                                   |
| Minimalsystem | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>Srpabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt die Software Einschränkungs Richtlinie (Software Einschränkungs Richtlinie, SRP) für die Anwendung. Wenn diese Eigenschaft auf true festgelegt ist, wird die SRPTrustLevel-Eigenschaft für die Anwendung verwendet. Wenn false festgelegt ist, werden die Richtlinien für Software Einschränkung aus den lokalen Sicherheitseinstellungen verwendet. Die lokalen Sicherheitseinstellungen werden über das Snap-in "lokale Sicherheitsrichtlinie" der Microsoft Management Console gesteuert. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                                 |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) der Anwendung an. Diese Eigenschaft wird nur verwendet, wenn die srpabled-Eigenschaft auf true festgelegt ist. Die SRP-Vertrauens Ebene bezieht sich auf die Vertrauens Ebene, die Sie einer Anwendung bereitstellen möchten. Eine uneingeschränkte SRP-Vertrauens Ebene entspricht dem \_ fulllytrusted-Enumerationswert der sichereren levelid \_ , während eine unzulässige SRP-Vertrauens Ebene dem sichereren \_ levelid-Enumerationswert entspricht \_ . Die Enumeration für die Vertrauens Ebenen ist in winsafer. h definiert. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| type           | Lange mögliche Werte: sicherere \_ levelid nicht \_ zulässig (0x0) sicherere \_ levelid \_ fullytrusted (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Standard        | Sicherere \_ levelid \_ fullytrusted (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Einer Anwendung, die Sie mit uneingeschränktem Zugriff als vertrauenswürdig einstufen möchten, sollte die strengste Sicherheit angefügt werden. Anwendungen, die uneingeschränkt sind, können nur unbeschränkte Komponenten laden, während unzulässige Anwendungen nicht ausgeführt werden dürfen und somit keine Komponenten laden können.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
