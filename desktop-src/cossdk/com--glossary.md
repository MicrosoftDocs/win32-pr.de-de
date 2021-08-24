---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: COM+-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda1c62c8edee1e15df33b63a9d4894639dd9e5637ed3e87a747d724f9e9040e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638720"
---
# <a name="com-glossary"></a>COM+-Glossar

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**Zugriffstoken**
</dt> <dd>

Ein Objekt, das den Sicherheitskontext eines Prozesses oder Threads beschreibt. Die Informationen in einem Token umfassen die Identität und die Berechtigungen des Benutzerkontos, das dem Prozess oder Thread zugeordnet ist. Wenn sich ein Benutzer anmeldet, überprüft das System das Kennwort des Benutzers, indem es es mit den in einer Sicherheitsdatenbank gespeicherten Informationen vergleicht. Wenn das Kennwort authentifiziert ist, erzeugt das System ein Zugriffstoken. Jeder Prozess, der im Namen dieses Benutzers ausgeführt wird, verfügt über eine Kopie dieses Zugriffstokens.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID-Eigenschaften**
</dt> <dd>

Ein Akronym, das von Transaktionsverarbeitungsabständen für atomar, konsistent, isoliert und dauerhaft verwendet wird. Diese Eigenschaften stellen ein vorhersagbares Verhalten sicher und verstärken die Rolle von Transaktionen als Alles-oder-Keine-Sätze, die für konsistente und vorhersagbare Ergebnisse in einer verteilten Umgebung entwickelt wurden, wenn unabhängige Fehler auftreten können.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**Aktivierung**
</dt> <dd>

Die Kette von Ereignissen, die zur Erstellung eines COM-Objekts und zur Rückgabe eines gültigen Zeigers auf eine Schnittstelle für dieses Objekt führt. In COM+ wird ein Objekt entweder im eigenen Kontext oder in dem seines Erstellers aktiviert (ein Objekt, das die Aktivierung des Objekts angefordert hat). COM+-Dienste basieren auf einer geeigneten Aktivierung eines Objekts basierend auf der Konfiguration des Objekts. Während der Aktivierung bestimmt das System den Kontext, in dem das Objekt ausgeführt wird, initialisiert die Kontexteigenschaften, überprüft Zugriffsberechtigungen und richtet eine Sicherheitsidentität ein.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**Aktivierungssicherheit**
</dt> <dd>

Eine Form des Sicherheitsschutzes, der bestimmt, wer einen Server starten kann. Die Aktivierungssicherheit wird automatisch vom Dienststeuerungs-Manager (Service Control Manager, SCM) eines bestimmten Computers angewendet. Nach Dem Empfang einer Anforderung von einem Client zum Aktivieren eines Objekts überprüft der SCM die Anforderung anhand der in seiner Registrierung gespeicherten Aktivierungssicherheitsinformationen. Die Aktivierungssicherheit wird auch auf Aktivierungen auf demselben Computer überprüft. Wird auch als *Startsicherheit* bezeichnet.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**Aktivierungstyp**
</dt> <dd>

Aktivierungskategorie für eine COM+-Anwendung, die angibt, ob die Anwendung im oder außerhalb des Prozessbereichs ihres Clients ausgeführt wird (je nachdem, ob es sich um eine Bibliothek oder Serveranwendung bzw. um eine Serveranwendung) und ob die Anwendung als Dienst ausgeführt wird.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**Aktivität**
</dt> <dd>

In COM+ ein logischer Thread, der eine oder mehrere Transaktionen umfasst und eine Auflistung von Komponenten enthält, die in einer COM+-Anwendung gruppiert sind. Jedes COM-Objekt gehört zu einer Aktivität. Die Zuordnung zwischen einem Objekt und einer Aktivität kann nicht geändert werden.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**Apartmentmodellprozess**
</dt> <dd>

Ein Prozess, der über zwei oder mehr Singlethread-Apartments und keine Multithread-Apartments verfügt.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**Anwendungsproxy**
</dt> <dd>

Eine Gruppe von Dateien mit Registrierungsinformationen, die einem Client den Remotezugriff auf eine COM+-Serveranwendung ermöglichen. Bei der Installation auf einem Clientcomputer schreibt eine Anwendungsproxydatei Informationen über die Serveranwendung auf den Clientcomputer. der Client kann dann remote auf die Serveranwendung zugreifen.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Authentifizierung**
</dt> <dd>

Der Sicherheitsprozess, bei dem bestimmt wird, ob ein Aufrufer einer Anwendung tatsächlich die Person ist, die er anfordert, und die Authentizität eines Identitätsanspruchs wird überprüft. Bei COM+-Anwendungen kann die Authentifizierung aktiviert und administrativ konfiguriert werden. Danach funktioniert sie für die Anwendung transparent.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**Autorisierung**
</dt> <dd>

Der Sicherheitsprozess, bei dem bestimmt wird, ob ein Aufrufer einer Anwendung berechtigt ist, das zu tun, wozu er aufgefordert wird.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Zwischenspeichern des Ressourcen-Managers**
</dt> <dd>

Ein Ressourcen-Manager, der als Front-End für einen anderen Ressourcen-Manager fungiert und Informationen lokal zwischenspeichert, wodurch die Kosten für den Zugriff auf die zugrunde liegende Ressource reduziert werden. Im Gegensatz zu einem herkömmlichen Ressourcen-Manager ist ein Cacheressourcen-Manager nicht an der Wiederherstellung beteiligt, da er die zugrunde liegenden Daten nie dauerhaft speichert.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**Aufrufen der Sicherheit**
</dt> <dd>

Eine Form des Sicherheitsschutzes, mit der der Zugriff auf die Methoden eines Serverobjekts nach dem Start eines Servers gesteuert wird.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**-Klasse (COM)**
</dt> <dd>

Eine benannte, konkrete Implementierung einer oder mehrerer Schnittstellen. Eine COM-Klasse wird durch eine CLSID und manchmal auch durch eine ProgID identifiziert.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**Cloaking**
</dt> <dd>

Die Fähigkeit eines Servers, seine eigene Identität zu maskieren, wenn Aufrufe im Namen eines Clients ausgeführt werden. Wenn die Verleumdung aktiviert ist, können Aufrufe, die vom Server ausgeführt werden, der die Identität des Clients an sich nimmt, unter der Identität des Clients erfolgen. Wenn die Verleumdung deaktiviert ist, werden Aufrufe vom Server unter der Identität des Servers ausgeführt.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+-Anwendung**
</dt> <dd>

Die primäre Verwaltungs- und Sicherheitseinheit für Komponentendienste. Eine COM+-Anwendung ist eine Gruppe von COM-Komponenten, die im Allgemeinen verwandte Funktionen ausführen. Diese Komponenten bestehen außerdem aus COM-Schnittstellen und -Methoden.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+-Anwendungspooling**
</dt> <dd>

Ein Komponentendienstfeature, das die Skalierung von Singlethreadprozessen ermöglicht und Ihnen auch bei der Wiederherstellung nach Fehlern in einzelnen Prozessen helfen kann, indem andere ausgeführte Prozesse zur Verfügung gestellt werden, die Aktivierungen verarbeiten können.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+-Anwendungswiederverwendung**
</dt> <dd>

Ein Komponentendienstfeature, das die allgemeine Stabilität Ihrer Anwendungen erheblich erhöht, indem es Ihnen ermöglicht wird, einen Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß herunterzufahren und neu zu starten.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+-Katalog** 
</dt> <dd>

Der Datenspeicher, der COM+-Konfigurationsdaten enthält. Die Leistung von COM+-Verwaltungsaufgaben erfordert das Lesen und Schreiben von daten, die im Katalog gespeichert sind. Auf den Katalog kann nur über das Verwaltungstool Komponentendienste oder über die COMAdmin-Bibliothek zugegriffen werden.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+-Ereignisse**
</dt> <dd>

COM+-Ereignisse stimmt mit Verlegern und Abonnenten über ein lose gekoppeltes Ereignissystem überein und verbindet sie. Ein Herausgeber ruft die -Methode auf, um ein Ereignis zu initiieren, und ein Abonnent empfängt diese Aufrufe über das Ereignissystem und nicht direkt vom Verleger. Der COM+-Ereignisdienst verwaltet die Liste der interessierten Abonnenten, die die Anrufe empfangen, und leitet diese Aufrufe weiter, ohne dass die Kenntnis des Herausgebers erforderlich ist.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+-Bibliotheksanwendung**
</dt> <dd>

Eine COM+-Anwendung, die im Prozess des Clients ausgeführt wird, der sie erstellt. Bibliotheksanwendungen können rollenbasierte Sicherheit verwenden, unterstützen jedoch keinen Remotezugriff oder Komponenten in der Warteschlange.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+-Objektpooling**
</dt> <dd>

Ein von COM+ bereitgestellter automatischer Dienst, mit dem Sie eine Komponente so konfigurieren können, dass Instanzen von sich selbst in einem Pool aktiv bleiben und von jedem Client verwendet werden können, der die Komponente anfordert.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+-Partitionen**
</dt> <dd>

Ein COM+-Dienst, der auf einem einzelnen Computer die Erstellung separater Ausführungsräume für Anwendungen ermöglicht.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+-Partitionssätze**
</dt> <dd>

Eine Gruppe von COM+-Partitionen, die einer bestimmten Benutzer-ID in Active Directory zugeordnet ist.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+-Komponenten in der Warteschlange**
</dt> <dd>

Ein COM+-Dienst, der auf Microsoft Message Queuing basiert und eine einfache Möglichkeit zum asynchronen Aufrufen und Ausführen von Komponenten bietet. Die Nachrichtenverarbeitung kann ohne Berücksichtigung der Verfügbarkeit oder Barrierefreiheit des Absenders oder Empfängers erfolgen.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+-Serveranwendung**
</dt> <dd>

Eine COM+-Anwendung, die in einem eigenen Prozess ausgeführt wird. Serveranwendungen können alle COM+-Dienste unterstützen.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+-SOAP**
</dt> <dd>

Ein Komponentendienstfeature, mit dem Sie eine COM+-Anwendung als XML-Webdienst verfügbar machen können. COM+-SOAP ermöglicht ihnen auch die Verwendung eines XML-Webdiensts als COM-Komponente.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM-Komponente**
</dt> <dd>

Eine binäre Codeeinheit, die Paket- und Registrierungscode enthält und COM-Objekte erstellt. Alle COM+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**Commitstruktur**
</dt> <dd>

In einem verteilten Transaktionssystem die konzeptionelle Darstellung einer Transaktion als basierend auf den hierarchischen Beziehungen zwischen einzelnen Transaktions-Managern, die an einer verteilten Transaktion teilnehmen. In dieser Hierarchie sind die eingetragenen Ressourcen-Manager enthalten, die den Transaktions-Managern zugeordnet sind.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM-Objekt**
</dt> <dd>

Im COM-Programmiermodell kapselt eine Programmierstruktur sowohl Daten als auch Funktionen, die als einzelne Einheit definiert und zugeordnet werden und für die der einzige öffentliche Zugriff über die Schnittstellen der Programmierstruktur erfolgt. Ein COM-Objekt muss mindestens die [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) unterstützen, die das Vorhandensein des Objekts bei seiner Verwendung beibehält und Zugriff auf die anderen Schnittstellen des Objekts bietet.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Kompensierende Resource Manager (CRM)**
</dt> <dd>

Ein COM+-Feature, das es nicht transaktionalen Ressourcen ermöglicht, an einer zweistufigen Committransaktion mit dem Microsoft Distributed Transaction Coordinator (DTC) teilzunehmen. In der Regel bieten CRMs nicht die Isolationsfunktionen von vollständigen Ressourcen-Managern, aber sie bieten transaktionale Atomarität und Dauerhaftigkeit, indem sie in ein Protokoll schreiben.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Verwaltungstool "Komponentendienste"**
</dt> <dd>

Ein Benutzeroberflächen-Snap-In, über das Administratoren und Entwickler COM+-Anwendungen erstellen, konfigurieren und verwalten sowie verteilte Transaktionen und speicherresidente Datenbanken verwalten können. Das Verwaltungstool Komponentendienste kann auch verwendet werden, um Systemereignisse anzuzeigen und Systemdienste lokal auf dem Computer zu verwalten, auf dem das Tool installiert ist.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**konzeptionelles Modell**
</dt> <dd>

Der erste Schritt in der Entwurfsphase der COM+-Anwendung, in der der Entwickler die zu lösenden Geschäftsprobleme definiert und entscheidet, welche Komponenten und Dienste erforderlich sind.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**Parallelität**
</dt> <dd>

Die Möglichkeit, dass mehrere Transaktionen oder Prozesse gleichzeitig auf dieselben Daten zugreifen können. COM+ verwaltet die Parallelität in der Regel durch Synchronisierung.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**Konfigurierte Komponente**
</dt> <dd>

Eine COM-Komponente, die in einer COM+-Anwendung installiert wurde. Nach der Installation wird die Komponente im COM+-Katalog so konfiguriert, dass die verfügbaren COM+-Dienste verwendet werden.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**Kontext**
</dt> <dd>

Ein Satz von Laufzeiteigenschaften, die einem oder mehrere COM-Objekten zugeordnet sind, die zum Bereitstellen von Diensten für diese Objekte verwendet werden. Jedes COM-Objekt wird in einem einzigen Kontext von der Aktivierung bis zur Deaktivierung (immer innerhalb desselben Apartment) ausgeführt. Wenn ein Objekt aktiviert wird, stellen Kontexteigenschaften, z. B. Sicherheitskontexteigenschaften, die Laufzeitanforderungen eines Objekts dar.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**Datenebene**
</dt> <dd>

Im Architekturmodell mit drei Ebenen für Geschäftsanwendungen ist die DBMS-Zugriffsebene, auf die über die mittlere Ebene oder Die Ebene der Geschäftsdienste und gelegentlich über die Präsentationsebene oder die Benutzerdienstebene zugegriffen werden kann. Die Datenschicht besteht aus Datenzugriffskomponenten (anstelle von unformatierten DBMS-Verbindungen), um die Ressourcenfreigabe zu unterstützen und die Konfiguration von Clients zu ermöglichen, ohne die DBMS-Bibliotheken und ODBC-Treiber auf jedem Client zu installieren. Wird auch als *Datendienstebene bezeichnet.*

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Deadlock**
</dt> <dd>

In Multithreadanwendungen tritt ein Threadingproblem auf, das auftritt, wenn jeder Member einer Gruppe von Threads auf einen anderen Member der Gruppe wartet.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegation**
</dt> <dd>

Eine Form des Identitätswechsels, die einen Server autorisiert, im Auftrag eines Clients zu agieren, was dem Server die Möglichkeit gibt, die Identität von Clients über das Netzwerk zu imitieren.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**Verteilte Transaktion**
</dt> <dd>

Eine Transaktion, die mehrere Ressourcen-Manager umfasst, die sich auf demselben oder unterschiedlichen Computern finden können.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**
</dt> <dd>

Ein Systemdienst, der Transaktionen und transaktionsbezogene Kommunikation verwaltet, die auf zwei oder mehr Ressourcen-Manager auf einem oder mehreren Systemen verteilt sind, um sicherzustellen, dass die ACID-Transaktionen korrekt sind.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**Dynamisches Verkleinern**
</dt> <dd>

Eine Form der Überhingung, bei der die ursprüngliche Clientidentität bei jedem Methodenaufruf an den Downstreamserver als Serverthreadzugriffstoken gefunden wird. Obwohl die dargestellte Identität dynamisch bestimmt werden kann, kann der dafür erforderliche Mehraufwand erheblich teurer sein. Für COM+-Anwendungen ist die Standardkonfiguration für die dynamische Verkleinerungsfunktion bestimmt, da sie die Flexibilität bietet, die in der Regel für Umstände erforderlich ist, die von Anfang an identitätswechseln müssen.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**Enumeratorobjekt**
</dt> <dd>

Ermöglicht das Aufzählen der Elemente in einer Auflistung.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**Ereignis**
</dt> <dd>

Eine Aktion, die von einem Objekt erkannt wird, z. B. durch Klicken mit der Maus oder Drücken einer Taste, und für die Sie Code schreiben können, um zu reagieren.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**Ereignisklassenobjekt**
</dt> <dd>

Eine konfigurierte Komponente, die einen persistenten Datensatz im COM+-Ereignissystem bietet, um die Herausgeber und die den Herausgebern zugeordneten ausschaltenden Schnittstellen zu beschreiben.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event-Methode**
</dt> <dd>

Eine Methode in einer COM+-Schnittstelle, die ein COM+-Ereignis identifiziert. Ereignismethoden müssen eindeutig benannt werden und dürfen nur Eingabeparameter enthalten. Der Rückgabewert muss ein **HRESULT sein.**

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**Event-Objekt**
</dt> <dd>

Ein COM-Objekt, das einem oder mehreren Threads signalisieren kann, dass ein Ereignis aufgetreten ist. Jeder Thread innerhalb eines Prozesses kann ein Ereignisobjekt erstellen.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**Ausnahme**
</dt> <dd>

Ein ungewöhnlicher Zustand oder Fehler, der während der Ausführung eines Programms auftritt und die Ausführung von Software außerhalb des normalen Ablaufs der Kontrolle erfordert.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**Failover**
</dt> <dd>

In einem Clusternetzwerksystem wird eine überladene oder fehlerhafte Ressource (z. B. ein Server, ein Laufwerk oder ein Netzwerk) in die Sicherungskomponente umverteilt.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**Freethread-Prozess**
</dt> <dd>

Ein Prozess, der über ein Multithread-Apartment und keine Singlethread-Apartments verfügt.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**globaler Commit-Koordinator**
</dt> <dd>

Auf einem microsoft Windows-basierten verteilten Transaktionssystem der Stammtransaktions-Manager der Commitstruktur. Dieser Koordinator trifft die Entscheidung, eine bestimmte Transaktion entweder zu commiten oder zu abbrechen, und ist nie im Zweifelsfall.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**Identitätswechsel**
</dt> <dd>

Die Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem prozess, der den Thread besitzt, auszuführen. Der Serverthread verwendet ein Zugriffstoken, das die Anmeldeinformationen des Clients darstellt. Damit kann er auf Ressourcen zugreifen, auf die der Client zugreifen kann.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**Identitätswechselebene**
</dt> <dd>

Die Einstellung, die vom Client verwendet wird, um dem Server eine bestimmte Autorität zum Ausführen von Aktionen im Auftrag des Clients zu gewähren. In COM+ kann dies nur für COM+-Serveranwendungen festgelegt werden.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**Abfangen**
</dt> <dd>

Für ein Objekt, das in einem bestimmten Kontext aktiviert wird, der Prozess der Verarbeitung von Aufrufen dieses Objekts über die Kontextgrenze hinweg. Aufrufe im kontextübergreifenden Bereich werden mit einfachen Schnittstellen-Proxys verarbeitet, die alle erforderlichen Aufrufe verarbeiten, um die Laufzeitumgebung von einer Umgebung anzupassen, die den Aufrufer an einen aufruft, der den Aufrufer aufnehmen kann.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**Schnittstelle**
</dt> <dd>

Bei der COM-basierten Programmierung eine Auflistung verwandter öffentlicher Funktionen, die Zugriff auf ein COM-Objekt bereitstellen. Der Satz von Schnittstellen in einem COM-Objekt erstellt einen Vertrag, der angibt, wie Programme und andere Objekte mit dem COM-Objekt interagieren können.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**Schnittstellenproxy**
</dt> <dd>

Ein schnittstellenspezifisches Objekt, das Parameter für diese Schnittstelle als Vorbereitung für einen Remotemethodeaufruf verpackt (marshallt) und die Rückgabewerte aus dem Schnittstellenstub entpackt (entpackt). Ein Proxy wird im Adressraum des Absenders ausgeführt und kommuniziert mit einem entsprechenden Stub im Adressraum des Empfängers.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**Schnittstellenstub**
</dt> <dd>

Ein schnittstellenspezifisches Objekt, das gemarshallte Parameter entpackt, die erforderliche Methode aufruft und Pakete (Marshalls) Werte aus der aufgerufenen Methode zurückgeben. Der Stub wird im Adressraum des Empfängers ausgeführt und kommuniziert mit einem entsprechenden Schnittstellenproxy im Adressraum des Absenders.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**Inneres Objekt**
</dt> <dd>

In einer Transaktionshierarchie ein beliebiges Objekt unter dem Stammobjekt.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**Just-In-Time-Aktivierung (JIT)**
</dt> <dd>

Ein automatischer Dienst von COM+, der eine produktivere Verwendung von Serverressourcen im Leerlauf ermöglicht. Wenn eine Komponente als JIT-aktiviert konfiguriert ist, kann COM+ eine Instanz davon deaktivieren, während ein Client noch einen aktiven Verweis auf das Objekt enthält. Wenn der Client das nächste Mal eine Methode für das Objekt aufruft, reaktiviert COM+ das Objekt für den Client transparent just-in-time.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**Legacykomponente**
</dt> <dd>

Eine nicht konfigurierte Komponente, die in einer COM+-Anwendung installiert wurde.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Listener**
</dt> <dd>

Ein Architekturelement des COM+-Diensts für Warteschlangenkomponenten. Der Listener ist ein COM-Objekt, das die der Hostanwendung zugeordnete Nachrichtenwarteschlange öffnet und auf den Eintreffen von Nachrichten wartet. Wenn Nachrichten eintreffen, versendet der Listener Threads, die Nachrichten verarbeiten.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logisches Modell**
</dt> <dd>

Der zweite Schritt in einem COM+-Anwendungsentwurfsprozess, bei dem das konzeptionelle Modell wie folgt in die logischen Ebenen der Drei-Ebenen-Architektur aufgebrochen wird: präsentationsschicht oder Benutzerdienste; die mittlere Ebene oder Geschäftsdienste; und die Datenebene oder Datendienste.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**Lose gekoppeltes Ereignis**
</dt> <dd>

Ein Ereignis, dessen Absender (Herausgeber) und Empfänger (Abonnent) nicht eng gebunden sind. In einem lose gekoppelten Ereignissystem, z. B. COM+-Ereignissen, werden Ereignisinformationen von verschiedenen Herausgebern in einem Ereignisspeicher beibehalten. Abonnenten fragen diesen Speicher ab und wählen die Ereignisse aus, die sie empfangen möchten. Wenn Sie Ereignisinformationen aus dem Ereignisspeicher auswählen, wird ein Abonnement erstellt. Wenn ein Ereignis auftritt, sucht das Ereignissystem in dieser Datenbank und sucht die interessierten Abonnenten, erstellt ein neues Objekt jeder interessierten Klasse und ruft eine Methode für dieses Objekt auf.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**Marshalling**
</dt> <dd>

Der Prozess des Packens und Entpackens von Schnittstellenmethode-Parametern über Thread- oder Prozessgrenzen hinweg, sodass ein Remoteprozeduraufruf ausgeführt werden kann.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**Message Mover**
</dt> <dd>

Das Architekturelement des COM+-Diensts für Warteschlangenkomponenten, der fehlerhafte Nachrichten zurück in die Eingabewarteschlange verschiebt, damit sie wiederholt werden können.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**
</dt> <dd>

Ein Ereignistyp, der vom COM+-Ereignissystem verwendet wird, um die interessierten Abonnenten zu benachrichtigen, wenn Ereignisklassenobjekte oder -abonnements erstellt, geändert oder entfernt werden.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**Methode**
</dt> <dd>

Bei der COM-basierten Programmierung ein Prozess, der von einem COM-Objekt ausgeführt wird, wenn es eine Nachricht empfängt.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**Mittlere Ebene**
</dt> <dd>

Im Architekturmodell mit drei Ebenen für Geschäftsanwendungen ist dies die Ebene, die die Geschäftslogik und Datenregeln umfasst. Die Komponenten der mittleren Ebene können verwendet werden, um Geschäftsregeln wie Geschäftsalgorithmen, gesetzliche oder behördliche Vorschriften und Datenregeln durchzusetzen, die darauf ausgelegt sind, die Datenstrukturen innerhalb bestimmter oder mehrerer Datenbanken konsistent zu halten. Da diese Komponenten der mittleren Ebene nicht an einen bestimmten Client gebunden sind, können sie von allen Anwendungen verwendet und an verschiedene Speicherorte verschoben werden, wenn die Antwortzeit und andere Regeln dies erfordern. Wird auch *als Geschäftsdienstebene oder* *Geschäftslogikebene bezeichnet.*

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**Gemischter Modellprozess**
</dt> <dd>

Ein Prozess, der über ein Multithread-Apartment und mindestens ein Singlethread-Apartment verfügt.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Ein Name, der ein COM-Objekt eindeutig identifiziert. Auf die gleiche Weise wie ein Pfad eine Datei im Dateisystem identifiziert, identifiziert ein Moniker ein COM-Objekt im Verzeichnisnamespace.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi-Datei**
</dt> <dd>

Eine Datei, die vom Component Services-Verwaltungstool erstellt wird, wenn Sie eine COM+-Anwendung oder einen Anwendungsproxy für die Installation auf einem anderen Computer exportieren. Die .msi kann auf jedem Windows-basierten Client mithilfe des Windows installiert werden.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**Multithread-Apartmentmodell**
</dt> <dd>

Ein Apartmentmodell, bei dem sich alle Threads im Prozess, die als Freethreading initialisiert wurden, in einem einzelnen Apartment befinden. Daher ist es nicht notwendig, zwischen Threads zu marshallen. Die Threads müssen keine Nachrichten abrufen und senden, da COM in diesem Modell keine Fenstermeldungen verwendet.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**Geschachtelte Transaktion**
</dt> <dd>

Eine sekundäre Transaktion, die innerhalb einer vorhandenen primären oder übergeordneten Transaktionsgrenze initiiert wird. Für die primäre Transaktion wird erst dann ein Commit ausgeführt, wenn für alle untergeordneten oder geschachtelten Transaktionen ein Commit ausgeführt wird. COM+ unterstützt keine geschachtelten Transaktionen.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**Neutrales Apartmentmodell**
</dt> <dd>

Ein Threadingmodell, bei dem Objekte die Richtlinien für Multithread-Apartments befolgen, aber für jede Art von Thread ausgeführt werden können. Das neutrale Apartmentmodell ist das empfohlene Threadingmodell für COM-Komponenten und COM+-Anwendungen.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**Persistentes Objekt**
</dt> <dd>

Ein COM-Objekt, das seinen internen Zustand speichern kann, wenn es von einem Client dazu aufgefordert wird, und das com-definierten Standards entspricht, mit denen Clients Objekte anfordern können, die initialisiert, geladen und aus einem Datenspeicher (z. B. Flatdatei, strukturierter Speicher oder Arbeitsspeicher) gespeichert werden sollen. Es liegt in der Verantwortung des Clients, den Speicherort der persistenten Daten des Objekts zu verwalten, aber nicht das Format der Daten.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**Persistente Objektschnittstelle**
</dt> <dd>

Eine COM-Schnittstelle, die von einem persistenten -Objekt implementiert wird. Clients verwenden persistente Objektschnittstellen, um diese persistenten Objekte darüber zu informieren, wann und wo sie ihren Zustand speichern.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**Benachrichtigungsschnittstelle für Phase 0**
</dt> <dd>

COM+-Schnittstelle, mit der Anwendungen erkennen können, wann eine Transaktion bereit ist, mit einem zweiphasenbasierten Commitprotokoll fortzufahren, sodass sie die erforderlichen Benachrichtigungsvorgänge ausführen und mit dem Transaktions-Manager kommunizieren kann, wenn die Vorgänge abgeschlossen sind.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**Physisches Modell**
</dt> <dd>

Der dritte und letzte Schritt im COM+-Anwendungsentwurfsprozess, bei dem der Entwickler bestimmt, wo sich die Komponenten physisch befinden und wie sie codiert werden sollen.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Spieler**
</dt> <dd>

Das Architekturelement des COM+-Diensts für Warteschlangenkomponenten, der die Nachricht aus einer Warteschlange abruft und dann das Serverobjekt und die Standardschnittstellenstubs lädt, um daten zu entmarshalieren und Servermethoden aufaufrufen. Der Player demarshaliert den Sicherheitskontext des Clients auf serverseitiger Seite, ruft dann die Serverkomponente auf und sendet die gleichen Methodenaufrufe. Die Methodenaufrufe werden erst dann vom Player abgespielt, wenn die Clientkomponente abgeschlossen ist und die Transaktion, die die Methode aufgezeichnet hat, Commits aufruft.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**Präsentationsebene**
</dt> <dd>

Im Architekturmodell mit drei Ebenen für Geschäftsanwendungen ist dies die Ebene, die dem Benutzer Daten präsentiert und optional die Datenbearbeitung und Dateneingabe ermöglicht. Die beiden Haupttypen der Benutzeroberfläche für die Präsentationsebene sind die herkömmliche Anwendung und die webbasierte Anwendung. Wird auch als *Benutzerdienstebene bezeichnet.*

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**Primäres Zugriffstoken**
</dt> <dd>

Beschreibt den Sicherheitskontext des Benutzerkontos, das einem Prozess zugeordnet ist.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Proxy-Manager**
</dt> <dd>

Beim Standard-Marshalling eine Komponente, die alle Schnittstellenproxies für ein einzelnes Objekt verwaltet.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**Pseudoobjekt**
</dt> <dd>

Ein Typ eines enthaltenen Objekts, z. B. eine Benutzerauswahl in einem Dokument, ein Zellenbereich in einer Kalkulationstabelle oder ein Zeichenbereich in einem Textdokument. Dieser Objekttyp wird als Pseudoobjekt bezeichnet, da er erst dann als eindeutiges Objekt behandelt wird, wenn ein Benutzer die Auswahl markiert.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**Verlag**
</dt> <dd>

Der Absender eines Ereignisses. In der COM+-Ereignisarchitektur gibt der Herausgeber den Methodenaufruf aus, um ein Ereignis zu initiieren.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**Warteschlangenmoniker**
</dt> <dd>

Der Moniker, der zum Aktivieren einer Komponente in der Warteschlange verwendet wird.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**Racebedingung**
</dt> <dd>

In einer Multithreadanwendung tritt eine Bedingung auf, die auftritt, wenn mehrere Threads ohne Koordination auf ein Datenelement zugreifen, was möglicherweise inkonsistente Ergebnisse verursacht, je nachdem, welcher Thread zuerst das Datenelement erreicht. COM bietet einige Funktionen, die speziell entwickelt wurden, um Racebedingungen auf Out-of-Process-Servern zu vermeiden.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**Recorder**
</dt> <dd>

Das Architekturelement des COM+ Queued Components-Diensts, der den Sicherheitskontext des Clients in eine Nachricht marshallt und alle Methodenaufrufe für ein Objekt auf zeichnet. Die Aufzeichnung ist ein vom System bereitgestellter Proxy-Manager, der Schnittstellen aus den Warteschlangenschnittstellen im COM+-Katalog auswählt.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**Ressourcenspender**
</dt> <dd>

Im COM+-Programmiermodell eine Komponente, die den nicht ablaufbaren freigegebenen Zustand im Auftrag der Anwendungskomponenten innerhalb eines Prozesses verwaltet. Ressourcensender ähneln Ressourcen-Managern, aber ohne Garantie der Dauerhaftigkeit.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Resource Manager**
</dt> <dd>

Ein Dienst, der persistente oder dauerhafte Daten in Datenbanken, dauerhaften Nachrichtenwarteschlangen oder Transaktionsdateisystemen verwaltet. Es ist der Ressourcen-Manager, der weiß, wie Daten gespeichert und eine Notfallwiederherstellung durchzuführen ist. COM+-Serveranwendungen verwenden Ressourcen-Manager, um den dauerhaften Zustand einer Anwendung zu verwalten, z. B. den Bestand, ausstehende Bestellungen und Konten. Ressourcen-Manager arbeiten in Zusammenarbeit mit dem Microsoft Distributed Transaction Coordinator (DTC) zusammen, um Atomarität und Isolation für eine Anwendung zu gewährleisten.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**Rollenbasierte Sicherheit**
</dt> <dd>

Ein COM+-Sicherheitsdienst, der für COM+-Anwendungen bereitgestellt wird. Eine Rolle stellt eine Kategorie von Benutzern dar, die für eine COM+-Anwendung definiert sind, um Zugriffsberechtigungen für die Ressourcen der Anwendung zu bestimmen. Rollen werden von einem Entwickler Komponenten, Schnittstellen und Methoden zugewiesen. Benutzer werden von einem Administrator den entsprechenden Rollen zugewiesen, sodass ein Benutzer innerhalb einer bestimmten Rolle auf alle Ressourcen zugreifen kann, denen diese Rolle zugewiesen ist.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**Root-Objekt**
</dt> <dd>

Das erste Objekt einer Transaktion, das als Stamm der Transaktion bezeichnet wird und immer an einer neuen Transaktionsgrenze platziert wird. Es kann nur ein Stammobjekt in einer Transaktion geben. Alle anderen Objekte in der Transaktionshierarchie unter dem Stammobjekt werden als innere Objekte bezeichnet.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Stammtransaktions-Manager**
</dt> <dd>

Der Transaktions-Manager auf dem System, der eine Transaktion initiiert. Die Transaktion wird erst abgeschlossen, wenn der Stammtransaktions-Manager den Status der Transaktion bestimmt (entweder ein Committed oder ein Abbruch).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**Semaphor**
</dt> <dd>

Ein Kernelobjekt, mit dem der Zugriff auf eine freigegebene Ressource geerbte wird.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Dienststeuerungs-Manager (Service Control Manager, SCM)**
</dt> <dd>

Ein Microsoft Windows-Serverprozess, der alle Dienste in der Windows verwaltet.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Shared Property Manager (SPM)**
</dt> <dd>

In Com+ ein Ressourcensender, den Sie verwenden können, um den nicht vorhandenen Zustand für mehrere Objekte innerhalb eines Serverprozesses frei zu geben.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**Singlethreadprozess**
</dt> <dd>

Ein Prozess, der aus nur einem Singlethread-Apartment besteht, das wiederum aus genau einem Thread besteht. Alle COM-Objekte, die in einem Singlethread-Apartment leben, können Methodenaufrufe nur von dem einen Thread empfangen, der zu diesem Apartment gehört.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**Seife**
</dt> <dd>

Ein einfaches, XML-basiertes Protokoll zum Austauschen strukturierter und Typinformationen im Web. Das Protokoll enthält keine Anwendungs- oder Transportsemantik, wodurch es sehr modular und erweiterbar ist.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**Registrierung aufteilen**
</dt> <dd>

Für Komponenten, die bereits com-Komponenten sind und in der COM+-Dienstumgebung verwendet werden, wird die Registrierungsanordnung, in der der grundlegende COM-Aspekt der Registrierung in der Windows-Registrierung gespeichert ist, sowie neue COM+-Dienste und -Attribute (z. B. Warteschlangenkomponenten) in der COM+-Registrierungsdatenbank gespeichert. Jedes Komponentenattribut wird entweder in der Windows oder in der COM+-Registrierungsdatenbank gespeichert. Neue COM-Komponenten werden ausschließlich in der COM+-Registrierungsdatenbank registriert, mit einer Duplizierung in Windows Registrierung, damit vorhandene Tools sie verwenden können.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**Stateful**
</dt> <dd>

Von oder bezieht sich auf ein System oder einen Prozess, das bzw. der alle Details des Status einer Aktivität überwacht, an der sie beteiligt ist.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**Staatenlos**
</dt> <dd>

Von oder bezieht sich auf ein System oder einen Prozess, das bzw. der an der Aktivität beteiligt ist, ohne alle Details seines Zustands zu überwachen.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**Statische Verkleinerung**
</dt> <dd>

Eine Form der Überhingung, bei der die ursprüngliche Clientidentität einmal einem Downstreamserver präsentiert werden kann, wobei die ursprüngliche Clientidentität einmal auf dem Proxy konfiguriert wird. Diese Clientidentität wird als Serverthreadtoken dargestellt, das bei nachfolgenden Methodenaufrufen verwendet wird.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Abonnenten**
</dt> <dd>

Der Empfänger eines Ereignisses. In der COM+-Ereignisarchitektur empfängt der Abonnent die Aufrufe des Herausgebers.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**Abonnementobjekt**
</dt> <dd>

Im COM+-Ereignissystem ein Objekt, das von einem Abonnenten erstellt wurde, um die Übermittlung von Ereignissen anzufordern und zu verwalten.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**Synchronisierung**
</dt> <dd>

In COM+ ein Dienst, der von Komponente zu Komponente fließt und verhindert, dass mehr als ein Aufrufer zu einem bestimmten Zeitpunkt in die Komponente eintritt. Die Synchronisierung bestimmt, wann Threads Aufrufe an ein Objekt senden können.

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**Architekturmodell mit drei Ebenen**
</dt> <dd>

Das grundlegende Framework für das logische Entwurfsmodell unterteilt die Komponenten einer Anwendung wie folgt in drei Dienstesebenen: die Präsentationsebene oder Benutzerdienste. mittlere Ebene oder Geschäftsdienste; und die Datenebene oder Datendienste. Diese Ebenen entsprechen nicht notwendigerweise physischen Standorten auf verschiedenen Computern in einem Netzwerk, sondern logischen Ebenen der Anwendung.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**Eng gekoppeltes Ereignis**
</dt> <dd>

Ein Ereignis, dessen Absender (Herausgeber) und Empfänger (Abonnent) eng gebunden sind. In einem eng gekoppelten Ereignissystem wird dem Verleger eine Schnittstelle bereitgestellt, über die eine Methode aufgerufen werden kann, wenn eine Änderung auftritt. Der Abonnent weiß, von welchem Herausgeber Benachrichtigungen angefordert werden sollen und welche Schnittstellen verfügbar gemacht werden. Ein eng gekoppeltes Ereignissystem erfordert, dass sowohl der Verleger als auch der Abonnent jederzeit ausgeführt werden.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Ablaufverfolgungsprotokoll**
</dt> <dd>

Eine Protokolldatei, die automatisch vom Microsoft Distributed Transaction Coordinator generiert wird und Daten im Zusammenhang mit einer oder mehreren verteilten Transaktionen anzeigt. Beispiele für Daten in einem Ablaufverfolgungsprotokoll sind Transaktions-ID, Transaktionszeit und Meldungen, die das Transaktionsergebnis angeben.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**Transaktion**
</dt> <dd>

Eine Arbeitseinheit, in der während eines Anwendungsprozesses eine Reihe verwandter Vorgänge ausgeführt wird. Eine Transaktion wird genau einmal ausgeführt und ist atomar– entweder ist die gesamte Arbeit abgeschlossen oder keine davon.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**
</dt> <dd>

Transaction Internet Protocol ist ein standardmäßiges zweistufiges Commitprotokoll, mit dem heterogene Transaktions-Manager verteilte Transaktionen koordinieren können, insbesondere über das Internet. Das tip-Protokoll für zweistufige Commits ist einfach zu implementieren und unabhängig vom Kommunikationsprotokoll zwischen Anwendungen, sodass es mit jedem Anwendungsprotokoll, aber insbesondere http verwendet werden kann.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Transaktions-Manager**
</dt> <dd>

Der Teil des Microsoft Distributed Transaction Coordinator (DTC), der auf jedem Computer ausgeführt wird, der an einer verteilten Transaktion teilnimmt und die Aktivitäten im Zusammenhang mit dem Committen oder Abbrechen dieses Teils der Transaktion verwaltet.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**Transaktionsverarbeitungsanwendung**
</dt> <dd>

Eine Sammlung von Transaktionsvorgängen, die eine bestimmte Geschäftsaufgabe automatisieren.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**Transaktionsverarbeitungssystem**
</dt> <dd>

Ein vollständiges System, das sowohl Computerhardware als auch Software umfasst und eine Transaktionsverarbeitungsanwendung hostet, um routinemäßige Transaktionen auszuführen, die für die Durchführung von Vorgängen erforderlich sind.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Zweiphasencommitprotokoll**
</dt> <dd>

Ein Protokoll, das nur in verteilten Transaktionen verwendet wird, stellt sicher, dass das Ergebnis einer Transaktion für alle Transaktions-Manager, die an der Transaktion teilnehmen, konsistent ist. Das Protokoll arbeitet in zwei unterschiedlichen Phasen, um letztendlich einen Commit oder Abbruch einer Transaktion auszuführen: Phase 1 wertet die Bedingung jedes Ressourcen-Managers aus, und Phase 2 schließt die Transaktion ab.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**Nicht konfigurierte Komponente**
</dt> <dd>

Eine COM-Komponente, die nicht im COM+-Katalog konfiguriert wurde. Nicht konfigurierte Komponenten können com+-Dienste nicht verwenden.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Aufenthaltsort**
</dt> <dd>

Bei DTC-Transaktionen eine nicht transparente Datenstruktur, die die Adresse des Transaktions-Managers des Ressourcen-Managers darstellt.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA-Schnittstellen**
</dt> <dd>

Ein Standardsatz von Programmierschnittstellen, mit denen COM+-Anwendungsentwickler auf XA-kompatible Datenbanken zugreifen und Ressourcen-Manager erstellen können, die mit relationalen Datenbanken, Nachrichtenwarteschlangen, Transaktionsdateien und objektorientierten Datenbanken arbeiten. Obwohl Microsoft das XA-Protokoll nicht direkt unterstützt, unterstützt Microsoft Übersetzungsmöglichkeiten zwischen OLE-Transaktionen und XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML-Webdienste**
</dt> <dd>

Einheiten der Anwendungslogik, die Daten und Dienste für andere Anwendungen bereitstellen. Anwendungen greifen über Standardwebprotokolle wie SOAP auf XML-Webdienste zu.

</dd> </dl>

 

 
