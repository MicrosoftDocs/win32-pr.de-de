---
description: Enthält ein-Objekt für jede Komponente in der zugehörigen Anwendung.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Components-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524216"
---
# <a name="components-collection"></a>Components-Sammlung

Enthält ein-Objekt für jede Komponente in der zugehörigen Anwendung. Die **Komponenten** Sammlung bezieht sich immer auf ein Objekt in der [**Anwendungs**](applications.md) Auflistung. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, halten Einstellungen auf Komponentenebene.

Diese Auflistung unterstützt die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, jedoch nicht die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode. Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren oder zu importieren.

## <a name="members"></a>Member

Die **Components** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Interfakesforcomponent**](interfacesforcomponent.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Rolesforcomponent**](rolesforcomponent.md)
-   [**Abonnement forcomponent**](subscriptionsforcomponent.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   ["Zuweisung"](#allowinprocsubscribers)
-   [ApplicationId](#applicationid)
-   [Bitness](#bitness)
-   [CLSID](#multiinterfacepublisherfilterclsid)
-   [Componentaccesschecksenabled](#componentaccesschecksenabled)
-   [Componenttransaktiontimeout](#componenttransactiontimeoutenabled)
-   [Componenttransaktiontimeoutenabled](#componenttransactiontimeoutenabled)
-   [Comtiintrinsie](#comtiintrinsics)
-   [Konstruktionaktiviert](#constructionenabled)
-   [Constructor String](#constructorstring)
-   ["Kreationtimeout"](#creationtimeout)
-   [Beschreibung](#description)
-   [DLL](#dll)
-   [EventTrackingEnabled](#eventtrackingenabled)
-   [exceptionClass](#exceptionclass)
-   ["Freinparallel"](#fireinparallel)
-   [Iisintrinsics](#iisintrinsics)
-   [Initializeserverapplication](#initializeserverapplication)
-   [IsEnabled](#isenabled)
-   [Isiebziger Class](#iseventclass)
-   [IsInstalled](#isinstalled)
-   [Isprivatecomponent](#isprivatecomponent)
-   [JustInTimeActivation](#justintimeactivation)
-   [LoadBalancingSupported](#loadbalancingsupported)
-   [MaxPoolSize](#maxpoolsize)
-   [MinPoolSize](#minpoolsize)
-   [Multiinterfacepublisherfilterclsid](#multiinterfacepublisherfilterclsid)
-   [Mustrauuninclientcontext](#mustruninclientcontext)
-   [Mustranunindefehlercontext](#mustrunindefaultcontext)
-   [Objectpoolingenabled](#objectpoolingenabled)
-   [ProgID](#progid)
-   [PublisherID](#publisherid)
-   [Soapassemblyname](#soapassemblyname)
-   [Soaptyname](#soaptypename)
-   [Synchronisierung](#synchronization)
-   [ThreadingModel](#threadingmodel)
-   [Transaktion](#componenttransactiontimeout)
-   [Txisolationlevel](#txisolationlevel)
-   [VersionBuild](#versionbuild)
-   [VersionMajor](#versionmajor)
-   [VersionMinor](#versionminor)
-   [Versionsubbuild](#versionsubbuild)

### <a name="allowinprocsubscribers"></a>"Zuweisung"



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------|
| BESCHREIBUNG    | Aktiviert in Prozess Abonnenten, wenn die Komponente eine Ereignisklasse ist. |
| Access         | ReadWrite                                                          |
| type           | Bool                                                               |
| Standard        | Richtig                                                               |
| Minimalsystem | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Die GUID für die Anwendung, die die Komponente enthält. Muss eine gültige Anwendungs-GUID sein, die überprüft wird, bevor [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) aufgerufen wird. Wenn dieser Wert in eine GUID für eine andere Anwendung geändert wird, wechselt die Komponente in diese Anwendung. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                        |
| type           | String                                                                                                                                                                                                                                                                                           |
| Standard        | –                                                                                                                                                                                                                                                                                              |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>Bitness



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Stellt den binären bikretivität einer Komponente dar. Auf Systemen, die 64-Bit-Windows verwenden, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten. |
| Access         | ReadOnly                                                                                                                                                            |
| type           | Lange mögliche Werte: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                       |
| Standard        | –                                                                                                                                                                 |
| Minimalsystem | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID für die Komponente. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | –                                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>Componentaccesschecksenabled



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob rollenbasierte Zugriffs Überprüfungen bei Aufrufen der Komponente ausgeführt werden und in Verbindung mit den Eigenschaften AccessChecksLevel und applicationaccesschecksenabled der Anwendung funktionieren. |
| Access         | ReadWrite                                                                                                                                                                                                  |
| type           | Bool                                                                                                                                                                                                       |
| Standard        | Falsch                                                                                                                                                                                                      |
| Minimalsystem | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>Componenttransaktiontimeout



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt bei Verwendung in einer Transaktion den Zeitraum an, in dem diese Komponente zum Timeout der Transaktion veranlasst. Der Standardwert ist 60 Sekunden und darf nicht länger als 3600 Sekunden (1 Stunde) sein. Der Timeout Wert kann auf 0 festgelegt werden und einen unbegrenzten Transaktions Timeout Zeitraum angeben. Damit diese Eigenschaft verwendet werden kann, muss componenttransaktiontimeoutenabled den Wert "true" aufweisen. Der Wert dieser Eigenschaft überschreibt den globalen Transaktions Timeout, der durch die transaktiontimeout-Eigenschaft der [**LocalComputer**](localcomputer.md) -Auflistung angegeben wird. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| type           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Standard        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>Componenttransaktiontimeoutenabled



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob der Transaktions Timeout Zeitraum für diese Komponente aktiviert ist. Standardmäßig ist das Timeout Feature für Transaktionen deaktiviert. Wenn diese Eigenschaft auf true festgelegt ist, wird das von componenttransaktiontimeout angegebene Timeout verwendet. Wenn diese Eigenschaft auf false festgelegt ist, wird das von der transaktiontimeout-Eigenschaft der [**LocalComputer**](localcomputer.md) -Auflistung angegebene Timeout verwendet. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                      |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>Comtiintrinsie



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht das Übergeben von Kontexteigenschaften aus dem com Transaction Integrator (COMTI) in den Kontext für diese Klasse. Die COMTI vereinfacht die Aufgabe zum Umwickeln von Main Frame Transaktionen und Geschäftslogik als COM-Komponenten. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| type           | Bool                                                                                                                                                                                                                 |
| Standard        | Falsch                                                                                                                                                                                                                |
| Minimalsystem | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>Konstruktionaktiviert



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob der konstruktorstring beim Konstruieren an das-Objekt übergeben wird. |
| Access         | ReadWrite                                                                                |
| type           | Bool                                                                                     |
| Standard        | Falsch                                                                                    |
| Minimalsystem | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>Constructor String



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Initialisierungs Zeichenfolge für die Komponenten Konstruktion. Sie können unterschiedliche Objekte aus derselben generischen Komponente erstellen, indem Sie objektkonstruktorzeichenfolgen verwenden. Wenn constructionaktivierte den Wert false hat, wird diese Eigenschaft ignoriert. |
| Access         | ReadWrite                                                                                                                                                                                                          |
| type           | String                                                                                                                                                                                                             |
| Standard        | ""                                                                                                                                                                                                                 |
| Minimalsystem | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>"Kreationtimeout"



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Wenn das Objekt erstellt wird, wird die Anzahl von Millisekunden vor dem zurückgegebenen Timeout Fehler zurückgegeben. Das maximale Timeout beträgt 2147483647 Millisekunden (ungefähr 25 Tage). |
| Access         | ReadWrite                                                                                                                                              |
| type           | Long (0-2147483647)                                                                                                                                    |
| Standard        | 0                                                                                                                                                      |
| Minimalsystem | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|--------------------------|
| BESCHREIBUNG    | Beschreibt die Komponente. |
| Access         | ReadWrite                |
| type           | String                   |
| Standard        | ""                       |
| Minimalsystem | Windows 2000             |



 

### <a name="dll"></a>DLL



| Eingabe | Wert |
|----------------|---------------------------------------------------------|
| BESCHREIBUNG    | Der Name und der Pfad der Datei, die die Komponente enthält. |
| Access         | ReadOnly                                                |
| type           | String                                                  |
| Standard        | –                                                     |
| Minimalsystem | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob Ereignisse nachverfolgt werden. Zu den Ereignissen gehören Aktionen wie das Herunterfahren der Anwendung. Objekt Erstellung und-Freigabe; Objekt Verweise, Konsistenz, Aktivierung und decoaktivierung; Methodenaufrufe, Rückgaben und Ausnahmen; Starten der Transaktion, Vorbereitung auf den Commit und Abbrechen; Verbindung, Zuordnung und Wiederverwendung des Ressourcen Verteilers Thread Zuordnung und-Wiederverwendung. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                     |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| Standard        | Richtig                                                                                                                                                                                                                                                                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>exceptionClass



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Die CLSID, bei der es sich um eine GUID oder eine Monikerzeichenfolge handeln kann, um ein alternatives Programm während des Vorgangs zu aktivieren, das wiederholt fehlerhafte Komponenten in der Warteschlange verarbeitet. |
| Access         | ReadWrite                                                                                                                                                                 |
| type           | String                                                                                                                                                                    |
| Standard        | ""                                                                                                                                                                        |
| Minimalsystem | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>"Freinparallel"



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht das parallele Auslösen von Ereignissen, wenn die Komponente eine Ereignisklasse ist. |
| Access         | ReadWrite                                                                  |
| type           | Bool                                                                       |
| Standard        | Falsch                                                                      |
| Minimalsystem | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>Iisintrinsics



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ermöglicht das Übergeben von IIS-Kontexteigenschaften, z. b. eines Anwendungs Sitzungs Objekts oder eines Benutzer Sitzungs Objekts, in den Kontext für diese Klasse. |
| Access         | ReadWrite                                                                                                                                   |
| type           | Bool                                                                                                                                        |
| Standard        | Falsch                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>Initializeserverapplication



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die-Komponente verwendet wird, um eine Serveranwendung zu initialisieren. |
| Access         | ReadWrite                                                                   |
| type           | Bool                                                                        |
| Standard        | Falsch                                                                       |
| Minimalsystem | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>isEnabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | False, wenn die COM+-Anwendung oder-Komponente deaktiviert ist. Wenn die COM+-Anwendung oder-Komponente aktiviert ist, ist isaktivierte "true". |
| Access         | ReadWrite                                                                                                                   |
| type           | Bool                                                                                                                        |
| Standard        | Richtig                                                                                                                        |
| Minimalsystem | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>Isiebziger Class



| Eingabe | Wert |
|----------------|----------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Komponente eine Ereignisklasse ist. |
| Access         | ReadOnly                                           |
| type           | Bool                                               |
| Standard        | Falsch                                              |
| Minimalsystem | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Komponente in einer Anwendung installiert ist. |
| Access         | ReadOnly                                                        |
| type           | Bool                                                            |
| Standard        | Falsch                                                           |
| Minimalsystem | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>Isprivatecomponent



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob eine Serveranwendung eine private Komponente ist. Eine private Komponente in einer Serveranwendung kann nur innerhalb der Anwendung aktiviert werden. Wenn Sie z. b. [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) für eine private Komponente aufrufen, tritt ein Fehler außerhalb des Prozesses auf, aber der Prozess ist erfolgreich. Wenn Sie dagegen **cokreateinstance** für eine öffentliche Komponente aufrufen, ist Sie sowohl in-Process als auch außerhalb des Prozesses erfolgreich. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                               |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob die [JIT-Aktivierung](enabling-jit-activation-for-a-component.md) für die Komponente aktiviert ist. Diese Eigenschaft wird auf true festgelegt, wenn die [Transaktionsunterstützung](setting-the-transaction-attribute.md) auf erforderlich festgelegt ist, New oder supported erfordert. Wenn JustInTimeActivation auf true festgelegt ist, muss die [Synchronisierungs Unterstützung](setting-the-synchronization-attribute.md) auf Required (Standardeinstellung) festgelegt oder auf New festgelegt werden. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Wenn der Komponenten Lastenausgleich-Dienst auf dem Server installiert und aktiviert ist, bestimmt, ob die Komponente am Lastenausgleich beteiligt ist. |
| Access         | ReadWrite                                                                                                                                        |
| type           | Bool                                                                                                                                             |
| Standard        | Falsch                                                                                                                                            |
| Minimalsystem | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| Eingabe | Wert |
|----------------|-----------------------------------|
| BESCHREIBUNG    | Maximale Anzahl von Objekten in einem Pool. |
| Access         | ReadWrite                         |
| type           | Long (1-1048576)                  |
| Standard        | 1048576                           |
| Minimalsystem | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| Eingabe | Wert |
|----------------|-----------------------------------|
| BESCHREIBUNG    | Minimale Anzahl von Objekten in einem Pool. |
| Access         | ReadWrite                         |
| type           | Long (0-1048576)                  |
| Standard        | 0                                 |
| Minimalsystem | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>Multiinterfacepublisherfilterclsid



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------|
| BESCHREIBUNG    | CLSID für den Herausgeber Filter, der verwendet wird, wenn die Komponente eine Ereignisklasse ist. |
| Access         | ReadWrite                                                               |
| type           | String                                                                  |
| Standard        | –                                                                     |
| Minimalsystem | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>Mustrauuninclientcontext



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, dass die Komponente im Kontext des ursprünglichen Aufrufers aktiviert werden muss. Andernfalls schlägt die Aktivierung fehl. |
| Access         | ReadWrite                                                                                                 |
| type           | Bool                                                                                                      |
| Standard        | Falsch                                                                                                     |
| Minimalsystem | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>Mustranunindefehlercontext



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, dass die Komponente im Kontext des Standard Aufrufers aktiviert werden muss. Andernfalls schlägt die Aktivierung fehl. |
| Access         | ReadWrite                                                                                                    |
| type           | Bool                                                                                                         |
| Standard        | Falsch                                                                                                        |
| Minimalsystem | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>Objectpoolingenabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob das [com+-Objekt Pooling](com--object-pooling.md) für die Komponente aktiviert ist. |
| Access         | ReadWrite                                                                                       |
| type           | Bool                                                                                            |
| Standard        | Falsch                                                                                           |
| Minimalsystem | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Anzeige Name, der zum Identifizieren der Komponente verwendet wird. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                              |
| type           | String                                                                                                                                                                                |
| Standard        | –                                                                                                                                                                                   |
| Minimalsystem | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Bezeichner für den Ereignis Herausgeber, wenn die Komponente eine Ereignisklasse ist. |
| Access         | ReadWrite                                                              |
| type           | String                                                                 |
| Standard        | ""                                                                     |
| Minimalsystem | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>Soapassemblyname



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID, die die GAC-Assembly identifiziert, die ausgeführt wird, wenn die Komponente als SOAP-Dienst aufgerufen wird. |
| Access         | ReadWrite                                                                                        |
| type           | String                                                                                           |
| Standard        | NULL                                                                                             |
| Minimalsystem | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>Soaptyname



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der verwaltete Typname für eine Komponente, die als SOAP-Dienst aufgerufen werden kann. |
| Access         | ReadWrite                                                                    |
| type           | String                                                                       |
| Standard        | NULL                                                                         |
| Minimalsystem | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>Synchronization



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt die Rückruf [Synchronisierung](setting-the-synchronization-attribute.md) für die Komponente.                                                                                                     |
| Access         | ReadWrite                                                                                                                                                                                           |
| type           | Lange mögliche Werte: comadminsynchronizationignorierte (0) comadminsynchronizationnone (1) comadminsynchronizationsupported (2) comadminsynchronizationrequired (3) comadminsynchronizationrequirements (4) |
| Standard        | Comadminsynchronizationignoriignoriert (0)                                                                                                                                                                  |
| Minimalsystem | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, wie Instanzen der Komponente Threads zur Methoden Ausführung zugewiesen werden. Werte entsprechen com-Threading Modellen.                                                                                        |
| Access         | ReadOnly                                                                                                                                                                                                                  |
| type           | Lange mögliche Werte: comadminthreadingmodelapartment (0) comadminthreadingmodelfree (1) comadminthreadingmodelmain (2) comadminthreadingmodelboth (3) comadminthreadingmodelneutral (4) comadminthreadingmodelnotangegeben (5) |
| Standard        | –                                                                                                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>Transaktion



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, wie eine Komponente [Transaktionen](setting-the-transaction-attribute.md)unterstützt. Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden. |
| Access         | ReadWrite                                                                                                                                                                              |
| type           | Lange mögliche Werte: comadmintransaktionignorierte (0) comadmintransaktionsnone (1) comadmintransaktionssupported (2) comadmintransaktionrequired (2) comadmintransaktionrequirements (3) comadmintransaktiongsnew (4)        |
| Standard        | Comadmintransaktionnone (1)                                                                                                                                                            |
| Minimalsystem | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>Txisolationlevel



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt die Transaktions Isolations Stufen an. Es gibt fünf Isolations Stufen: None, Read uncommit, Read Commit, Repeatable Read und serialized. Die Standard Isolationsstufe wird serialisiert.                           |
| Access         | ReadWrite                                                                                                                                                                                                                  |
| type           | Lange mögliche Werte: comadmintxisolationlevelany (0) comadmintxisolationlevelleuncommit (1) comadmintxisolationlevellecommit (2) comadmintxisolationlevelrepeatableread (3) comadmintxisolationlevelserialisierbar (4) |
| Standard        | Comadmintxisolationlevelserialisierbar (4)                                                                                                                                                                                   |
| Minimalsystem | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| Eingabe | Wert |
|----------------|---------------------------|
| BESCHREIBUNG    | Buildbezeichner der Version. |
| Access         | ReadOnly                  |
| type           | String                    |
| Standard        | ""                        |
| Minimalsystem | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| Eingabe | Wert |
|----------------|---------------------|
| BESCHREIBUNG    | Versions Bezeichner. |
| Access         | ReadOnly            |
| type           | String              |
| Standard        | ""                  |
| Minimalsystem | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| Eingabe | Wert |
|----------------|-------------------------|
| BESCHREIBUNG    | Versions Unterzeichner. |
| Access         | ReadOnly                |
| type           | String                  |
| Standard        | ""                      |
| Minimalsystem | Windows 2000            |



 

### <a name="versionsubbuild"></a>Versionsubbuild



| Eingabe | Wert |
|----------------|-------------------------------|
| BESCHREIBUNG    | Versionssubbuildbezeichner. |
| Access         | ReadOnly                      |
| type           | String                        |
| Standard        | ""                            |
| Minimalsystem | Windows 2000                  |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
