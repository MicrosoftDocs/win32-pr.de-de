---
description: Es ist wichtig, dass Sie die erforderliche DLL-Struktur eines Filter Handlers verstehen (eine Implementierung der IFilter-Schnittstelle).
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: Implementieren von Filter Handlern in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5f326440b31b62ff5697274962f4d4a2cfe7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346078"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>Implementieren von Filter Handlern in Windows Search

Es ist wichtig, dass Sie die erforderliche DLL-Struktur eines Filter Handlers verstehen (eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle).

Dieses Thema ist wie folgt organisiert:

- [Implementieren und Exportieren der DLL-Einstiegspunkte](#implementing-and-exporting-the-dll-entry-points)
- [Implementieren der IFilter-Klasse und der Klassenfactory](#implementing-the-ifilter-class-and-class-factory)
- [Vererbung der COM-Schnittstellen](#inheriting-the-com-interfaces)
- [Implementieren der Methoden der COM-Schnittstelle](#implementing-the-com-interface-methods)
  - [Nicht implementierte com-Methoden](#com-methods-that-are-not-implemented)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>Implementieren und Exportieren der DLL-Einstiegspunkte

Jede [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll (durch Ifilter.dll in diesem Abschnitt bezeichnet) muss die folgenden Einstiegspunkte implementieren und exportieren. Diese Einstiegspunkte werden in der Regel mit einer Modul Definitionsdatei (. def) für die **IFilter** -Schnittstelle oder mit dem **\_ \_ declspec (dllexport)** -Schlüsselwort exportiert. Die DLL-Datei kann in einem beliebigen Ordner registriert werden, befindet sich jedoch in der Regel im Ordner "% SystemRoot% \\ system32".

DLL-Einstiegspunkte werden in der folgenden Tabelle aufgelistet und beschrieben.

| DLL-Name                                                                                     | DLL-beschreibung                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | Der [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Einstiegspunkt registriert die dll als Filter in der Registrierung. Sie registrieren die dll, indem Sie das regsvr32.exe Programm mit dem Dateinamen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle als Argument ausführen: `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [DllUnregisterServer-Funktion](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | Der Einstiegspunkt der [DllUnregisterServer-Funktion](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entfernt die dll als permanenten Handler in der Registrierung. Sie heben die Registrierung der dll auf, indem Sie das regsvr32.exe Programm mit dem folgenden `/u` Flag ausführen: `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [DllGetClassObject-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | Der Inhalts Indizierungs Client ruft den Einstiegspunkt der [DllGetClassObject-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) über Component Object Model (com) auf, um ein klassenfactoryobjekt für die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle zu erstellen und einen Zeiger auf die Klassenfactoryschnittstelle dieses Objekts zu erhalten.                                               |
| [DllCanUnloadNow-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | Der Content-Indizierungs Client ruft den [DllCanUnloadNow-Funktions](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) Einstiegspunkt über com auf, um zu bestimmen, ob es möglich ist, die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  -dll zu entladen. Die **IFilter** -Schnittstelle wird entladen, wenn Sie für ein Zeitintervall nicht verwendet wird, wie im Registrierungs Wert filteridletimeout angegeben. |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>Implementieren der IFilter-Klasse und der Klassenfactory

Mindestens zwei Klassen, z. b. cfilter und cfiltercf, werden in der Regel von jeder [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll implementiert. Die cfilter-Klasse erzeugt das IFilter-Schnittstellen Objekt, das die Inhalts **Filterungs** Funktion implementiert. Seine Member-Funktionen implementieren die Schnittstellen Methoden der **IFilter** -Schnittstelle. Jede **IFilter** -Klasse benötigt eine eindeutige Klassen-ID (CLSID), die der Implementierer der **IFilter** -Schnittstelle generiert.

Die cfiltercf-Klasse erzeugt das klassenfactoryobjekt für die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle. Die Klassenfactory wird durch die Schnittstelle der [IClassFactory-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) durch den Einstiegspunkt der [DllGetClassObject-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) der dll aufgerufen. Die cfiltercf-Klasse erstellt das cfilter-Objekt und gibt einen Zeiger auf [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)zurück. In komplexeren Fällen kann ein **IFilter** eine Klassenhierarchie anstelle der einzelnen cfilter-Klasse implementieren.

## <a name="inheriting-the-com-interfaces"></a>Vererbung der COM-Schnittstellen

Windows Search 3,0 und höher erfordert die Verwendung von [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) aus den folgenden Gründen:

- Um Leistung und zukünftige Kompatibilität zu gewährleisten.
- , Um die Sicherheit zu erhöhen. Mit [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) implementierte IFilters sind sicherer, da der Kontext, in dem die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle ausgeführt wird, nicht die Berechtigung zum Öffnen von Dateien auf dem Datenträger oder über das Netzwerk benötigt.
- Obwohl bei Windows Search nur [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)verwendet wird, kann die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Interface-Klasse auch die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) und/oder [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) Interface-Implementierungen aus Gründen der Abwärtskompatibilität erben.

Diese Schnittstellen werden in Dateien deklariert, die aus dem MSSDK \\ include-Verzeichnis eingeschlossen werden und über vordefinierte Schnittstellen Bezeichner (IIDs) verfügen. Der Inhalts Indizierungs Client fragt die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle über [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) ab, um zu bestimmen, welche dieser Schnittstellen beim Filtern von Inhalten verwendet werden sollen.

## <a name="implementing-the-com-interface-methods"></a>Implementieren der Methoden der COM-Schnittstelle

Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle implementiert die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methoden für die **IFilter** -Schnittstellen Klasse und die **IFilter** -schnittstellenklassenfactory. In der folgenden Tabelle werden die Schnittstellen spezifischen Schnittstellen und Methoden der **IFilter** -Schnittstelle aufgelistet, die von der **IFilter** -Schnittstelle implementiert werden sollten. Die **IFilter** -Schnittstelle muss mindestens [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)implementieren, kann jedoch zusätzliche Schnittstellen, die von ipersistent abgeleitet werden, implementieren.

| COM-Schnittstelle                                                                             | Methode                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IClassFactory-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | "Kreatabstance", "LockServer"                                                                                                                                                                                                                                                     |
| [IClassFactory2-Schnittstelle](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | GetLicInfo, RequestLicKey, kreateingestancelic                                                                                                                                                                                                                                   |
| [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init), [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext), [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue), [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [Ipersistent-Schnittstelle](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty, Load, Save, saveabgeschlossene, getcurrfile                                                                                                                                                                                                                                 |
| [IPersistStorage-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty, Load, Save, GetSizeMax                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty, Load, Save, GetSizeMax                                                                                                                                                                                                                                                |

Die Referenzseite für jede Methode gibt die Parameter und das funktionale Verhalten für diese Methode an. Jede Verweisseite gibt auch die Ergebnis Codes an, die für diese Methode implementiert werden. Die Verweis Seiten für die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Methoden geben die schnittstellenspezifischen [Codes in den \_ in der Einrichtung](../com/codes-in-facility-itf.md) -Ergebnis Codes-Ergebnis Codes implementierten Codes an, und der Inhalts Indizierungs Client kann auch jeden der allgemeinen Ergebnis Codes verarbeiten, wie z. b. die Funktion \_ null und die Win32-Anlage \_ . Weitere Informationen finden Sie unter [Struktur von com-Fehler Codes](../com/structure-of-com-error-codes.md).

### <a name="com-methods-that-are-not-implemented"></a>Nicht implementierte com-Methoden

Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle muss mindestens [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)implementieren, aber es müssen keine weiteren von ipersistent abgeleiteten Schnittstellen implementiert werden.

Die in der folgenden Tabelle aufgeführten com-Methoden müssen von Windows Search nicht implementiert werden.

| Nicht erforderliche Methode                               | BESCHREIBUNG                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream:: IsDirty                                   | Filter sollten E \_ notimpl zurückgeben. |
| IPersistStream:: Save                                      | Filter sollten E \_ notimpl zurückgeben. |
| IPersistStream:: GetSizeMax                                | Filter sollten E \_ notimpl zurückgeben. |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Filter sollten E \_ notimpl zurückgeben. |

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

[Grundlegendes zu Filter Handlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)

[Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)

[Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)

[Testen von Filter Handlern](-search-ifilter-testing-filters.md)
