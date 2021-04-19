---
title: COM-Glossar
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339516"
---
# <a name="com-glossary"></a>COM-Glossar

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**Aktivierung**
</dt> <dd>

Der Prozess, bei dem ein Objekt in den Arbeitsspeicher geladen wird, das in den Status wird ausgeführt versetzt wird.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**aktiver Status**
</dt> <dd>

Ein COM-Objekt, das sich im Status wird ausgeführt befindet und über eine sichtbare Benutzeroberfläche verfügt.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absoluter Moniker**
</dt> <dd>

Ein Moniker, der den absoluten Speicherort eines Objekts angibt. Ein absoluter Moniker ist analog zu einem vollständigen Pfad.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**Beratender Inhaber**
</dt> <dd>

Ein COM-Objekt, das Benachrichtigungen über Änderungen an den Beratungs senken von Container Anwendungen zwischenspeichert, verwaltet und sendet.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**Beratungs Senke**
</dt> <dd>

Ein COM-Objekt, das Benachrichtigungen über Änderungen in einem eingebetteten Objekt oder verknüpften Objekt empfangen kann, da es die [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) -oder [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) -Schnittstelle implementiert. Container, die über Änderungen in Objekten benachrichtigt werden müssen, implementieren eine Beratungs Senke. Benachrichtigungen stammen aus dem Server, der ein beratendes Halter Objekt zum Zwischenspeichern und Verwalten von Benachrichtigungen an Container verwendet.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**Aggregat Objekt**
</dt> <dd>

Ein COM-Objekt, das aus einem oder mehreren anderen COM-Objekten besteht. Ein Objekt im Aggregat ist das steuernde Objekt, das steuert, welche Schnittstellen im Aggregat verfügbar gemacht und welche privat sind. Dieses steuernde Objekt verfügt über eine spezielle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Implementierung, die als kontrollierendes **IUnknown** bezeichnet wird. Alle Objekte im Aggregat müssen Aufrufe an **IUnknown** -Methoden über die steuernde **IUnknown**-Methode übergeben.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**Stellung**
</dt> <dd>

Eine Kompositionstechnik zum Implementieren von COM-Objekten. Damit können Sie ein neues-Objekt erstellen, indem Sie mindestens eine der Schnittstellen Implementierungen vorhandener Objekte wieder verwenden. Das Aggregat Objekt wählt aus, welche Schnittstellen für Clients verfügbar gemacht werden, und die Schnittstellen werden so verfügbar gemacht, als wären Sie durch das Aggregat Objekt implementiert worden. Clients des Aggregat Objekts kommunizieren nur mit dem Aggregat Objekt.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**Ambient-Eigenschaft**
</dt> <dd>

Eine Lauf Zeit Eigenschaft, die verwaltet und vom Container verfügbar gemacht wird. In der Regel stellt eine Ambient-Eigenschaft eine Eigenschaft eines Formulars dar, z. b. Hintergrundfarbe, die an ein Steuerelement übermittelt werden muss, damit das Steuerelement das Aussehen und Gefühl der umgebenden Umgebung annehmen kann.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**Anti-Moniker**
</dt> <dd>

Die Umkehrung einer Datei, eines Elements oder eines zeigermonikers. Ein Anti-Moniker wird am Ende einer Datei, eines Elements oder eines zeigermonikers hinzugefügt, um ihn zu nullisieren. Anti-Moniker werden bei der Erstellung relativer Moniker verwendet.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**künstliche Verweis Zählung**
</dt> <dd>

Eine Technik, die verwendet wird, um ein Objekt vor dem Aufrufen einer Funktion oder Methode zu schützen, die das Objekt vorzeitig zerstören könnte. Ein Programm ruft **IUnknown:: adressf** auf, um den Verweis Zähler des Objekts zu erhöhen, bevor er den Aufruf durchführen kann, der das Objekt freigeben könnte. Nachdem die Funktion zurückgegeben wurde, ruft das Programm **IUnknown:: Release** auf, um die Anzahl zu verringern.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchrone Bindung**
</dt> <dd>

Ein Bindungstyp, bei dem der Prozess asynchron ausgeführt werden muss, um Leistungseinbußen für den Endbenutzer zu vermeiden. In der Regel wird die asynchrone Bindung in verteilten Umgebungen wie dem World Wide Web verwendet. OLE unterstützt asynchrone Monikerklassen und Rückruf Mechanismen, die das Auffinden und Initialisieren eines Objekts in einer verteilten Umgebung ermöglichen, während andere Vorgänge ausgeführt werden.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchroner Rückruf**
</dt> <dd>

Ein Aufruf einer Funktion, die separat ausgeführt wird, sodass der Aufrufer die Verarbeitung von Anweisungen fortsetzen kann, ohne darauf zu warten, dass die Funktion zurückgibt.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchroner Moniker**
</dt> <dd>

Ein Moniker, der die asynchrone Bindung unterstützt. Instanzen der vom System bereitgestellten URL-Monikerklasse sind z. b. asynchrone Moniker.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**sierungen**
</dt> <dd>

Eine Möglichkeit, die Objekte einer Anwendung von außerhalb der Anwendung zu bearbeiten. Automation wird in der Regel zum Erstellen von Anwendungen verwendet, die Objekte für Programmier Tools und Makro Sprachen verfügbar machen, die Objekte einer Anwendung aus anderen Anwendungen erstellen und bearbeiten oder Tools für den Zugriff und die Bearbeitung von Objekten erstellen.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**Bindungs Kontext**
</dt> <dd>

Ein COM-Objekt, das die [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) -Schnittstelle implementiert. Bindungs Kontexte werden in monikervorgängen verwendet, um Verweise auf die Objekte zu speichern, die aktiviert werden, wenn ein Moniker gebunden ist. Der Bindungs Kontext enthält Parameter, die für alle Vorgänge während der Bindung eines generischen zusammengesetzten Monikers gelten und die monikerimplementierung mit Zugriff auf Informationen über Ihre Umgebung bereitstellt.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**lichere**
</dt> <dd>

Zuordnen eines Namens zu seinem Referenten Insbesondere das Auffinden des Objekts, das von einem Moniker benannt wird, wobei es den Status "wird ausgeführt" aufweist, wenn es nicht bereits vorhanden ist, und ein Schnittstellen Zeiger darauf zurückgibt. Objekte können zur Laufzeit (auch als späte Bindung oder dynamische Bindung bezeichnet) oder zur Kompilierzeit (auch als statische Bindung bezeichnet) gebunden werden.

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**Speichern**
</dt> <dd>

Ein (normalerweise temporär) lokaler Informationsspeicher. In OLE enthält ein Cache Informationen, die die Darstellung eines verknüpften oder eingebetteten Objekts definieren, wenn der Container geöffnet wird.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**Cache Initialisierung**
</dt> <dd>

Auffüllen des Caches eines verknüpften oder eingebetteten Objekts mit Präsentationsdaten. Die [**iolecache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) -Schnittstelle stellt Methoden bereit, die ein Container zum Steuern der Daten, die für verknüpfte oder eingebettete Objekte zwischengespeichert werden, aufruft.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**klassi**
</dt> <dd>

Die Definition eines Objekts im Code. In C++ ist die Klasse eines Objekts als Datentyp definiert, aber dies ist in anderen Sprachen nicht der Fall. Da OLE in jeder Sprache codiert werden kann, wird die-Klasse verwendet, um auf die allgemeine Objektdefinition zu verweisen.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**Klassenfactory**
</dt> <dd>

Ein COM-Objekt, das die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle implementiert und eine oder mehrere Instanzen eines Objekts erstellt, das durch eine angegebene Klassen-ID (CLSID) identifiziert wird.

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**Klassen Bezeichner (CLSID)**
</dt> <dd>

Eine Globally Unique Identifier (GUID), die einem OLE-Klassenobjekt zugeordnet ist. Wenn ein Klassenobjekt verwendet wird, um mehr als eine Instanz eines Objekts zu erstellen, sollte die zugehörige Serveranwendung Ihre CLSID in der Systemregistrierung registrieren, damit Clients den mit den Objekten verknüpften ausführbaren Code suchen und laden können. Jeder OLE-Server oder-Container, der die Verknüpfung mit seinen eingebetteten Objekten ermöglicht, muss für jede unterstützte Objektdefinition eine CLSID registrieren.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**Class-Objekt**
</dt> <dd>

Bei der objektorientierten Programmierung ein Objekt, dessen Zustand von allen Objekten in einer Klasse gemeinsam genutzt wird und dessen Verhalten auf diese classwide State-Daten angewendet wird. In com werden Klassen Objekte als Klassenfactorys bezeichnet und weisen in der Regel kein Verhalten auf, es sei denn, es werden neue Instanzen der Klasse erstellt.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**ent**
</dt> <dd>

Ein COM-Objekt, das Dienste von einem anderen Objekt anfordert.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**Client Standort**
</dt> <dd>

Die Anzeige Site für ein eingebettetes oder verknüpftes Objekt innerhalb eines Verbund Dokuments. Der Client Standort ist das wichtigste Mittel, mit dem ein Objekt Dienste aus seinem Container anfordert.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**
</dt> <dd>

Eine Globally Unique Identifier (GUID), die einem OLE-Klassenobjekt zugeordnet ist. Wenn ein Klassenobjekt verwendet wird, um mehr als eine Instanz eines Objekts zu erstellen, sollte die zugehörige Serveranwendung Ihre CLSID in der Systemregistrierung registrieren, damit Clients den mit den Objekten verknüpften ausführbaren Code suchen und laden können. Jeder OLE-Server oder-Container, der die Verknüpfung mit seinen eingebetteten Objekten ermöglicht, muss für jede unterstützte Objektdefinition eine CLSID registrieren.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**einzusetzen**
</dt> <dd>

So speichern Sie dauerhaft Änderungen an einem Speicher-oder Streamobjekt, die seit dem Öffnen oder letzten Speichern der Änderungen vorgenommen wurden.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**Zulieferern**
</dt> <dd>

Ein-Objekt, das sowohl Daten als auch Code kapselt und einen ordnungsgemäß angegebenen Satz öffentlich verfügbarer Dienste bereitstellt.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (com)**
</dt> <dd>

Das OLE-objektorientierte Programmiermodell, das definiert, wie Objekte innerhalb eines einzelnen Prozesses oder zwischen Prozessen interagieren. In com haben Clients Zugriff auf ein Objekt über Schnittstellen, die für das Objekt implementiert werden.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**zusammengesetzte Menüleiste**
</dt> <dd>

Eine freigegebene Menüleiste, die aus Menü Gruppen aus einer Containeranwendung und einer direkt aktivierten Serveranwendung besteht.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**zusammengesetzter Moniker**
</dt> <dd>

Ein Moniker, der aus zwei oder mehr Monikern besteht, die als Einheit behandelt werden. Ein zusammengesetzter Moniker kann nicht generisch sein, was bedeutet, dass seine komponentenmoniker über besondere Kenntnisse untereinander oder generisch verfügen, was bedeutet, dass seine komponentenmoniker nichts über einander wissen, außer dass es sich um Moniker handelt.

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**Verbund Dokument**
</dt> <dd>

Ein Dokument, das verknüpfte oder eingebettete Objekte sowie die eigenen systemeigenen Daten enthält.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**Verbund Datei**
</dt> <dd>

Eine durch OLE bereitgestellte strukturierte Speicher Implementierung.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM-Objekt**
</dt> <dd>

Ein-Objekt, das dem OLE-Component Object Model (com) entspricht. Ein COM-Objekt ist eine Instanz einer Objektdefinition, die die Daten des Objekts und eine oder mehrere Implementierungen von Schnittstellen für das Objekt angibt. Clients interagieren mit einem COM-Objekt nur über die Schnittstellen.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**Verbindungs fähigen-Objekt**
</dt> <dd>

Ein COM-Objekt, das mindestens die [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle für die Verwaltung von Verbindungspunkt Objekten implementiert. Verbindungs fähige Objekte unterstützen die Kommunikation zwischen dem Server und dem Client. Ein Verbindungs fähigen-Objekt erstellt und verwaltet ein oder mehrere Verbindungspunkt unter Objekte, die Ereignisse von Schnittstellen empfangen, die auf anderen Objekten implementiert sind, und diese an den Client senden.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**Verbindungspunkt Objekt**
</dt> <dd>

Ein COM-Objekt, das von einem Verbindungs fähigen Objekt verwaltet wird und die [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) -Schnittstelle implementiert. Ein oder mehrere Verbindungspunkt Objekte können von einem Verbindungs fähigen Objekt erstellt und verwaltet werden. Jedes Verbindungspunkt Objekt verwaltet eingehende Ereignisse von einer bestimmten Schnittstelle auf einem anderen Objekt und sendet diese Ereignisse an den Client.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**Containeranwendung**
</dt> <dd>

Eine Anwendung, die Verbund Dokumente unterstützt. Die Containeranwendung bietet Speicher für ein eingebettetes oder verknüpftes Objekt, eine Site für die Anzeige, den Zugriff auf die Anzeige Site und eine Beratungs Senke für den Empfang von Benachrichtigungen über Änderungen im Objekt.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**Begrenzung**
</dt> <dd>

Eine Kompositionstechnik zum Implementieren von COM-Objekten. Es ermöglicht einem Objekt, einige oder alle der Schnittstellen Implementierungen von einem oder mehreren anderen Objekten wiederzuverwenden. Das äußere Objekt fungiert als Client für die anderen Objekte und delegiert die Implementierung, wenn die Dienste von einem der enthaltenen Objekte verwendet werden sollen.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**Kontext**
</dt> <dd>

In com+ ein Satz von Lauf Zeiteigenschaften, die einem oder mehreren COM-Objekten zugeordnet sind, die für die Bereitstellung von Diensten für diese Objekte verwendet werden.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**Steuerelement**
</dt> <dd>

Ein einbettbares, wiederverwendbares com-Objekt, das mindestens die [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) -Schnittstelle unterstützt. Steuerelemente werden in der Regel der Benutzeroberfläche zugeordnet. Sie unterstützen auch die Kommunikation mit einem Container und können von mehreren Clients abhängig von den Lizenzierungs Kriterien wieder verwendet werden.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**Steuerelement Container**
</dt> <dd>

Eine Anwendung, die die Einbettung von-Steuerelementen durch Implementieren der [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) -Schnittstelle unterstützt.

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Control-Eigenschaft**
</dt> <dd>

Eine Lauf Zeit Eigenschaft, die vom Steuerelement selbst bereitgestellt und verwaltet wird. Die vom Steuerelement verwendeten Schriftart und Textgröße sind z. b. Steuerelement Eigenschaften.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**Steuern von Objekten**
</dt> <dd>

Das-Objekt innerhalb eines Aggregat Objekts, das steuert, welche Schnittstellen innerhalb des Aggregat Objekts verfügbar gemacht und welche privat sind. Die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle des steuernden Objekts wird als kontrollierendes **IUnknown** bezeichnet. Aufrufe von **IUnknown** -Methoden anderer Objekte im Aggregat müssen an das steuernde **IUnknown**-Objekt übermittelt werden.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**Steuerungs Website**
</dt> <dd>

Eine-Struktur, die von einem Steuerelement Container zum Verwalten der Anzeige und des Speichers eines-Steuer Elements implementiert wird. Innerhalb eines bestimmten Containers verfügt jedes Steuerelement über eine entsprechende Steuerungs Site.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**Datenübertragungs Objekt**
</dt> <dd>

Ein Objekt, das die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle implementiert und Daten enthält, die entweder über die Zwischenablage oder Drag & Drop-Vorgänge von einem Objekt in ein anderes übertragen werden sollen.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**Standard Objekt Handler**
</dt> <dd>

Eine mit OLE bereitgestellte DLL, die als Ersatz im Verarbeitungsbereich der Containeranwendung für das echte Objekt fungiert.

Mit dem Standard Objekt Handler ist es möglich, die gespeicherten Daten eines Objekts zu überprüfen, ohne das Objekt tatsächlich zu aktivieren. Der Standard Objekt Handler führt andere Aufgaben aus, z. b. das Rendern eines Objekts aus dem zwischengespeicherten Zustand, wenn das Objekt in den Arbeitsspeicher geladen wird.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**abhängiges Objekt**
</dt> <dd>

Ein COM-Objekt, das in der Regel von einem anderen Objekt initialisiert wird (das Host Objekt). Obwohl die Lebensdauer des abhängigen Objekts möglicherweise nur während der Lebensdauer des Host Objekts sinnvoll ist, funktioniert das Host Objekt nicht als kontrollierendes [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für das abhängige Objekt. Im Gegensatz dazu ist ein Objekt ein aggregiertes Objekt, wenn seine Lebensdauer (durch den Verweis Zähler) vollständig vom Verwaltungs Objekt gesteuert wird.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direkt Zugriffsmodus**
</dt> <dd>

Einer von zwei Zugriffs Modi, in denen ein Speicher Objekt geöffnet werden kann. Im direkten Modus werden alle Änderungen sofort an das Stamm Speicher Objekt übertragen.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**Document-Objekt**
</dt> <dd>

Ein OLE-Dokument, in dem eine oder mehrere direkt aktivierte Sichten der Daten in einem systemeigenen oder fremd Rahmen (z. b. einem Browser) angezeigt werden können, während die vollständige Kontrolle über die Benutzeroberfläche beibehalten wird. Zusätzlich zur Implementierung des üblichen OLE-Dokuments und der direkten Aktivierungs Schnittstellen muss ein Dokument Objekt [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)implementieren, und jede seiner Sichten (in Form eines Dokument Ansichts Objekts) muss [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview)implementieren.

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**Dokument Objekt Container**
</dt> <dd>

Eine Containeranwendung, die in der Lage ist, eine oder mehrere Ansichten von einem oder mehreren Dokument Objekten anzuzeigen und alle enthaltenen Dokument Objekte innerhalb einer Datei zu verwalten. Jedes Dokument Objekt ist einer Dokument Site zugeordnet, und jede Dokument Site enthält mindestens eine Dokument Ansichts Site, die den vom Dokument Objekt unterstützten Sichten entspricht. Ein Dokument Objekt Container enthält außerdem einen Container Rahmen, der die Aushandlung von Menüs und Symbolleisten sowie die Enumeration von enthaltenen Objekten behandelt.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**Dokument Objekt Server**
</dt> <dd>

Eine Serveranwendung, die Dokument Objekte bereitstellen können.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**Dokument Website**
</dt> <dd>

Eine Client Site, die von einem Dokument Objekt Container zum Verwalten der Anzeige und Speicherung eines Dokument Objekts implementiert wird. Jedes Dokument Objekt in einem Container verfügt über eine entsprechende Dokument Site.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**Dokument Standort Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) -Schnittstelle implementiert, zusätzlich zu den üblichen Client Standort Schnittstellen (z. b. [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**Dokument Ansicht**
</dt> <dd>

Eine bestimmte Präsentation der Daten eines Dokuments. Ein einzelnes Dokument Objekt kann über eine oder mehrere Sichten verfügen, aber eine einzelne Dokument Ansicht kann nur zu einem einzigen Dokument Objekt gehören.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**Dokument Ansichts Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) -Schnittstelle implementiert und einer bestimmten Dokument Ansicht entspricht. Ein Objekt mit mehreren Dokument Sichten aggregiert für jede Ansicht ein separates Dokument Ansichts Objekt.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**Website für die Dokument Ansicht**
</dt> <dd>

Ein Objekt, das von einem Dokument Standort Objekt zum Verwalten des Anzeige Raums für eine bestimmte Ansicht eines Dokument Objekts aggregiert wird. Innerhalb einer bestimmten Dokument Website verfügt jede Dokument Ansicht über eine entsprechende Dokument Ansichts Website.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**Website Objekt der Dokument Ansicht**
</dt> <dd>

Ein COM-Objekt, das in einem Dokument Standort Objekt aggregiert wird und die [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) -Schnittstelle und optional die [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) -Schnittstelle implementiert.

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**Drag & Drop**
</dt> <dd>

Ein Vorgang, bei dem der Endbenutzer die Maus oder ein anderes Zeigegerät verwendet, um Daten an eine andere Stelle im selben Fenster oder in einem anderen Fenster zu verschieben.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Einbinden**
</dt> <dd>

, Wenn ein Objekt in einem Verbund Dokument so eingefügt werden soll, dass die in diesem Objekt nativen Datenformate erhalten bleiben und es mithilfe von Tools, die von seinem Server bereitgestellt werden, in seinem Container bearbeitet werden kann.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**eingebettetes Objekt**
</dt> <dd>

Ein Objekt, dessen Daten in einem Verbund Dokument gespeichert werden, das Objekt jedoch im Prozessraum des Servers ausgeführt wird. Der Standard Objekt Handler stellt ein Ersatz Zeichen im Verarbeitungsbereich der Containeranwendung für das echte Objekt bereit.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**Erweiterte Eigenschaft**
</dt> <dd>

Eine Lauf Zeit Eigenschaft, z. b. die Position und die Größe eines Steuer Elements, die ein Benutzer annehmen würde, wenn er vom-Steuerelement verfügbar gemacht wird, aber vom Container bereitgestellt und verwaltet wird.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**dateimoniker**
</dt> <dd>

Ein Moniker, der auf einem Pfad im Dateisystem basiert. Dateimoniker können verwendet werden, um Objekte zu identifizieren, die in ihren eigenen Dateien gespeichert werden. Ein dateimoniker ist ein COM-Objekt, das die vom System bereitgestellte Implementierung der [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle für die dateimonikerklasse unterstützt.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**Font-Objekt**
</dt> <dd>

Ein COM-Objekt, das Zugriff auf Graphics Device Interface (GDI)-Schriftarten ermöglicht, indem die [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) -Schnittstelle implementiert wird.

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**Format Bezeichner**
</dt> <dd>

Eine GUID, die einen persistenten Eigenschaften Satz identifiziert. Wird auch als fmtid bezeichnet.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**Dr**
</dt> <dd>

Der Teil einer Containeranwendung, die für das Aushandeln von Menüs, Zugriffstasten, Symbolleisten und anderen freigegebenen Benutzeroberflächen Elementen mit einem eingebetteten com-Objekt oder einem Dokument Objekt zuständig ist.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**Frame-Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) -Schnittstelle und optional die [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) -Schnittstelle implementiert.

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generischer zusammengesetzter Moniker**
</dt> <dd>

Eine sequenzierte Auflistung von Monikern, beginnend mit einem dateimoniker zum Bereitstellen des Pfads auf Dokument Ebene und fortsetzen mit einem oder mehreren elementmonikern, die als Ganzes übernommen werden, identifiziert ein Objekt eindeutig.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**Hilfsfunktion**
</dt> <dd>

Eine Funktion, die Aufrufe anderer Funktionen und Schnittstellen Methoden kapselt, die im OLE SDK öffentlich verfügbar sind. Hilfsfunktionen sind eine bequeme Möglichkeit, häufig verwendete Sequenzen von Funktions-und Methoden aufrufen aufzurufen, die häufige Aufgaben ausführen.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**Host Objekt**
</dt> <dd>

Ein COM-Objekt, das eine hierarchische Beziehung mit einem oder mehreren anderen COM-Objekten bildet, die als abhängige Objekte bezeichnet werden. In der Regel werden die abhängigen Objekte vom Host Objekt instanziiert, und Ihr vorhanden sein ist nur innerhalb der Lebensdauer des Host Objekts sinnvoll. Das Host Objekt fungiert jedoch nicht als kontrollierendes [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für die abhängigen Objekte und delegiert es nicht direkt an die Schnittstellen Implementierungen dieser Objekte.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**
</dt> <dd>

Ein nicht transparentes Ergebnis Handle, das für eine erfolgreiche Rückgabe einer Funktion und ungleich 0 (null) definiert ist, wenn Fehler-oder Statusinformationen zurückgegeben werden.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**Hyperlink-Objekt**
</dt> <dd>

Ein COM-Objekt, das mindestens die [**ihlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) -Schnittstelle implementiert und als Link zu einem Objekt an einem anderen Speicherort (dem Ziel) fungiert. Ein Hyperlink besteht aus vier Teilen: einem Moniker, der den Speicherort des Ziels identifiziert. eine Zeichenfolge für den Speicherort innerhalb des Ziels. ein benutzerfreundlicher oder anzeigbarer Name für das Ziel. und eine Zeichenfolge, die zusätzliche Parameter enthalten kann.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**Hyperlink zum Durchsuchen**
</dt> <dd>

Ein COM-Objekt, das die [**ihlinkbrowsecontext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) -Schnittstelle implementiert und den Hyperlink-Navigations Stapel verwaltet. Das Kontext Objekt durchsuchen verwaltet das Fenster des Hyperlink-Frame Fensters und das Hyperlink-Zielobjekt.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**Hyperlink-Container**
</dt> <dd>

Eine Containeranwendung, die Hyperlinks unterstützt, indem die [**ihlinksite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) -Schnittstelle implementiert wird, und, wenn die Objekte des Containers Ziele anderer Hyperlinks sein können, die [**ihlinktarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) -Schnittstelle.

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**Hyperlink-Frame Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**ihlinkframe**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) -Schnittstelle implementiert, und steuert die Navigation und die Anzeige von Links auf der obersten Ebene für den Container des Frames und den Server des Hyperlink-Ziels.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**Hyperlink-Standort Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**ihlinksite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) -Schnittstelle implementiert und entweder den Moniker oder den Schnittstellen Bezeichner des Hyperlink-Containers bereitstellt. Eine Hyperlink-Site kann mehrere Hyperlinks verarbeiten.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**Hyperlink-Zielobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**ihlinktarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) -Schnittstelle implementiert und den Moniker, anzeigen Amen und andere Informationen bereitstellt, die von anderen Hyperlink-Objekten verwendet werden, um dorthin zu navigieren.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in-Parameter**
</dt> <dd>

Ein Parameter, der vom Aufrufer einer Funktion oder Schnittstellen Methode zugeordnet, festgelegt und freigegeben wird. Ein in-Parameter wird von der aufgerufenen Funktion nicht geändert.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out-Parameter**
</dt> <dd>

Ein Parameter, der anfänglich vom Aufrufer einer Funktion oder Schnittstellen Methode zugeordnet wird und ggf. durch den aufgerufenen Prozess festgelegt, freigegeben und neu zugeordnet wird.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**direkte Aktivierung**
</dt> <dd>

Bearbeiten eines eingebetteten Objekts innerhalb des Fensters seines Containers mithilfe der vom Server bereitgestellten Tools. Verknüpfte Objekte unterstützen keine direkte Aktivierung. Sie werden immer im Fenster des Servers bearbeitet.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**Prozess interne Server**
</dt> <dd>

Ein als DLL implementierter Server, der im Prozessbereich des Clients ausgeführt wird.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**lichen**
</dt> <dd>

Ein-Objekt, für das der Arbeitsspeicher zugeordnet ist oder der persistent ist.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**berfläche**
</dt> <dd>

Eine Gruppe semantisch verwandter Funktionen, die Zugriff auf ein COM-Objekt bereitstellen. Jede OLE-Schnittstelle definiert einen Vertrag, der das interagieren von Objekten gemäß der Component Object Model (com) zulässt. Obwohl OLE viele Schnittstellen Implementierungen bereitstellt, können die meisten Schnittstellen auch von Entwicklern implementiert werden, die OLE-Anwendungen entwerfen.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**Schnittstellen Bezeichner (IID)**
</dt> <dd>

Eine Globally Unique Identifier (GUID), die einer Schnittstelle zugeordnet ist. Einige Funktionen akzeptieren IIDs als Parameter, um dem Aufrufer zu gestatten, den Schnittstellen Zeiger anzugeben, der zurückgegeben werden soll.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**elementmoniker**
</dt> <dd>

Ein Moniker auf der Grundlage einer Zeichenfolge, die ein Objekt in einem Container identifiziert. Elementmoniker können Objekte identifizieren, die kleiner als eine Datei sind, einschließlich eingebetteter Objekte in einem Verbund Dokument, oder ein Pseudo Objekt (z. b. einen Zellbereich in einer Kalkulations Tabelle).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**Genehmigung**
</dt> <dd>

Eine com-Funktion, die die Steuerung der Objekt Erstellung ermöglicht. Lizenzierte Objekte können nur von Clients erstellt werden, die zur Verwendung autorisiert sind. Die Lizenzierung wird in com über die [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) -Schnittstelle und durch Unterstützung eines Lizenzschlüssels implementiert, der zur Laufzeit übermittelt werden kann.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**Link-Objekt**
</dt> <dd>

Ein COM-Objekt, das erstellt wird, wenn ein verknüpftes com-Objekt erstellt oder geladen wird. Das Link Objekt wird von OLE bereitgestellt und implementiert die [**iolelink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) -Schnittstelle.

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**Verknüpftes Objekt**
</dt> <dd>

Ein COM-Objekt, dessen Quelldaten physisch dort gespeichert sind, wo es ursprünglich erstellt wurde. Nur ein Moniker, der die Quelldaten und die entsprechenden Präsentationsdaten darstellt, wird mit dem Verbund Dokument beibehalten. An der Verknüpfungs Quelle vorgenommene Änderungen werden automatisch in das verknüpfte Objekt übernommen.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**Quelle verknüpfen**
</dt> <dd>

Die Daten, die die Quelle eines verknüpften Objekts sind. Eine Verknüpfungs Quelle kann eine Datei oder ein Teil einer Datei sein, z. b. ein ausgewählter Bereich von Zellen in einer Datei (auch als Pseudo Objekt bezeichnet).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**geladener Zustand**
</dt> <dd>

Der Zustand eines Objekts, nachdem die Datenstrukturen in den Arbeitsspeicher geladen wurden und für den Client Prozess zugänglich sind.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**lokaler Server**
</dt> <dd>

Einen Out-of-Process-Server, der als implementiert ist. EXE-Anwendung, die auf dem gleichen Computer wie die Client Anwendung ausgeführt wird.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**Sperre**
</dt> <dd>

Ein Zeiger, der auf und möglicherweise ein Verweis Zähler auf einem laufenden Objekt inkrementiert wird. OLE definiert zwei Arten von Sperren, die für ein Objekt gehalten werden können: stark und schwach. Zum Implementieren einer starken Sperre muss ein Server sowohl einen Zeiger als auch einen Verweis Zähler verwalten, damit das Objekt zumindest so lange im Arbeitsspeicher gesperrt bleibt, bis der Server [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufruft. Um eine schwache Sperre zu implementieren, behält der Server nur einen Zeiger auf das-Objekt bei, sodass das Objekt von einem anderen Prozess zerstört werden kann.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**Marshalling**
</dt> <dd>

Verpacken und Senden von Schnittstellen Methoden aufrufen über Thread-oder Prozess Grenzen hinweg.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**Medientyp**
</dt> <dd>

Eine Erweiterung von MIME, die die Datenformat Aushandlung zwischen einem Client und einem-Objekt zulässt.

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME-Inhaltstyp**
</dt> <dd>

Eine Erweiterung von MIME, die die Datenformat Aushandlung zwischen einem Client und einem-Objekt zulässt.

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Mehrzweck-Internet Mail Erweiterung (MIME)**
</dt> <dd>

Ein Internet Protokoll, das ursprünglich entwickelt wurde, um den Austausch elektronischer e-Mail-Nachrichten mit umfangreichen Inhalten in heterogenen Netzwerk-, Computer-und e- In der Praxis wurde MIME auch von nicht-e-Mail-Anwendungen übernommen und erweitert.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Ein Objekt, das die [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle implementiert. Ein Moniker fungiert als Name, der ein COM-Objekt eindeutig identifiziert. Auf dieselbe Weise, wie ein Pfad eine Datei im Dateisystem identifiziert, identifiziert ein Moniker ein COM-Objekt im Verzeichnis Namespace.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**Monikerklasse**
</dt> <dd>

Eine Implementierung der [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle. Zu den vom System bereitgestellten Monikerklassen zählen dateimoniker, elementmoniker, generische zusammengesetzte Moniker, Anti-Moniker, zeigermoniker und URL-Moniker.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**monikerclient**
</dt> <dd>

Eine Anwendung, die Moniker zum Abrufen von Schnittstellen Zeigern für Objekte verwendet, die von einer anderen Anwendung verwaltet werden.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**monikeranbieter**
</dt> <dd>

Eine Anwendung, die verfügbare Moniker zur Identifizierung der von ihm verwalteten Objekte bereitstellt, sodass andere Anwendungen auf die Objekte zugreifen können.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**Namespace Erweiterung**
</dt> <dd>

Ein in-Process-COM-Objekt, das [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**ipersistfolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)und [**ishellview**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview)implementiert, die manchmal auch als Namespace-Erweiterungs Schnittstellen bezeichnet werden. Eine Namespace Erweiterung wird entweder zum Erweitern des-Namespace der Shell oder zum Erstellen eines separaten Namespaces verwendet. Primäre Benutzer sind die Dialogfelder Windows-Explorer und allgemeine Datei.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**Native Daten**
</dt> <dd>

Die Daten, die von einer OLE-Serveranwendung beim Bearbeiten eines eingebetteten Objekts verwendet werden.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**Objekt**
</dt> <dd>

In OLE ist eine Programmier Struktur sowohl Daten als auch Funktionen kapselt, die als einzelne Einheit definiert und zugeordnet sind und für die der einzige öffentliche Zugriff über die Schnittstellen der Programmier Struktur erfolgt. Ein COM-Objekt muss mindestens die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützen, die das vorhanden sein des Objekts während der Verwendung beibehält und Zugriff auf die anderen Schnittstellen des Objekts bietet.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**Objektstatus** 
</dt> <dd>

Die Beziehung zwischen einem Verbund Dokument Objekt in seinem Container und der für die Erstellung des Objekts Verantwortlichen Anwendung: aktiv, passiv, geladen oder wird ausgeführt. Passive Objekte werden auf dem Datenträger oder in einer Datenbank gespeichert, und das Objekt ist nicht ausgewählt oder aktiv. Im geladenen Zustand wurden die Datenstrukturen des Objekts in den Arbeitsspeicher geladen, sind aber nicht für Vorgänge wie z. b. die Bearbeitung verfügbar. Das Ausführen von Objekten wird geladen und ist für alle Vorgänge verfügbar. Aktive Objekte führen Objekte aus, die über eine sichtbare Benutzeroberfläche verfügen.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**Objekttyp Name**
</dt> <dd>

Eine eindeutige Identifikations Zeichenfolge, die als Teil der Informationen, die für ein Objekt in der Registrierungsdatenbank verfügbar sind, gespeichert wird.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**Schieren**
</dt> <dd>

Die objektbasierte Technologie von Microsoft für die gemeinsame Nutzung von Informationen und Diensten über Prozess-und Computer Grenzen hinweg.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**Out-of-Process-Server**
</dt> <dd>

Ein Server, der als implementiert ist. EXE-Anwendung, die außerhalb des Prozesses des Clients ausgeführt wird, entweder auf demselben Computer oder auf einem Remote Computer.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out-Parameter**
</dt> <dd>

Ein out-Parameter wird von der aufgerufenen Funktion zugeordnet und vom Aufrufer freigegeben.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passiver Status**
</dt> <dd>

Der Status eines COM-Objekts, wenn es gespeichert wird (auf einem Datenträger oder in einer Datenbank). Das Objekt ist nicht ausgewählt oder aktiv.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistente Eigenschaft**
</dt> <dd>

Informationen, die dauerhaft als Teil eines Speicher Objekts, z. b. einer Datei oder eines Verzeichnisses, gespeichert werden können. Persistente Eigenschaften werden in Eigenschafts Sätze gruppiert, die angezeigt und bearbeitet werden können.

Eine persistente Eigenschaft unterscheidet sich von den Lauf Zeiteigenschaften von Objekten, die mit OLE-Steuerelementen und Automatisierungstechnologien erstellt wurden, die verwendet werden können, um das Systemverhalten zu beeinflussen. Die [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) -Struktur definiert alle gültigen Typen von permanenten Eigenschaften, während die **Variant** -Struktur alle gültigen Typen von Lauf Zeiteigenschaften definiert.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistenter Speicher**
</dt> <dd>

Speicherung einer Datei oder eines Objekts in einem Medium, z. b. ein Dateisystem oder eine Datenbank, sodass das Objekt und seine Daten beibehalten werden, wenn die Datei geschlossen und zu einem späteren Zeitpunkt erneut geöffnet wird.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**Bild Objekt**
</dt> <dd>

Ein COM-Objekt, das den Zugriff auf GDI-Images durch Implementieren der [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) -Schnittstelle ermöglicht.

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**zeigermoniker**
</dt> <dd>

Ein Moniker, der einen Schnittstellen Zeiger einem Objekt im Arbeitsspeicher zuordnet. Während die meisten Moniker Objekte identifizieren, die dauerhaft gespeichert werden können, identifizieren Zeiger Moniker Objekte, die nicht möglich sind. Dadurch können solche Objekte an einem Monikerbindungsvorgang teilnehmen.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**Präsentationsdaten**
</dt> <dd>

Die Daten, die von einem Container verwendet werden, um eingebettete oder verknüpfte Objekte anzuzeigen.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primäres Verb**
</dt> <dd>

Die Aktion, die dem gängigsten oder bevorzugten Vorgang zugeordnet ist, den Benutzer für ein Objekt ausführen. Das primäre Verb wird in der System Registrierungsdatenbank immer als Verb NULL definiert. Das primäre Verb eines Objekts wird durch Doppelklicken auf das-Objekt ausgeführt.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Property**
</dt> <dd>

Informationen, die einem Objekt zugeordnet sind. In OLE werden Eigenschaften in zwei Kategorien unterteilt: Lauf Zeiteigenschaften und persistente Eigenschaften. Lauf Zeiteigenschaften werden normalerweise steuerungsobjekten oder deren Containern zugeordnet. Beispielsweise ist die Hintergrundfarbe eine Lauf Zeit Eigenschaft, die durch den Container eines Steuer Elements festgelegt wird. Persistente Eigenschaften werden gespeicherten Objekten zugeordnet.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**Eigenschaften Rahmen**
</dt> <dd>

Der Benutzeroberflächen Mechanismus, der eine oder mehrere Eigenschaften Seiten für ein Steuerelement anzeigt. Das Laufzeitsystem der OLE-Steuerelemente stellt eine Standard Implementierung eines Eigenschaften Rahmens bereit, auf den über die Hilfsfunktion " [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) " zugegriffen werden kann.

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**Eigenschafts Bezeichner**
</dt> <dd>

Eine 4-Byte-Ganzzahl mit Vorzeichen, die eine persistente Eigenschaft innerhalb eines Eigenschaften Satzes identifiziert.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**Eigenschaften Seite**
</dt> <dd>

Ein COM-Objekt mit einer eigenen CLSID, die Teil einer Benutzeroberfläche ist, von einem-Steuerelement implementiert wird und das Anzeigen und Festlegen der Eigenschaften des Steuer Elements ermöglicht. Eigenschaften Seiten Objekte implementieren die [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) -Schnittstelle.

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**Website für Eigenschaften Seite**
</dt> <dd>

Die Position innerhalb eines Eigenschaften Rahmens, an der eine Eigenschaften Seite angezeigt wird. Der Eigenschaften Frame implementiert die [**ipropertypagesite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) -Schnittstelle, die Methoden zum Verwalten der Standorte der einzelnen Eigenschaften Seiten enthält, die von einem Steuerelement bereitgestellt werden.

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**Eigenschaften Satz**
</dt> <dd>

Eine logisch verwandte Gruppe von Eigenschaften, die einem permanent gespeicherten Objekt zugeordnet ist. Um eine oder mehrere Eigenschaften Sätze zu erstellen, zu öffnen, zu löschen oder aufzulisten, implementieren Sie die [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) -Schnittstelle. Wenn Sie Verbund Dateien verwenden, können Sie die OLE-Implementierung dieser Schnittstelle verwenden, anstatt ihre eigenen zu implementieren.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**Eigenschaften Satz-Speicher**
</dt> <dd>

Ein com-Speicher Objekt, das einen Eigenschaften Satz enthält. Ein Eigenschaften Satz Speicher ist ein abhängiges Objekt, das einem Speicher Objekt zugeordnet ist und von ihm verwaltet wird.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**Eigenschaften Blatt**
</dt> <dd>

Ein Satz von Eigenschaften Seiten für ein oder mehrere-Objekte.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**Proxy**
</dt> <dd>

Ein Schnittstellen spezifisches Objekt, das Parameter für diese Schnittstelle in Vorbereitung auf einen Remote Methodenaufrufe verpackt. Ein Proxy wird im Adressraum des Absenders ausgeführt und kommuniziert mit einem entsprechenden Stub im Adressraum des Empfängers.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Proxy-Manager**
</dt> <dd>

Beim Standardmarshalling ein Proxy, der alle Schnittstellen Proxys für ein einzelnes Objekt verwaltet.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**Pseudo Objekt**
</dt> <dd>

Ein Teil eines Dokuments oder eingebetteten Objekts, z. b. ein Bereich von Zellen in einer Kalkulations Tabelle, der die Quelle für ein COM-Objekt sein kann.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**Verweis Zählung**
</dt> <dd>

Behalten Sie die Anzahl der einzelnen Schnittstellen Zeiger für ein Objekt, um sicherzustellen, dass das Objekt nicht zerstört wird, bevor alle Verweise darauf freigegeben werden.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relativer Moniker**
</dt> <dd>

Ein Moniker, der die Position eines Objekts relativ zum Speicherort eines anderen Objekts angibt. Ein relativer Moniker ist analog zu einem relativen Pfad, z. b.. \\ Backup \\ Report. Old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**Remote Server**
</dt> <dd>

Eine als exe implementierte Serveranwendung, die auf einem anderen Computer als die Client Anwendung ausgeführt wird.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**umzukehren**
</dt> <dd>

, Um Änderungen zu verwerfen, die seit dem letzten Commit der Änderungen an einem Objekt vorgenommen wurden oder der Speicher des Objekts geöffnet wurde.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**Stamm Speicher Objekt**
</dt> <dd>

Das äußerste Speicher Objekt in einem Dokument. Ein Stamm Speicher Objekt kann andere, in der Tabelle eingefügte Speicher-und Streamobjekte enthalten. Beispielsweise wird ein Verbund Dokument als eine Reihe von Speicher-und Streamobjekten in einem Stamm Speicher Objekt auf dem Datenträger gespeichert.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**Status wird ausgeführt**
</dt> <dd>

Der Status eines COM-Objekts, wenn die Serveranwendung ausgeführt wird und es möglich ist, auf seine Schnittstellen zuzugreifen und Benachrichtigungen über Änderungen zu erhalten.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**Running Object Table (rot)**
</dt> <dd>

Eine Global barrierefreie Tabelle auf allen Computern, die alle COM-Objekte im Zustand "wird ausgeführt" nachverfolgt, die von einem Moniker identifiziert werden können. Monikeranbieter registrieren ein Objekt in der Tabelle, wodurch der Verweis Zähler des Objekts erhöht wird. Bevor das Objekt zerstört werden kann, muss der zugehörige Moniker aus der Tabelle freigegeben werden.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Lauf Zeit Eigenschaft**
</dt> <dd>

Diskrete Zustandsinformationen, die einem Steuerelement Objekt oder seinem Container zugeordnet sind. Es gibt drei Arten von Lauf Zeiteigenschaften: Umgebungs Eigenschaften, Steuerelement Eigenschaften und erweiterte Eigenschaften.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**Selbstregistrierung**
</dt> <dd>

Der Prozess, mit dem ein Server seine eigenen Registrierungs Vorgänge ausführen kann.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**Serveranwendung**
</dt> <dd>

Eine Anwendung, die COM-Objekte erstellen kann. Container Anwendungen können dann diese Objekte einbetten oder verknüpfen.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**statisches Objekt**
</dt> <dd>

Ein-Objekt, das nur eine Präsentation ohne systemeigene Daten enthält. Ein Container kann ein statisches Objekt so behandeln, als ob es sich um ein verknüpftes oder eingebettetes Objekt handelt, außer dass es nicht möglich ist, ein statisches Objekt zu bearbeiten.

Ein statisches Objekt kann z. b. aus dem Umbruch eines Links in einem verknüpften Objekt resultieren, d. h., die Serveranwendung ist nicht verfügbar, oder der Benutzer möchte nicht, dass das verknüpfte Objekt nicht mehr aktualisiert wird.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**Speicher Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle implementiert. Ein Speicher Objekt enthält geschachtelte Speicher Objekte oder Streamobjekte, was zu einer Verzeichnis-/Dateistruktur in einer einzelnen Datei führt.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**Stream-Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle implementiert. Ein Stream-Objekt ist analog zu einer Datei in einem Verzeichnis-/Dateisystem.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Strukturierter Speicher**
</dt> <dd>

OLE-Technologie zum Speichern von Verbund Dateien in systemeigenen Dateisystemen.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Stub**
</dt> <dd>

Wenn die Parameter einer Funktion oder der Schnittstellen Methode über eine Prozess Grenze hinweg gemarshallt werden, ist der Stub ein Schnittstellen spezifisches Objekt, das die gemarshallten Parameter entpackt und die erforderliche Methode aufruft. Der Stub wird im Adressraum des Empfängers ausgeführt und kommuniziert mit einem entsprechenden Proxy im Adressbereich des Absenders.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Stub-Manager**
</dt> <dd>

Verwaltet alle schnittstellenstubobjekte für ein einzelnes Objekt.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchroner Rückruf**
</dt> <dd>

Ein Funktionsaufruf, bei dem keine weiteren Anweisungen im aufrufenden Prozess ausgeführt werden können, bis die Funktion zurückgibt.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Systemregistrierung**
</dt> <dd>

Ein systemweites Repository von Informationen, die von Windows unterstützt werden und Informationen über das System und seine Anwendungen enthalten, einschließlich OLE-Clients und-Servern.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**Transaktiver Zugriffsmodus**
</dt> <dd>

Einer von zwei Zugriffs Modi, in denen ein Speicher Objekt geöffnet werden kann. Wenn Sie im transaktiven Modus geöffnet werden, werden die Änderungen in Puffern gespeichert, bis das Stamm Speicher Objekt die Änderungen übernimmt.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**Typinformationen**
</dt> <dd>

Informationen über die Klasse eines Objekts, das von einer Typbibliothek bereitgestellt wird. Zum Bereitstellen von Typinformationen implementiert ein COM-Objekt die [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstelle.

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**einheitliche Datenübertragung**
</dt> <dd>

Ein Modell zum Übertragen von Daten über die Zwischenablage, Drag & Drop oder Automation. Objekte, die diesem Modell entsprechen, implementieren die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle. Dieses Modell ersetzt DDE (dynamischer Datenaustausch).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**Unmarshalling**
</dt> <dd>

Entpacken von Parametern, die über Prozess Grenzen hinweg an einen Proxy gesendet wurden.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universelle ressourcenlocator (URL)**
</dt> <dd>

Der Bezeichner, der vom World Wide Web für die Namen und Speicherorte von Objekten im Internet verwendet wird. OLE stellt eine Monikerklasse, einen URL-Moniker, bereit, deren Implementierung verwendet werden kann, um einen Client an Objekte zu binden, die durch eine URL identifiziert werden.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL-Moniker**
</dt> <dd>

Ein Moniker, der auf einer URL (Universal Resource Serverlocatorpunkt) basiert. Ein Client kann URL-Moniker zum Binden an Objekte verwenden, die sich im Internet befinden. Die vom System bereitgestellte URL-Monikerklasse unterstützt sowohl die synchrone als auch die asynchrone Bindung.

</dd> </dl>

 

 