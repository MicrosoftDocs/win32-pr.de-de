---
title: Technische Übersicht über COM
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: Weitere Informationen finden Sie unter Technische Übersicht über COM.
keywords:
- COM Technical Overview COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851a2147c1bbe31dd8c212f7f23089c522cf7998bc2d336e95120277fba84275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854760"
---
# <a name="com-technical-overview"></a>Technische Übersicht über COM

Dieses Thema bietet eine Übersicht über microsoft Component Object Model (COM):

-   [Einführung in COM](#introduction-to-com)
-   [Objekte und Schnittstellen](#objects-and-interfaces)
-   [Schnittstellenimplementierung](#interface-implementation)
-   [Die IUnknown-Schnittstelle](#the-iunknown-interface)
-   [Das Client-/Servermodell](#the-clientserver-model)
-   [Dienststeuerungs-Manager](#service-control-manager)
-   [Wiederverwendbarkeit](#reusability)
-   [Storage und Streamen von Objekten](#storage-and-stream-objects)
-   [Datenübertragung](#data-transfer)
-   [Remoting](#remoting)
-   [Sicherheit](#security)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-com"></a>Einführung in COM

Der Microsoft Component Object Model (COM) definiert einen binären Interoperabilitätsstandard zum Erstellen wiederverwendbarer Softwarebibliotheken, die zur Laufzeit interagieren. Sie können COM-Bibliotheken verwenden, ohne sie in Ihre Anwendung kompilieren zu müssen. COM ist die Grundlage für eine Reihe von Microsoft-Produkten und -Technologien, z. B. Windows Media Player und Windows Server.

COM definiert einen binären Standard, der für viele Betriebssysteme und Hardwareplattformen gilt. Für Das Netzwerkcomputing definiert COM ein Standardmäßiges Kabelformat und -protokoll für die Interaktion zwischen Objekten, die auf verschiedenen Hardwareplattformen ausgeführt werden. COM ist unabhängig von der Implementierungssprache. Das bedeutet, dass Sie COM-Bibliotheken mit verschiedenen Programmiersprachen erstellen können, z. B. C++ und denen in der .NET Framework.

Die COM-Spezifikation bietet alle grundlegenden Konzepte, die die plattformübergreifende Wiederverwendung von Software ermöglichen:

-   Ein binärer Standard für Funktionsaufrufe zwischen Komponenten.
-   Eine Bereitstellung für stark typierte Gruppierungen von Funktionen in Schnittstellen.
-   Eine Basisschnittstelle, die Polymorphie, Featureermittlung und Objektlebensdauerverfolgung bietet.
-   Ein Mechanismus, der Komponenten und ihre Schnittstellen eindeutig identifiziert.
-   Ein Komponentenlader, das Komponenteninstanzen aus einer Bereitstellung erstellt.

COM besteht aus einer Reihe von Teilen, die zusammenarbeiten, um die Erstellung von Anwendungen zu ermöglichen, die aus wiederverwendbaren Komponenten erstellt werden:

-   Ein *Hostsystem,* das eine Laufzeitumgebung bietet, die der COM-Spezifikation entspricht.
-   *Schnittstellen,* die Featureverträge definieren, und *Komponenten,* die Schnittstellen implementieren.
-   *Server,* die Komponenten für das System bereitstellen, *und* Clients, die die von -Komponenten bereitgestellten Funktionen verwenden.
-   Eine *Registrierung,* die verfolgt, wo Komponenten auf lokalen und Remotehosts bereitgestellt werden.
-   Ein *Dienststeuerungs-Manager,* der Komponenten auf lokalen und Remotehosts sucht und Server mit Clients verbindet.
-   Ein *strukturiertes Speicherprotokoll,* das definiert, wie der Inhalt von Dateien im Dateisystem des Hosts navigiert wird.

Die Aktivierung der Übergreifenden Verwendung von Code über Hosts und Plattformen hinweg ist für COM von zentraler Bedeutung. Eine wiederverwendbare Schnittstellenimplementierung heißt eine *Komponente,* ein *Komponentenobjekt* oder ein *COM-Objekt.* Eine Komponente implementiert eine oder mehrere COM-Schnittstellen.

Sie definieren eine benutzerdefinierte COM-Bibliothek, indem Sie die Schnittstellen entwerfen, die ihre Bibliothek implementiert. Benutzer Ihrer Bibliothek können ihre Features entdecken und verwenden, ohne die Bereitstellungs- und Implementierungsdetails Ihrer Bibliothek zu wissen.

## <a name="objects-and-interfaces"></a>Objekte und Schnittstellen

Ein COM-Objekt macht seine Features über eine Schnittstelle *verfügbar,* bei der es sich um eine Auflistung von Memberfunktionen handelt. Eine COM-Schnittstelle definiert das erwartete Verhalten und die Verantwortlichkeiten einer Komponente und gibt einen stark typierten Vertrag an, der einen kleinen Satz verwandter Vorgänge bietet. Die gesamte Kommunikation zwischen COM-Komponenten erfolgt über Schnittstellen, und alle dienste, die von einer Komponente angeboten werden, werden über ihre Schnittstelle verfügbar gemacht. Ein Aufrufer kann nur auf die Schnittstellen-Memberfunktionen zugreifen. Der interne Zustand ist für einen Aufrufer nicht verfügbar, es sei denn, er wird in der Schnittstelle verfügbar gemacht.

Schnittstellen sind stark typiert. Jede Schnittstelle verfügt über einen eigenen eindeutigen Schnittstellenbezeichner, der als IID bezeichnet wird, wodurch Kollisionen beseitigt werden, die mit für Menschen lesbaren Namen auftreten können. Die IID ist ein global eindeutiger Bezeichner (Globally Unique Identifier, GUID), der mit der UUID (Universally Unique ID) identisch ist, die von der Distributed Computing Environment (DCE) von Open Software Foundation (OSF) definiert wird. Wenn Sie eine neue Schnittstelle erstellen, müssen Sie einen neuen Bezeichner für diese Schnittstelle erstellen. Wenn ein Aufrufer eine Schnittstelle verwendet, muss er den eindeutigen Bezeichner verwenden. Diese explizite Identifizierung verbessert die Stabilität, indem Benennungskonflikte beseitigt werden, die zu Laufzeitfehlern führen würden.

Wenn Sie eine neue Schnittstelle definieren, können Sie eine Schnittstellendefinition mithilfe der Interface Definition Language (IDL) erstellen. Aus dieser Schnittstellendefinition generiert der Microsoft IDL-Compiler Headerdateien zur Verwendung durch Anwendungen mithilfe der -Schnittstelle und Quellcode zur Handhabung von Remoteprozeduraufrufen. Die von Microsoft bereitgestellte IDL basiert auf einfachen Erweiterungen von DCE IDL, einem Branchenstandard für RPC-basiertes verteiltes Computing. IDL ist ein Tool zur Vereinfachung des Schnittstellen-Designers und nicht von zentraler Bedeutung für die COM-Interoperabilität. Mit IDL müssen Sie headerdateien nicht manuell für jede Programmierumgebung erstellen. Weitere Informationen finden Sie unter [Definieren von COM-Schnittstellen.](defining-com-interfaces.md)

Vererbung wird in COM-Schnittstellen nur wenig verwendet. COM unterstützt schnittstellenvererbung nur, um einen Vertrag wiederzuverwenden, der einer Basisschnittstelle zugeordnet ist. COM unterstützt keine selektive Vererbung. Wenn also eine Schnittstelle von einer anderen erbt, enthält sie alle Funktionen, die die Basisschnittstelle definiert. Darüber hinaus verwenden Schnittstellen nur eine einzelne Vererbung anstelle von mehrfacher Vererbung, um Funktionen von einer Basisschnittstelle zu erhalten.

## <a name="interface-implementation"></a>Schnittstellenimplementierung

Sie können eine Instanz einer COM-Schnittstelle nicht selbst erstellen. Stattdessen erstellen Sie eine Instanz einer Klasse, die die -Schnittstelle implementiert. In C++ wird eine COM-Schnittstelle als abstrakte Basisklasse modelliert, was bedeutet, dass die Schnittstelle eine C++-Klasse ist, die nur reine virtuelle Memberfunktionen enthält. Eine C++-Bibliothek implementiert COM-Objekte, indem sie die Memberfunktionssignaturen von einer oder mehrere Schnittstellen erbt, jede Memberfunktion überschreiben und eine Implementierung für jede Funktion bereitstellen.

Sie können eine beliebige Programmiersprache verwenden, die das Konzept von Funktionszelern unterstützt, um eine COM-Schnittstelle zu implementieren. In C ist eine Schnittstelle beispielsweise eine -Struktur, die einen Zeiger auf eine Tabelle mit Funktionszeigern enthält, einen für jede Methode in der Schnittstelle.

Wenn Sie eine Schnittstelle implementieren, muss Ihre Klasse eine Implementierung für jede Funktion in der Schnittstelle bereitstellen. Wenn die Klasse in einer Schnittstellenfunktion keine Arbeit zu tun hat, kann die Implementierung eine einzelne return-Anweisung sein.

Eine COM-Klasse wird mithilfe einer eindeutigen 128-Bit-Klassen-ID (CLSID) identifiziert, die eine Klasse einer bestimmten Bereitstellung im Dateisystem zu ordnet, bei der es sich bei Windows um eine DLL oder EXE handelt. Eine CLSID ist eine GUID, was bedeutet, dass keine andere Klasse dieselbe CLSID hat. Die Verwendung eindeutiger Klassenbezeichner verhindert Namenskollisionen zwischen Klassen. Beispielsweise können zwei verschiedene Anbieter eine Klasse mit dem Namen CStack schreiben, aber beide Klassen verfügen über eine eindeutige CLSID, sodass jede Möglichkeit eines Zusammenstoßes vermieden wird.

Sie rufen eine neue CLSID ab, indem Sie die [**CoCreateGuid-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) oder ein COM-Erstellungstool wie Visual Studio verwenden, das diese Funktion intern aufruft.

## <a name="the-iunknown-interface"></a>Die IUnknown-Schnittstelle

Alle COM-Schnittstellen erben von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Die **IUnknown-Schnittstelle** enthält die grundlegenden COM-Vorgänge für Polymorphie und Die Verwaltung der Instanzlebensdauer. Die **IUnknown-Schnittstelle** verfügt über drei Memberfunktionen namens [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Alle COM-Objekte sind erforderlich, um die **IUnknown-Schnittstelle zu** implementieren.

Die [**QueryInterface-Memberfunktion**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) stellt Polymorphie für COM zur Verfügung. Rufen **Sie QueryInterface auf,** um zur Laufzeit zu bestimmen, ob ein COM-Objekt eine bestimmte Schnittstelle unterstützt. Das COM-Objekt gibt einen Schnittstellenzeiger im -Parameter zurück, wenn es die angeforderte Schnittstelle `ppvObject` implementiert, andernfalls `NULL` wird zurückgegeben. Die **QueryInterface-Memberfunktion** ermöglicht die Navigation zwischen allen Schnittstellen, die ein COM-Objekt unterstützt.

Die Lebensdauer einer COM-Objektinstanz wird durch die *Verweisanzahl gesteuert.* Die [**IUnknown-Memberfunktionen**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) steuern die Anzahl. **AddRef** erhöht die Anzahl, **und Release** dekrementiert die Anzahl. Wenn die Verweisanzahl 0 (null) erreicht, kann die **Release-Memberfunktion** die Instanz frei geben, da sie von keinen Aufrufern verwendet wird.

## <a name="the-clientserver-model"></a>Das Client-/Servermodell

Eine COM-Klasse implementiert eine Reihe von COM-Schnittstellen. Die Implementierung besteht aus Binärdateien, die ausgeführt werden, wenn ein Aufrufer mit einer Instanz der COM-Klasse interagiert. COM ermöglicht die Verwendung einer Klasse in verschiedenen Anwendungen, einschließlich Anwendungen, die ohne Kenntnis einer bestimmten Klasse geschrieben wurden. Auf einer Windows-Plattform sind Klassen entweder in einer DLL (Dynamic Linked Library) oder in einer anderen Anwendung (EXE) vorhanden.

Auf dem Hostsystem verwaltet COM eine Registrierungsdatenbank aller CLSIDs für die auf dem System installierten COM-Objekte. Die Registrierungsdatenbank ist eine Zuordnung zwischen jeder CLSID und dem Speicherort der DLL oder EXE, die die entsprechende Klasse enthält. COM fragt diese Datenbank immer dann ab, wenn ein Aufrufer eine Instanz einer COM-Klasse erstellen möchte. Der Aufrufer muss nur die CLSID kennen, um eine neue Instanz der -Klasse an fordern zu können.

Die Interaktion zwischen einem COM-Objekt und seinen Aufrufern wird als Client-/Serverbeziehung modelliert. Der Client ist der Aufrufer, der ein COM-Objekt vom System an fordert, und der Server ist das Modul, das COM-Objekte enthält, die Dienste für Clients bieten.

Ein COM-Client ist ein beliebiger Aufrufer, der eine CLSID an das System übergibt, um eine Instanz eines COM-Objekts an fordern zu können. Die einfachste Möglichkeit zum Erstellen einer Instanz ist das Aufrufen der COM-Funktion [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt eine Instanz der angegebenen CLSID und gibt einen Schnittstellenzeiger des vom Client angeforderten Typs zurück. Der Client ist für die Verwaltung der Lebensdauer der Instanz verantwortlich, indem er seine [**Release-Funktion**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufruft, wenn der Client die Verwendung beendet hat. Um mehrere Objekte basierend auf einer einzelnen CLSID zu erstellen, rufen Sie die [**CoGetClassObject-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) auf. Um eine Verbindung mit einem Objekt herzustellen, das bereits erstellt und ausgeführt wird, rufen Sie die [**GetActiveObject-Funktion**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) auf.

Ein COM-Server stellt eine COM-Implementierung für das System zur Verfügung. Ein Server ordnet einer COM-Klasse eine CLSID zu, enthält die Implementierung der -Klasse, implementiert eine Klassen factory zum Erstellen von Instanzen der -Klasse und stellt das Entladen des Servers zur Verfügung.

> [!Note]  
> Ein COM-Server ist nicht mit dem COM-Objekt identisch, das er dem System zur Verfügung stellt.

 

Um das Erstellen eines COM-Objekts zu aktivieren, muss ein COM-Server eine Implementierung der [**IClassFactory-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) bereitstellen. Clients können die [**CreateInstance-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) aufrufen, um eine neue Instanz eines COM-Objekts an fordern. In der Regel werden solche Anforderungen jedoch in der [**CoCreateInstance-Funktion gekapselt.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Sie können einen COM-Server entweder als freigegebene Bibliothek bereitstellen, die zur Laufzeit in den Prozess des Clients geladen wird (DLL auf Windows-Plattformen) oder als ausführbares Modul (EXE auf Windows-Plattformen). Weitere Informationen finden Sie unter [Registrieren von COM-Anwendungen.](registering-com-applications.md)

## <a name="service-control-manager"></a>Dienststeuerungs-Manager

Der Dienststeuerungs-Manager (Service Control Manager, SCM) verarbeitet die Clientanforderung für eine Instanz eines COM-Objekts. Die folgende Liste zeigt die Abfolge der Ereignisse:

-   Ein Client fordert einen Schnittstellenzeiger auf ein COM-Objekt aus der COM-Bibliothek an, indem er eine Funktion wie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der CLSID des COM-Objekts aufruft.
-   Die COM-Bibliothek fragt den SCM ab, um den Server zu finden, der der angeforderten CLSID entspricht.
-   Der SCM sucht den Server und fordert die Erstellung des COM-Objekts von der Klassen factory an, die vom Server bereitgestellt wird.
-   Bei Erfolg gibt die COM-Bibliothek einen Schnittstellenzeiger auf den Client zurück.

Nachdem das COM-System ein Serverobjekt mit einem Client verbindet, kommunizieren Client und Objekt direkt. Der Aufruf über eine zwischengeschaltete Laufzeit verursacht keinen zusätzlichen Mehraufwand.

Wenn Sie einen COM-Server beim Hostsystem registrieren, können Sie verschiedene Möglichkeiten für die Aktivierung des Servers angeben. Die folgende Liste zeigt die drei Möglichkeiten, wie der SCM einen COM-Server aktivieren kann:

-   In-Process: Der SCM gibt den Dateipfad der DLL zurück, die die Objektserverimplementierung enthält. Die COM-Bibliothek lädt die DLL und fragt sie nach ihrem Klassen factory-Schnittstellenzeiger ab.
-   Lokal: Der SCM startet die lokale ausführbare Datei, die eine Klassen factory beim Start registriert, und der Schnittstellenzeiger ist für das System und die Clients verfügbar.
-   Remote: Der lokale SCM erhält einen Klassen-Factoryschnittstellenzeiger vom SCM, der auf einem Remotecomputer ausgeführt wird.

Wenn ein Client ein COM-Objekt an fordert, kontaktiert die COM-Bibliothek den SCM auf dem lokalen Host. Der SCM sucht den entsprechenden COM-Server, der lokal oder remote sein kann, und der Server gibt einen Schnittstellenzeiger auf die Klassen factory des Servers zurück. Wenn die Klassen factory verfügbar ist, kann die COM-Bibliothek oder der Client die Klassen factory verwenden, um das angeforderte Objekt zu erstellen. Weitere Informationen finden Sie unter [Implementieren von IClassFactory.](implementing-iclassfactory.md)

## <a name="reusability"></a>Wiederverwendbarkeit

COM unterstützt *die Blackbox-Wiederverwendbarkeit,* was bedeutet, dass die Implementierungsdetails einer wiederverwendbaren Komponente nicht für Clients verfügbar gemacht werden. Com unterstützt zwei Mechanismen, mit denen ein Objekt ein anderes wiederverwenden kann, um die Wiederverwendbarkeit der Blackbox zu erreichen. Die beiden Formen der Wiederverwendung werden als *Containment und* Aggregation *bezeichnet.* Standardmäßig wird das objekt, das wiederverwendet wird, als inneres Objekt bezeichnet, und das Objekt, das das innere Objekt verwendet, wird als *äußeres Objekt bezeichnet.*

In der Hülle verhält sich das äußere Objekt wie ein Client des inneren Objekts. Das äußere Objekt ist ein logischer Container für das innere Objekt, und wenn das äußere Objekt die Dienste des inneren Objekts verwendet, delegiert das äußere Objekt die Implementierung an die Schnittstellen des inneren Objekts. Dies bedeutet, dass das äußere Objekt in Bezug auf die Dienste des inneren Objekts implementiert wird. Das äußere Objekt unterstützt möglicherweise nicht die gleichen Schnittstellen wie das innere Objekt, und das äußere Objekt kann die -Schnittstelle eines inneren Objekts verwenden, um Teile einer anderen Schnittstelle im äußeren Objekt zu implementieren.

Bei der Aggregation macht das äußere Objekt Schnittstellen aus dem inneren Objekt verfügbar, als ob sie auf dem äußeren Objekt implementiert würden. Dies ist nützlich, wenn das äußere Objekt jeden Aufruf für eine seiner Schnittstellen immer an dieselbe Schnittstelle des inneren Objekts delegieren würde. Aggregation ist eine Praktische, die es dem äußeren Objekt ermöglicht, zusätzlichen Implementierungsaufwand zu vermeiden.

Weitere Informationen finden Sie unter [Wiederverwendung von Objekten.](reusing-objects.md)

## <a name="storage-and-stream-objects"></a>Storage und Streamen von Objekten

COM-Objekte speichern den Zustand in einer Datei mithilfe von strukturiertem *Speicher.* Dabei handelt es sich um eine Form von beständiger Speicherung, die die Navigation des Inhalts einer Datei mithilfe der Dateisystemsemantik ermöglicht. Wenn Sie den Inhalt einer Datei auf diese Weise behandeln, werden Features wie inkrementeller Zugriff, Transaktionen und die Freigabe zwischen Prozessen ermöglicht.

Die COM-Spezifikation für persistenten Speicher bietet zwei Arten von Speicherelementen: Speicherobjekte und Streamobjekte. Diese Objekte werden von der COM-Bibliothek implementiert, und Benutzeranwendungen implementieren diese Speicherelemente nur selten. Storage implementieren die [**IStorage-Schnittstelle,**](/windows/desktop/api/objidl/nn-objidl-istorage) und Streamobjekte implementieren [**die IStream-Schnittstelle.**](/windows/desktop/api/objidl/nn-objidl-istream)

Ein Streamobjekt enthält Daten und ähnelt konzeptionell einer einzelnen Datei in einem Dateisystem. Jeder Stream verfügt über Zugriffsrechte und einen einzelnen Suchzeiger. Über die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) können Sie die zugrunde liegenden Daten des Streams lesen, schreiben, suchen und andere Vorgänge ausführen. Ein Stream wird mithilfe einer Textzeichenfolge benannt. Sie kann eine beliebige interne Struktur enthalten, da es sich um einen flachen Bytedatenstrom handelt. Darüber hinaus ähneln die Funktionen in der **IStream-Schnittstelle** standardmäßigen auf Dateihandbüchern basierenden Funktionen, z. B. funktionen in der ANSI C-Laufzeitbibliothek.

Ein Speicherobjekt ähnelt konzeptionell einem Verzeichnis in einem Dateisystem. Jeder Speicher kann eine beliebige Anzahl von Untergeordneten Speicherobjekten und eine beliebige Anzahl von Streams enthalten. Jeder Speicher verfügt über eigene Zugriffsrechte. Über die [**IStorage-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istorage) können Sie Vorgänge wie aufzählen, verschieben, kopieren, umbenennen, erstellen und löschen. Ein Speicherobjekt speichert keine anwendungsdefinierten Daten, sondern implizit die Namen der Elemente (Speicher und Streams), die es enthält.

Storage- und Streamobjekte sind zwischen Prozessen sharable, wenn sie gemäß der COM-Spezifikation auf einer Hostplattform implementiert werden. Dadurch erhalten Objekte, die prozess- oder out-of-process ausgeführt werden, den gleichen inkrementellen Zugriff auf ihren Dateispeicher. Da COM separat in jeden Prozess geladen wird, werden vom Betriebssystem unterstützte Shared Memory-Mechanismen verwendet, um den Zustand geöffneter Elemente und deren Zugriffsmodi zwischen Prozessen zu kommunizieren.

Jedes Speicher- und Streamobjekt in einer strukturierten Datei hat einen Namen, um es zu identifizieren. Der Name ist eine Zeichenfolge, die einer bestimmten Konvention folgt. Weitere Informationen finden Sie unter [Storage-Namenskonventionen](/windows/desktop/Stg/storage-object-naming-conventions)für Objekte. Der Name wird an [**IStorage-Funktionen übergeben,**](/windows/desktop/api/objidl/nn-objidl-istorage) um anzugeben, welches Element im Speicher verwendet werden soll. Die Namen von Stammspeicherobjekten sind mit den Dateinamen im zugrunde liegenden Dateisystem identisch, und diese Namen müssen den Konventionen und Einschränkungen des Dateisystems entsprechen. Zeichenfolgen, die an speicherbezogene Funktionen übergeben werden, die Namendateien ohne Interpretation oder Änderungen an das Dateisystem übergeben werden.

Namen von Elementen, die in Speicherobjekten enthalten sind, werden von der Implementierung des jeweiligen Speicherobjekts verwaltet. Alle Implementierungen von Speicherobjekten müssen Elementnamen unterstützen, die 32 Zeichen lang sind, und einige Implementierungen unterstützen möglicherweise längere Namen. Namen werden mit beibehaltener Groß-/Kleinschreibung gespeichert, aber sie werden als ohne Unterscheidung nach Groß-/Kleinschreibung verglichen. Anwendungen, die Speicherelementnamen definieren, müssen Namen auswählen, die in beiden Situation funktionieren.

Sie greifen auf jedes Element in einer strukturierten Speicherdatei mithilfe von Funktionen und Schnittstellen zu, die von COM implementiert werden. Dies bedeutet, dass andere Anwendungen die Datei durchsuchen können, indem sie mit den [**IStorage-Schnittstellenfunktionen**](/windows/desktop/api/objidl/nn-objidl-istorage) navigieren, die verzeichnisbasierte Dienste bereitstellen. Außerdem können andere Anwendungen die Daten der Datei verwenden, ohne die Anwendung ausführen zu müssen, die die Datei geschrieben hat. Wenn eine COM-Anwendung auf die strukturierten Speicherdateien einer anderen Anwendung zutritt, gelten Windows Standardzugriffsrechte, und die Anwendung muss über ausreichende Berechtigungen verfügen.

Ein COM-Objekt kann sich selbst lesen und in beständigen Speicher schreiben. Ein Client fragt abhängig vom Kontext des Vorgangs eine der persistenzbezogenen Schnittstellen für das COM-Objekt ab. COM-Objekte können eine beliebige Kombination der folgenden Schnittstellen implementieren:

-   [**IPersistStorage:**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)Das COM-Objekt liest und schreibt seinen persistenten Zustand in ein Speicherobjekt. Der Client stellt dem Objekt über diese Schnittstelle einen [**IStorage-Zeiger**](/windows/desktop/api/objidl/nn-objidl-istorage) bereit. Dies ist die einzige Persistenzschnittstelle, die Semantik für den inkrementellen Zugriff enthält.
-   [**IPersistStream:**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)Das COM-Objekt liest und schreibt seinen persistenten Zustand in ein Streamobjekt. Der Client stellt über diese Schnittstelle [**einen IStream-Zeiger**](/windows/desktop/api/objidl/nn-objidl-istream) für das Objekt bereit.
-   [**IPersistFile:**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)Das COM-Objekt liest und schreibt seinen persistenten Zustand direkt in eine Datei im zugrunde liegenden System. Diese Schnittstelle umfasst [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) nur, wenn über diese Schnittstellen auf die zugrunde liegende Datei zugegriffen wird, aber die **IPersistFile-Schnittstelle** verfügt über keine Semantik für Speicher und Streams. Der Client stellt dem Objekt einen Dateinamen zur Verfügung und ruft die [**Funktionen Speichern**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) oder [**Laden**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) auf.

## <a name="data-transfer"></a>Datenübertragung

Strukturierter Speicher stellt die Grundlage für den Datenaustausch zwischen COM-Objekten und -Prozessen dar, der als *einheitliche Datenübertragung bezeichnet wird.* Bevor COM in OLE 2 implementiert wurde, wurde die Datenübertragung auf Windows durch Übertragungsprotokolle wie die Zwischenablage und drag-drop-Protokolle angegeben. Jedes Übertragungsprotokoll hatte einen eigenen Satz von Funktionen, die das Protokoll an die Abfrage gebunden haben, und es war spezifischer Code erforderlich, um die einzelnen Protokolle und Austauschprozeduren zu verarbeiten. Die einheitliche Datenübertragung stellt alle Datenübertragungen mithilfe der [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) dar, die allgemeine Datenaustauschvorgänge vom Übertragungsprotokoll trennt.

Die [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) kapselt die standardmäßigen Get- und Set-Vorgänge für Daten, Abfragen und Enumerationen sowie Benachrichtigungen, die erkennen, wenn sich Daten in einem Objekt ändern. Die einheitliche Datenübertragung ermöglicht umfassende Beschreibungen von Datenformaten sowie die Verwendung verschiedener Speichermedien für die Datenübertragung.

Während der einheitlichen Datenübertragung tauschen alle Protokolle einen Zeiger auf eine [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) aus. Der Server ist die Quelle der Daten und implementiert ein Datenobjekt, das in jedem Datenaustauschprotokoll verwendet werden kann. Der Client nutzt die Daten und fordert Daten von einem Datenobjekt an, wenn er einen **IDataObject-Zeiger** von einem beliebigen Protokoll empfängt. Nachdem der Zeigeraustausch stattgefunden hat, verarbeiten beide Seiten den Datenaustausch einheitlich über die **IDataObject-Schnittstelle.**

COM definiert zwei Datenstrukturen, die eine einheitliche Datenübertragung ermöglichen. Die [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) stellt ein generalisiertes Zwischenablageformat dar, und die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) stellt das Übertragungsmedium als Speicherhandle dar.

Der Client erstellt eine [**FORMATETC-Struktur,**](/windows/win32/api/objidl/ns-objidl-formatetc) um den Datentyp anzugeben, den er von einer Datenquelle anfordert, und wird von der Datenquelle verwendet, um zu beschreiben, welche Formate er bereitstellt. Der Client fragt eine Datenquelle nach den verfügbaren Formaten ab, indem er die [**IEnumFORMATETC-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) anfordert. Weitere Informationen finden Sie unter [The FORMATETC Structure](the-formatetc-structure.md).

Der Client erstellt eine [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) und übergibt sie an die [**GetData-Methode,**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) und das Datenobjekt gibt die Daten in der bereitgestellten **STGMEDIUM-Struktur** zurück.

Die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) ermöglicht clients und datenquellen die Auswahl des effizientesten Austauschmediums. Wenn die auszutauschenden Daten beispielsweise sehr groß sind, kann die Datenquelle anstelle des Hauptspeichers ein datenträgerbasiertes Medium als bevorzugtes Format angeben. Diese Flexibilität ermöglicht einen effizienten Datenaustausch, der so schnell sein kann wie die Übergabe eines Zeigers an einen [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) oder einen [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Weitere Informationen finden Sie unter [Die STGMEDIUM-Struktur.](the-stgmedium-structure.md)

Ein Client einer Datenquelle erfordert möglicherweise eine Benachrichtigung, wenn sich die Daten ändern. COM verarbeitet Datenänderungsbenachrichtigungen mithilfe eines *Advise-Senkenobjekts,* das die [**IAdviseSink-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) implementiert. Das Advise-Senkenobjekt und die **IAdviseSink-Schnittstelle** werden vom Client implementiert, der einen **IAdviseSink-Zeiger** an die Datenquelle übergibt. Wenn die Datenquelle eine Änderung der zugrunde liegenden Daten erkennt, ruft sie eine **IAdviseSink-Methode** auf, um den Client zu benachrichtigen. Weitere Informationen finden Sie unter [Datenbenachrichtigung.](data-notification.md)

## <a name="remoting"></a>Remoting

COM ermöglicht remote und verteilte Berechnungen. *Schnittstellenremoting* ermöglicht es einer Memberfunktion, einen Schnittstellenzeiger auf ein COM-Objekt zurückzugeben, das sich in einem anderen Prozess oder auf einem anderen Hostcomputer befindet. Die Infrastruktur, die das Schnittstellenremoting ausführt, ist sowohl für den Client als auch für den Objektserver transparent. Weder der Client noch der Server benötigen die Bereitstellungsdetails des jeweils anderen, um über eine Remoteschnittstelle zu kommunizieren. Ein Client ruft Memberfunktionen auf derselben Schnittstelle auf, um mit einem COM-Objekt zu kommunizieren, das prozessintern, prozessintern auf dem lokalen Host oder auf einem Remotecomputer ausgeführt wird. Lokale und Remoteaufrufe auf derselben Schnittstelle können für den Client nicht unterschieden werden.

Um mit einem COM-Objekt zu kommunizieren, ruft ein Client immer eine Prozessimplementierung auf. Wenn das COM-Objekt in Bearbeitung ist, ist der Aufruf direkt. Wenn sich das COM-Objekt außerhalb des Prozesses oder remote befindet, stellt COM eine *Proxyimplementierung* bereit, die den Aufruf des Objekts mithilfe des RPC-Protokolls (Remote Procedure Call) weiterleitet.

Ein COM-Objekt empfängt immer Aufrufe von einem Client über eine In-Process-Implementierung. Wenn der Aufrufer in Bearbeitung ist, ist der Aufruf direkt. Wenn sich der Aufrufer außerhalb des Prozesses oder remote befindet, stellt COM eine *Stubimplementierung* bereit, die den Remoteprozeduraufruf vom Proxy im Clientprozess empfängt.

*Marshalling* ist das Verfahren zum Packen der Aufrufliste für die Übertragung vom Proxy an den Stub. *Unmarshaling* ist das Entpacken, das am empfangenden Ende auftritt. Rückgabewerte werden gemarshallt und vom Stub an den Proxy nicht gemarshallt. Diese Art der Kommunikation wird auch als Senden eines Anrufs *über das Kabel* bezeichnet.

Jeder andere Datentyp verfügt über Regeln für das Marshalling. Schnittstellenzeiger verfügen auch über ein Marshallingprotokoll, das in der [**CoMarshalInterface-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) gekapselt ist. In den meisten Fällen ist das *Standardmäßige Schnittstellen-Marshalling,* das vom System bereitgestellt wird, ausreichend, aber ein COM-Objekt kann optional *benutzerdefiniertes Schnittstellen-Marshalling* implementieren, um die Erstellung von Remoteobjektproxys für sich selbst zu steuern. Weitere Informationen finden Sie unter [Kommunikation zwischen Objekten.](inter-object-communication.md)

## <a name="security"></a>Sicherheit

COM bietet zwei Formen der Anwendungssicherheit. Eine davon ist *die Aktivierungssicherheit,* die angibt, wie neue Objekte erstellt werden, wie Clients eine Verbindung mit neuen und vorhandenen Objekten herstellen und wie bestimmte öffentliche Dienste wie die Klassentabelle und die Tabelle für ausgeführte Objekte geschützt werden. Die andere ist *die Aufrufsicherheit,* die angibt, wie die Sicherheit in einer hergestellten Verbindung zwischen einem Client und einem COM-Objekt funktioniert.

Die Aktivierungssicherheit wird automatisch vom Dienststeuerungs-Manager (Service Control Manager, SCM) angewendet. Wenn der SCM eine Anforderung zum Abrufen eines COM-Objekts empfängt, überprüft er die Anforderung anhand von Sicherheitsinformationen, die in der Registrierung gespeichert sind.

SCM-Implementierungen bieten in der Regel eine registrierungsgesteuerte Konfiguration für die Verwaltung bereitgestellter Klassen und für bestimmte Benutzerkonten auf dem Host. Weitere Informationen finden Sie unter [Aktivierungssicherheit.](activation-security.md)

Die Aufrufsicherheit wird automatisch angewendet oder von der Anwendung erzwungen. Wenn die Anwendung Setupinformationen bereitstellt, führt COM die erforderlichen Überprüfungen aus, um die Anwendung zu schützen.

Der automatische Mechanismus überprüft die Sicherheit für den Prozess, jedoch nicht für einzelne Objekte oder Methoden. Wenn eine Anwendung eine differenziertere Sicherheit erfordert, stellt COM Funktionen bereit, die Von Anwendungen verwendet werden können, um ihre eigene Sicherheitsüberprüfung durchführen zu können.

Die automatischen und benutzerdefinierten Mechanismen können zusammen verwendet werden, sodass eine Anwendung COM auffordern kann, eine automatische Sicherheitsüberprüfung durchzuführen und dann eine eigene durchzuführen.

COM-Aufrufsicherheitsdienste sind in die folgenden Kategorien unterteilt:

-   Allgemeine Funktionen, die sowohl von Clients als auch von Servern aufgerufen werden, mit denen der automatische Sicherheitsmechanismus initialisiert und automatische Authentifizierungsdienste registriert werden können. Die allgemeinen Aufrufsicherheits-APIs sind die Funktionen [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) und [**CoQueryAuthenticationServices.**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
-   Schnittstellen für Clientproxys, die es dem Client ermöglichen, die Sicherheit bei Aufrufen einzelner Schnittstellen zu steuern. Die [**IClientSecurity-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) und die Funktionen [**CoQueryProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)und [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) bieten Aufrufsicherheit für ein Remoteobjekt.
-   Serverseitige Funktionen und Aufrufkontextschnittstellen, die es dem Server ermöglichen, Sicherheitsinformationen zu einem Aufruf abzurufen und die Identität des Aufrufers zu annehmen. Die [**IServerSecurity-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) und die Funktionen [**CoGetCallContext,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)und [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) bieten serverseitige Aufrufsicherheit.

Häufig fragt der Client das COM-Objekt für die [**IClientSecurity-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) ab, die lokal von der Remotingschicht implementiert wird. Der Client verwendet diese Schnittstelle, um die Sicherheit einzelner Schnittstellenproxys für das COM-Objekt zu steuern, bevor er einen Aufruf für eine der Schnittstellen vornimmt.

Wenn ein Aufruf beim Server eintrifft, kann der Server die [**CoGetCallContext-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) aufrufen, um eine [**IServerSecurity-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) abzurufen, die es dem Server ermöglicht, die Authentifizierung des Clients zu überprüfen und bei Bedarf die Identität des Clients zu annehmen. Das **IServerSecurity-Objekt** ist für die Dauer des Aufrufs gültig.

Rufen Sie die [**CoInitializeSecurity-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) auf, um die Sicherheitsschicht zu initialisieren und die angegebenen Werte als Sicherheitsstandards festzulegen. Wenn ein Prozess **CoInitializeSecurity** nicht aufruft, ruft COM es automatisch auf, wenn eine Schnittstelle zum ersten Mal gemarshallt oder nicht gemarshallt wird, wodurch die Standardsicherheit des Systems registriert wird. Mit der **CoInitializeSecurity-Funktion** kann der Client die Standardaufrufsicherheit für den Prozess einrichten, wodurch die Verwendung von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) für einzelne Proxys vermieden wird. Mit **der CoInitializeSecurity-Funktion** kann ein Server automatische Authentifizierungsdienste für den Prozess registrieren. Weitere Informationen finden Sie unter [Setting Process-Wide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> <dt>

[Definieren von COM-Schnittstellen](defining-com-interfaces.md)
</dt> <dt>

[Registrieren von COM-Anwendungen](registering-com-applications.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> </dl>

 

 
