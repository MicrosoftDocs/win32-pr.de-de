---
title: Implementierungsprobleme bei ADSI-Anbietern
description: Implementierungsprobleme bei ADSI-Anbietern
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- Implementierungsprobleme für ADSI-Anbieter ADSI
- Anbieter ADSI, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c362b04244580e448e7bb7bd78889e66db12fe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391023"
---
# <a name="implementation-issues-for-adsi-providers"></a>Implementierungsprobleme bei ADSI-Anbietern

Implementieren Sie zum Implementieren von ADSI-Schnittstellen zuerst die COM-Schnittstelle [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Wenn Sie diese Schnittstelle als minimale Verwaltungsebene bereitstellen, stellen Sie Client Anwendungen das Steuerelement bereit, das für den Zugriff auf Verzeichnisobjekte direkt aus dem Verzeichnis und nicht über den ADSI-Cache benötigt wird. Dadurch wird die Netzwerkleistung optimiert. Durch die Verwendung dieser Schnittstelle wird auch Ihre eigene Implementierung mit der höchsten Flexibilität bereitgestellt.

Implementieren Sie zweitens die grundlegenden ADSI-Schnittstellen, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)und die [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)-, [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)-, [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Eigenschaften Cache Schnittstellen. [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) und [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) sind auch Schnittstellen, die häufig von der System Verwaltungssoftware abhängig sind.

Implementieren Sie Drittens die Schema Verwaltungs Schnittstellen, wenn Ihr Verzeichnisdienst über ein zugrunde liegendes Schema verfügt: [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax). Wenn kein zugrunde liegendes Schema vorhanden ist, verwenden Sie diese Schnittstellen, um die vom Verzeichnisdienst verwendeten Klassen und Eigenschaften zu abstrahieren. Schemas können zum Veröffentlichen der Features Ihres Verzeichnis Dienstanbieter auf ADSI-Clients verwendet werden.

## <a name="collections"></a>Sammlungen

ADSI-Anbieter Komponenten können einem von drei Modellen zum Zwischenspeichern von Auflistungen während der Enumeration folgen. Die Auswahl eines cachingmodells bestimmt das Verhalten von ADSI, wenn ein Objekt in einer Sammlung aus dem zugrunde liegenden Verzeichnisdienst außerhalb von ADSI gelöscht wird.

Die cachingmodelle umfassen Folgendes:

-   Im Voraus zwischengespeicherte Sammlungen. Die Auflistung von Objektinstanzen wird vollständig aus dem zugrunde liegenden Verzeichnisdienst abgerufen, wenn [**iadscollection:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) aufgerufen wird, um ein neues Enumeratorobjekt zu erstellen. Wenn das Quell Objekt für eine Active Directory Objektinstanz in der abgerufenen Sammlung aus dem zugrunde liegenden Verzeichnisdienst gelöscht wird, erkennt der Client den Löschvorgang erst, wenn ein [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) oder [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) auf die Auflistung zugreift.
-   Sammlungen werden inkrementell zwischengespeichert Die Auflistung wird von dem zugrunde liegenden Verzeichnisdienst ein Objekt zu einem Zeitpunkt abgerufen, wenn [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) aufgerufen wird. [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) kehrt zum Anfang der Auflistung im Cache zurück, und **IEnumVARIANT:: Next** gibt zwischengespeicherte Objekte zurück, bis das Ende des Caches erreicht ist. zu diesem Zeitpunkt werden neue Objekte aus dem zugrunde liegenden Speicher hinzugefügt. Wenn sich eine Active Directory Objektinstanz im Cache befindet, erkennt der Client den Löschvorgang vom zugrunde liegenden Verzeichnisdienst erst, wenn ein [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -oder [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Versuch versucht, auf das Objekt zuzugreifen.
-   Sammlungen werden nicht zwischengespeichert. Die Auflistung wird von dem zugrunde liegenden Verzeichnisdienst ein Objekt zu einem Zeitpunkt abgerufen, wenn [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) aufgerufen wird. [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) kehrt zum Anfang der Auflistung im zugrunde liegenden Speicher zurück. **IEnumVARIANT:: Next** -und **IEnumVARIANT:: Reset** -Vorgänge können keine gelöschten Objekte abrufen, da die Objekte Bedarfs gesteuert vom zugrunde liegenden Verzeichnisdienst abgerufen werden. Nur das aktuelle Objekt wird zwischengespeichert. Wenn das aktuelle-Objekt gelöscht wird, erkennt der Client seinen Löschvorgang nicht mehr vom zugrunde liegenden Verzeichnisdienst, bis ein [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -oder [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Versuch versucht, auf das Objekt zuzugreifen.

Ungeachtet des cachingmodells sollten Sie beachten, dass die ADSI-Enumeration Active Directory Dienst Schnittstellen an den Aufrufer zurückgibt. Um den mehr Aufwand für das Abrufen eines neuen Schnittstellen Zeigers zu vermeiden, sollten ADSI-Anwendungen die zurückgegebenen Schnittstellen Zeiger für Objekte zwischenspeichern, die Sie bearbeiten möchten. Beispielsweise kann eine Visual Basic Anwendung, die einen Container auflistet und ein Listenfeld mit Namen auffüllt, die Schnittstellen Zeiger Zwischenspeichern, die den Namen für die spätere Verwendung zugeordnet sind. Diese Vorgehensweise bietet eine höhere Leistung als das Auffüllen des Listen Felds während der Enumeration und das Abrufen eines neuen Schnittstellen Zeigers, wenn der Benutzer eine Auswahl trifft.

## <a name="about-dispatch-ids"></a>Informationen zu dispatchids

[**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) ist eine von com definierte Automatisierungsschnittstelle für Controller, die keine COM-Schnittstellen direkt verwenden. Der Zugriff auf ein Objekt über **IDispatch** wird namens gebunden oder spät gebundener Zugriff, da es zur Laufzeit ("spät") auftritt und Zeichen folgen Namen von Eigenschaften und Methoden verwendet, um Verweise aufzulösen ("Name"). Zur Laufzeit übergeben Clients den Zeichen folgen Namen der Eigenschaft oder Methode, die Sie aufrufen möchten, an die Methode [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)(). Wenn die Eigenschaft oder Methode für das Objekt vorhanden ist, wird der Dispatchbezeichner (DISPID) der entsprechenden Funktion abgerufen. Die DISPID wird dann verwendet, um die Funktion über [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)() auszuführen. Mithilfe von **IDispatch** werden Eigenschaften und Methoden für die Schnittstellen, die von einem einzelnen-Objekt verfügbar gemacht werden, als flache Liste angezeigt. Da der namens gebundene Zugriff zwei Funktionsaufrufe erfordert, ist er weniger effizient als die direkte Verwendung einer COM-Schnittstelle. Clients wird empfohlen, die ADSI-COM-Schnittstellen für die Objekte zu verwenden, wenn die Leistung berücksichtigt wird. Erweiterte Automatisierungs Controller, wie z. b. Visual Basic 4,0, können andere COM-Schnittstellen sowie **IDispatch** aufrufen, wenn die Schnittstellen den Automatisierungs Einschränkungen für Datentypen und Parameter Übergabe entsprechen.

ADSI-Anbieter generieren für jedes Active Directory Objekt dynamisch DispIds. Die DispIds, die über [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) für ein bestimmtes Objekt abgerufen werden, sind die generierten Werte, jedoch nicht die Werte, die in der IDL für das Objekt enthalten sind. [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) -Benutzer müssen **GetIDsOfNames** aufrufen, um zur Laufzeit gültige DispIds zu erhalten.

## <a name="type-information-and-type-libraries"></a>Typinformationen und Typbibliotheken

Das ADSI SDK stellt eine Typbibliothek, activeds. tlb, bereit, die alle von ADSI unterstützten Standardschnittstellen dokumentiert. Ein Anbieter muss eine ähnliche Typbibliothek für alle in activeds. tlb gefundenen Schnittstellen sowie alle zusätzlichen Typdaten für die Schnittstellen bereitstellen, die in der Anbieter Komponente implementiert werden.

Im folgenden finden Sie ein Beispiel für einen IDL-Code.

``` syntax
[ object, uuid(IID_IADsXYZ), oleautomation, dual ]
interface IADsXYZ: IDispatch
{
// Read-only properties.
[propget]
HRESULT AReadOnlyProp ([out, retval]BSTR *pbstrAReadOnlyProp);
 
// Read/write properties.
[propget]
HRESULT AReadWriteProp ([out, retval]long *plAReadWriteProp);
[propput]
HRESULT AReadWriteProp ([in]long lAReadWriteProp);
 
// Methods.
HRESULT AMethod ([in]DATE dateInParameter,
[out, retval]BSTR *pbstrReturnValue);
};
```

## <a name="thread-safety"></a>Threadsicherheit

In der Component Object Model (com) werden die folgenden drei Threading Modelle beschrieben. COM-Anwendungen geben an, welches Modell beim Initialisieren der com-Bibliothek verwendet wird, indem die [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) -und [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktionen verwendet werden:

-   Single Threading. Das Single Thread-Modell geht davon aus, dass ein einzelner Ausführungs Thread in einem Prozess ausgeführt wird. dabei wird davon ausgegangen, dass com-Datenstrukturen in einem Prozess keine Zugriffsserialisierung
-   Apartment Threading. Ein COM-Objekt ist dem Thread zugeordnet, der ihn erstellt hat. Aufrufe eines Objekts in einem anderen Thread müssen von dem Thread ausgeführt werden, der das Objekt erstellt hat. Um dies zu erreichen, ruft der Quell Thread einen Client Proxy auf, der den Methodenaufruf anordnet und ihn über die Win32-Nachrichten Warteschlange, die dem Zielthread zugeordnet ist, an eine Serverstub-Funktion im Zielthread übergibt.
-   Kostenloses Threading. Es wird davon ausgegangen, dass COM-Objekte Thread sicher sind. Mehreren Threads wird der Zugriff auf jedes Objekt im Prozess gestattet, ohne dass eine Serialisierung erzwungen wird.

ADSI nimmt kein bestimmtes Threading Modell an. Writer von Anbieter Komponenten sollten das kostenlose Threading Modell annehmen und die Konsistenz Ihrer internen Datenstrukturen gewährleisten, indem Sie Sie vor Thread unsicheren, d. h. nicht koordinierten Updates durch die Verwendung von Synchronisierungs Objekten, wie z. b. kritischen Abschnitten oder Semaphore, schützen.

## <a name="object-locking"></a>Objekt Sperrung

ADSI erzwingt oder definiert kein Objekt Sperr Schema. Anbieter für Namespaces, die die Zugriffsserialisierung mithilfe von Sperren unterstützen, können das zugrunde liegende Sperr Schema über anbieterspezifische Erweiterungen von ADSI verfügbar machen.

## <a name="property-names-within-a-schema"></a>Eigenschaftsnamen innerhalb eines Schemas

ADSI stellt Eigenschaften als Eigenschafts Objekte innerhalb des ADSI-Schema Containers dar. Dies erfordert, dass Eigenschaftsnamen innerhalb der einzelnen Schema Container eindeutig sind. Der Anbieter muss sicherstellen, dass keine Namenskollisionen vorhanden sind.

## <a name="primary-interface"></a>Primäre Schnittstelle

Wenn ein Anbieter nicht ermitteln kann, welche Schnittstelle als primäre Schnittstelle zurückgegeben werden soll, sollten **IID- \_ IADs** zurückgegeben werden. Dies ermöglicht den namens gebundenen Zugriff auf alle Eigenschaften eines Objekts über [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) und die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get)-, [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex)-, [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put)-und [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methoden.

 

 