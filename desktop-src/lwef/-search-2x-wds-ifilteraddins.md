---
title: Entwickeln von IFilter-Add-ins
description: Sie können Microsoft Windows Desktop Search (WDS) mit Filter-Add-Ins, Komponenten, die ifilterinterface implementieren, erweitern, um neue Dateitypen einzubeziehen.
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f846cf2101eefc17b1e92fbd7992529a06fb43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473028"
---
# <a name="developing-ifilter-add-ins"></a>Entwickeln von IFilter-Add-ins

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Sie können Microsoft Windows Desktop Search (WDS) mit Filter-Add-Ins, Komponenten, die die [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle implementieren, erweitern, um neue Dateitypen einzubeziehen. Filter sind für den Zugriff und die Datenverarbeitung in Dateien und für das Zurückgeben von Paaren von Eigenschaften und Werten sowie von Textabschnitten für die Indizierung verantwortlich. Während des Indizierungs Vorgangs ruft WDS den entsprechenden Filter mit der URL für jede Datei oder jedes Element auf. Der Filter extrahiert zuerst Metadaten, die Eigenschaften entsprechen, die im WDS-Schema als abrufbar gekennzeichnet sind, z. b. Titel, Dateigröße und Datum der letzten Änderung. Anschließend wird der Element Inhalt in Textblöcke aufgeteilt. WDS fügt dem Katalog die Eigenschaften und den Text hinzu, die vom Filter zurückgegeben werden. WDS kann jeden Dateityp indizieren, für den er einen registrierten Filter hat.

In einigen Fällen müssen Sie keinen neuen Filter schreiben. WDS 2. x enthält Filter für mehr als 200 Typen von Elementen (einschließlich Klartext-Elemente wie HTML-, XML-und Quell Code Dateien) und verwendet dieselbe [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Technologie wie SharePoint Services. Wenn Sie bereits Filter für die Dateitypen installiert haben, kann WDS diese vorhandenen Filter verwenden, um diese Daten zu indizieren. Außerdem enthält WDS einen allgemeinen Filter für Dateitypen, die nur-Text-basiert sind. Wenn Sie über einen Dateityp verfügen, der entweder von einem vorhandenen SharePoint Services-Filter oder dem Klartext-Filter verarbeitet werden kann, können Sie die Dateinamenerweiterung und die Filter-GUID der Registrierung hinzufügen, sodass Sie von WDS gefunden und verwendet werden kann. (Weitere Informationen finden Sie [unter Registrieren eines Filter-Add-ins](#to-register-a-filter-add-in) .)

Wenn Sie jedoch ein nicht-Klartext-und ein proprietäres Daten-oder Dateiformat haben, ist das Schreiben einer benutzerdefinierten Filter Implementierung der einzige Weg, um sicherzustellen, dass WDS das Dateiformat im Katalog indizieren kann. Sie können nur ein Filter-Add-in für einen Dateityp haben, sodass es möglich ist, einen vorhandenen Filter zu überschreiben oder einen anderen Filter für einen bestimmten Dateityp zu überschreiben.

Dieser Abschnitt enthält die folgenden Themen:

-   [Erforderliche Filter Schnittstellen](#required-filter-interfaces)
    -   [IFilter-Schnittstelle](#ifilter-interface)
    -   [IPersistStream](#ipersiststream)
    -   [IPersistFile](#ipersistfile)
    -   [IPersistStorage](#ipersiststorage)
-   [Ausgabe von Eigenschaften mit Filtern](#outputting-properties-with-filters)
    -   [Eigenschaftswerte](#property-values)
-   [Installation des Add-ins Filtern](#filter-add-in-installation)
    -   [Für die Registrierung erforderliche CLSIDs](#clsids-required-for-registration)
    -   [Registrierungs Modell](#registration-model)
    -   [So registrieren Sie ein Filter-Add-in](#to-register-a-filter-add-in)
-   [Zugehörige Themen](#related-topics)

## <a name="required-filter-interfaces"></a>Erforderliche Filter Schnittstellen

Ein Filter-Add-in muss die [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle und eine der folgenden Schnittstellen implementieren:

-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -zum Laden von Daten aus einem Stream. Dies ist sicherer als die Verwendung von Dateien, da nichts auf den Datenträger geschrieben wird. Die IPersistStream-Schnittstelle ist die bevorzugte Methode für die Vorwärtskompatibilität mit Windows Vista.
-   [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) : zum Laden von Daten aus einer Datei. Diese Schnittstelle wird in Windows Vista nicht unterstützt.
-   [IPersistStorage-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersiststorage) : zum Laden von Daten aus einem strukturierten OLE-com-Speicher.

Ein Filter-Add-in verwendet diese Schnittstellen, um den Inhalt des Elements zu erhalten und Sie iterativ an den Index zurückzugeben, bis das Ende der Datei erreicht ist. Ein Filter-Add-in sollte so robust wie möglich sein, damit beschädigte Dateien verarbeitet werden können, die nicht den erwarteten Eingabe Formaten entsprechen.

### <a name="ifilter-interface"></a>IFilter-Schnittstelle

Dies ist eine erforderliche Schnittstelle für eine Filter Implementierung. Weitere Informationen finden Sie in der Referenz zur [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle.



| Methode       | BESCHREIBUNG                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init ()       | Initialisiert eine Filter Sitzung.                                                       |
| GetChunk ()   | Positioniert den Filter am Anfang des ersten oder nächsten Blocks und gibt einen Deskriptor zurück. |
| Gettext ()    | Ruft Text aus dem aktuellen Segment ab.                                                 |
| GetValue()   | Ruft Eigenschaftswerte aus dem aktuellen Segment ab.                                      |
| BindRegion () | Derzeit für die interne Verwendung reserviert. nicht implementieren. Diese Methode gibt "E \_ notimpl" zurück. |



 

### <a name="ipersiststream"></a>IPersistStream

Diese Schnittstelle lädt eine Datei aus einem Stream für eine sicherere Verarbeitung als die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) , da der Kontext, in dem ein [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Filter ausgeführt wird, nicht die Berechtigung zum Öffnen von Dateien auf dem Datenträger oder über das Netzwerk benötigt. Von den beiden Methoden für den Zugriff auf eine einzelne Datei wird dies als bevorzugte Methode für die Vorwärtskompatibilität mit Windows empfohlen.



| Methode       | BESCHREIBUNG                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty ()    | Prüft, ob eine Änderung vorliegt. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                                                      |
| InitNew ()    | Erstellt einen neuen Speicher. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                                                                  |
| Load ()       | Initialisiert ein Objekt aus dem Stream, in dem es zuvor gespeichert wurde.                                                                               |
| Speichern ()       | Speichert ein Objekt in den angegebenen Stream und gibt an, ob das Objekt das geänderte Flag zurücksetzen soll. Diese Methode gibt "E \_ notimpl" in Filtern zurück. |
| GetSizeMax () | Gibt die Größe des Streams in Bytes zurück, der für das Speichern des Objekts benötigt wird. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                      |



 

### <a name="ipersistfile"></a>IPersistFile

Diese Schnittstelle lädt eine Datei nach dem absoluten Pfad und wird in Windows Vista nicht unterstützt.



| Methode          | BESCHREIBUNG                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| Getcurrfile ()    | Ruft den aktuellen Namen der Datei ab, die dem-Objekt zugeordnet ist. Gibt den in Load () angegebenen Pfad zurück.                          |
| Load ()          | Öffnet die angegebene Datei, und initialisiert ein Objekt aus dem Dateiinhalt. Sie können das Öffnen der Datei verzögern, bis Sie Sie benötigen. |
| GetClassID ()    | Gibt den Klassen Bezeichner (CLSID) für den neuen Dateityp zurück. Verwenden Sie uuidgen.exe, um eine eindeutige CLSID zu generieren.           |
| IsDirty ()       | "E \_ notimpl" muss nur in Filtern zurückgegeben werden.                                                                                       |
| Speichern ()          | "E \_ notimpl" muss nur in Filtern zurückgegeben werden.                                                                                       |
| Saveabgeschlossen () | "E \_ notimpl" muss nur in Filtern zurückgegeben werden.                                                                                       |



 

### <a name="ipersiststorage"></a>IPersistStorage

Diese Schnittstelle unterstützt das strukturierte Speichermodell, in dem jedes enthaltene Objekt über einen eigenen Speicher verfügt, der im Speicher des Containers geschachtelt ist. Ebenso wie die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile)wird diese Schnittstelle nach dem absoluten Pfad geladen und wird in Windows Vista nicht unterstützt.



| Methode            | BESCHREIBUNG                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty ()         | Prüft, ob eine Änderung vorliegt. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                 |
| InitNew ()         | Erstellt einen neuen Speicher. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                             |
| Load ()            | Speichert den Speicher. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                                 |
| Speichern ()            | Gibt die Größe des Streams in Bytes zurück, der für das Speichern des Objekts benötigt wird. Diese Methode gibt "E \_ notimpl" in Filtern zurück. |
| Saveabgeschlossen ()   | Für die interne Verwendung reserviert. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                         |
| HandsOffStorage () | Für die interne Verwendung reserviert. Diese Methode gibt "E \_ notimpl" in Filtern zurück.                                         |



 

## <a name="outputting-properties-with-filters"></a>Ausgabe von Eigenschaften mit Filtern

Der Zweck eines Filters besteht darin, den Inhalt und die Eigenschaften von Dateien zu extrahieren, die in den Volltextindex eingeschlossen werden sollen. WDS ruft zuerst die Load-Methode für die Implementierungen IPersistFile, IPersistStream oder IPersistStorage auf und ruft dann die Init-Methode der IFilter-Implementierung auf. **GetChunk** wird aufgerufen, um Segmente von Text-oder Eigenschafts Wert Daten abzurufen, und dann wird entweder **gettext** oder **GetValue** so oft wie nötig aufgerufen, um alle dem Block zugeordneten Text-oder Eigenschaftswerte abzurufen. Dieser Prozess wird wiederholt, bis **GetChunk** meldet, dass im Dokument keine weiteren Segmente vorhanden sind.

Die **GetChunk** -Methode ruft Informationen zum ersten oder nächsten logischen Informationsblock aus der zu filternden Datei ab und gibt diese Informationen in einer stat-Blockstruktur zurück. \_ einschließlich einer monoton zunehmenden Block-ID, Statusinformationen darüber, wie sich der aktuelle Block auf den vorherigen Block bezieht, ein Flag, das angibt, ob der Block Text oder einen Wert, das Gebiets Schema des Segments und die Eigenschafts Spezifikation des Segments enthält. Die Eigenschafts Spezifikation ist eine [**fullpropspec**](/windows/desktop/api/filter/ns-filter-fullpropspec) , die aus einer CLSID und einem ganzzahligen Eigenschafts Bezeichner (z. b. D5CDD505-2E9C-101B-9397-08002B2CF9AE/wahrnehmvedtype) besteht. Sie identifiziert den Typ der Eigenschaft und nicht den Eigenschafts Wert selbst.

Der Gebiets Schema Bezeichner "Block" wird verwendet, um eine entsprechende Wörter Trennung auszuwählen, und es ist sehr wichtig, dass Sie ihn ordnungsgemäß identifizieren. Wenn der Filter das Gebiets Schema des Texts nicht ermitteln kann, sollte er das standardmäßige System Gebiets Schema annehmen, das mit **GetSystemDefaultLCID** verfügbar ist. Wenn Sie das Dateiformat Steuern und es derzeit keine Gebiets Schema Informationen enthält, sollten Sie eine Benutzerfunktion hinzufügen, um die ordnungsgemäße Gebiets Schema Identifizierung zu aktivieren. Wenn eine nicht übereinstimmende Wörter Trennung verwendet wird, kann dies zu einer ungültigen Abfrageleistung für den Benutzer führen.

**GetChunk** verwaltet nur den Zugriff auf Blöcke und gibt weder den Text noch den Eigenschafts Wert selbst zurück. Stattdessen rufen nachfolgende Aufrufe von **gettext** und **GetValue** den Text des Segments ab. **Gettext** gibt Textblöcke zurück, bei denen es sich um Unicode-Zeichen folgen aus dem aktuellen \_ Block Textabschnitt handelt. Wenn der aktuelle Block zu groß ist, können mehrere Aufrufe der **gettext** -Methode erforderlich sein. Jeder Aufrufen der **gettext** -Methode ruft Text ab, der direkt auf den Text des letzten Aufrufens der **gettext** -Methode folgt. Beispielsweise kann das letzte Zeichen eines Aufrufes in der Mitte eines Worts sein, und das erste Zeichen im nächsten-Befehl würde dieses Wort fortsetzen. Diese Situation muss von Suchmaschinen behandelt werden.

**GetValue** gibt Eigenschaftswerte für den aktuellen Block \_ Wert Block in PROPVARIANT-Strukturen zurück, die eine Vielzahl von Datentypen enthalten können. " **GetValue** " muss die PROPVARIANT-Struktur selbst mithilfe von "CoTaskMemAlloc" zuordnen. Der Aufrufer von **GetValue** ist verantwortlich für das Freigeben von Speicher, auf den von der PROPVARIANT mithilfe von propvariantclear verwiesen wird, und zum Freigeben der Struktur selbst mit CoTaskMemFree. Weitere Informationen zu propvarianten finden Sie in der Referenz zu [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

### <a name="property-values"></a>Eigenschaftswerte

Filter sollten mindestens die folgenden Eigenschaften ausgeben, bei denen es sich um die Standard Spalten in der WDS-Ergebnis Ansicht handelt.



| GUID                                 | PROPSPEC      | Anzeigename  | BESCHREIBUNG                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | Primarytitle   | Der Titel, der für dieses Element angezeigt wird.                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | Primaryauthors | Person, die diesem Element am meisten zugeordnet ist.                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | Primarydate   | Primarydate    | Das wichtigste Datum für ein Element, z. b. für e-Mail empfangene oder für Dateien geänderte Datumsangaben.                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | Wahrnehmungstyp | Wahrnehmungstyp  | Der Typ der Datei, die analysiert wird. Muss einem der Typen von Windows-Desktop Suchtypen entsprechen, die unter von WDS [erkannte](-search-2x-wds-perceivedtype.md)Typen aufgeführt sind. |



 

Für nur-Text-Elemente extrahiert WDS alle Text-und System definierten Eigenschaften, z. b. Dateigröße oder Erweiterung, bei denen neue Klartext-Dateitypen in den Index eingeschlossen werden. Weitere Eigenschaften, die an den Index zurückgegeben werden können, sind:

-   Für Dateien: Autor, Titel, Status, Schlüsselwörter
-   Für Medien: Album, Genre, Kamera Marke, ergriffene Datumsangaben
-   Für die Kommunikation: from, to, CC, Wichtigkeit
-   Für Kontakte: Berufsbezeichnung, geschäftlich Telefon, Unternehmen

Die obige Liste gruppiert Eigenschaften, die einem angegebenen wahrgenommenen Typ gemeinsam sind. Allerdings kann jede Eigenschaft unabhängig vom Typ verwendet werden. Beispielsweise könnte Company für den Arbeitgeber Namen eines Kontakts verwendet werden und kann auch verwendet werden, um auf den Namen eines Clients zu verweisen, auf den sich die Datei bezieht. Viele dieser Eigenschaften werden verwendet, um Suchergebnisse in der WDS-Ergebnis Ansicht anzuzeigen. Beispielsweise wird die Title-Eigenschaft einer Datei in der Standard Ergebnis Ansicht als Haupt Spalte angezeigt. IFilter-Objekte sollten alle Eigenschaften ausgeben, die mit dem Elementtyp in Zusammenhang stehen, den Sie untersuchen. In WDS 2. x können keine benutzerdefinierten Eigenschaften hinzugefügt werden. Eine vollständige Liste der verfügbaren Eigenschaften finden Sie im [WDS-Schema](-search-2x-wds-schematable.md).

## <a name="filter-add-in-installation"></a>Installation des Add-ins Filtern

Die Installation des Filters umfasst das Kopieren der dll an einen geeigneten Speicherort im Verzeichnis "Programme" und deren Registrierung. Filter sollten die Selbstregistrierung für die Installation implementieren und die folgenden Richtlinien befolgen:

-   Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.
-   Anmerkungen zu dieser Version müssen bereitgestellt werden.
-   Ein Eintrag zum **Hinzufügen/Entfernen von Programmen** muss für jedes installierte Add-in erstellt werden.
-   Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.
-   Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktion wiederherzustellen und Sie als Standard-Add-in für diesen Dateityp oder-Speicher zu speichern.

### <a name="clsids-required-for-registration"></a>Für die Registrierung erforderliche CLSIDs

Es gibt drei Klassen Bezeichner (CLSIDs), die mit jedem Filter verknüpft sind. Zum Registrieren des Filter-Add-Ins müssen Sie mindestens einen der folgenden (verwenden Sie uuidgen.exe) generieren.

-   Der erste identifiziert den persistenten Handler für alle Filter, IID \_ IFilter, der {89bcb740-6119-101A-bcb7-00dd010655af} ist. Diese CLSID ist für alle Filter, die IFilter implementieren, konstant.
-   Der zweite Wert (der Wert des IID- \_ IFilter-Schlüssels) identifiziert die IFilter-Implementierung für den Dateityp. Dieser Schlüssel enthält einen InprocServer32-Wert, der den DLL-Namen nach Pfad und dem Threading Modell angibt. Wenn sich der Filter im Systempfad befindet, wie z. b. das Verzeichnis System32, genügt ein Dateiname. Andernfalls sollte dieser Wert über eine vollständige Pfadspezifikation verfügen.
-   Das dritte identifiziert den Dateityp, den der Filter verarbeitet, und wird von der GetClassID-Methode in ihrer ipersistent-Schnittstelle zurückgegeben.

> [!Note]
>
> In zukünftigen Versionen von Microsoft-Betriebssystemen kann das Installieren von Dateien im Verzeichnis "System32" schwieriger werden. Daher wird empfohlen, dass Sie die Dateien unter "Programme" installieren und einen vollständigen Pfad zum Filter in der Registrierung einschließen. Aus Sicherheitsgründen ist es auch ratsam, in der Registrierung einen vollständigen Pfad zu Ihrer DLL anzugeben. Andernfalls könnte eine "Trojaner"-Version der DLL geladen werden, wenn Sie sich vor der Version im Prozess Pfad befinden.

 

### <a name="registration-model"></a>Registrierungs Modell

Wenn WDS bereit ist, eine Datei zu filtern, wird die Registrierung in der Registrierung unter der Dateierweiterung ermittelt, um zu ermitteln, welcher Filter geladen werden soll. Anschließend folgt eine Reihe von Registrierungs Links, um den Namen der Filter-DLL in dieser Reihenfolge zu finden:

1.  Von CLSIDs unter:

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ rsSearch \\ contentindexcommon \\ Filters \\ override \\ rsapp**

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ rsSearch \\ contentindexcommon \\ Filters**

2.  Aus dem Datei Inhaltstyp:

    **HKEY \_ - \_ \\ Software \\ Klassen der \\ MIME- \\ Datenbank- \\ Inhaltstyp**

3.  Aus der Dateinamenerweiterung (identisch mit der Win32-loadifilter-API) unter:

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ rsSearch \\ contentindexcommon \\ Filters \\ override \\ rsapp**

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ rsSearch \\ contentindexcommon \\ Filters**

    **HKEY \_ \_ -Klassen root \\ extpersistenthandler->CLSID->IID \_ IFilter->CLSID**

4.  Standardmäßig:

    **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ rsSearch \\ contentindexcommon \\ Filters**

### <a name="to-register-a-filter-add-in"></a>So registrieren Sie ein Filter-Add-in

Sie müssen insgesamt acht Einträge in der Registrierung vornehmen, um das Filter-Add-in zu registrieren, wobei Folgendes gilt:

-   **. ext** ist die neue Dateinamenerweiterung.
-   **GUID \_ 1** kann jede neue GUID sein, die für diese Erweiterung generiert wurde.
-   **89bcb740-6119-101A-bcb7-00dd010655af** ist die GUID der IFilter-Schnittstelle, die eine Konstante für alle IFilter-Implementierungen ist.

1.  Registrieren Sie den persistenten Handler für die Dateinamenerweiterung mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  Registrieren Sie die IFilter-Implementierung mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  Registrieren Sie die IFilter-Implementierung bei der Windows-Desktop Suche mit dem folgenden Schlüssel und Wert:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Schema Tabelle](-search-2x-wds-schematable.md)
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 