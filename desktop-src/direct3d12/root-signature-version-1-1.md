---
title: Stamm Signatur Version 1,1
description: Der Zweck der Stamm Signatur Version 1,1 besteht darin, dass Anwendungen den Treibern zuweisen können, wenn sich Deskriptoren in einem deskriptorheap nicht ändern oder die Daten Deskriptoren nicht geändert werden.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d0a107b4186f164e60a6225f55c5ba3f4f06b2
ms.sourcegitcommit: f5a319899176e2df564bdb4d9eaffc32140452a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2020
ms.locfileid: "104548708"
---
# <a name="root-signature-version-11"></a>Stamm Signatur Version 1,1

Der Zweck der Stamm Signatur Version 1,1 besteht darin, dass Anwendungen den Treibern zuweisen können, wenn sich Deskriptoren in einem deskriptorheap nicht ändern oder die Daten Deskriptoren nicht geändert werden. Dies ermöglicht es der Option für Treiber, Optimierungen zu erstellen, bei denen möglicherweise ein Deskriptor oder der Arbeitsspeicher, auf den er verweist, für einen bestimmten Zeitraum statisch ist.

-   [Übersicht](#overview)
-   [Statische und flüchtige Flags](#static-and-volatile-flags)
    -   [Deskriptoren \_ flüchtig](#descriptors_volatile)
    -   [Daten \_ flüchtig](#data_volatile)
    -   [Daten \_ beim \_ \_ festlegen \_ bei der \_ Ausführung statisch](#data_static_while_set_at_execute)
    -   [Daten \_ statisch](#data_static)
    -   [Kombinieren von Flags](#combining-flags)
    -   [Flag-Zusammenfassung](#flag-summary)
-   [API-Zusammenfassung der Version 1,1](#version-11-api-summary)
    -   [Enumerationen](#enums)
    -   [Strukturen](#helper-structures)
    -   [Funktionen](#functions)
    -   [Methoden](#methods)
    -   [Hilfsstrukturen](#helper-structures)
-   [Folgen des Verstoßes gegen statische Flags](#consequences-of-violating-static-ness-flags)
-   [Versionsverwaltung](#version-management)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Mit der Stamm Signatur Version 1,0 können die Inhalte von deskriptorheaps und der Arbeitsspeicher, auf die Sie verweisen, jederzeit von Anwendungen frei geändert werden. Häufig ist es jedoch nicht erforderlich, dass Anwendungen die Flexibilität ändern, Deskriptoren oder Speicher zu ändern, nachdem Befehle aufgezeichnet wurden, die auf Sie verweisen.

Anwendungen sind häufig in den folgenden Fällen trivial:

-   Richten Sie vor dem Binden von deskriptortabellen oder Stamm Deskriptoren in einer Befehlsliste oder einem Bündel Deskriptoren (und möglicherweise den Speicher, auf den Sie verweisen) ein.
-   Stellen Sie sicher, dass diese Deskriptoren erst geändert werden, wenn die Ausführung der Befehlsliste/Bundles die auf Sie verweist, das letzte Mal abgeschlossen wurde.
-   Stellen Sie sicher, dass die Daten, auf die die Deskriptoren zeigen, sich für dieselbe vollständige Dauer nicht ändern.

Alternativ kann eine Anwendung nur beachten, dass sich die Daten für einen kürzeren Zeitraum nicht ändern. In bestimmten Daten kann für das Zeitfenster während der Ausführung der Befehlsliste statisch sein, dass eine Stamm Parameter Bindung (Deskriptortabelle oder Stamm Deskriptor) aktuell auf die Daten zeigt. Anders ausgedrückt: eine Anwendung möchte möglicherweise die Ausführung auf der GPU-Zeitachse ausführen, mit der einige Daten Zwischenzeit Räumen aktualisiert werden, in denen Sie über einen Root-Parameter festgelegt wird. Sie werden feststellen, dass Sie als statisch festgelegt werden.

Wenn Deskriptoren oder die Daten Deskriptoren auf verweisen, werden die spezifischen Optimierungs Treiber möglicherweise Hardware Anbieter spezifisch sein, und wichtig ist, dass Sie das Verhalten nicht ändern, außer möglicherweise die Leistung zu verbessern. Wenn Sie so viel Wissen über Anwendungs Absicht wie möglich beibehalten, werden Anwendungen nicht belastet.

Eine Optimierung besteht darin, dass viele Treiber effizientere Speicherzugriffe durch Shader erstellen können, wenn Sie die Zusagen kennen, die eine Anwendung über die statische Bedeutung von Deskriptoren und Daten treffen kann. Beispielsweise können Treiber eine Dereferenzierungsebene für den Zugriff auf einen Deskriptor in einem Heap entfernen, indem Sie Sie in einen Stamm Deskriptor umrechnen, wenn die jeweilige Hardware nicht für die Stamm Argument Größe sensibel ist.

Die zusätzliche Aufgabe für Entwickler, die Version 1,1 verwenden, besteht darin, nach Möglichkeit Zusagen zur Volatilität und statischen Daten der Daten zu machen, damit Treiber die Optimierungen vornehmen können, die sinnvoll sind. Entwickler müssen keine Zusagen über die statische Bedeutung haben.

Die Stamm Signatur Version 1,0 funktioniert unverändert, obwohl Anwendungen, die Stamm Signaturen neu kompilieren, standardmäßig die Stamm Signatur 1,1 (mit der Option zum Erzwingen der Version 1,0, wenn gewünscht) verwendet werden.

## <a name="static-and-volatile-flags"></a>Statische und flüchtige Flags

Die folgenden Flags sind Teil der Stamm Signatur, damit Treiber eine Strategie auswählen können, mit der Sie einzelne Stamm Argumente am besten verarbeiten können, wenn Sie festgelegt sind. Außerdem können Sie dieselben Annahmen in Pipeline Zustands Objekte (PSOs) einbetten, wenn Sie ursprünglich kompiliert werden, da die Stamm Signatur Teil eines PSO ist.

Die folgenden Flags werden von der APP festgelegt und gelten für Deskriptoren oder Daten.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_FLAGS
{
    D3D12_DESCRIPTOR_RANGE_FLAG_NONE    = 0,
    D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE    = 0x1,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE   = 0x2,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE    = 0x4,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC = 0x8
} D3D12_DESCRIPTOR_RANGE_FLAGS;

typedef enum D3D12_ROOT_DESCRIPTOR_FLAGS
{
    D3D12_ROOT_DESCRIPTOR_FLAG_NONE = 0,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE    = 0x2,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE = 0x4,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC  = 0x8
} D3D12_ROOT_DESCRIPTOR_FLAGS;
```

### <a name="descriptors_volatile"></a>Deskriptoren \_ flüchtig

Wenn dieses Flag festgelegt ist, können die Deskriptoren in einem deskriptorheap, auf die von einer stammdeskriptortabelle verwiesen wird, von der Anwendung jederzeit geändert werden, außer wenn die Befehlsliste/die Pakete, die die Deskriptortabelle binden, übermittelt wurden und die Ausführung noch nicht abgeschlossen ist. Beispielsweise ist das Aufzeichnen einer Befehlsliste und das anschließende Ändern von Deskriptoren in einem deskriptorheap, auf den verwiesen wird, *bevor* die Befehlsliste für die Ausführung übermittelt wird, gültig. Dies ist das einzige unterstützte Verhalten der Stamm Signatur Version 1,0.

Wenn das Flag " \_ volatile" für Deskriptoren *nicht* festgelegt ist, sind Deskriptoren statisch. Es gibt kein Flag für diesen Modus. Statische Deskriptoren bedeuten, dass die Deskriptoren in einem deskriptorheap, auf den von einer stammdeskriptortabelle verwiesen wird, durch den Zeitpunkt der Festlegung der Deskriptortabelle in einer Befehlsliste/einem Paket (während der Aufzeichnung) initialisiert wurden und die Deskriptoren nicht geändert werden können, bis die Ausführung der Befehlsliste bzw. des Pakets zum letzten Mal abgeschlossen ist. *Bei der Stamm Signatur Version 1,1 sind statische Deskriptoren die Standard Annahme*, und die Anwendung muss ggf. das-Flag für das Deskriptoren \_ volatile angeben.

Bei Paketen, die deskriptortabellen mit statischen Deskriptoren verwenden, müssen die Deskriptoren zum Zeitpunkt der Aufzeichnung des Pakets bereit sein (im Gegensatz zum Zeitpunkt, an dem das Paket aufgerufen wird) und nicht geändert werden, bis die Ausführung des Pakets zum letzten Mal abgeschlossen ist. Deskriptortabellen, die auf statische Deskriptoren zeigen, müssen während der Paket Aufzeichnung festgelegt und nicht in das Paket geerbt werden. Es ist zulässig, dass eine Befehlsliste eine Deskriptortabelle mit statischen Deskriptoren verwendet, die in einem Bündel festgelegt und an die Befehlsliste zurückgegeben wurde.

Wenn Deskriptoren statisch sind, gibt es eine andere Änderung des Verhaltens, das erfordert, dass das \_ Flag für flüchtiges Deskriptoren festgelegt wird. Der Zugriff auf alle Puffer Sichten (im Gegensatz zu Texture1D/2D/3D/Cube-Sichten) ist ungültig und erzeugt nicht definierte Ergebnisse, einschließlich möglicher Geräte Zurücksetzung, anstatt Standardwerte für Lese-oder Löschvorgänge zurückzugeben. Der Zweck, dass Anwendungen nicht mehr von der Überprüfung der Hardware abhängig sind, besteht darin, dass Sie es den Treibern ermöglichen, statische deskriptorzugriffe auf den Zugriff auf root-Deskriptoren herauf zusetzen, wenn Sie dies als effizienter betrachten. Stamm Deskriptoren unterstützen keine Überprüfung außerhalb der Grenzen.

Wenn Anwendungen beim Zugriff auf Deskriptoren von einem sicheren Speicherzugriffs Verhalten abhängig sind, müssen Sie die Deskriptorbereiche, die auf diese Deskriptoren zugreifen, als Deskriptoren als "volatile" kennzeichnen \_ .

### <a name="data_volatile"></a>Daten \_ flüchtig

Wenn dieses Flag festgelegt ist, können die Daten, auf die von Deskriptoren verwiesen wird, von der CPU jederzeit geändert werden, außer wenn die Befehlsliste bzw. die Pakete, die die Deskriptortabelle binden, übermittelt wurden und die Ausführung noch nicht abgeschlossen ist. Dies ist das einzige unterstützte Verhalten der Stamm Signatur Version 1,0.

Das-Flag ist in den deskriptorbereichsflags und den stammdeskriptorflags verfügbar.

### <a name="data_static_while_set_at_execute"></a>Daten \_ beim \_ \_ festlegen \_ bei der \_ Ausführung statisch

Wenn dieses Flag festgelegt ist, können die Daten, auf die von Deskriptoren verwiesen wird, beginnend ab nicht mehr geändert werden, wenn die zugrunde liegende stammdeskriptor-oder Deskriptortabelle bei der Ausführung auf der GPU-Zeitachse auf einer Befehlsliste/einem Paket festgelegt ist, und endet, wenn nachfolgende Zeichnungen/Verteiler nicht mehr

Bevor eine stammdeskriptor-oder Deskriptortabelle auf der GPU festgelegt wurde, *können* diese Daten sogar durch dieselbe Befehlsliste/jedes Paket geändert werden. Die Daten können auch geändert werden, während ein stammdeskriptor oder eine Deskriptortabelle, auf die verwiesen wird, weiterhin in der Befehlsliste bzw. im Bundle festgelegt ist, solange Draw/Dispatches, die darauf verweisen, abgeschlossen ist. Dies erfordert jedoch, dass die Deskriptortabelle erneut in die Befehlsliste aufgenommen wird, bevor die stammdeskriptor-oder Deskriptortabelle das nächste Mal dereferenziert wird. Dadurch kann der Treiber wissen, dass die Daten, auf die von einem stammdeskriptor oder einer Deskriptortabelle verwiesen wird, geändert wurden.

Der wesentliche Unterschied zwischen \_ Daten \_ , die während \_ \_ \_ der Ausführung bei EXECUTE und Data volatile festgelegt \_ sind, besteht darin, dass \_ ein Treiber nicht erkennen kann, ob Datenkopien in einer Befehlsliste die Daten, auf die von einem Deskriptor verwiesen wird, geändert haben, ohne dass eine zusätzliche Zustandsüberwachung Wenn z. b. ein Treiber eine beliebige Art von Daten in der Befehlsliste einfügen kann (um den Shader-Zugriff auf bekannte Daten effizienter zu machen, beispielsweise \_ \_ können die Daten, \_ die während der Ausführung von festgelegt werden, \_ vom Treiber informiert werden, dass \_ Sie nur die vorab abzurufenden Daten ausführen müssen, wenn Sie über " [**setgraphicsrootdescriptortable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable)", " [**setcomputerootdescriptortable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) " oder eine der Methoden zum Festlegen der Konstanten Puffer Ansicht, der shaderressourcenansicht oder der ungeordneten Zugriffs Ansicht festgelegt

Bei Paketen ist die Zusicherung, dass Daten statisch sind, während Sie bei EXECUTE festgelegt ist, für jede Ausführung des Bündels eindeutig.

Das-Flag ist in den deskriptorbereichsflags und den stammdeskriptorflags verfügbar.

### <a name="data_static"></a>Daten \_ statisch

Wenn dieses Flag festgelegt ist, werden die Daten, auf die von Deskriptoren verwiesen wird, von dem Zeitpunkt initialisiert, zu dem eine stammdeskriptor-oder Deskriptortabelle, die auf den Arbeitsspeicher verweist, während der Aufzeichnung in einer Befehlsliste/einem Paket festgelegt wurde, und die Daten können erst geändert werden, wenn die Ausführung der Befehlsliste bzw

Bei Paketen beginnt die statische Dauer bei der Erstellung des Stamm Deskriptors oder der Deskriptortabelle während der Aufzeichnung des Pakets, im Gegensatz zur Aufzeichnung einer aufrufenden Befehlsliste. Außerdem muss eine Deskriptortabelle, die auf statische Daten verweist, im Paket festgelegt und nicht vererbt werden. Eine Befehlsliste kann eine Deskriptortabelle verwenden, die auf statische Daten verweist, die in einem Bündel festgelegt und an die Befehlsliste zurückgegeben wurden.

Das-Flag ist in den deskriptorbereichsflags und den stammdeskriptorflags verfügbar.

### <a name="combining-flags"></a>Kombinieren von Flags

Höchstens eines der datenflags kann gleichzeitig angegeben werden, mit Ausnahme der Sampler-Deskriptorbereiche, die keine datenflags unterstützen, da Samplern nicht auf Daten verweisen.

Das Fehlen von datenflags für SRV-und CBV-Deskriptorbereiche bedeutet, dass der Standardwert der Daten \_ statisch \_ ist, während \_ \_ beim Festlegen beim \_ Ausführungs Verhalten angenommen wird. Der Grund, warum dieser Standardwert anstelle von Daten statisch gewählt wird, \_ ist, dass Daten, die \_ \_ während \_ \_ der Ausführung festgelegt \_ werden, in den meisten Fällen sehr wahrscheinlich ein sicherer Standard \_ Wert sind

Das Fehlen von datenflags für UAV-Deskriptorbereiche bedeutet, dass standardmäßig Daten \_ flüchtiges Verhalten angenommen wird, wenn in der Regel UAVs in geschrieben werden.

Deskriptoren \_ flüchtig *können nicht* mit statischen Daten kombiniert werden \_ , Sie *können* jedoch mit den anderen datenflags kombiniert werden. Die Grund Deskriptoren \_ volatile können mit statischen Daten kombiniert werden, \_ \_ während Sie \_ \_ bei EXECUTE festgelegt \_ sind, dass flüchtige Deskriptoren weiterhin erfordern, dass die Deskriptoren während der Befehlsliste/Paket Ausführung bereit sind, und Daten, die \_ \_ während der Ausführung auf Execute festgelegt sind, \_ nur für \_ \_ die statische entigkeit innerhalb einer Teilmenge der Befehlsliste/Paket Ausführung Zusagen.

### <a name="flag-summary"></a>Flag-Zusammenfassung

In den folgenden Tabellen werden die zu verwendenden Flag-Kombinationen zusammengefasst.



|                                                                |                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Gültige D3D12- \_ Einstellungen für deskriptorbereichsflags \_ \_**             | **Beschreibung**                                                                                                                                                                                                                                                                                                                                      |
| Keine Flags festgelegt.                                                   | Deskriptoren sind statisch (Standardeinstellung). Standard Annahmen für Daten: für SRV/CBV: Data \_ static \_ \_ \_ , bei EXECUTE festgelegt \_ , und für UAV: Data \_ volatile. Diese Standardeinstellungen für SRV/CBV passen sicher zu den Verwendungs Mustern für die Mehrzahl der Stamm Signaturen.                                                                                              |
| Daten \_ statisch                                                   | Beide Deskriptoren und Daten sind statisch. Dadurch wird das Potenzial für die Treiber Optimierung maximiert.                                                                                                                                                                                                                                                          |
| Daten \_ flüchtig                                                 | Deskriptoren sind statisch, und die Daten sind flüchtig.                                                                                                                                                                                                                                                                                                     |
| Daten \_ beim \_ \_ festlegen \_ bei der \_ Ausführung statisch                          | Deskriptoren sind statisch, und Daten sind statisch, während Sie bei EXECUTE festgelegt werden.                                                                                                                                                                                                                                                                                      |
| Deskriptoren \_ flüchtig                                          | Deskriptoren sind flüchtig, und es werden Standard Annahmen zu Daten gemacht: für SRV/CBV: Data \_ static, \_ \_ \_ bei EXECUTE festgelegt \_ , und für UAV: Data \_ volatile.                                                                                                                                                                                              |
| Deskriptoren \_ flüchtiger \| Daten \_ flüchtig                        | Sowohl Deskriptoren als auch Daten sind flüchtig, äquivalent zur Stamm Signatur 1,0.                                                                                                                                                                                                                                                                            |
| Deskriptoren \_ volatile \| - \_ Daten \_ beim \_ festlegen \_ bei \_ Execute | Deskriptoren sind flüchtig, aber beachten Sie, dass Sie Sie während der Ausführung der Befehlsliste trotzdem nicht ändern können. Daher ist es zulässig, die zusätzliche Deklaration zu kombinieren, bei der Daten während der Ausführung über die stammdeskriptortabelle festgelegt werden – die zugrunde liegenden Deskriptoren sind für einen längeren Zeitraum statisch, als die Daten als statisch festgelegt werden. |



 



|                                                   |                                                                                                                                                                                                                   |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Gültige D3D12 \_ - \_ stammdeskriptorflags- \_ Einstellungen** | **Beschreibung**                                                                                                                                                                                                   |
| Keine Flags festgelegt.                                      | Standard Annahmen für Daten: für SRV/CBV: Data \_ static \_ \_ \_ , bei EXECUTE festgelegt \_ , und für UAV: Data \_ volatile. Diese Standardeinstellungen für SRV/CBV passen sicher zu den Verwendungs Mustern für die Mehrzahl der Stamm Signaturen. |
| Daten \_ statisch                                      | Daten sind statisch, das beste Potenzial für die Treiber Optimierung.                                                                                                                                                       |
| Daten \_ beim \_ \_ festlegen \_ bei der \_ Ausführung statisch             | Daten sind statisch, während Sie bei EXECUTE festgelegt werden.                                                                                                                                                                              |
| Daten \_ flüchtig                                    | Entspricht der Stamm Signatur 1,0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>API-Zusammenfassung der Version 1,1

Die folgenden API-Aufrufe aktivieren Version 1,1.

### <a name="enums"></a>Enumerationen

Diese Enumerationen enthalten die Schlüsselflags zum Angeben von Deskriptoren und Daten Schwankungen.

-   [**D3D \_ Stamm \_ Signatur \_ Version**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : Versions-IDs.
-   [**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) : ein Bereich von Flags, der bestimmt, ob Deskriptoren oder Daten flüchtig oder statisch sind.
-   [**D3D12 \_ \_ \_ Stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) : ein ähnlicher Bereich von Flags für [**D3D12- \_ deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags), mit dem Unterschied, dass nur datenflags auf Stamm Deskriptoren angewendet werden.

### <a name="structures"></a>Strukturen

Aktualisierte Strukturen (ab Version 1,0) enthalten Verweise auf die Flags/static-Flags.

-   [**D3D12 \_ Funktions \_ Daten \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) -Stamm Signatur: übergeben Sie diese Struktur an [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) , um die Unterstützung der Stamm Signatur Version 1,1 zu überprüfen.
-   [**D3D12 \_ \_ \_ \_ DESC für versionierte Stamm Signatur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) : kann eine beliebige Version einer Stamm Signatur Beschreibung enthalten und ist für die Verwendung mit den unten aufgeführten Serialisierungs-/Deserialisierungsfunktionen vorgesehen.
-   Diese Strukturen entsprechen den in Version 1,0 verwendeten, mit der Hinzufügung neuer Flags-Felder für Deskriptorbereiche und Stamm Deskriptoren:

    -   [**D3D12 \_ root \_ Signature \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**D3D12- \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12-Stamm \_ \_ Deskriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**D3D12 \_ root \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Functions

Die hier aufgeführten Methoden ersetzen die ursprünglichen [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) -und [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) -Funktionen, da Sie für eine beliebige Version der Stamm Signatur entwickelt wurden. Die serialisierte Form wird an [**die API "**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API-API" übergeben. Wenn ein Shader mit einer Stamm Signatur erstellt wurde, enthält der kompilierte Shader bereits eine serialisierte Stamm Signatur.

-   [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) : Wenn eine Anwendung prozedurale die Datenstruktur der Stamm [**\_ \_ \_ Signatur D3D12 mit Versions**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) Angabe generiert, muss Sie das serialisierte Formular mithilfe dieser Funktion erstellen.
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) : generiert eine Schnittstelle, die die deserialisierte Datenstruktur über [**getunconvertedrootsignaturedesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)zurückgeben kann.

### <a name="methods"></a>Methoden

Die [**ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) -Schnittstelle wird erstellt, um die Datenstruktur der Stamm Signatur zu deserialisieren.

-   [**Getrootsignaturedescatversion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) : konvertiert Stamm Signatur Beschreibungs Strukturen in eine angeforderte Version.
-   [**Getunconvertedrootsignaturedesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) : gibt einen Zeiger auf eine mit [**D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) -Struktur zurück.

### <a name="helper-structures"></a>Hilfsstrukturen

Hilfsstrukturen wurden hinzugefügt, um die Initialisierung einiger der 1,1-Strukturen zu unterstützen.

-   CD3DX12- \_ Deskriptor \_ Bereich1
-   CD3DX12 \_ root \_ PARAMETER1
-   CD3DX12 \_ static \_ SAMPLER1
-   CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC

Weitere Informationen finden Sie unter [Hilfsstrukturen und Funktionen für D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="consequences-of-violating-static-ness-flags"></a>Folgen des Verstoßes gegen statische Flags

Die oben beschriebenen Deskriptoren und datenflags (sowie die Standardwerte, die durch das Fehlen bestimmter Flags impliziert werden) definieren eine Zusage, die die Anwendung für den Treiber über die Art der Verhalten hat. Wenn eine Anwendung die Zusage verletzt, ist dies ein ungültiges Verhalten: die Ergebnisse sind nicht definiert und unterscheiden sich möglicherweise für verschiedene Treiber und Hardware.

Die Debug-Ebene verfügt über Optionen zum Überprüfen, ob Anwendungen ihre Zusagen einhalten, einschließlich der Standard Zusagen, die bei der Verwendung der Stamm Signatur Version 1,1 enthalten sind, ohne dass Flags festgelegt werden.

## <a name="version-management"></a>Versionsverwaltung

Bei der Kompilierung von Stamm Signaturen, die an Shaders angefügt sind, wird die Stamm Signatur von neueren HLSL-Compilern standardmäßig in Version 1,1 kompiliert, während alte HLSL-Compiler nur 1,0 unterstützen. Beachten Sie, dass 1,1 Stamm Signaturen nicht auf Betriebssystemen funktionieren, die Stamm Signatur 1,1 nicht unterstützen.

Die mit einem Shader kompilierte Stamm Signatur Version kann mithilfe von für eine bestimmte Version erzwungen werden `/force_rootsig_ver <version>` . Die Erzwingung der Version ist erfolgreich, wenn der Compiler das Verhalten der Stamm Signatur beibehalten kann, die in der erzwungenen Version kompiliert wird, z. b. durch das Löschen nicht unterstützter Flags in der Stamm Signatur, die nur für Optimierungszwecke dienen, aber keine Auswirkungen auf das Verhalten haben.

Auf diese Weise kann eine Anwendung beispielsweise eine 1,1-Stamm Signatur sowohl bei der Erstellung der Anwendung sowohl bei 1,0 als auch bei 1,1 kompilieren und abhängig von der Betriebssystemunterstützung die geeignete Version zur Laufzeit auswählen. Dies wäre jedoch der größte Speicherplatz, wenn eine Anwendung Stamm Signaturen einzeln (insbesondere, wenn mehrere Versionen benötigt werden), getrennt von Shadern, kompiliert werden muss. Auch wenn Shader nicht anfänglich mit einer angefügten Stamm Signatur kompiliert werden, kann der Vorteil der compilerüberprüfung der Stamm Signatur Kompatibilität mit einem Shader mithilfe der- `/verifyrootsignature` Compileroption beibehalten werden. Später zur Laufzeit können PSOs mithilfe von Shadern erstellt werden, die keine Stamm Signaturen aufweisen, während die gewünschte Stamm Signatur (möglicherweise die vom Betriebssystem unterstützte Version) als separater Parameter übergeben wird.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Erstellen einer Stamm Signatur](creating-a-root-signature.md)
</dt> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> <dt>

[Angeben von Stamm Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




