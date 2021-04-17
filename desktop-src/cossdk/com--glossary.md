---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Com+-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483158"
---
# <a name="com-glossary"></a>Com+-Glossar

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**Zugriffs Token**
</dt> <dd>

Ein-Objekt, das den Sicherheitskontext eines Prozesses oder Threads beschreibt. Die Informationen in einem Token enthalten die Identität und die Berechtigungen des dem Prozess oder Thread zugeordneten Benutzerkontos. Wenn sich ein Benutzer anmeldet, überprüft das System das Kennwort des Benutzers, indem es mit in einer Sicherheitsdatenbank gespeicherten Informationen vergleicht. Wenn das Kennwort authentifiziert ist, erstellt das System ein Zugriffs Token. Jeder Prozess, der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID-Eigenschaften**
</dt> <dd>

Ein Akronym, das von dem Transaktions Verarbeitungs Pionier für atomarisch, konsistent, isoliert und dauerhaft geprägt ist. Diese Eigenschaften stellen ein vorhersagbares Verhalten sicher und verstärken die Rolle von Transaktionen als all-oder-None-Angebote, um konsistente und vorhersagbare Ergebnisse in einer verteilten Umgebung bereitzustellen, wenn unabhängige Fehler auftreten können.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**Aktivierung**
</dt> <dd>

Die Kette der Ereignisse, die zur Erstellung eines COM-Objekts und zum Zurückgeben eines gültigen Zeigers auf eine Schnittstelle für dieses Objekt führt. In com+ wird ein Objekt entweder in einem eigenen Kontext oder in dessen Ersteller (ein Objekt, das das aktivierte Objekt angefordert hat) aktiviert. Com+-Dienste basieren auf der geeigneten Aktivierung eines Objekts, das auf der Konfiguration des Objekts basiert. Im Verlauf der Aktivierung bestimmt das System den Kontext, in dem das Objekt ausgeführt wird, initialisiert die Kontexteigenschaften, überprüft Zugriffsberechtigungen und richtet eine Sicherheitsidentität ein.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**Aktivierungs Sicherheit**
</dt> <dd>

Eine Form von Sicherheitsschutz, die bestimmt, wer einen Server starten kann. Die Aktivierungs Sicherheit wird automatisch durch den Dienststeuerungs-Manager (Service Control Manager, SCM) eines bestimmten Computers angewendet. Beim Empfang einer Anforderung von einem Client zum Aktivieren eines Objekts prüft der SCM die Anforderung anhand der in der Registrierung gespeicherten Aktivierungs Sicherheitsinformationen. Die Aktivierungs Sicherheit wird auch auf die gleichen Computer Aktivierungen geprüft. Wird auch als *Start Sicherheit* bezeichnet.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**Aktivierungstyp**
</dt> <dd>

Aktivierungs Kategorie für eine COM+-Anwendung, die angibt, ob die Anwendung im Prozessbereich des Clients (abhängig davon, ob es sich um eine Bibliothek oder eine Serveranwendung handelt) ausgeführt wird, und ob die Anwendung als Dienst ausgeführt wird.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**aktiv**
</dt> <dd>

In com+ ein logischer Thread, der eine oder mehrere Transaktionen umfasst und eine Auflistung von Komponenten enthält, die in einer COM+-Anwendung gruppiert sind. Jedes COM-Objekt gehört zu einer Aktivität. Die Zuordnung zwischen einem Objekt und einer Aktivität kann nicht geändert werden.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**Apartment modellprozess**
</dt> <dd>

Ein Prozess, der über mindestens zwei Single Thread-Apartments und keine Multithread-Apartments verfügt.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**Anwendungs Proxy**
</dt> <dd>

Ein Satz von Dateien, die Registrierungsinformationen enthalten, die einem Client den Remote Zugriff auf eine COM+-Serveranwendung ermöglichen. Bei der Installation auf einem Client Computer werden von der Anwendungs Proxy Dateiinformationen zur Serveranwendung auf den Client Computer geschrieben. der Client kann dann Remote auf die Serveranwendung zugreifen.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Genehmigung**
</dt> <dd>

Der Sicherheitsprozess, bei dem festgestellt wird, dass der Aufrufer einer Anwendung tatsächlich besagt, dass es sich um die Gültigkeit eines Identitäts Anspruchs handelt – Für COM+-Anwendungen kann die Authentifizierung auf administrativer Weise aktiviert und konfiguriert werden. danach funktioniert Sie transparent mit der Anwendung.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**Autorisierungs**
</dt> <dd>

Der Sicherheitsprozess, der bestimmt, ob ein Aufrufer einer Anwendung autorisiert ist, den Vorgang durchzuführen.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Caching-Ressourcen-Manager**
</dt> <dd>

Ein Ressourcen-Manager, der als Front-End zu einem anderen Ressourcen-Manager fungiert und Informationen lokal zwischenspeichert, wodurch die Kosten für den Zugriff auf die zugrunde liegende Ressource gesenkt werden. Anders als bei einem konventionellen Ressourcen-Manager ist ein Cache Ressourcen-Manager nicht an der Wiederherstellung beteiligt, da er die zugrunde liegenden Daten niemals dauerhaft speichert.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**Sicherheit anrufen**
</dt> <dd>

Eine Form von Sicherheitsschutz, mit der der Zugriff auf die Methoden eines Server Objekts nach dem Start eines Servers gesteuert werden kann.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**Klasse (com)**
</dt> <dd>

Eine benannte, konkrete Implementierung von einer oder mehreren Schnittstellen. Eine COM-Klasse wird durch eine CLSID und manchmal durch eine ProgID identifiziert.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**Cloaking**
</dt> <dd>

Die Fähigkeit eines Servers, seine eigene Identität bei Aufrufen im Auftrag eines Clients zu maskieren. Wenn das Cloaking aktiviert ist, können Aufrufe von dem Server, der die Identität des Clients annimmt, unter der Identität des Clients vorgenommen werden. Wenn das Cloaking deaktiviert ist, werden Aufrufe durch den Server unter der Identität des Servers vorgenommen.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Com+-Anwendung**
</dt> <dd>

Die primäre Verwaltungs-und Sicherheitseinheit für Komponenten Dienste. Eine COM+-Anwendung ist eine Gruppe von COM-Komponenten, die im allgemeinen verwandte Funktionen ausführen. Diese Komponenten bestehen weiter aus COM-Schnittstellen und-Methoden.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Com+-Anwendungs Pooling**
</dt> <dd>

Ein Komponenten Dienst Feature, mit dem Single Thread-Prozesse skaliert werden können. Außerdem können Sie Sie bei Fehlern in einzelnen Prozessen wiederherstellen, indem Sie andere laufende Prozesse zur Behandlung von Aktivierungen bereitstellen.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Com+-Anwendungs Wiederverwendung**
</dt> <dd>

Ein Komponenten Dienst Feature, das die Gesamtstabilität Ihrer Anwendungen erheblich erhöht, indem es Ihnen ermöglicht, einen Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß herunterzufahren und neu zu starten.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Com+-Katalog** 
</dt> <dd>

Der Datenspeicher, der com+-Konfigurationsdaten enthält. Die Leistung von com+-Verwaltungs Tasks erfordert das Lesen und Schreiben von Daten, die im Katalog gespeichert sind. Der Zugriff auf den Katalog ist nur über das Verwaltungs Programmkomponenten Dienste oder über die COMAdmin-Bibliothek möglich.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Com+-Ereignisse**
</dt> <dd>

Com+-Ereignisse stimmen mit einem locker gekoppelten Ereignis System überein und verbinden Verleger und Abonnenten. Ein Verleger führt den Methodenaufruf aus, um ein Ereignis zu initiieren, und ein Abonnent empfängt diese Aufrufe nicht direkt vom Verleger, sondern über das Ereignis System. Der com+-Ereignis Dienst verwaltet die Liste der Abonnenten, die die Anrufe erhalten, und leitet diese Anrufe weiter, ohne dass die Kenntnisse des Verlegers erforderlich sind.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Com+-Bibliotheks Anwendung**
</dt> <dd>

Eine COM+-Anwendung, die im Prozess des Clients ausgeführt wird, von dem Sie erstellt wird. Bibliotheksanwendungen können rollenbasierte Sicherheit verwenden, aber keinen Remote Zugriff oder in die Warteschlange eingereihten Komponenten unterstützen.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Com+-Objekt Pooling**
</dt> <dd>

Ein von com+ bereitgestellter automatischer Dienst, mit dem Sie eine-Komponente so konfigurieren können, dass Instanzen von selbst in einem Pool aktiv gehalten werden und von jedem Client verwendet werden können, der die Komponente anfordert.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Com+-Partitionen**
</dt> <dd>

Ein com+-Dienst, der auf einem einzelnen Computer die Erstellung separater Ausführungs Räume für Anwendungen ermöglicht.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Com+-Partitions Sätze**
</dt> <dd>

Eine Gruppe von COM+-Partitionen, die einer bestimmten Benutzer-ID in Active Directory zugeordnet sind.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Com+-Komponenten in der Warteschlange**
</dt> <dd>

Ein com+-Dienst, der auf Microsoft Message Queuing basiert und eine einfache Möglichkeit zum asynchronen Aufrufen und Ausführen von Komponenten bietet. Die Nachrichtenverarbeitung kann ohne Rücksicht auf die Verfügbarkeit oder den Zugriff des Absenders oder des Empfängers erfolgen.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+-Serveranwendung**
</dt> <dd>

Eine COM+-Anwendung, die in einem eigenen Prozess ausgeführt wird. Server Anwendungen können alle com+-Dienste unterstützen.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**com+-SOAP**
</dt> <dd>

Ein Komponenten Dienst Feature, mit dem Sie eine COM+-Anwendung als XML-Webdienst verfügbar machen können. Mit com+ SOAP können Sie auch einen XML-Webdienst als COM-Komponente verwenden.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM-Komponente**
</dt> <dd>

Eine binäre Einheit von Code, die Paket-und Registrierungscode umfasst und COM-Objekte erstellt. Alle com+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**Commit-Struktur**
</dt> <dd>

In einem verteilten Transaktionssystem die konzeptionelle Darstellung einer Transaktion als Grundlage der hierarchischen Beziehungen zwischen einzelnen Transaktions-Managern, die an einer verteilten Transaktion teilnehmen. In dieser Hierarchie sind die eingetragenen Ressourcen-Manager enthalten, die den Transaktions-Managern zugeordnet sind.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM-Objekt**
</dt> <dd>

Im COM-Programmiermodell ist eine Programmier Struktur, die sowohl Daten als auch Funktionen kapselt, die als einzelne Einheit definiert und zugeordnet sind und für die der einzige öffentliche Zugriff über die Schnittstellen der Programmier Struktur erfolgt. Ein COM-Objekt muss mindestens die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützen, die das vorhanden sein des Objekts während der Verwendung beibehält und Zugriff auf die anderen Schnittstellen des Objekts bietet.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Kompensierende Ressourcen-Manager (CRM)**
</dt> <dd>

Ein com+-Feature, mit dem nicht transaktionale Ressourcen an einer Zweiphasencommit-Transaktion mit dem Microsoft Distributed Transaction Coordinator (DTC) teilnehmen können. In der Regel bieten CRMs nicht die Isolations Funktionen von vollständigen Ressourcen-Managern, aber Sie bieten transaktionale Atomizität und Dauerhaftigkeit durch Schreiben in ein Protokoll.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Verwaltungs Tool für Komponenten Dienste**
</dt> <dd>

Ein Benutzeroberflächen-Snap-in, über das Administratoren und Entwickler com+-Anwendungen erstellen, konfigurieren und warten sowie verteilte Transaktionen und Speicher residente Datenbanken verwalten können. Mit dem Verwaltungs Programmkomponenten Dienste können auch Systemereignisse angezeigt und Systemdienste lokal auf dem Computer verwaltet werden, auf dem das Tool installiert ist.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**konzeptionelles Modell**
</dt> <dd>

Der erste Schritt in der com+-Anwendungs Entwurfsphase, in der der Entwickler die zu lösenden Geschäftsprobleme definiert und entscheidet, welche Komponenten und Dienste erforderlich sind.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**Concurrency**
</dt> <dd>

Die Fähigkeit von mehr als einer Transaktion oder einem Prozess, gleichzeitig auf dieselben Daten zuzugreifen. Com+ verwaltet die Parallelität im Allgemeinen durch Synchronisierung.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**konfigurierte Komponente**
</dt> <dd>

Eine COM-Komponente, die in einer COM+-Anwendung installiert wurde. Nach der Installation wird die Komponente im com+-Katalog konfiguriert, um die verfügbaren com+-Dienste nutzen zu können.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**Kontext**
</dt> <dd>

Ein Satz von Lauf Zeiteigenschaften, die einem oder mehreren COM-Objekten zugeordnet sind und zum Bereitstellen von Diensten für diese Objekte verwendet werden. Jedes COM-Objekt wird in einem einzigen Kontext von der Aktivierung bis zur Deaktivierung ausgeführt (immer innerhalb desselben Apartment). Wird initialisiert, wenn ein Objekt aktiviert wird. Kontexteigenschaften, wie z. b. Sicherheitskontext Eigenschaften, stellen die Lauf Zeitanforderungen eines Objekts dar.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**Datenebene**
</dt> <dd>

Das dreistufige Architekturmodell für Geschäftsanwendungen, die DBMS-Zugriffsebene, auf die über die mittlere Ebene, über die Business Services-Ebene und gelegentlich über die Präsentationsebene oder über die Benutzer Dienst Ebene zugegriffen werden kann. Die Datenebene besteht aus Datenzugriffs Komponenten (anstelle von unformatierten DBMS-Verbindungen), um die Ressourcen Freigabe zu unterstützen und Clients zu ermöglichen, ohne die DBMS-Bibliotheken und ODBC-Treiber auf jedem Client zu installieren. Wird auch als *Data Services-Ebene* bezeichnet.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Sackgasse**
</dt> <dd>

Bei Multithreadanwendungen ein Threading Problem, das auftritt, wenn jedes Mitglied einer Gruppe von Threads auf einen anderen Member des Satzes wartet.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegations**
</dt> <dd>

Eine Form des Identitäts Wechsels, die einen Server autorisiert, auf den Namen eines Clients zu reagieren. Dadurch kann der Server die Identität des Clients über das Netzwerk annehmen.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**verteilte Transaktion**
</dt> <dd>

Eine Transaktion, die mehrere Ressourcen-Manager umfasst, die sich auf demselben Computer oder auf unterschiedlichen Computern befinden können.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**
</dt> <dd>

Ein-Systemdienst, der Transaktionen und transaktionsbezogene Kommunikationen verwaltet, die auf einem oder mehreren Systemen auf zwei oder mehr Ressourcen-Manager verteilt werden, um korrekte ACID-Transaktionen sicherzustellen.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**Dynamisches Cloaking**
</dt> <dd>

Eine Art von Verstopfungen, bei der die ursprüngliche Client Identität bei jedem Methodenaufrufe des Downstreamservers als Server Thread-Zugriffs Token erkannt wird. Obwohl die angegebene Identität dynamisch bestimmt werden kann, kann der Aufwand, der dazu erforderlich ist, erheblich teurer werden. Für COM+-Anwendungen ist die Standardkonfiguration für die Funktion für dynamisches abgleichen vorgesehen, da Sie die Flexibilität bereitstellt, die normalerweise von Umständen benötigt wird, die die Verwendung des Identitäts Wechsels an erster Stelle erfordern.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**Enumeratorobjekt**
</dt> <dd>

Ermöglicht das Aufzählen der Elemente in einer Auflistung.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**Veranstalter**
</dt> <dd>

Eine Aktion, die von einem Objekt erkannt wird, z. b. das Klicken auf die Maus oder das Drücken einer Taste, und für das Sie Code schreiben können, der antwortet.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**Event Class-Objekt**
</dt> <dd>

Eine konfigurierte Komponente, die einen persistenten Datensatz im com+-Ereignis System bereitstellt, um die Herausgeber und die auslösenden Schnittstellen zu beschreiben

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**Ereignismethode**
</dt> <dd>

Eine Methode in einer COM+-Schnittstelle, die ein com+-Ereignis identifiziert. Ereignis Methoden müssen eindeutig benannt werden und dürfen nur Eingabeparameter enthalten. Der Rückgabewert muss ein **HRESULT** sein.

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**Ereignis Objekt**
</dt> <dd>

Ein COM-Objekt, das einem oder mehreren Threads signalisieren kann, dass ein Ereignis aufgetreten ist. Jeder Thread in einem Prozess kann ein Ereignis Objekt erstellen.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**distanzieren**
</dt> <dd>

Eine ungewöhnliche Bedingung oder ein Fehler, die während der Ausführung eines Programms auftritt und die Ausführung von Software außerhalb der normalen Ablauf Steuerung erfordert.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**Failover**
</dt> <dd>

In einem Cluster Netzwerksystem der Prozess, bei dem ein überladener oder fehlerhafter Ressourcen – wie z. b. ein Server, ein Laufwerk oder ein Netzwerk – zu seiner Sicherungs Komponente verschoben werden.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**frei Thread Prozess**
</dt> <dd>

Ein Prozess, der über ein Multithread-Apartment und keine Single Thread-Apartments verfügt.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**globaler Commit-Koordinator**
</dt> <dd>

Der Stamm Transaktions-Manager der commitstruktur auf einem Microsoft Windows – basierten verteilten Transaktionssystem. Dieser Koordinator trifft die Entscheidung, eine bestimmte Transaktion entweder zu commitden oder abzubrechen und ist nie unsicher.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**Identitätswechsel**
</dt> <dd>

Die Fähigkeit eines Threads, in einem Sicherheitskontext auszuführen, der sich von dem Prozess unterscheidet, der den Thread besitzt. Der Server Thread verwendet ein Zugriffs Token, das die Anmelde Informationen des Clients darstellt, und damit kann er auf Ressourcen zugreifen, auf die der Client zugreifen kann.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**Identitätswechsel Ebene**
</dt> <dd>

Die Einstellung, die vom Client verwendet wird, um dem Server eine bestimmte Berechtigungsebene zum Ausführen von Aktionen im Auftrag des Clients zu erteilen. In com+ kann dies nur für com+-Server Anwendungen festgelegt werden.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**geschützt**
</dt> <dd>

Für ein Objekt, das in einem bestimmten Kontext aktiviert ist, der Prozess der Verarbeitung von Aufrufen an dieses Objekt über die Kontext Grenze hinweg. Aufrufe über den Kontext werden mithilfe von Lightweight-Schnittstellen Proxys verarbeitet, die alle erforderlichen Vermittlungsarbeiten zur Anpassung der Laufzeitumgebung von einem verwenden, der den Aufrufer für den aufgerufener verwendet.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**berfläche**
</dt> <dd>

Bei der com-basierten Programmierung eine Auflistung von zugehörigen öffentlichen Funktionen, die Zugriff auf ein COM-Objekt bereitstellen. Der Satz von Schnittstellen für ein COM-Objekt besteht aus einem Vertrag, der angibt, wie Programme und andere Objekte mit dem COM-Objekt interagieren können.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**Schnittstellen Proxy**
</dt> <dd>

Ein Schnittstellen spezifisches Objekt, das die Parameter für diese Schnittstelle für die Vorbereitung eines Remote Methoden Aufrufes verpackt und die Rückgabewerte aus dem schnittstellenstub entpackt (marshunkt). Ein Proxy wird im Adressraum des Absenders ausgeführt und kommuniziert mit einem entsprechenden Stub im Adressraum des Empfängers.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**schnittstellenstub**
</dt> <dd>

Ein Schnittstellen spezifisches Objekt, das gemarshallte Parameter entpackt, die erforderliche Methode aufruft und Pakete (Marshaller) Werte von der aufgerufenen Methode zurückgibt. Der Stub wird im Adressraum des Empfängers ausgeführt und kommuniziert mit einem entsprechenden Schnittstellen Proxy im Adressbereich des Absenders.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**Inneres Objekt**
</dt> <dd>

In einer transaktionalen Hierarchie ein beliebiges Objekt unter dem Stamm Objekt.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**Just-in-time (JIT)-Aktivierung**
</dt> <dd>

Ein von com+ bereitgestellter automatischer Dienst, mit dem Server Ressourcen im Leerlauf produktiver verwendet werden können. Wenn eine Komponente als JIT aktiviert konfiguriert ist, kann com+ eine Instanz davon deaktivieren, während ein Client weiterhin einen aktiven Verweis auf das Objekt enthält. Wenn der Client das nächste Mal eine Methode für das Objekt aufruft, aktiviert com+ das Objekt auf die gleiche Weise transparent auf dem Client, Just-in-Time.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**Legacy Komponente**
</dt> <dd>

Eine nicht konfigurierte Komponente, die in einer COM+-Anwendung installiert wurde.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**empfunden**
</dt> <dd>

Ein Architecture-Element des com+-Dienstanbieter in der Warteschlange. Der Listener ist ein COM-Objekt, das die der Host Anwendung zugeordnete Meldungs Warteschlange öffnet und darauf wartet, dass Nachrichten eintreffen. Beim Eintreffen von Nachrichten sendet der Listener Threads, die Nachrichten verarbeiten.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logisches Modell**
</dt> <dd>

Der zweite Schritt in einem com+-Anwendungs Entwurfsprozess, bei dem das konzeptionelle Modell wie folgt in die logischen Ebenen der dreistufigen Architektur aufgeteilt wird: die Präsentationsebene oder die Benutzerdienste. die mittlere Ebene oder Unternehmens Dienste; und die Datenebene oder Datendienste.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**lose gekoppelter Ereignis**
</dt> <dd>

Ein Ereignis, dessen Absender (Verleger) und Empfänger (Abonnent) nicht eng gebunden sind. In einem locker gekoppelten Ereignis System, z. b. com+-Ereignisse, werden Ereignis Informationen von verschiedenen Verlegern in einem Ereignisspeicher persistent gespeichert. Abonnenten Fragen diesen Speicher ab und wählen die Ereignisse aus, die Sie empfangen möchten. Durch die Auswahl von Ereignis Informationen aus dem Ereignisspeicher wird ein Abonnement erstellt. Wenn ein Ereignis auftritt, sucht das Ereignis System in dieser Datenbank nach den interessierten Abonnenten, erstellt ein neues Objekt für jede interessierte Klasse und ruft eine Methode für dieses Objekt auf.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**Marshalling**
</dt> <dd>

Der Prozess, bei dem Schnittstellen Methoden Parameter über Thread-oder Prozess Grenzen hinweg verpackt und entpacken werden, sodass ein Remote Prozedur Rückruf stattfinden kann.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**Nachrichten Verschiebe Vorgang**
</dt> <dd>

Das Architecture-Element des com+-Dienstanbieter für die Warteschlange, der fehlerhafte Nachrichten zurück in die Eingabe Warteschlange verschiebt, damit Sie wiederholt werden können.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**Meta-Ereignis**
</dt> <dd>

Ein Ereignistyp, der vom com+-Ereignis System verwendet wird, um interessierte Abonnenten zu benachrichtigen, wenn Ereignis Klassen Objekte oder-Abonnements erstellt, geändert oder entfernt werden.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**anzuwenden**
</dt> <dd>

Bei der com-basierten Programmierung ein Prozess, der von einem COM-Objekt ausgeführt wird, wenn eine Nachricht empfangen wird.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**mittlere Ebene**
</dt> <dd>

Im dreistufigen Architekturmodell für Geschäftsanwendungen die Ebene, die die Geschäftslogik und die Daten Regeln umfasst. Die Komponenten, aus denen die mittlere Ebene besteht, können verwendet werden, um Geschäftsregeln zu erzwingen, z. b. Geschäfts Algorithmen, gesetzliche oder behördliche Vorschriften und Daten Regeln, die so entworfen wurden, dass die Datenstrukturen innerhalb bestimmter oder mehrerer Datenbanken konsistent bleiben. Da diese Komponenten der mittleren Ebene nicht an einen bestimmten Client gebunden sind, können Sie von allen Anwendungen verwendet werden und können als Antwortzeit und andere Regeln an verschiedene Speicherorte verschoben werden. Wird auch als *Geschäfts Dienst Ebene* oder *Geschäftslogik Ebene* bezeichnet.

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**Gemischter modellprozess**
</dt> <dd>

Ein Prozess, der über ein Multithread-Apartment und eine oder mehrere Single Thread-Apartments verfügt.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Ein Name, der ein COM-Objekt eindeutig identifiziert. Auf dieselbe Weise, wie ein Pfad eine Datei im Dateisystem identifiziert, identifiziert ein Moniker ein COM-Objekt im Verzeichnis Namespace.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**MSI-Datei**
</dt> <dd>

Eine Datei, die vom Verwaltungs Programmkomponenten Dienste beim Exportieren einer COM+-Anwendung oder eines Anwendungs Proxys für die Installation auf einem anderen Computer erstellt wurde. Die MSI-Datei kann auf jedem Windows-basierten Client mithilfe Windows Installer installiert werden.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**Multithread-Apartment Modell**
</dt> <dd>

Ein Apartment Modell, in dem alle Threads im Prozess, die als "frei Thread" initialisiert wurden, sich in einem einzigen Apartment befinden. Daher ist es nicht erforderlich, zwischen Threads zu Mars Hallen. Die Threads müssen keine Nachrichten abrufen und verteilen, weil com in diesem Modell keine Fenster Meldungen verwendet.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**eine Transaktion**
</dt> <dd>

Eine sekundäre Transaktion, die von innerhalb einer vorhandenen primären oder übergeordneten Transaktionsgrenze initiiert wurde. Der Commit der primären Transaktion wird erst durchführt, wenn alle untergeordneten oder nicht untergeordneten Transaktionen committet wurden. Com+ unterstützt keine netsted Transactions.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutrales Apartment Modell**
</dt> <dd>

Ein Threading Modell, in dem Objekte den Richtlinien für multithreadwohnungen entsprechen, aber in jeder Art von Thread ausgeführt werden können. Das neutrale Apartment Modell ist das empfohlene Threading Modell für COM-Komponenten und com+-Anwendungen.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistentes Objekt**
</dt> <dd>

Ein COM-Objekt, das seinen internen Zustand speichern kann, wenn es von einem Client dazu aufgefordert wird und com-definierte Standards entspricht, über die Clients das Initialisieren, laden und Speichern von Objekten in einem Datenspeicher anfordern können (z. b. Flatfile, strukturierter Speicher oder Arbeitsspeicher). Der Client ist dafür verantwortlich, den Speicherort zu verwalten, an dem die persistenten Daten des Objekts gespeichert werden, aber nicht das Format der Daten.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistente Objektschnittstelle**
</dt> <dd>

Eine COM-Schnittstelle, die von einem permanenten Objekt implementiert wird. Clients verwenden persistente Objekt Schnittstellen, um den persistenten Objekten mitzuteilen, wann und wo ihr Zustand gespeichert werden soll.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**Benachrichtigungs Schnittstelle für Phase Zero**
</dt> <dd>

Com+-Schnittstelle, die es Anwendungen ermöglicht, zu erkennen, wann eine Transaktion mit einem Zweiphasencommit-Protokoll fortgesetzt werden kann, um die erforderlichen Benachrichtigungs Vorgänge auszuführen und mit dem Transaktions-Manager zu kommunizieren, wenn die Vorgänge abgeschlossen sind.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physisches Modell**
</dt> <dd>

Der dritte und letzte Schritt im com+-Anwendungs Entwurfsprozess, bei dem der Entwickler bestimmt, wo sich die Komponenten physisch befinden und wie Sie codiert werden sollen.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Feldspieler**
</dt> <dd>

Das Architecture-Element des com+-Dienstanbieter für die Warteschlange, der die Nachricht aus einer Warteschlange abruft und dann das Server Objekt und die standardschnittstellenstubvorgänge lädt, um Daten zu entfernen und Server Methoden aufzurufen. Der Player gibt den Sicherheitskontext des Clients auf der Serverseite aus und ruft dann die Serverkomponente auf und führt die gleichen Methodenaufrufe aus. Die Methodenaufrufe werden vom Player nicht wiedergegeben, bis die Client Komponente abgeschlossen ist, und die Transaktion, die die Methode aufgezeichnet hat, führt Commits aus.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**Präsentationsebene**
</dt> <dd>

In den dreistufigen Architekturmodellen für Geschäftsanwendungen die Ebene, die Daten für den Benutzer darstellt und optional Datenbearbeitung und Dateneingabe zulässt. Die zwei Haupttypen von Benutzeroberflächen für die Präsentationsebene sind die herkömmliche Anwendung und die webbasierte Anwendung. Wird auch als *Benutzer Dienst Ebene* bezeichnet.

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primäres Zugriffs Token**
</dt> <dd>

Beschreibt den Sicherheitskontext des Benutzerkontos, das einem Prozess zugeordnet ist.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Proxy-Manager**
</dt> <dd>

Beim Standardmarshalling eine Komponente, die alle Schnittstellen Proxys für ein einzelnes Objekt verwaltet.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**Pseudo Objekt**
</dt> <dd>

Ein Typ eines enthaltenen Objekts, z. b. eine Benutzer Auswahl in einem Dokument, ein Bereich von Zellen in einer Kalkulations Tabelle oder ein Zeichenbereich in einem Textdokument. Dieser Objekttyp wird als Pseudo Objekt bezeichnet, da es nicht als eindeutiges Objekt behandelt wird, bis ein Benutzer die Auswahl markiert.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**Gebers**
</dt> <dd>

Der Absender eines Ereignisses. In der Architektur der com+-Ereignisse führt der Herausgeber den Methoden aufzurufen, um ein Ereignis zu initiieren.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**Warteschlangen-Moniker**
</dt> <dd>

Der Moniker, mit dem eine in der Warteschlange befindliche Komponente aktiviert wird.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**Racebedingung**
</dt> <dd>

Eine Bedingung in einer Multithreadanwendung, die auftritt, wenn mehrere Threads auf ein Datenelement ohne Koordination zugreifen und möglicherweise inkonsistente Ergebnisse verursachen, je nachdem, welcher Thread zuerst das Datenelement erreicht. COM bietet einige Funktionen, die speziell entwickelt wurden, um Racebedingungen in Prozess externen Servern zu vermeiden.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**aufzunehmen**
</dt> <dd>

Das Architecture-Element des com+-Diensts für Warteschlangen Komponenten, der den Sicherheitskontext des Clients in eine Nachricht marshallt und alle Methodenaufrufe für ein Objekt aufzeichnet. Der Recorder ist ein vom System bereitgestellter Proxy Manager, der Schnittstellen aus den Warteschlangen fähigen Schnittstellen im com+-Katalog auswählt.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**Ressourcen Verteiler**
</dt> <dd>

Eine Komponente im COM+-Programmiermodell, die den nicht permanenten Freigabe Zustand im Namen der Anwendungskomponenten innerhalb eines Prozesses verwaltet. Ressourcen Spender ähneln Ressourcen-Managern, ohne dass die Dauerhaftigkeit gewährleistet ist.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Ressourcen-Manager**
</dt> <dd>

Ein Dienst, der persistente oder dauerhafte Daten in Datenbanken, permanenten Nachrichten Warteschlangen oder transaktionalen Dateisystemen verwaltet. Es ist der Ressourcen-Manager, der weiß, wie Daten gespeichert und eine Notfall Wiederherstellung durchgeführt werden. Com+-Server Anwendungen verwenden Ressourcen-Manager, um den dauerhaften Status einer Anwendung aufrechtzuerhalten, z. b. den Datensatz des Bestands, ausstehende Bestellungen und Konten, die Sie empfangen können. Ressourcen-Manager arbeiten in Zusammenarbeit mit dem Microsoft Distributed Transaction Coordinator (DTC) zusammen, um die Unteilbarkeit und Isolation von Anwendungen zu gewährleisten.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**Rollenbasierte Sicherheit**
</dt> <dd>

Ein com+-Sicherheitsdienst für COM+-Anwendungen. Eine Rolle stellt eine Kategorie von Benutzern dar, die für eine COM+-Anwendung definiert sind, um die Zugriffsberechtigungen für die Ressourcen der Anwendung zu bestimmen. Rollen werden von einem Entwickler Komponenten, Schnittstellen und Methoden zugewiesen. Benutzer werden von einem Administrator den entsprechenden Rollen zugewiesen, sodass ein Benutzer in einer bestimmten Rolle auf alle Ressourcen zugreifen kann, denen diese Rolle zugewiesen ist.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**Root-Objekt**
</dt> <dd>

Das erste Objekt einer Transaktion, das als Stamm der Transaktion bezeichnet wird und immer in einer neuen Transaktionsgrenze platziert wird. Es darf nur ein Stamm Objekt in einer Transaktion vorhanden sein. Alle anderen Objekte in der transaktionalen Hierarchie unter dem Root-Objekt werden als innere Objekte bezeichnet.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**stammtransaktions-Manager**
</dt> <dd>

Der Transaktions-Manager auf dem System, der eine Transaktion initiiert. Die Transaktion wird erst beendet, wenn der Stamm Transaktions-Manager den Status der Transaktion ermittelt hat (entweder zugesichert oder abgebrochen).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**Semaphor**
</dt> <dd>

Ein Kernel Objekt, das verwendet wird, um den Zugriff auf eine freigegebene Ressource zu bestimmen.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Dienststeuerungs-Manager (SCM)**
</dt> <dd>

Ein Microsoft Windows Server-Prozess, mit dem alle Dienste in der Windows-Registrierung verwaltet werden.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**frei gegebener Eigenschaften-Manager (SPM)**
</dt> <dd>

In com+ ein Ressourcen Verteiler, den Sie verwenden können, um einen nicht persistenten Status für mehrere Objekte innerhalb eines Server Prozesses freizugeben.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**Single Thread-Prozess**
</dt> <dd>

Ein Prozess, der aus nur einem Single Thread-Apartment besteht, das wiederum genau einen Thread umfasst. Alle COM-Objekte, die in einem Single Thread-Apartment Leben, können Methodenaufrufe von nur einem Thread empfangen, der zu diesem Apartment gehört.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**Soester**
</dt> <dd>

Ein einfaches XML-basiertes Protokoll zum Austauschen strukturierter und Typinformationen im Web. Das Protokoll enthält keine Anwendungs-oder Transport Semantik, wodurch es stark modular und erweiterbar ist.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**geteilte Registrierung**
</dt> <dd>

Für Komponenten, die bereits vorhandene COM-Komponenten sind und in der com+-Dienst Umgebung verwendet werden, wird die Registrierungs Anordnung, bei der der grundlegende com-Aspekt der Registrierung in der Windows-Registrierung gespeichert ist, und neue COM+-Dienste und-Attribute (z. b. in der Warteschlange befindliche Komponenten) in der COM+-Registrierungsdatenbank gespeichert. Die einzelnen Komponenten Attribute werden entweder in der Windows-Registrierung oder in der COM+-Registrierungsdatenbank gespeichert. Neue COM-Komponenten werden ausschließlich in der COM+-Registrierungsdatenbank registriert, wobei eine Duplizierung in der Windows-Registrierung möglich ist, damit vorhandene Tools Sie verwenden können.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**Zustands behafteten**
</dt> <dd>

Von oder im Zusammenhang mit einem System oder Prozess, das alle Details des Zustands einer Aktivität überwacht, an der es beteiligt ist.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**Zustands losen**
</dt> <dd>

Von oder im Zusammenhang mit einem System oder Prozess, der an Aktivitäten teilnimmt, ohne alle Details seines Zustands zu überwachen.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**statischer Cloaking**
</dt> <dd>

Eine Art von Verstopfungen, bei der die ursprüngliche Client Identität einmal an einen Downstreamserver präsentiert werden kann, wobei die ursprüngliche Client Identität einmal auf dem Proxy festgelegt wird. Diese Client Identität wird als Server Thread Token dargestellt, das bei nachfolgenden Methoden aufrufen verwendet wird.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Abonnenten**
</dt> <dd>

Der Empfänger eines Ereignisses. In der Architektur der com+-Ereignisse empfängt der Abonnent die vom Verleger ausgeführten Aufrufe.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**Abonnement Objekt**
</dt> <dd>

Ein Objekt im com+-Ereignis System, das von einem Abonnenten erstellt wurde, um die Übermittlung von Ereignissen anzufordern und zu verwalten.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchron**
</dt> <dd>

In com+ ein Dienst, der von Komponente zu Komponente fließt und verhindert, dass mehr als ein Aufrufer zu einem bestimmten Zeitpunkt in die Komponente wechselt. Die Synchronisierung bestimmt, wann Threads Aufrufe an ein-Objekt senden können.

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**dreistufiges Architekturmodell**
</dt> <dd>

Das grundlegende Framework für das logische Entwurfs Modell segmentiert die Komponenten einer Anwendung wie folgt in drei Dienst Ebenen: die Präsentationsebene oder die Benutzerdienste. die mittlere Ebene oder Unternehmens Dienste; und die Datenebene oder Datendienste. Diese Ebenen entsprechen nicht notwendigerweise physischen Standorten auf verschiedenen Computern in einem Netzwerk, sondern eher auf logischen Ebenen der Anwendung.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**eng verbundenes Ereignis**
</dt> <dd>

Ein Ereignis, dessen Absender (Verleger) und Empfänger (Abonnent) eng gebunden sind. In einem eng gekoppelten Ereignis System wird dem Verleger eine Schnittstelle zur Verfügung gestellt, auf der eine Methode aufgerufen werden soll, wenn eine Änderung auftritt. Der Abonnent weiß, von welchem Verleger eine Benachrichtigung angefordert werden soll, und die verfügbaren Schnittstellen. Ein eng gekoppeltes Ereignis System erfordert, dass sowohl der Verleger als auch der Abonnent jederzeit ausgeführt werden.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Ablauf Verfolgungs Protokoll**
</dt> <dd>

Eine Protokolldatei, die automatisch vom Microsoft-Distributed Transaction Coordinator generiert wird und Daten enthält, die mit einer oder mehreren verteilten Transaktionen verknüpft sind. Beispiele für Daten in einem Ablauf Verfolgungs Protokoll sind Transaktions-ID, Transaktionszeit und Nachrichten, die das Transaktions Ergebnis angeben.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**Geschäfte**
</dt> <dd>

Eine Arbeitseinheit, bei der während eines Anwendungsprozesses eine Reihe verwandter Vorgänge stattfindet. Eine Transaktion wird genau einmal ausgeführt und ist atomarisch – entweder ist entweder die gesamte Arbeit abgeschlossen, oder es ist kein Wert.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (Tipp)**
</dt> <dd>

Das Internetprotokoll der Transaktion ist ein Standardmäßiges Zweiphasencommit-Protokoll, das heterogenen Transaktions-Managern ermöglicht, verteilte Transaktionen zu koordinieren, insbesondere über das Internet. Das Zweiphasencommit-Protokoll von Tip ist einfach zu implementieren und ist unabhängig vom Anwendungs-zu-Anwendungs-Kommunikationsprotokoll, sodass es mit jedem beliebigen Anwendungsprotokoll, jedoch insbesondere mit http, verwendet werden kann.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Transaktions-Manager**
</dt> <dd>

Der Teil des Microsoft Distributed Transaction Coordinator (DTC), der auf allen Computern ausgeführt wird, die an einer verteilten Transaktion teilnehmen und die Aktivitäten im Zusammenhang mit dem Commit oder Abbruch dieses Teils der Transaktion verwalten.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**Transaktions Verarbeitungs Anwendung**
</dt> <dd>

Eine Auflistung von Transaktions Vorgängen, die eine bestimmte Geschäftsaufgabe automatisieren.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**Transaktions Verarbeitungssystem**
</dt> <dd>

Ein vollständiges System, das sowohl Computer Hardware als auch Software umfasst, das eine Transaktions Verarbeitungs Anwendung hostet, um routinemäßige Transaktionen auszuführen, die für das Durchführen von Geschäfts

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Zweiphasencommit-Protokoll**
</dt> <dd>

Ein Protokoll, das nur in verteilten Transaktionen verwendet wird, stellt sicher, dass das Ergebnis einer Transaktion über alle Transaktions-Manager hinweg konsistent ist, die an der Transaktion beteiligt sind. Das Protokoll arbeitet in zwei unterschiedlichen Phasen, um letztendlich einen Commit oder Abbruch einer Transaktion durchzusetzen: Phase 1 wertet die Bedingung der einzelnen Ressourcen-Manager aus, und Phase 2 schließt die Transaktion ab.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**nicht konfigurierte Komponente**
</dt> <dd>

Eine COM-Komponente, die nicht im com+-Katalog konfiguriert wurde. Nicht konfigurierte Komponenten können die com+-Dienste nicht verwenden.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Positions**
</dt> <dd>

Für DTC-Transaktionen eine nicht transparente Datenstruktur, die die Adresse des Transaktions-Managers des Ressourcen-Managers darstellt.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA-Schnittstellen**
</dt> <dd>

Ein Standardsatz von Programmierschnittstellen, die com+-Anwendungsentwicklern ermöglichen, auf XA-kompatible Datenbanken zuzugreifen und Ressourcen-Manager zu erstellen, die mit relationalen Datenbanken, Message Queueing, Transaktions Dateien und objektorientierten Datenbanken arbeiten. Obwohl Microsoft das XA-Protokoll nicht direkt unterstützt, unterstützt Microsoft Übersetzungsfunktionen zwischen OLE-Transaktionen und XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML-Webdienste**
</dt> <dd>

Einheiten der Anwendungslogik, die Daten und Dienste für andere Anwendungen bereitstellt. Anwendungen greifen mithilfe standardmäßiger Webprotokolle wie SOAP auf XML-Webdienste zu.

</dd> </dl>

 

 
