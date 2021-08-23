---
title: COM-Glossar
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0c4c1aa78c81484666311dfcdd6bae8b4e6daaa45581af98f50171f48b4b58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048508"
---
# <a name="com-glossary"></a>COM-Glossar

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**Aktivierung**
</dt> <dd>

Der Prozess des Ladens eines Objekts in den Arbeitsspeicher, wodurch es in den Ausführungszustand versetzt wird.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**Aktiver Zustand**
</dt> <dd>

Ein COM-Objekt, das sich im Ausführungszustand befindet und über eine sichtbare Benutzeroberfläche verfügt.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**Absoluter Moniker**
</dt> <dd>

Ein Moniker, der die absolute Position eines Objekts angibt. Ein absoluter Moniker entspricht einem vollständigen Pfad.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**Advisory Holder**
</dt> <dd>

Ein COM-Objekt, das Benachrichtigungen über Änderungen an den Empfehlungssenken von Containeranwendungen zwischenspeichert, verwaltet und sendet.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**Advisory-Senke**
</dt> <dd>

Ein COM-Objekt, das Benachrichtigungen über Änderungen in einem eingebetteten Objekt oder verknüpften Objekt empfangen kann, da es die [**IAdviseSink-**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) oder [**IAdviseSink2-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) implementiert. Container, die über Änderungen in Objekten benachrichtigt werden müssen, implementieren eine Empfehlungssenke. Benachrichtigungen stammen vom Server, der ein Advisory Holder-Objekt verwendet, um Benachrichtigungen an Container zwischenzuspeichern und zu verwalten.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**Aggregatobjekt**
</dt> <dd>

Ein COM-Objekt, das aus einem oder mehreren anderen COM-Objekten besteht. Ein Objekt im Aggregat wird als steuerungsobjekt festgelegt, das steuert, welche Schnittstellen im Aggregat verfügbar gemacht werden und welche privat sind. Dieses steuernde Objekt verfügt über eine spezielle Implementierung von [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) die als steuernde **IUnknown** bezeichnet wird. Alle Objekte im Aggregat müssen Aufrufe an **IUnknown-Methoden** über das steuernde **IUnknown** übergeben.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**Aggregation**
</dt> <dd>

Eine Kompositionstechnik zum Implementieren von COM-Objekten. Sie können ein neues Objekt erstellen, indem Sie die Schnittstellenimplementierungen eines oder mehrerer vorhandener Objekte wiederverwenden. Das Aggregatobjekt wählt aus, welche Schnittstellen für Clients verfügbar gemacht werden sollen, und die Schnittstellen werden so verfügbar gemacht, als ob sie vom Aggregatobjekt implementiert würden. Clients des Aggregatobjekts kommunizieren nur mit dem Aggregatobjekt.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**Ambient-Eigenschaft**
</dt> <dd>

Eine Laufzeiteigenschaft, die vom Container verwaltet und verfügbar gemacht wird. In der Regel stellt eine Ambient-Eigenschaft ein Merkmal eines Formulars dar, z. B. eine Hintergrundfarbe, die an ein Steuerelement kommuniziert werden muss, damit das Steuerelement das Aussehen und Das gefühl seiner Umgebung annehmen kann.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**Antimoniker**
</dt> <dd>

Die Umkehrung eines Datei-, Element- oder Zeigermonikers. Ein Antimoniker wird am Ende einer Datei, eines Elements oder eines Zeigermonikers hinzugefügt, um ihn auf null zu kennzeichnen. Antimoniker werden bei der Erstellung relativer Moniker verwendet.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**künstliche Verweiszählung**
</dt> <dd>

Eine Technik, die verwendet wird, um ein Objekt vor dem Aufrufen einer Funktion oder Methode zu schützen, die es vorzeitig zerstören könnte. Ein Programm ruft **IUnknown::AddRef** auf, um den Verweiszähler des Objekts vor dem Aufruf zu erhöhen, der das Objekt freigeben könnte. Nachdem die Funktion zurückgegeben wurde, ruft das Programm **IUnknown::Release** auf, um die Anzahl zu dekrementen.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchrone Bindung**
</dt> <dd>

Ein Bindungstyp, bei dem es erforderlich ist, dass der Prozess asynchron ausgeführt wird, um Leistungseinbußen für den Endbenutzer zu vermeiden. In der Regel wird die asynchrone Bindung in verteilten Umgebungen wie der World Wide Web verwendet. OLE unterstützt asynchrone Monikerklassen und Rückrufmechanismen, die es ermöglichen, ein Objekt in einer verteilten Umgebung zu suchen und zu initialisieren, während andere Vorgänge ausgeführt werden.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchroner Aufruf**
</dt> <dd>

Ein Aufruf einer Funktion, die separat ausgeführt wird, sodass der Aufrufer die Verarbeitung von Anweisungen fortsetzen kann, ohne auf die Rückgabe der Funktion zu warten.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchroner Moniker**
</dt> <dd>

Ein Moniker, der die asynchrone Bindung unterstützt. Instanzen der vom System bereitgestellten URL-Monikerklasse sind beispielsweise asynchrone Moniker.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**Automatisierung**
</dt> <dd>

Eine Möglichkeit, die Objekte einer Anwendung von außerhalb der Anwendung zu bearbeiten. Automatisierung wird in der Regel verwendet, um Anwendungen zu erstellen, die Objekte für Programmiertools und Makrosprachen verfügbar machen, die Objekte einer Anwendung aus anderen Anwendungen zu erstellen und zu bearbeiten oder um Tools für den Zugriff auf und die Bearbeitung von Objekten zu erstellen.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**Bindungskontext**
</dt> <dd>

Ein COM-Objekt, das die [**IBindCtx-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) implementiert. Bindungskontexte werden in Monikervorgängen verwendet, um Verweise auf die Objekte zu speichern, die aktiviert werden, wenn ein Moniker gebunden wird. Der Bindungskontext enthält Parameter, die für alle Vorgänge während der Bindung eines generischen zusammengesetzten Monikers gelten, und bietet der Monikerimplementierungen Zugriff auf Informationen über seine Umgebung.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**Bindung**
</dt> <dd>

Zuordnen eines Namens zu seinem Referenz. Suchen Sie insbesondere das Objekt mit dem Namen eines Monikers, versetzen Sie es in seinen Ausführungszustand, sofern es noch nicht vorhanden ist, und geben Sie einen Schnittstellenzeiger darauf zurück. Objekte können zur Laufzeit (auch als späte Bindung oder dynamische Bindung bezeichnet) oder zur Kompilierzeit (auch als statische Bindung bezeichnet) gebunden werden.

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**Cache**
</dt> <dd>

Ein (in der Regel temporärer) lokaler Informationsspeicher. In OLE enthält ein Cache Informationen, die die Darstellung eines verknüpften oder eingebetteten Objekts definieren, wenn der Container geöffnet wird.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**Cacheinitialisierung**
</dt> <dd>

Auffüllen des Caches eines verknüpften oder eingebetteten Objekts mit Präsentationsdaten. Die [**IOleCache-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) stellt Methoden bereit, die ein Container aufrufen kann, um die Daten zu steuern, die für verknüpfte oder eingebettete Objekte zwischengespeichert werden.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**Klasse**
</dt> <dd>

Die Definition eines Objekts im Code. In C++ ist die Klasse eines Objekts als Datentyp definiert, aber dies ist in anderen Sprachen nicht der Fall. Da OLE in einer beliebigen Sprache codiert werden kann, wird die -Klasse verwendet, um auf die allgemeine Objektdefinition zu verweisen.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**Klassenfactory**
</dt> <dd>

Ein COM-Objekt, das die [**IClassFactory-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) implementiert und eine oder mehrere Instanzen eines Objekts erstellt, das durch einen angegebenen Klassenbezeichner (CLSID) identifiziert wird.

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**Klassenbezeichner (CLSID)**
</dt> <dd>

Ein GUID (Globally Unique Identifier), der einem OLE-Klassenobjekt zugeordnet ist. Wenn ein Klassenobjekt verwendet wird, um mehrere Instanzen eines Objekts zu erstellen, sollte die zugeordnete Serveranwendung ihre CLSID in der Systemregistrierung registrieren, damit Clients den ausführbaren Code finden und laden können, der den Objekten zugeordnet ist. Jeder OLE-Server oder -Container, der das Verknüpfen mit eingebetteten Objekten zulässt, muss eine CLSID für jede unterstützte Objektdefinition registrieren.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**Klassenobjekt**
</dt> <dd>

Bei der objektorientierten Programmierung ein Objekt, dessen Zustand von allen Objekten in einer Klasse gemeinsam genutzt wird und dessen Verhalten auf diese klassenweiten Zustandsdaten angewendet wird. In COM werden Klassenobjekte als Klassenfactorys bezeichnet und weisen in der Regel kein Verhalten auf, außer neue Instanzen der -Klasse zu erstellen.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**Kunde**
</dt> <dd>

Ein COM-Objekt, das Dienste von einem anderen -Objekt anfordert.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**Clientstandort**
</dt> <dd>

Die Anzeigewebsite für ein eingebettetes oder verknüpftes Objekt in einem zusammengesetzten Dokument. Der Clientstandort ist das Prinzipal, mit dem ein Objekt Dienste von seinem Container anfordert.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**Clsid**
</dt> <dd>

Ein GUID (Globally Unique Identifier), der einem OLE-Klassenobjekt zugeordnet ist. Wenn ein Klassenobjekt verwendet wird, um mehrere Instanzen eines Objekts zu erstellen, sollte die zugeordnete Serveranwendung ihre CLSID in der Systemregistrierung registrieren, damit Clients den ausführbaren Code finden und laden können, der den Objekten zugeordnet ist. Jeder OLE-Server oder -Container, der das Verknüpfen mit eingebetteten Objekten zulässt, muss eine CLSID für jede unterstützte Objektdefinition registrieren.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**begehen**
</dt> <dd>

Zum dauerhaften Speichern von Änderungen, die seit dem Öffnen oder letzten Speichern von Änderungen an einem Speicher- oder Streamobjekt vorgenommen wurden.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**Komponente**
</dt> <dd>

Ein Objekt, das sowohl Daten als auch Code kapselt und einen gut angegebenen Satz öffentlich verfügbarer Dienste bereitstellt.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**
</dt> <dd>

Das objektorientierte OLE-Programmiermodell, das definiert, wie Objekte innerhalb eines einzelnen Prozesses oder zwischen Prozessen interagieren. In COM haben Clients Zugriff auf ein Objekt über Schnittstellen, die für das Objekt implementiert sind.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**Zusammengesetzte Menüleiste**
</dt> <dd>

Eine freigegebene Menüleiste, die aus Menügruppen aus einer Containeranwendung und einer direkt aktivierten Serveranwendung besteht.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**Zusammengesetzter Moniker**
</dt> <dd>

Ein Moniker, der aus zwei oder mehr Monikern besteht, die als Einheit behandelt werden. Ein zusammengesetzter Moniker kann nicht generisch sein, was bedeutet, dass seine Komponentenmoniker über besondere Kenntnisse untereinander verfügen, oder generisch, was bedeutet, dass seine Komponentenmoniker nichts übereinander wissen, außer dass es sich um Moniker handelt.

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**Verbunddokument**
</dt> <dd>

Ein Dokument, das verknüpfte oder eingebettete Objekte sowie eigene native Daten enthält.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**Verbunddatei**
</dt> <dd>

Eine von OLE bereitgestellte Strukturierte Storage-Implementierung.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM-Objekt**
</dt> <dd>

Ein Objekt, das dem OLE-Component Object Model (COM) entspricht. Ein COM-Objekt ist eine Instanz einer Objektdefinition, die die Daten des Objekts und eine oder mehrere Implementierungen von Schnittstellen für das Objekt angibt. Clients interagieren nur über seine Schnittstellen mit einem COM-Objekt.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**Verbindungsfähiges Objekt**
</dt> <dd>

Ein COM-Objekt, das mindestens die [**IConnectionPointContainer-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) für die Verwaltung von Verbindungspunktobjekten implementiert. Miteinander verbindende Objekte unterstützen die Kommunikation zwischen dem Server und dem Client. Ein verbindungsfähiges Objekt erstellt und verwaltet mindestens ein Verbindungspunkt-Unterobjekt, das Ereignisse von Schnittstellen empfängt, die für andere Objekte implementiert sind, und diese an den Client sendet.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**Verbindungspunktobjekt**
</dt> <dd>

Ein COM-Objekt, das von einem verbindungsfähigen Objekt verwaltet wird und die [**IConnectionPoint-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) implementiert. Ein oder mehrere Verbindungspunktobjekte können von einem verbundenen Objekt erstellt und verwaltet werden. Jedes Verbindungspunktobjekt verwaltet eingehende Ereignisse von einer bestimmten Schnittstelle auf einem anderen Objekt und sendet diese Ereignisse an den Client.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**Containeranwendung**
</dt> <dd>

Eine Anwendung, die zusammengesetzte Dokumente unterstützt. Die Containeranwendung stellt Speicher für ein eingebettetes oder verknüpftes Objekt, eine Website für die Anzeige, den Zugriff auf die Anzeigewebsite und eine Empfehlungssenke zum Empfangen von Benachrichtigungen über Änderungen im Objekt bereit.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**Containment**
</dt> <dd>

Eine Kompositionstechnik zum Implementieren von COM-Objekten. Es ermöglicht einem Objekt, einige oder alle Schnittstellenimplementierungen eines oder mehrerer anderer Objekte wiederzuverwenden. Das äußere Objekt fungiert als Client an die anderen Objekte und delegiert die Implementierung, wenn es die Dienste eines der enthaltenen Objekte verwenden möchte.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**Kontext**
</dt> <dd>

In COM+ ein Satz von Laufzeiteigenschaften, die einem oder mehreren COM-Objekten zugeordnet sind, die zum Bereitstellen von Diensten für diese Objekte verwendet werden.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**Steuerung**
</dt> <dd>

Ein einbettbares, wiederverwendbares COM-Objekt, das mindestens die [**IOleControl-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) unterstützt. Steuerelemente sind in der Regel der Benutzeroberfläche zugeordnet. Sie unterstützen auch die Kommunikation mit einem Container und können je nach Lizenzierungskriterien von mehreren Clients wiederverwendet werden.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**Steuerelementcontainer**
</dt> <dd>

Eine Anwendung, die das Einbetten von Steuerelementen durch Implementieren der [**IOleControlSite-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) unterstützt.

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Control-Eigenschaft**
</dt> <dd>

Eine Laufzeiteigenschaft, die vom Steuerelement selbst verfügbar gemacht und verwaltet wird. Beispielsweise sind die vom Steuerelement verwendeten Schrift- und Textgrößen Steuerelementeigenschaften.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**Steuern des Objekts**
</dt> <dd>

Das Objekt in einem Aggregatobjekt, das steuert, welche Schnittstellen innerhalb des Aggregatobjekts verfügbar gemacht werden und welche privat sind. Die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) des steuernden Objekts wird als steuernde **IUnknown** bezeichnet. Aufrufe von **IUnknown-Methoden** anderer Objekte im Aggregat müssen an das steuernde **IUnknown** übergeben werden.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**Steuerungsstandort**
</dt> <dd>

Eine Struktur, die von einem Steuerelementcontainer zum Verwalten der Anzeige und Speicherung eines Steuerelements implementiert wird. Innerhalb eines bestimmten Containers verfügt jedes Steuerelement über eine entsprechende Steuerelementsite.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**Datenübertragungsobjekt**
</dt> <dd>

An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**Standardobjekthandler**
</dt> <dd>

Eine mit OLE bereitgestellte DLL, die als Ersatz im Verarbeitungsbereich der Containeranwendung für das echte Objekt fungiert.

Mit dem Standardobjekthandler ist es möglich, die gespeicherten Daten eines Objekts zu betrachten, ohne das Objekt tatsächlich zu aktivieren. Der Standardobjekthandler führt andere Aufgaben aus, z. B. das Rendern eines Objekts aus seinem zwischengespeicherten Zustand, wenn das Objekt in den Arbeitsspeicher geladen wird.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**Abhängiges Objekt**
</dt> <dd>

Ein COM-Objekt, das in der Regel von einem anderen -Objekt (dem Hostobjekt) initialisiert wird. Obwohl die Lebensdauer des abhängigen Objekts nur während der Lebensdauer des Hostobjekts sinnvoll sein kann, funktioniert das Hostobjekt nicht als steuernde [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für das abhängige Objekt. Im Gegensatz dazu ist ein Objekt ein aggregiertes Objekt, wenn seine Lebensdauer (mithilfe des Verweiszählers) vollständig durch das verwaltende Objekt gesteuert wird.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**Direktzugriffsmodus**
</dt> <dd>

Einer von zwei Zugriffsmodi, in denen ein Speicherobjekt geöffnet werden kann. Im direkten Modus werden alle Änderungen sofort an das Stammspeicherobjekt übergeben.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**Dokumentobjekt**
</dt> <dd>

Ein OLE-Dokument, das eine oder mehrere direkt aktivierte Ansichten seiner Daten in einem nativen oder fremden Frame anzeigen kann, z. B. in einem Browser, während die vollständige Kontrolle über die Benutzeroberfläche erhalten bleibt. Zusätzlich zur Implementierung der üblichen OLE-Dokument- und Direktaktivierungsschnittstellen muss ein Dokumentobjekt [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)implementieren, und jede seiner Ansichten (in Form eines Dokumentansichtsobjekts) muss [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview)implementieren.

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**Dokumentobjektcontainer**
</dt> <dd>

Eine Containeranwendung, die eine oder mehrere Ansichten eines oder mehrerer Dokumentobjekte anzeigen und alle enthaltenen Dokumentobjekte in einer Datei verwalten kann. Jedes Dokumentobjekt ist einer Dokumentwebsite zugeordnet, und jede Dokumentwebsite enthält mindestens einen Dokumentansichtsstandort, der den vom Dokumentobjekt unterstützten Ansichten entspricht. Ein Dokumentobjektcontainer enthält auch einen Containerrahmen, der die Menü- und Symbolleistenaushandlung und die Enumeration enthaltener Objekte behandelt.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**Dokumentobjektserver**
</dt> <dd>

Eine Serveranwendung, die Dokumentobjekte bereitstellen kann.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**Dokumentwebsite**
</dt> <dd>

Ein Clientstandort, der von einem Dokumentobjektcontainer zum Verwalten der Anzeige und Speicherung eines Dokumentobjekts implementiert wird. Jedes Dokumentobjekt in einem Container verfügt über eine entsprechende Dokumentwebsite.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**Dokumentstandortobjekt**
</dt> <dd>

Ein COM-Objekt, das zusätzlich zu den üblichen Clientstandortschnittstellen (z. B. [**IOleClientSite) die IOleDocumentSite-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)implementiert. [](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite)

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**Dokumentansicht**
</dt> <dd>

Eine bestimmte Darstellung der Daten eines Dokuments. Ein einzelnes Dokumentobjekt kann über eine oder mehrere Ansichten verfügen, aber eine einzelne Dokumentansicht kann nur zu einem Dokumentobjekt gehören.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**Dokumentansichtsobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**IOleDocumentView-Schnittstelle**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) implementiert und einer bestimmten Dokumentansicht entspricht. Ein Objekt mit mehreren Dokumentansichten aggregiert ein separates Dokumentansichtsobjekt für jede Ansicht.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**Website der Dokumentansicht**
</dt> <dd>

Ein Objekt, das von einem Dokumentwebsiteobjekt aggregiert wird, um den Anzeigebereich für eine bestimmte Ansicht eines Dokumentobjekts zu verwalten. Innerhalb einer bestimmten Dokumentwebsite verfügt jede Dokumentansicht über eine entsprechende Website für die Dokumentansicht.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**Websiteobjekt der Dokumentansicht**
</dt> <dd>

Ein COM-Objekt, das in einem Dokumentwebsiteobjekt aggregiert wird und die [**IOleInPlaceSite-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) und optional die [**IContinueCallback-Schnittstelle**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) implementiert.

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**
</dt> <dd>

Ein Vorgang, bei dem der Endbenutzer die Maus oder ein anderes zeigendes Gerät verwendet, um Daten an eine andere Position im gleichen Fenster oder in einem anderen Fenster zu verschieben.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Einbinden**
</dt> <dd>

So fügen Sie ein Objekt in ein zusammengesetztes Dokument so ein, dass die für dieses Objekt nativen Datenformate beibehalten werden, und damit es mithilfe von Tools, die vom Server verfügbar gemacht werden, aus dem Container heraus bearbeitet werden kann.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**Eingebettetes Objekt**
</dt> <dd>

Ein Objekt, dessen Daten in einem zusammengesetzten Dokument gespeichert sind, das objekt jedoch im Prozessbereich des Servers ausgeführt wird. Der Standardobjekthandler stellt ein Ersatzzeichen im Verarbeitungsbereich der Containeranwendung für das echte Objekt bereit.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**erweiterte Eigenschaft**
</dt> <dd>

Eine Laufzeiteigenschaft, z. B. die Position und Größe eines Steuerelements, von der ein Benutzer ausgehen würde, dass sie vom Steuerelement verfügbar gemacht, aber vom Container verfügbar gemacht und verwaltet wird.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**Dateimoniker**
</dt> <dd>

Ein Moniker, der auf einem Pfad im Dateisystem basiert. Dateimoniker können verwendet werden, um Objekte zu identifizieren, die in ihren eigenen Dateien gespeichert sind. Ein Dateimoniker ist ein COM-Objekt, das die vom System bereitgestellte Implementierung der [**IMoniker-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) für die Dateimonikerklasse unterstützt.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font-Objekt**
</dt> <dd>

Ein COM-Objekt, das durch Implementierung der [**IFont-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) Zugriff auf Graphics Device Interface -Schriftarten (GDI) bietet.

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**Formatbezeichner**
</dt> <dd>

Eine GUID, die einen permanenten Eigenschaftensatz identifiziert. Wird auch als FMTID bezeichnet.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**Rahmen**
</dt> <dd>

Der Teil einer Containeranwendung, der für das Aushandeln von Menüs, Zugriffstasten, Symbolleisten und anderen freigegebenen Benutzeroberflächenelementen mit einem eingebetteten COM-Objekt oder einem Dokumentobjekt zuständig ist.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**Frameobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**IOleInPlaceFrame-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) und optional die [**IOleCommandTarget-Schnittstelle**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) implementiert.

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**Generischer zusammengesetzter Moniker**
</dt> <dd>

Eine sequenzierte Sammlung von Monikern, beginnend mit einem Dateimoniker, um den Pfad auf Dokumentebene bereitzustellen und mit einem oder mehreren Elementmonikern fortzufahren, die als Ganzes ein Objekt eindeutig identifizieren.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**Hilfsfunktion**
</dt> <dd>

Eine Funktion, die Aufrufe anderer Funktionen und Schnittstellenmethoden kapselt, die im OLE SDK öffentlich verfügbar sind. Hilfsfunktionen sind eine praktische Möglichkeit zum Aufrufen häufig verwendeter Sequenzen von Funktions- und Methodenaufrufen, die allgemeine Aufgaben erfüllen.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**Hostobjekt**
</dt> <dd>

Ein COM-Objekt, das eine hierarchische Beziehung mit einem oder mehr anderen COM-Objekten bildet, die als abhängige Objekte bezeichnet werden. In der Regel instanziiert das Hostobjekt die abhängigen Objekte, und ihr Vorhandensein ist nur innerhalb der Lebensdauer des Hostobjekts sinnvoll. Das Hostobjekt wird jedoch nicht als steuernde [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) für die abhängigen Objekte fungieren und auch nicht direkt an die Schnittstellenimplementierungen dieser Objekte delegiert.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**Hresult**
</dt> <dd>

Ein nicht transparentes Ergebnishand handle, das für eine erfolgreiche Rückgabe einer Funktion auf 0 festgelegt ist, und ungleich 0 (null), wenn Fehler- oder Statusinformationen zurückgegeben werden.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**Hyperlinkobjekt**
</dt> <dd>

Ein COM-Objekt, das mindestens die [**IHlink-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) implementiert und als Link zu einem Objekt an einer anderen Position (dem Ziel) fungiert. Ein Link besteht aus vier Teilen: einem Moniker, der die Position des Ziels identifiziert. eine Zeichenfolge für den Speicherort innerhalb des Ziels; einen anzeigebaren Namen für das Ziel; und eine Zeichenfolge, die zusätzliche Parameter enthalten kann.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**Kontext zum Durchsuchen von Links**
</dt> <dd>

Ein COM-Objekt, das die [**IHlinkBrowseContext-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) implementiert und den Linknavigationsstapel verwaltet. Das Durchsuchenkontextobjekt verwaltet das Fenster des Hyperlinkframefensters und des Hyperlinkzielobjekts.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**Hyperlinkcontainer**
</dt> <dd>

Eine Containeranwendung, die Hyperlinks unterstützt, indem die [**IHlinkSite-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) implementiert wird, und, wenn die Objekte des Containers Ziele anderer Links sein können, die [**IHlinkTarget-Schnittstelle.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85))

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**Hyperlinkframe-Objekt**
</dt> <dd>

Ein COM-Objekt, das die [**IHlinkFrame-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) implementiert und die Navigation auf oberster Ebene und die Anzeige von Links für den Container des Frames und den Server des Linkziels steuert.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**Linkwebsiteobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**IHlinkSite-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) implementiert und entweder den Moniker oder den Schnittstellenbezeichner des Hyperlinkcontainers liefert. Eine Linkwebsite kann mehrere Links bedienen.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**Linkzielobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**IHlinkTarget-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) implementiert und seinen Moniker, den Angezeigtennamen und andere Informationen zur Verfügung stellt, die andere Linkobjekte verwenden, um zu ihr zu navigieren.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in-Parameter**
</dt> <dd>

Ein Parameter, der vom Aufrufer einer Funktion oder Schnittstellenmethode zugeordnet, festgelegt und freigibt. Ein in-Parameter wird von der aufgerufenen Funktion nicht geändert.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**In-/Out-Parameter**
</dt> <dd>

Ein Parameter, der anfänglich vom Aufrufer einer Funktion oder Schnittstellenmethode zugeordnet und bei Bedarf durch den aufgerufenen Prozess festgelegt, frei und neu zugeordnet wird.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**In-Place-Aktivierung**
</dt> <dd>

Bearbeiten eines eingebetteten Objekts innerhalb des Fensters seines Containers mithilfe der vom Server bereitgestellten Tools. Verknüpfte Objekte unterstützen keine direkt aktivierte Aktivierung. sie werden immer im Fenster des Servers bearbeitet.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**In-Process-Server**
</dt> <dd>

Ein Als DLL implementierter Server, der im Prozessbereich des Clients ausgeführt wird.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**Instanz**
</dt> <dd>

Ein Objekt, für das Arbeitsspeicher zugeordnet wird oder das persistent ist.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**Schnittstelle**
</dt> <dd>

Eine Gruppe semantisch verwandter Funktionen, die Zugriff auf ein COM-Objekt bereitstellen. Jede OLE-Schnittstelle definiert einen Vertrag, der es Objekten ermöglicht, entsprechend dem Component Object Model (COM) zu interagieren. OLE bietet zwar viele Schnittstellenimplementierungen, die meisten Schnittstellen können jedoch auch von Entwicklern implementiert werden, die OLE-Anwendungen entwerfen.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**Schnittstellenbezeichner (INTERFACE Identifier, IID)**
</dt> <dd>

Ein GUID (Globally Unique Identifier), der einer Schnittstelle zugeordnet ist. Einige Funktionen verwenden IIDs als Parameter, damit der Aufrufer angeben kann, welcher Schnittstellenzeiger zurückgegeben werden soll.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**Elementmoniker**
</dt> <dd>

Ein Moniker, der auf einer Zeichenfolge basiert, die ein Objekt in einem Container identifiziert. Elementmoniker können Objekte identifizieren, die kleiner als eine Datei sind, einschließlich eingebetteter Objekte in einem Verbunddokument oder eines Pseudoobjekts (z. B. ein Zellenbereich in einer Kalkulationstabelle).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**Lizenzierung**
</dt> <dd>

Ein Feature von COM, das die Kontrolle über die Objekterstellung bietet. Lizenzierte Objekte können nur von Clients erstellt werden, die für deren Verwendung autorisiert sind. Die Lizenzierung wird in COM über die [**IClassFactory2-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) und durch Unterstützung eines Lizenzschlüssels implementiert, der zur Laufzeit übergeben werden kann.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link-Objekt**
</dt> <dd>

Ein COM-Objekt, das erstellt wird, wenn ein verknüpftes COM-Objekt erstellt oder geladen wird. Das Linkobjekt wird von OLE bereitgestellt und implementiert die [**IOleLink-Schnittstelle.**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**Verknüpftes Objekt**
</dt> <dd>

Ein COM-Objekt, dessen Quelldaten sich physisch dort befinden, wo sie ursprünglich erstellt wurden. Nur ein Moniker, der die Quelldaten und die entsprechenden Präsentationsdaten darstellt, wird im Verbunddokument beibehalten. Änderungen an der Linkquelle werden automatisch im verknüpften Objekt widergespiegelt.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**Linkquelle**
</dt> <dd>

Die Daten, die die Quelle eines verknüpften Objekts sind. Eine Linkquelle kann eine Datei oder ein Teil einer Datei sein, z. B. ein ausgewählter Zellenbereich innerhalb einer Datei (auch als Pseudoobjekt bezeichnet).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**Geladener Zustand**
</dt> <dd>

Der Zustand eines Objekts, nachdem seine Datenstrukturen in den Arbeitsspeicher geladen wurden und für den Clientprozess zugänglich sind.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**Lokaler Server**
</dt> <dd>

Ein Out-of-Process-Server, der als .EXE anwendung implementiert ist, die auf demselben Computer wie die Clientanwendung ausgeführt wird.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**Sperren**
</dt> <dd>

Ein Zeiger, der auf gehalten wird, und möglicherweise eine Verweisanzahl, die auf einem ausgeführten Objekt inkrementiert wird. OLE definiert zwei Arten von Sperren, die für ein Objekt gehalten werden können: stark und schwach. Um eine starke Sperre zu implementieren, muss ein Server sowohl einen Zeiger als auch einen Verweiszähler verwalten, damit das Objekt mindestens im Arbeitsspeicher "gesperrt" bleibt, bis der Server [**IUnknown::Release aufruft.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Um eine schwache Sperre zu implementieren, verwaltet der Server nur einen Zeiger auf das Objekt, sodass das Objekt von einem anderen Prozess zerstört werden kann.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**Marshalling**
</dt> <dd>

Packen und Senden von Schnittstellenmethode-Aufrufen über Thread- oder Prozessgrenzen hinweg.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**Medientyp**
</dt> <dd>

Eine Erweiterung von MIME, die die Aushandlung des Datenformats zwischen einem Client und einem Objekt ermöglicht.

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME-Inhaltstyp**
</dt> <dd>

Eine Erweiterung von MIME, die die Aushandlung des Datenformats zwischen einem Client und einem Objekt ermöglicht.

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME) (Mehrzweck-Internet-E-Mail-Erweiterung (MIME))**
</dt> <dd>

Ein Internetprotokoll, das ursprünglich entwickelt wurde, um den Austausch von E-Mail-Nachrichten mit umfangreichem Inhalt über heterogene Netzwerk-, Computer- und E-Mail-Umgebungen hinweg zu ermöglichen. In der Praxis wurde MIME auch von Nicht-E-Mail-Anwendungen übernommen und erweitert.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Ein Objekt, das die [**IMoniker-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) implementiert. Ein Moniker fungiert als Name, der ein COM-Objekt eindeutig identifiziert. Auf die gleiche Weise wie ein Pfad eine Datei im Dateisystem identifiziert, identifiziert ein Moniker ein COM-Objekt im Verzeichnisnamespace.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker-Klasse**
</dt> <dd>

Eine Implementierung der [**IMoniker-Schnittstelle.**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) Vom System bereitgestellte Monikerklassen umfassen Dateimoniker, Elementmoniker, generische zusammengesetzte Moniker, Antimoniker, Zeigermoniker und URL-Moniker.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**Monikerclient**
</dt> <dd>

Eine Anwendung, die Moniker verwendet, um Schnittstellenzeger auf Objekte zu erhalten, die von einer anderen Anwendung verwaltet werden.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**Monikeranbieter**
</dt> <dd>

Eine Anwendung, die Moniker zur Verfügung stellt, die die von ihr verwalteten Objekte identifizieren, sodass auf die Objekte für andere Anwendungen zugegriffen werden kann.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**Namespaceerweiterung**
</dt> <dd>

Ein prozessin bearbeitungsbasiertes COM-Objekt, das [**IShellFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)und [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview)implementiert, die manchmal als Namespaceerweiterungsschnittstellen bezeichnet werden. Eine Namespaceerweiterung wird entweder verwendet, um den Namespace der Shell zu erweitern oder einen separaten Namespace zu erstellen. Primäre Benutzer sind die Windows Explorer und allgemeine Dateidialogfelder.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**Native Daten**
</dt> <dd>

Die Daten, die von einer OLE-Serveranwendung beim Bearbeiten eines eingebetteten Objekts verwendet werden.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**Objekt**
</dt> <dd>

In OLE eine Programmierstruktur, die sowohl Daten als auch Funktionen kapselt, die als einzelne Einheit definiert und zugeordnet sind und für die der einzige öffentliche Zugriff über die Schnittstellen der Programmierstruktur erfolgt. Ein COM-Objekt muss mindestens die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) unterstützen, die das Vorhandensein des Objekts bei der Verwendung beibeträgt und Zugriff auf die anderen Schnittstellen des Objekts bietet.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**Objektzustand** 
</dt> <dd>

Die Beziehung zwischen einem zusammengesetzten Dokumentobjekt in seinem Container und der Anwendung, die für die Erstellung des Objekts verantwortlich ist: aktiv, passiv, geladen oder ausgeführt. Passive Objekte werden auf dem Datenträger oder in einer Datenbank gespeichert, und das Objekt ist nicht ausgewählt oder aktiv. Im geladenen Zustand wurden die Datenstrukturen des Objekts in den Arbeitsspeicher geladen, sind aber nicht für Vorgänge wie die Bearbeitung verfügbar. Ausgeführte Objekte werden geladen und sind für alle Vorgänge verfügbar. Aktive Objekte werden ausgeführt, die über eine sichtbare Benutzeroberfläche verfügen.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**Objekttypname**
</dt> <dd>

Eine eindeutige Identifikationszeichenfolge, die als Teil der Informationen gespeichert wird, die für ein Objekt in der Registrierungsdatenbank verfügbar sind.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**Ole**
</dt> <dd>

Die objektbasierte Technologie von Microsoft zum freigeben von Informationen und Diensten über Prozess- und Computergrenzen hinweg.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**Out-of-Process-Server**
</dt> <dd>

Ein Server, der als .EXE-Anwendung implementiert ist und außerhalb des Prozesses des Clients ausgeführt wird, entweder auf demselben Computer oder einem Remotecomputer.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out-Parameter**
</dt> <dd>

Ein out-Parameter wird von der aufgerufenen Funktion zugeordnet und vom Aufrufer freigibt.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passiver Zustand**
</dt> <dd>

Der Zustand eines COM-Objekts, wenn es gespeichert wird (auf dem Datenträger oder in einer Datenbank). Das Objekt ist nicht ausgewählt oder aktiv.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**Persistente Eigenschaft**
</dt> <dd>

Informationen, die dauerhaft als Teil eines Speicherobjekts gespeichert werden können, z. B. eine Datei oder ein Verzeichnis. Persistente Eigenschaften werden in Eigenschaftensätze eingekreist, die angezeigt und bearbeitet werden können.

Eine persistente Eigenschaft ist anders als die Laufzeiteigenschaften von Objekten, die mit OLE-Steuerelementen und Automatisierungstechnologien erstellt wurden, die verwendet werden können, um das Systemverhalten zu beeinflussen. Die [**PROPVARIANT-Struktur**](/windows/win32/api/propidl/ns-propidl-propvariant) definiert alle gültigen Typen von persistenten Eigenschaften, während die **VARIANT-Struktur** alle gültigen Typen von Laufzeiteigenschaften definiert.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**Persistenter Speicher**
</dt> <dd>

Storage einer Datei oder eines Objekts in einem Medium wie einem Dateisystem oder einer Datenbank, sodass das Objekt und seine Daten beibehalten werden, wenn die Datei geschlossen und dann zu einem späteren Zeitpunkt erneut geöffnet wird.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**Bildobjekt**
</dt> <dd>

Ein COM-Objekt, das den Zugriff auf GDI-Bilder durch Implementierung der [**IPicture-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) ermöglicht.

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**Zeigermoniker**
</dt> <dd>

Ein Moniker, der einem Objekt im Arbeitsspeicher einen Schnittstellenzeiger zu ordnet. Während die meisten Moniker Objekte identifizieren, die dauerhaft gespeichert werden können, identifizieren Zeigermoniker Objekte, die dies nicht können. Sie ermöglichen es solchen Objekten, an einem Monikerbindungsvorgang teilzunehmen.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**Präsentationsdaten**
</dt> <dd>

Die Daten, die von einem Container zum Anzeigen eingebetteter oder verknüpfter Objekte verwendet werden.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primäres Verb**
</dt> <dd>

Die Aktion, die dem gängigsten oder bevorzugten Vorgang zugeordnet ist, den Benutzer für ein Objekt ausführen. Das primäre Verb wird in der Systemregistrierungsdatenbank immer als Verb 0 definiert. Das primäre Verb eines Objekts wird durch Doppelklicken auf das Objekt ausgeführt.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Eigenschaft**
</dt> <dd>

Informationen, die einem -Objekt zugeordnet sind. In OLE lassen sich Eigenschaften in zwei Kategorien unterteilen: Laufzeiteigenschaften und persistente Eigenschaften. Laufzeiteigenschaften werden in der Regel Steuerelementobjekten oder deren Containern zugeordnet. Beispielsweise ist die Hintergrundfarbe eine Laufzeiteigenschaft, die vom Container eines Steuerelements festgelegt wird. Persistente Eigenschaften sind gespeicherten Objekten zugeordnet.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**Eigenschaftenrahmen**
</dt> <dd>

Der Benutzeroberflächenmechanismus, der eine oder mehrere Eigenschaftenseiten für ein Steuerelement anzeigt. Das Ole Controls-Laufzeitsystem stellt eine Standardimplementierung eines Eigenschaftsrahmens zur Anwendung, auf den mithilfe der [**OleCreatePropertyFrame-Hilfsfunktion**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) zugegriffen werden kann.

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**Eigenschaftenbezeichner**
</dt> <dd>

Eine ganze Zahl mit Vier-Byte-Vorzeichen, die eine persistente Eigenschaft innerhalb eines Eigenschaftensets identifiziert.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**Eigenschaftenseite**
</dt> <dd>

Ein COM-Objekt mit eigener CLSID, das Teil einer Benutzeroberfläche ist, die von einem -Steuerelement implementiert wird und das Anzeigen und Festlegen der Eigenschaften des Steuerelements ermöglicht. Eigenschaftenseitenobjekte implementieren die [**IPropertyPage-Schnittstelle.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**Website der Eigenschaftenseite**
</dt> <dd>

Die Position innerhalb eines Eigenschaftsrahmens, an der eine Eigenschaftenseite angezeigt wird. Der Eigenschaftenrahmen implementiert die [**IPropertyPageSite-Schnittstelle,**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) die Methoden zum Verwalten der Websites der einzelnen Eigenschaftenseiten enthält, die von einem -Steuerelement bereitgestellt werden.

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**Eigenschaftensatz**
</dt> <dd>

Eine logisch verknüpfte Gruppe von Eigenschaften, die einem persistent gespeicherten Objekt zugeordnet ist. Implementieren Sie die [**IPropertySetStorage-Schnittstelle,**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) um einen oder mehrere Eigenschaftensätze zu erstellen, zu öffnen, zu löschen oder zu aufzählen. Wenn Sie Verbunddateien verwenden, können Sie die OLE-Implementierung dieser Schnittstelle verwenden, anstatt Ihre eigenen zu implementieren.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**Eigenschaftensatzspeicher**
</dt> <dd>

Ein COM-Speicherobjekt, das einen Eigenschaftensatz enthält. Ein Eigenschaftensatzspeicher ist ein abhängiges Objekt, das einem Speicherobjekt zugeordnet und von diesem verwaltet wird.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**Eigenschaftenblatt**
</dt> <dd>

Ein Satz von Eigenschaftenseiten für ein oder mehrere Objekte.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**Proxy**
</dt> <dd>

Ein schnittstellenspezifisches Objekt, das Parameter für diese Schnittstelle als Vorbereitung für einen Remotemethodeaufruf verpackt. Ein Proxy wird im Adressraum des Absenders ausgeführt und kommuniziert mit einem entsprechenden Stub im Adressraum des Empfängers.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Proxy-Manager**
</dt> <dd>

Beim Standard-Marshalling ein Proxy, der alle Schnittstellenproxys für ein einzelnes Objekt verwaltet.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**Pseudoobjekt**
</dt> <dd>

Ein Teil eines Dokuments oder eingebetteten Objekts, z. B. ein Zellenbereich in einem Arbeitsblatt, der die Quelle für ein COM-Objekt sein kann.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**Verweiszählung**
</dt> <dd>

Behalten Sie die Anzahl der einzelnen Schnittstellenzeiger für ein Objekt bei, um sicherzustellen, dass das Objekt nicht zerstört wird, bevor alle Verweise darauf freigegeben werden.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**Relativer Moniker**
</dt> <dd>

Ein Moniker, der die Position eines Objekts relativ zum Speicherort eines anderen Objekts angibt. Ein relativer Moniker entspricht einem relativen Pfad, z. B. . \\ backup \\ report.old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**Remoteserver**
</dt> <dd>

Eine Serveranwendung, die als EXE implementiert ist und auf einem anderen Computer als die Clientanwendung ausgeführt wird, die sie verwendet.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**Wiederherstellen**
</dt> <dd>

Zum Verwerfen von Änderungen, die seit dem letzten Committed der Änderungen oder dem Öffnen des Objektspeichers an einem Objekt vorgenommen wurden.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**Stammspeicherobjekt**
</dt> <dd>

Das äußerste Speicherobjekt in einem Dokument. Ein Stammspeicherobjekt kann andere geschachtelte Speicher- und Streamobjekte enthalten. Beispielsweise wird ein Verbunddokument als Eine Reihe von Speicher- und Streamobjekten in einem Stammspeicherobjekt auf dem Datenträger gespeichert.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**Ausführungsstatus**
</dt> <dd>

Der Zustand eines COM-Objekts, wenn seine Serveranwendung ausgeführt wird, und es ist möglich, auf seine Schnittstellen zu zugreifen und Benachrichtigungen über Änderungen zu erhalten.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**Running Object Table (ROT)**
</dt> <dd>

Eine global zugängliche Tabelle auf jedem Computer, die alle COM-Objekte im Ausführungszustand nachverfolgt, die durch einen Moniker identifiziert werden können. Monikeranbieter registrieren ein Objekt in der Tabelle, wodurch die Verweisanzahl des Objekts erhöht wird. Bevor das Objekt zerstört werden kann, muss sein Moniker aus der Tabelle freigegeben werden.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Laufzeiteigenschaft**
</dt> <dd>

Diskrete Zustandsinformationen, die einem Steuerelementobjekt oder dessen Container zugeordnet sind. Es gibt drei Typen von Laufzeiteigenschaften: Umgebungseigenschaften, Steuerelementeigenschaften und erweiterte Eigenschaften.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**Selbstregistrierung**
</dt> <dd>

Der Prozess, mit dem ein Server seine eigenen Registrierungsvorgänge ausführen kann.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**Serveranwendung**
</dt> <dd>

Eine Anwendung, die COM-Objekte erstellen kann. Containeranwendungen können dann einbetten oder mit diesen Objekten verknüpfen.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**Statisches Objekt**
</dt> <dd>

Ein Objekt, das nur eine Präsentation ohne native Daten enthält. Ein Container kann ein statisches Objekt so behandeln, als wäre es ein verknüpftes oder eingebettetes Objekt, mit der Ausnahme, dass es nicht möglich ist, ein statisches Objekt zu bearbeiten.

Ein statisches Objekt kann z. B. durch das Unterbrechen eines Links auf einem verknüpften Objekt entstehen, d.&a0;B. die Serveranwendung ist nicht verfügbar, oder der Benutzer möchte nicht mehr, dass das verknüpfte Objekt aktualisiert wird.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**Speicherobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**IStorage-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istorage) implementiert. Ein Speicherobjekt enthält geschachtelte Speicherobjekte oder Streamobjekte, was zur Entsprechung einer Verzeichnis-/Dateistruktur innerhalb einer einzelnen Datei führt.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**Streamobjekt**
</dt> <dd>

Ein COM-Objekt, das die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) implementiert. Ein Streamobjekt entspricht einer Datei in einem Verzeichnis/Dateisystem.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Strukturierte Storage**
</dt> <dd>

OLE-Technologie zum Speichern von Verbunddateien in nativen Dateisystemen.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Stub**
</dt> <dd>

Wenn die Parameter einer Funktion oder Schnittstellenmethode über eine Prozessgrenze gemarshallt werden, ist der Stub ein schnittstellenspezifisches Objekt, das die gemarshallten Parameter entpackt und die erforderliche Methode aufruft. Der Stub wird im Adressraum des Empfängers ausgeführt und kommuniziert mit einem entsprechenden Proxy im Adressraum des Absenders.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Stub-Manager**
</dt> <dd>

Verwaltet alle Schnittstellenstubs für ein einzelnes Objekt.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**Synchroner Aufruf**
</dt> <dd>

Ein Funktionsaufruf, der es nicht erlaubt, dass weitere Anweisungen im aufrufenden Prozess ausgeführt werden, bis die Funktion zurückgegeben wird.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Systemregistrierung**
</dt> <dd>

Ein systemweites Repository mit Informationen, die von Windows unterstützt werden, das Informationen über das System und seine Anwendungen enthält, einschließlich OLE-Clients und -Server.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**Transaktionszugriffsmodus**
</dt> <dd>

Einer von zwei Zugriffsmodi, in denen ein Speicherobjekt geöffnet werden kann. Beim Öffnen im transaktionsorientierten Modus werden Änderungen in Puffern gespeichert, bis das Stammspeicherobjekt einen Commit für die Änderungen ausgeführt hat.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**Typinformationen**
</dt> <dd>

Informationen über die Klasse eines Objekts, die von einer Typbibliothek bereitgestellt werden. Um Typinformationen zur Verfügung zu stellen, implementiert ein COM-Objekt die [**IProvideClassInfo-Schnittstelle.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**Einheitliche Datenübertragung**
</dt> <dd>

Ein Modell zum Übertragen von Daten durch die Zwischenablage, Drag & Drop oder Automation. Objekte, die diesem Modell entsprechen, implementieren die [**IDataObject-Schnittstelle.**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) Dieses Modell ersetzt DDE (dynamischer Datenaustausch).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**Unmarshaling**
</dt> <dd>

Entpacken von Parametern, die über Prozessgrenzen hinweg an einen Proxy gesendet wurden.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**Universal Resource Locator (URL)**
</dt> <dd>

Der bezeichner, der vom World Wide Web für die Namen und Speicherorte von Objekten im Internet verwendet wird. OLE stellt eine Monikerklasse( URL-Moniker) zur Verwendung, deren Implementierung verwendet werden kann, um einen Client an Objekte zu binden, die durch eine URL identifiziert werden.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL-Moniker**
</dt> <dd>

Ein Moniker, der auf einem universalen Ressourcenlocator (URL) basiert. Ein Client kann URL-Moniker verwenden, um eine Bindung an Objekte im Internet zu erstellen. Die vom System bereitgestellte URL-Monikerklasse unterstützt sowohl synchrone als auch asynchrone Bindungen.

</dd> </dl>

 

 