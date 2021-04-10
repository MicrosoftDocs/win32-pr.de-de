---
title: Technische Übersicht über com
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 'Weitere Informationen: Technische Übersicht über com'
keywords:
- Com Technical Overview com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5dc95ffae5166d86cd8110cab1a6b90e6ffa5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126607"
---
# <a name="com-technical-overview"></a>Technische Übersicht über com

Dieses Thema enthält eine Übersicht über die Microsoft Component Object Model (com):

-   [Einführung in COM](#introduction-to-com)
-   [Objekte und Schnittstellen](#objects-and-interfaces)
-   [Schnittstellen Implementierung](#interface-implementation)
-   [Die IUnknown-Schnittstelle](#the-iunknown-interface)
-   [Das Client/Server-Modell](#the-clientserver-model)
-   [Dienststeuerungs-Manager](#service-control-manager)
-   [Wiederverwendbarkeit](#reusability)
-   [Speicher-und Streamobjekte](#storage-and-stream-objects)
-   [Datenübertragung](#data-transfer)
-   [Remoting](#remoting)
-   [Security](#security)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-com"></a>Einführung in COM

Der Microsoft Component Object Model (com) definiert einen binären Interoperabilitäts Standard zum Erstellen von wiederverwendbaren Software Bibliotheken, die zur Laufzeit interagieren. Sie können com-Bibliotheken verwenden, ohne dass diese in Ihre Anwendung kompiliert werden müssen. COM ist die Grundlage für eine Reihe von Microsoft-Produkten und-Technologien, wie z. b. Windows Media Player und Windows Server.

COM definiert einen binären Standard, der für viele Betriebssysteme und Hardwareplattformen gilt. Für das Netzwerk Computing definiert com ein Standard-Wire-Format und-Protokoll für die Interaktion zwischen Objekten, die auf unterschiedlichen Hardwareplattformen ausgeführt werden. Com ist von der Implementierungssprache unabhängig, was bedeutet, dass Sie com-Bibliotheken mithilfe verschiedener Programmiersprachen erstellen können, wie z. b. C++ und denen in der .NET Framework.

Die com-Spezifikation bietet alle grundlegenden Konzepte, die die plattformübergreifende Wiederverwendung von Software ermöglichen:

-   Ein binärer Standard für Funktionsaufrufe zwischen Komponenten.
-   Eine Bereitstellung für stark typisierte Gruppierungen von Funktionen in Schnittstellen.
-   Eine Basisschnittstelle, die Polymorphie, die Funktions Ermittlung und die Überwachung der Objekt Lebensdauer bereitstellt.
-   Ein Mechanismus, mit dem Komponenten und ihre Schnittstellen eindeutig identifiziert werden.
-   Ein Komponenten Lade Modul, das Komponenten Instanzen aus einer Bereitstellung erstellt.

COM hat eine Reihe von Teilen, die zusammenarbeiten, um die Erstellung von Anwendungen zu ermöglichen, die aus wiederverwendbaren Komponenten erstellt werden:

-   Ein *Host System* , das eine Laufzeitumgebung bereitstellt, die der com-Spezifikation entspricht.
-   *Schnittstellen* , die Funktions Verträge definieren, sowie *Komponenten* , die Schnittstellen implementieren.
-   *Server* , die Komponenten für das System bereitstellen, und *Clients* , von denen die von-Komponenten bereitgestellten Funktionen verwendet werden.
-   Eine *Registrierung* , die nachverfolgt, wo-Komponenten auf lokalen und Remote Hosts bereitgestellt werden.
-   Ein *Dienststeuerungs-Manager* , der-Komponenten auf lokalen und Remote Hosts findet und Server mit Clients verbindet.
-   Ein *strukturiertes Speicher* Protokoll, das definiert, wie der Inhalt von Dateien im Dateisystem des Hosts navigiert werden soll.

Das Aktivieren der erneuten Verwendung von Code über Hosts und Plattformen hinweg ist für com von zentraler Bedeutung. Eine wiederverwendbare Schnittstellen Implementierung wird als *Komponente*, als *Komponenten Objekt* oder als *com-Objekt* bezeichnet. Eine Komponente implementiert mindestens eine COM-Schnittstelle.

Sie definieren eine benutzerdefinierte COM-Bibliothek durch Entwerfen der Schnittstellen, die von der Bibliothek implementiert werden. Consumer Ihrer Bibliothek können Ihre Features entdecken und verwenden, ohne dass Sie wissen über die Bereitstellungs-und Implementierungsdetails Ihrer Bibliothek verfügen.

## <a name="objects-and-interfaces"></a>Objekte und Schnittstellen

Ein COM-Objekt macht seine Funktionen über eine *Schnittstelle* verfügbar, bei der es sich um eine Auflistung von Element Funktionen handelt. Eine COM-Schnittstelle definiert das erwartete Verhalten und die Verantwortlichkeiten einer Komponente und gibt einen stark typisierten Vertrag an, der einen kleinen Satz verwandter Vorgänge bereitstellt. Die gesamte Kommunikation zwischen COM-Komponenten erfolgt über Schnittstellen, und alle von einer Komponente angebotenen Dienste werden über die Schnittstelle verfügbar gemacht. Ein Aufrufer kann nur auf die Schnittstellenmember-Funktionen zugreifen. Der interne Status ist für einen Aufrufer nur verfügbar, wenn er in der Schnittstelle verfügbar gemacht wird.

Schnittstellen sind stark typisiert. Jede Schnittstelle verfügt über einen eigenen eindeutigen Schnittstellen Bezeichner, der als IID bezeichnet wird, wodurch Konflikte vermieden werden, die mit lesbaren Namen auftreten können. Die IID ist eine Globally Unique Identifier (GUID), die mit der universellen eindeutigen ID (UUID) identisch ist, die von der DCE (Open Software Foundation) definiert wird. Wenn Sie eine neue Schnittstelle erstellen, müssen Sie einen neuen Bezeichner für diese Schnittstelle erstellen. Wenn ein Aufrufer eine Schnittstelle verwendet, muss er den eindeutigen Bezeichner verwenden. Diese explizite Identifizierung verbessert die Stabilität, indem Benennungs Konflikte vermieden werden, die zu Laufzeitfehlern führen.

Wenn Sie eine neue Schnittstelle definieren, können Sie eine Schnittstellen Definition mithilfe der Schnittstellen Definitions Sprache (IDL) erstellen. Aus dieser Schnittstellen Definition generiert der Microsoft IDL-Compiler Header Dateien, die von Anwendungen verwendet werden, die die-Schnittstelle verwenden, und Quellcode, um Remote Prozedur Aufrufe zu verarbeiten. Die von Microsoft bereitgestellte IDL basiert auf einfachen Erweiterungen der DCE-IDL, einem Industriestandard für Remote Prozedur Aufrufe (RPC)-basiertes verteiltes Computing. IDL ist ein Tool zum Zweck der Benutzeroberflächen-Designer und ist nicht für die COM-Interoperabilität von zentraler Bedeutung. Mit IDL müssen Sie keine Header Dateien für jede Programmierumgebung manuell erstellen. Weitere Informationen finden Sie unter [Definieren von COM-Schnittstellen](defining-com-interfaces.md).

Vererbung wird in COM-Schnittstellen sparsam verwendet. COM unterstützt die Schnittstellen Vererbung nur zur Wiederverwendung eines mit einer Basisschnittstelle verknüpften Vertrags. COM unterstützt keine selektive Vererbung. Wenn eine Schnittstelle von einer anderen Klasse erbt, enthält Sie daher alle Funktionen, die von der Basisschnittstelle definiert werden. Außerdem wird Durchschnitt stellen nur eine einzelne Vererbung anstelle mehrerer Vererbung zum Abrufen von Funktionen von einer Basisschnittstelle verwendet.

## <a name="interface-implementation"></a>Schnittstellen Implementierung

Eine Instanz einer COM-Schnittstelle kann nicht allein erstellt werden. Stattdessen erstellen Sie eine Instanz einer Klasse, die die-Schnittstelle implementiert. In C++ wird eine COM-Schnittstelle als *abstrakte Basisklasse* modelliert. Dies bedeutet, dass es sich bei der Schnittstelle um eine C++-Klasse handelt, die nur reine virtuelle Member-Funktionen enthält. Eine C++-Bibliothek implementiert com-Objekte, indem die Member-Funktions Signaturen von einer oder mehreren Schnittstellen geerbt werden, wobei die einzelnen Element Funktionen überschrieben werden und eine Implementierung für jede Funktion bereitgestellt wird.

Sie können jede beliebige Programmiersprache verwenden, die das Konzept der Funktionszeiger unterstützt, um eine COM-Schnittstelle zu implementieren. In C ist eine Schnittstelle z. b. eine Struktur, die einen Zeiger auf eine Tabelle mit Funktions Zeigern enthält, eine für jede Methode in der Schnittstelle.

Wenn Sie eine Schnittstelle implementieren, muss Ihre Klasse eine Implementierung für jede Funktion in der Schnittstelle bereitstellen. Wenn die Klasse in einer Schnittstellenfunktion keine Arbeit hat, kann die Implementierung eine einzelne Return-Anweisung sein.

Eine COM-Klasse wird mit einer eindeutigen 128-Bit-Klassen-ID (CLSID) identifiziert, die einer bestimmten Bereitstellung im Dateisystem eine Klasse zuordnet, bei der es sich für Windows um eine DLL oder exe handelt. Eine CLSID ist eine GUID, was bedeutet, dass keine andere Klasse dieselbe CLSID hat. Die Verwendung eindeutiger Klassen Bezeichner verhindert Namenskollisionen zwischen Klassen. Beispielsweise können zwei verschiedene Lieferanten eine Klasse mit dem Namen cstack schreiben, beide Klassen verfügen jedoch über eine eindeutige CLSID, sodass die Möglichkeit einer Kollision vermieden wird.

Sie erhalten eine neue CLSID mithilfe der [**cokreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) -Funktion oder mit einem com Authoring Tool, wie z. b. Visual Studio, das diese Funktion intern aufruft.

## <a name="the-iunknown-interface"></a>Die IUnknown-Schnittstelle

Alle COM-Schnittstellen erben von der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle. Die **IUnknown** -Schnittstelle enthält die grundlegenden com-Vorgänge für die Verwaltung von Polymorphie und Instanzen Lebensdauer. Die **IUnknown** -Schnittstelle verfügt über drei Element Funktionen mit den Namen [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Alle COM-Objekte sind erforderlich, um die **IUnknown** -Schnittstelle zu implementieren.

Die [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Member-Funktion stellt Polymorphie für com bereit. Ruft **QueryInterface** auf, um zur Laufzeit zu bestimmen, ob ein COM-Objekt eine bestimmte Schnittstelle unterstützt. Das COM-Objekt gibt einen Schnittstellen Zeiger im- `ppvObject` Parameter zurück, wenn die angeforderte Schnittstelle implementiert wird; andernfalls wird zurückgegeben `NULL` . Die **QueryInterface** -Member-Funktion ermöglicht die Navigation zwischen allen Schnittstellen, die ein COM-Objekt unterstützt.

Die Lebensdauer einer com-Objektinstanz wird durch Ihren *Verweis Zähler* gesteuert. Die Anzahl der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Member-Funktionen, die [**Adressierung**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) steuern. **Adressierungen** erhöht die Anzahl, und die **Freigabe** verringert die Anzahl. Wenn der Verweis Zähler Null erreicht, kann die **releasemember** -Funktion die Instanz freigeben, da Sie von keinen Aufrufern verwendet wird.

## <a name="the-clientserver-model"></a>Das Client/Server-Modell

Eine COM-Klasse implementiert eine Reihe von COM-Schnittstellen. Die-Implementierung besteht aus Binärdateien, die ausgeführt werden, wenn ein Aufrufer mit einer Instanz der com-Klasse interagiert. COM ermöglicht die Verwendung einer Klasse in verschiedenen Anwendungen, einschließlich Anwendungen, die ohne Kenntnis einer bestimmten Klasse geschrieben wurden. Auf einer Windows-Plattform sind Klassen entweder in einer Dynamic-Linked Library (dll) oder in einer anderen Anwendung (exe) vorhanden.

Auf dem Host System verwaltet com eine Registrierungsdatenbank aller CLSIDs für die auf dem System installierten COM-Objekte. Die Registrierungsdatenbank ist eine Zuordnung zwischen jeder CLSID und dem Speicherort der DLL oder exe, die die entsprechende Klasse enthält. COM fragt diese Datenbank immer dann ab, wenn ein Aufrufer eine Instanz einer com-Klasse erstellen möchte. Der Aufrufer muss nur die CLSID kennen, um eine neue Instanz der-Klasse anzufordern.

Die Interaktion zwischen einem COM-Objekt und seinen Aufrufern wird als Client/Server-Beziehung modelliert. Der Client ist der Aufrufer, der ein COM-Objekt vom System anfordert, und der Server ist das Modul, das COM-Objekte enthält, die Dienste für Clients bereitstellen.

Ein com-Client ist ein beliebiger Aufrufer, der eine CLSID an das System übergibt, um eine Instanz eines COM-Objekts anzufordern. Die einfachste Möglichkeit zum Erstellen einer Instanz besteht darin, die com-Funktion [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)aufzurufen.

Die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion erstellt eine Instanz der angegebenen CLSID und gibt einen Schnittstellen Zeiger des Typs zurück, der vom Client angefordert wurde. Der Client ist verantwortlich für die Verwaltung der Lebensdauer der-Instanz, indem er seine [**releasefunktion**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufgerufen, wenn der Client die Verwendung nicht mehr benötigt. Wenn Sie mehrere Objekte auf Grundlage einer einzelnen CLSID erstellen möchten, rufen Sie die [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) -Funktion auf. Um eine Verbindung mit einem Objekt herzustellen, das bereits erstellt wurde und ausgeführt wird, müssen Sie die [**GetActiveObject**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) -Funktion aufrufen.

Ein com-Server stellt eine com-Implementierung für das System bereit. Ein Server ordnet eine CLSID einer com-Klasse zu, enthält die Implementierung der-Klasse, implementiert eine Klassenfactory zum Erstellen von Instanzen der-Klasse und ermöglicht das Entladen des Servers.

> [!Note]  
> Ein com-Server ist nicht mit dem COM-Objekt identisch, das es dem System bereitstellt.

 

Um das Erstellen eines COM-Objekts zu aktivieren, muss ein com-Server eine Implementierung der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle bereitstellen. Clients können die Methode " [**feateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) " aufrufen, um eine neue Instanz eines COM-Objekts anzufordern, aber in der Regel sind diese Anforderungen in der [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion gekapselt.

Sie können einen com-Server entweder als freigegebene Bibliothek bereitstellen, die zur Laufzeit in den Client Prozess geladen wird (dll auf Windows-Plattformen), oder als ausführbares Modul (exe auf Windows-Plattformen). Weitere Informationen finden Sie unter [Registrieren von com-Anwendungen](registering-com-applications.md).

## <a name="service-control-manager"></a>Dienststeuerungs-Manager

Der Dienststeuerungs-Manager (Service Control Manager, SCM) verarbeitet die Client Anforderung für eine Instanz eines COM-Objekts. Die folgende Liste zeigt die Abfolge der Ereignisse:

-   Ein Client fordert einen Schnittstellen Zeiger auf ein COM-Objekt von der com-Bibliothek an, indem er eine Funktion wie z. b. [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der CLSID des COM-Objekts aufruft.
-   Die com-Bibliothek fragt den SCM ab, um den Server zu finden, der der angeforderten CLSID entspricht.
-   Der SCM sucht den Server und fordert die Erstellung des COM-Objekts aus der Klassenfactory an, die vom Server bereitgestellt wird.
-   Bei erfolgreicher Ausführung gibt die com-Bibliothek einen Schnittstellen Zeiger an den Client zurück.

Nachdem das com-System eine Verbindung zwischen einem Server Objekt und einem Client hergestellt hat, kommunizieren der Client und das Objekt direkt. Es gibt keinen zusätzlichen mehr Aufwand, der durch den Aufruf von über eine Vermittler Laufzeit verursacht wird.

Wenn Sie einen com-Server beim Host System registrieren, können Sie verschiedene Möglichkeiten angeben, wie der Server aktiviert werden soll. In der folgenden Liste werden die drei Möglichkeiten angezeigt, mit denen der SCM einen com-Server aktivieren kann:

-   In-Process: der SCM gibt den Dateipfad der DLL zurück, die die Implementierung des Objekt Servers enthält. Die com-Bibliothek lädt die dll und fragt Sie nach Ihrem Klassenfactory-Schnittstellen Zeiger ab.
-   Local: der SCM startet die lokale ausführbare Datei, die beim Start eine Klassenfactory registriert, und der Schnittstellen Zeiger ist für das System und die Clients verfügbar.
-   Remote: der lokale SCM erhält einen klassenfactoryschnittstellen Zeiger von dem SCM, der auf einem Remote Computer ausgeführt wird.

Wenn ein Client ein COM-Objekt anfordert, kontaktiert die com-Bibliothek den SCM auf dem lokalen Host. Der SCM findet den entsprechenden com-Server, der lokal oder Remote sein kann, und der Server gibt einen Schnittstellen Zeiger auf die Klassenfactory des Servers zurück. Wenn die Klassenfactory verfügbar ist, kann die com-Bibliothek oder der Client die Klassenfactory verwenden, um das angeforderte Objekt zu erstellen. Weitere Informationen finden Sie unter [Implementieren von IClassFactory](implementing-iclassfactory.md).

## <a name="reusability"></a>Wiederverwendbarkeit

COM unterstützt die *Wiederverwendbarkeit von Blackbox*, was bedeutet, dass die Implementierungsdetails einer wiederverwendbaren Komponente nicht für Clients verfügbar gemacht werden. Um die Wiederverwendbarkeit von Blackbox zu erreichen, unterstützt com zwei Mechanismen, durch die ein Objekt ein anderes wieder verwenden kann. Die zwei Arten der Wiederverwendung werden als *Containment* und *Aggregation* bezeichnet. Gemäß der Konvention wird das Objekt, das wieder verwendet wird, das *innere Objekt* genannt, und das Objekt, das das innere Objekt verwendet, wird als *Äußeres Objekt* bezeichnet.

In Containment verhält sich das äußere Objekt als Client des inneren Objekts. Das äußere Objekt ist ein logischer Container für das innere Objekt, und wenn das äußere Objekt die Dienste des inneren Objekts verwendet, delegiert das äußere Objekt die Implementierung an die Schnittstellen des inneren Objekts. Dies bedeutet, dass das äußere Objekt in Bezug auf die Dienste des inneren Objekts implementiert wird. Das äußere Objekt unterstützt möglicherweise nicht die gleichen Schnittstellen wie das innere Objekt, und das äußere Objekt kann die Schnittstelle eines inneren Objekts verwenden, um die Implementierung von Teilen einer anderen Schnittstelle für das äußere Objekt zu unterstützen.

In Aggregationen macht das äußere Objekt Schnittstellen vom inneren Objekt verfügbar, als wären Sie auf dem äußeren Objekt implementiert. Dies ist hilfreich, wenn das äußere Objekt immer jeden Aufruf an einer seiner Schnittstellen an dieselbe Schnittstelle des inneren Objekts delegiert. Die Aggregation ist eine einfache Möglichkeit, die es dem äußeren Objekt ermöglicht, zusätzlichen Implementierungsaufwand zu vermeiden.

Weitere Informationen finden Sie unter [wieder verwenden von Objekten](reusing-objects.md).

## <a name="storage-and-stream-objects"></a>Speicher-und Streamobjekte

COM-Objekte speichern den Zustand in einer Datei unter Verwendung von *strukturiertem Speicher*, bei dem es sich um eine Form eines permanenten Speichers handelt, der die Navigation zum Inhalt einer Datei mithilfe der Semantik des Dateisystems ermöglicht. Wenn Sie den Inhalt einer Datei auf diese Weise behandeln, werden Funktionen wie inkrementeller Zugriff, Transaktionen und Freigabe zwischen Prozessen ermöglicht.

Die permanente com-Speicher Spezifikation bietet zwei Typen von Speicherelementen: Speicher Objekte und Streamobjekte. Diese Objekte werden von der com-Bibliothek implementiert, und Benutzer Anwendungen implementieren diese Speicherelemente selten. Speicher Objekte implementieren die [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle, und Stream-Objekte implementieren die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle.

Ein Stream-Objekt enthält Daten und ist konzeptionell ähnlich wie eine einzelne Datei in einem Dateisystem. Jeder Stream verfügt über Zugriffsrechte und einen einzelnen Such Zeiger. Über die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle können Sie die zugrunde liegenden Daten des Streams lesen, schreiben, suchen und andere Vorgänge ausführen. Ein Datenstrom wird mit einer Text Zeichenfolge benannt. Sie kann eine beliebige interne Struktur enthalten, da es sich um einen flatstream von Bytes handelt. Außerdem ähneln die Funktionen in der **IStream** -Schnittstelle den Standardfunktionen, die auf Datei Handles basieren, wie z. b. denen in der ANSI C-Lauf Zeit Bibliothek.

Ein Speicher Objekt ähnelt konzeptionell einem Verzeichnis in einem Dateisystem. Jeder Speicher kann eine beliebige Anzahl von unter Speicher Objekten und eine beliebige Anzahl von Streams enthalten. Jeder Speicher verfügt über eigene Zugriffsrechte. Über die [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle können Sie Vorgänge ausführen, z. b. das aufzählen, verschieben, kopieren, umbenennen, erstellen und Löschen von Elementen. Ein Speicher Objekt speichert keine Anwendungs definierten Daten, sondern speichert implizit die Namen der Elemente (Storages und Streams), die darin enthalten sind.

Speicher-und Streamobjekte sind für Prozesse freigegeben, wenn Sie gemäß der com-Spezifikation auf einer Host Plattform implementiert werden. Dies ermöglicht, dass Objekte, die in-Process oder außerhalb des Prozesses ausgeführt werden, gleichen inkrementellen Zugriff auf Ihren Dateispeicher haben. Da com in jeden Prozess separat geladen wird, werden vom Betriebssystem unterstützte Shared Memory-Mechanismen verwendet, um den Zustand der geöffneten Elemente und deren Zugriffs Modi zwischen Prozessen zu übermitteln.

Jedes Speicher-und Streamobjekt in einer strukturierten Datei hat einen Namen, um es zu identifizieren. Der Name ist eine Zeichenfolge, die einer bestimmten Konvention folgt. Weitere Informationen finden Sie unter [Benennungs Konventionen für Speicher Objekte](/windows/desktop/Stg/storage-object-naming-conventions). Der Name wird an [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Funktionen weitergegeben, um anzugeben, auf welchem Element im Speicher gearbeitet werden soll. Namen von Stamm Speicher Objekten sind identisch mit den Dateinamen im zugrunde liegenden Dateisystem, und diese Namen müssen den Konventionen und Einschränkungen des Dateisystems entsprechen. An speicherbezogene Funktionen übergebenen Zeichen folgen, die namens Dateien ohne Interpretation oder Änderungen an das Dateisystem übermittelt werden.

Namen von Elementen, die in Speicher Objekten enthalten sind, werden von der Implementierung des betreffenden bestimmten Speicher Objekts verwaltet. Alle Implementierungen von Speicher Objekten müssen Elementnamen unterstützen, die 32 Zeichen lang sind, und einige Implementierungen unterstützen möglicherweise längere Namen. Namen werden mit der Groß-/Kleinschreibung gespeichert, aber Sie werden mit der Groß-/Kleinschreibung verglichen. Anwendungen, die Speicher Elementnamen definieren, müssen Namen auswählen, die in beiden Situationen funktionieren.

Sie können auf jedes Element in einer strukturierten Speicherdatei zugreifen, indem Sie Funktionen und Schnittstellen verwenden, die von com implementiert werden. Dies bedeutet, dass andere Anwendungen die Datei durchsuchen können, indem Sie mit den [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstellen Funktionen navigieren, die Verzeichnis ähnliche Dienste bereitstellen. Außerdem können andere Anwendungen die Datei Daten verwenden, ohne dass die Anwendung ausgeführt werden muss, die die Datei geschrieben hat. Wenn eine COM-Anwendung auf die strukturierten Speicherdateien einer anderen Anwendung zugreift, gelten standardmäßige Windows-Zugriffsrechte, und die Anwendung muss über ausreichende Berechtigungen verfügen.

Ein COM-Objekt kann sich selbst lesen und in persistenten Speicher schreiben. Ein Client fragt abhängig vom Kontext des Vorgangs eine der persistenzbezogenen Schnittstellen für das COM-Objekt ab. COM-Objekte können eine beliebige Kombination der folgenden Schnittstellen implementieren:

-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage): das COM-Objekt liest seinen permanenten Zustand und schreibt ihn in ein Speicher Objekt. Der Client stellt über diese Schnittstelle einen [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Zeiger für das-Objekt bereit. Dies ist die einzige Dauerhaftigkeits Schnittstelle, die Semantik für inkrementellen Zugriff einschließt.
-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream): das COM-Objekt liest seinen permanenten Zustand und schreibt ihn in ein Datenstrom Objekt. Der Client stellt über diese Schnittstelle einen [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Zeiger für das-Objekt bereit.
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile): das COM-Objekt liest und schreibt seinen permanenten Zustand direkt in eine Datei auf dem zugrunde liegenden System. Diese Schnittstelle bezieht sich nicht auf [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , es sei denn, der Zugriff auf die zugrunde liegende Datei erfolgt über diese Schnittstellen, aber die Schnittstelle **IPersistFile** hat keine Semantik für Speicher und Streams. Der Client stellt dem-Objekt einen Dateinamen bereit und ruft die [**Speicher**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) -oder [**Lade**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) Funktionen auf.

## <a name="data-transfer"></a>Datenübertragung

Die strukturierte Speicherung stellt die Grundlage für den Datenaustausch zwischen COM-Objekten und-Prozessen dar, die als *einheitliche Datenübertragungs Daten* bezeichnet werden. Bevor com in OLE 2 implementiert wurde, wurde die Datenübertragung unter Windows durch *Übertragungsprotokolle*, wie z. b. die Zwischenablage und die Drag-Drop-Protokolle, festgelegt. Jedes Übertragungsprotokoll besaß einen eigenen Funktions Satz, der das Protokoll an die Abfrage gebunden hat, und es war spezifischer Code erforderlich, um die verschiedenen Protokolle und Exchange-Prozeduren verarbeiten zu können. Die einheitliche Datenübertragung stellt alle Datenübertragungen mithilfe der [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle dar, die allgemeine Datenaustausch Vorgänge vom Übertragungsprotokoll trennt.

Die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle kapselt die standardmäßigen Get-und Set-Vorgänge für Daten, Abfragen und Enumerationen sowie Benachrichtigungen, die erkennen, wenn sich Daten in einem Objekt ändern. Die einheitliche Datenübertragung ermöglicht umfassende Beschreibungen von Datenformaten sowie die Verwendung unterschiedlicher Speichermedien für die Datenübertragung.

Während der gleichmäßigen Datenübertragung tauschen alle Protokolle einen Zeiger auf eine [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle aus. Der Server ist die Quelle der Daten und implementiert ein Datenobjekt, das in jedem Datenaustausch Protokoll verwendet werden kann. Der Client verarbeitet die Daten und fordert Daten von einem Datenobjekt an, wenn ein **IDataObject** -Zeiger von einem beliebigen Protokoll empfangen wird. Nachdem der Zeiger Austausch aufgetreten ist, verarbeiten beide Seiten den Datenaustausch auf einheitliche Weise über die **IDataObject** -Schnittstelle.

COM definiert zwei Datenstrukturen, die eine einheitliche Datenübertragung ermöglichen. Die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur stellt ein generalisiertes Zwischenablage Format dar, und die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur stellt das Übertragungsmedium als Speicher Handle dar.

Der Client erstellt eine [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur, um den Datentyp anzugeben, der von einer Datenquelle angefordert wird, und er wird von der Datenquelle verwendet, um zu beschreiben, welche Formate er bereitstellt. Der Client fragt eine Datenquelle nach den verfügbaren Formaten ab, indem er die [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) -Schnittstelle anfordert. Weitere Informationen finden Sie in [der FORMATETC-Struktur](the-formatetc-structure.md).

Der Client erstellt eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur und übergibt sie an die [**GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) -Methode, und das Datenobjekt gibt die Daten in der bereitgestellten **STGMEDIUM** -Struktur zurück.

Mit der [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur können sowohl Clients als auch Datenquellen das effizienteste Exchange-Medium auswählen. Wenn beispielsweise die auszutauschenden Daten sehr groß sind, kann die Datenquelle ein Datenträger basiertes Medium als bevorzugtes Format anstelle des Hauptspeichers angeben. Diese Flexibilität ermöglicht einen effizienten Datenaustausch, der so schnell sein kann wie das Übergeben eines Zeigers an einen [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) oder einen [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Weitere Informationen finden Sie in [der STGMEDIUM-Struktur](the-stgmedium-structure.md).

Ein Client einer Datenquelle erfordert möglicherweise eine Benachrichtigung, wenn sich die Daten ändern. COM verarbeitet Daten Änderungs Benachrichtigungen mithilfe eines *beratungsenke* -Objekts, das die [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) -Schnittstelle implementiert. Das "advisink"-Objekt und die **IAdviseSink** -Schnittstelle werden vom Client implementiert, der einen **IAdviseSink** -Zeiger an die Datenquelle übergibt. Wenn die Datenquelle eine Änderung in den zugrunde liegenden Daten erkennt, ruft Sie eine **IAdviseSink** -Methode auf, um den Client zu benachrichtigen. Weitere Informationen finden Sie unter [Daten Benachrichtigung](data-notification.md).

## <a name="remoting"></a>Remoting

COM ermöglicht eine Remote-und verteilte Berechnung. Mit *Interface Remoting* kann eine Member-Funktion einen Schnittstellen Zeiger auf ein COM-Objekt zurückgeben, das sich in einem anderen Prozess oder auf einem anderen Host Computer befindet. Die Infrastruktur, die das Schnittstellen Remoting ausführt, ist sowohl für den Client als auch den Objekt Server transparent. Weder der Client noch der Server benötigt die Bereitstellungs Details eines anderen, um über eine Remote Schnittstelle zu kommunizieren. Ein Client ruft Member-Funktionen für die gleiche Schnittstelle auf, um mit einem COM-Objekt zu kommunizieren, das in-Process, außerhalb des Prozesses auf dem lokalen Host oder auf einem Remote Computer ist. Lokale und Remote Aufrufe an derselben Schnittstelle sind nicht für den Client unterschieden.

Für die Kommunikation mit einem COM-Objekt ruft ein Client immer eine Prozess interne Implementierung auf. Wenn das COM-Objekt in Bearbeitung ist, wird der-Befehl direkt aufgerufen. Wenn das COM-Objekt out-of-Process oder Remote ist, bietet com eine *Proxy* Implementierung, die den Aufruf an das-Objekt weiterleitet, indem das RPC-Protokoll (Remote Procedure Aufruf) verwendet wird.

Ein COM-Objekt empfängt immer Aufrufe von einem Client über eine Prozess interne Implementierung. Wenn der Aufrufer in Bearbeitung ist, ist der Aufruf Direct. Wenn der Aufrufer außerhalb des Prozesses oder Remote ist, stellt com eine *Stub* -Implementierung bereit, die den Remote Prozedur Aufruf vom Proxy im Client Prozess empfängt.

Das Marshalling *ist das* Verfahren zum Verpacken der-Ereignis Stapel für die Übertragung vom Proxy zum Stub. Das *nicht-Marshalling ist das* entpacken, das am empfangenden Ende erfolgt. Rückgabewerte werden gemarshallt und aus dem Stub in den Proxy gemarshallt. Diese Art der Kommunikation wird auch als Senden eines Anrufe *über das* Netzwerk bezeichnet.

Jeder Datentyp hat Regeln für das Mars Hallen. Schnittstellen Zeiger verfügen auch über ein marshallingprotokoll, das in der [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) -Funktion gekapselt ist. In den meisten Fällen ist das Marshalling von *Standardschnittstellen*, das vom System bereitgestellt wird, ausreichend, aber ein COM-Objekt kann optional *benutzerdefiniertes Schnittstellen* Marshalling implementieren, um die Erstellung von Remote Objektproxys in sich selbst zu steuern. Weitere Informationen finden Sie unter [Kommunikation zwischen Objekten](inter-object-communication.md).

## <a name="security"></a>Sicherheit

COM bietet zwei Formen der Anwendungssicherheit. Eine ist die *Aktivierungs Sicherheit*, die angibt, wie neue Objekte erstellt werden, wie Clients eine Verbindung mit neuen und vorhandenen Objekten herstellen und wie bestimmte öffentliche Dienste, wie z. b. die Klassen Tabelle und die laufende Objekttabelle, gesichert werden. Die andere ist " *callsecurity*", die angibt, wie die Sicherheit in einer eingerichteten Verbindung zwischen einem Client und einem COM-Objekt funktioniert.

Die Aktivierungs Sicherheit wird automatisch vom Dienststeuerungs-Manager (Service Control Manager, SCM) angewendet. Wenn der SCM eine Anforderung zum Abrufen eines COM-Objekts empfängt, wird die Anforderung anhand der in der Registrierung gespeicherten Sicherheitsinformationen überprüft.

SCM-Implementierungen bieten in der Regel Registrierungs gesteuerte Konfiguration für die Verwaltung bereitgestellter Klassen und für bestimmte Benutzerkonten auf dem Host. Weitere Informationen finden Sie unter [Activation Security](activation-security.md).

Die Rückruf Sicherheit wird automatisch angewendet oder von der Anwendung erzwungen. Wenn die Anwendung Setup Informationen bereitstellt, führt com die erforderlichen Überprüfungen aus, um die Anwendung zu schützen.

Der automatische Mechanismus prüft die Sicherheit für den Prozess, jedoch nicht für einzelne Objekte oder Methoden. Wenn eine Anwendung eine präzisere Sicherheit erfordert, bietet com Funktionen, die von Anwendungen verwendet werden können, um eine eigene Sicherheitsüberprüfung durchzuführen.

Die automatischen und benutzerdefinierten Mechanismen können gleichzeitig verwendet werden, sodass eine Anwendung com dazu auffordern kann, eine automatische Sicherheitsüberprüfung durchzuführen und dann eine eigene zu durchführen.

COM-Aufrufe-Sicherheitsdienste sind in die folgenden Kategorien unterteilt:

-   Allgemeine Funktionen, die von Clients und Servern aufgerufen werden, sodass der automatische Sicherheitsmechanismus initialisiert und automatische Authentifizierungsdienste registriert werden können. Die allgemeinen aufrufssicherheits-APIs sind die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -und [**coqueryauthenticationservices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) -Funktionen.
-   Schnittstellen auf Client Proxys, die es dem Client ermöglichen, die Sicherheit bei Aufrufen von einzelnen Schnittstellen zu steuern. Die [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle und die Funktionen " [**coqueryproxyblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket)", " [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)" und " [**cocopyproxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) " bieten die Sicherheit von Aufrufen für ein Remote Objekt.
-   Serverseitige Funktionen und Aufruf Kontext Schnittstellen, die dem Server das Abrufen von Sicherheitsinformationen zu einem Aufruf und das Annehmen der Identität des Aufrufers ermöglichen. Die [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) -Schnittstelle und die Funktionen " [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)", " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" und " [**corevertstoself**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) " bieten serverseitige Aufruf Sicherheit.

Häufig fragt der Client das COM-Objekt für die [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle ab, die lokal von der Remote Schicht implementiert wird. Der Client verwendet diese Schnittstelle, um die Sicherheit einzelner Schnittstellen Proxys auf dem COM-Objekt zu steuern, bevor er eine der Schnittstellen aufruft.

Wenn ein Anruf beim Server eingeht, ruft der Server möglicherweise die [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) -Funktion auf, um eine [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) -Schnittstelle abzurufen, die es dem Server ermöglicht, die Authentifizierung des Clients zu überprüfen und ggf. die Identität des Clients anzunehmen. Das **IServerSecurity** -Objekt ist für die Dauer des Aufrufes gültig.

Ruft die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion auf, um die Sicherheitsebene zu initialisieren und die angegebenen Werte als Sicherheitsstandard festzulegen. Wenn ein Prozess nicht **CoInitializeSecurity** aufruft, ruft com ihn automatisch auf, wenn eine Schnittstelle zum ersten Mal gemarshallt oder gemarshallt wird. dabei wird die System Standard Sicherheit registriert. Die **CoInitializeSecurity** -Funktion ermöglicht es dem Client, eine standardmäßige aufrufssicherheit für den Prozess einzurichten, wodurch die Verwendung von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) in einzelnen Proxys vermieden wird. Die **CoInitializeSecurity** -Funktion ermöglicht es einem Server, automatische Authentifizierungsdienste für den Prozess zu registrieren. Weitere Informationen finden Sie unter [festlegen Process-Wide Sicherheit mit CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> <dt>

[Definieren von COM-Schnittstellen](defining-com-interfaces.md)
</dt> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 
