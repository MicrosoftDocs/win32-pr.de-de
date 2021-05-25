---
title: Stammsignatur, Version 1.1
description: Der Zweck von Version 1.1 der Stammsignatur ist es, Anwendungen zu ermöglichen, Treibern anzugeben, wenn sich Deskriptoren in einem Deskriptorhap nicht ändern oder die Datendeskriptoren, auf die zeigt, sich nicht ändern.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a7a32576efa4d93a8d26aa57282f06e0d5a02f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343665"
---
# <a name="root-signature-version-11"></a>Stammsignatur, Version 1.1

Der Zweck von Version 1.1 der Stammsignatur ist es, Anwendungen zu ermöglichen, Treibern anzugeben, wenn sich Deskriptoren in einem Deskriptorhap nicht ändern oder die Datendeskriptoren, auf die zeigt, sich nicht ändern. Dadurch können Treiber Optimierungen durchführen, die möglicherweise in dem Wissen möglich sind, dass ein Deskriptor oder der Arbeitsspeicher, auf den er zeigt, für einen bestimmten Zeitraum statisch ist.

-   [Übersicht](#overview)
-   [Statische und flüchtige Flags](#static-and-volatile-flags)
    -   [DESKRIPTOREN \_ VOLATILE](#descriptors_volatile)
    -   [DATA \_ VOLATILE](#data_volatile)
    -   [DATA \_ STATIC \_ WHILE \_ SET \_ AT \_ EXECUTE](#data_static_while_set_at_execute)
    -   [DATA \_ STATIC](#data_static)
    -   [Kombinieren von Flags](#combining-flags)
    -   [Flagzusammenfassung](#flag-summary)
-   [API-Zusammenfassung der Version 1.1](#version-11-api-summary)
    -   [Enumerationen](#enums)
    -   [Strukturen](#helper-structures)
    -   [Funktionen](#functions)
    -   [Methoden](#methods)
    -   [Hilfsstrukturen](#helper-structures)
-   [Folgen der Verletzung von Static-ness-Flags](#consequences-of-violating-static-ness-flags)
-   [Versionsverwaltung](#version-management)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Übersicht

Version 1.0 der Stammsignatur ermöglicht es, dass der Inhalt von Deskriptorhaps und der Arbeitsspeicher, auf den sie zeigen, von Anwendungen jederzeit frei geändert werden können, wenn Befehlslisten/Bündel, auf die sie verweisen, möglicherweise auf der GPU ausgeführt werden. Häufig benötigen Anwendungen jedoch nicht die Flexibilität, Deskriptoren oder Arbeitsspeicher zu ändern, nachdem Befehle aufgezeichnet wurden, die auf sie verweisen.

Anwendungen sind häufig trivial in der Lage:

-   Richten Sie Vor dem Binden von Deskriptortabellen oder Stammdeskriptoren für eine Befehlsliste oder ein Paket Deskriptoren ein (und möglichen Speicher, auf den sie zeigen).
-   Stellen Sie sicher, dass sich diese Deskriptoren erst ändern, wenn die Befehlsliste /bundles, auf die sie verweisen, die Ausführung zum letzten Mal beendet hat.
-   Stellen Sie sicher, dass sich die Daten, auf die die Deskriptoren zeigen, während derselben vollständigen Dauer nicht ändern.

Alternativ kann eine Anwendung nur in der Lage sein, zu beachten, dass sich die Daten für einen kürzeren Zeitraum nicht ändern. Insbesondere daten können während der Ausführung der Befehlsliste für das Zeitfenster statisch sein, das eine Stammparameterbindung (Deskriptortabelle oder Stammdeskriptor) derzeit auf die Daten verweist. Anders ausgedrückt: Eine Anwendung möchte möglicherweise die Ausführung auf der GPU-Zeitachse durchführen, die einige Daten zwischen Zeiträumen aktualisiert, in denen sie über einen Stammparameter festgelegt wird, wobei sie weiß, dass sie statisch ist, wenn sie festgelegt wird.

Wenn sich Deskriptoren oder die Datendeskriptoren, auf die verweisen, nicht ändern, sind die spezifischen Optimierungstreiber möglicherweise hardwareherstellerspezifisch, und wichtig ist, dass sie das Verhalten nur ändern, um die Leistung zu verbessern. Wenn Sie so viel Wissen über die Anwendungsabsicht wie möglich beibehalten, ist dies keine Belastung für Anwendungen.

Eine Optimierung besteht darin, dass viele Treiber effizientere Speicherzugriffe durch Shader erzeugen können, wenn sie die Zusagen kennen, die eine Anwendung hinsichtlich der statischen Freundlichkeit von Deskriptoren und Daten machen kann. Beispielsweise könnten Treiber eine Dekonstruktionsebene für den Zugriff auf einen Deskriptor in einem Heap entfernen, indem sie ihn in einen Stammdeskriptor konvertieren, wenn die hardwarespezifischen Hardware hinsichtlich der Größe des Stammarguments nicht vertraulich ist.

Die zusätzliche Aufgabe für Entwickler, die Version 1.1 verwenden, besteht darin, möglichst Zusagen hinsichtlich der Schwankungen und statischen Daten zu machen, damit Treiber die sinnvollen Optimierungen vornehmen können. Entwickler müssen keine Zusagen zur Statischen Ness machen.

Root Signature Version 1.0 funktioniert weiterhin unverändert, obwohl Anwendungen, die Stammsignaturen neu kompilieren, jetzt standardmäßig Stammsignatur 1.1 verwenden (mit einer Option zum Erzwingen von Version 1.0, falls gewünscht).

## <a name="static-and-volatile-flags"></a>Statische und flüchtige Flags

Die folgenden Flags sind Teil der Stammsignatur, damit Treiber eine Strategie auswählen können, wie einzelne Stammargumente am besten behandelt werden können, wenn sie festgelegt werden. Außerdem werden dieselben Annahmen in Pipelinezustandsobjekte (PSOs) eingebettet, wenn sie ursprünglich kompiliert wurden, da die Stammsignatur Teil eines PSO ist.

Die folgenden Flags werden von der App festgelegt und gelten für Deskriptoren oder Daten.

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

### <a name="descriptors_volatile"></a>DESKRIPTOREN \_ VOLATILE

Wenn dieses Flag festgelegt ist, können die Deskriptoren in einem Deskriptorhap, auf den eine Stammdeskriptortabelle verweist, jederzeit von der Anwendung geändert werden, es sei denn, die Befehlsliste/-bündel, die die Deskriptortabelle binden, wurden übermittelt und die Ausführung nicht abgeschlossen. Beispielsweise ist das Aufzeichnen einer Befehlsliste und das anschließende Ändern  von Deskriptoren in einem Deskriptorhap, auf den er verweist, vor dem Übermitteln der Befehlsliste zur Ausführung gültig. Dies ist das einzige unterstützte Verhalten von Root Signature Version 1.0.

Wenn das DESCRIPTORS \_ VOLATILE-Flag *nicht festgelegt* ist, sind Deskriptoren statisch. Für diesen Modus gibt es kein Flag. Statische Deskriptoren bedeuten, dass die Deskriptoren in einem Deskriptorhap, auf den von einer Stammdeskriptortabelle verwiesen wird, zu dem Zeitpunkt initialisiert wurden, zu dem die Deskriptortabelle für eine Befehlsliste/ein Bündel (während der Aufzeichnung) festgelegt wurde. Die Deskriptoren können erst geändert werden, wenn die Befehlsliste bzw. das Paket zum letzten Mal ausgeführt wurde. *Für Root Signature Version 1.1* sind statische Deskriptoren die Standardannahme, und die Anwendung muss bei Bedarf das DESCRIPTORS \_ VOLATILE-Flag angeben.

Bei Paketen, die Deskriptortabellen mit statischen Deskriptoren verwenden, müssen die Deskriptoren zum Zeitpunkt der Aufzeichnung des Pakets bereit sein (im Gegensatz zum Zeitpunkt des Bundles) und nicht geändert werden, bis die Ausführung des Pakets zum letzten Mal abgeschlossen ist. Deskriptortabellen, die auf statische Deskriptoren verweisen, müssen während der Bundleaufzeichnung festgelegt und nicht in das Paket geerbt werden. Es ist gültig, wenn eine Befehlsliste eine Deskriptortabelle mit statischen Deskriptoren verwendet, die in einem Paket festgelegt und an die Befehlsliste zurückgegeben wurde.

Wenn Deskriptoren statisch sind, gibt es eine weitere Änderung des Verhaltens, für die das DESCRIPTORS \_ VOLATILE-Flag festgelegt werden muss. Der Zugriff auf Pufferansichten (im Gegensatz zu Texture1D-/2D-/3D-/Cubeansichten) ist ungültig und führt zu nicht definierten Ergebnissen, einschließlich möglicher Gerätezurücksetzungen, anstatt Standardwerte für Lese- oder Schreibvorgänge zurückzusetzen. Der Zweck, anwendungen die Möglichkeit zu beseitigen, von Hardware aus der Begrenzung der Zugriffsüberprüfung abhängig zu sein, besteht im Zulassen, dass Treiber statische Deskriptorzugriffe auf Stammdeskriptorzugriffe fördern, wenn sie dies als effizienter einordnen. Stammdeskriptoren unterstützen keine Überprüfung über grenzenlose Grenzen.

Wenn Anwendungen beim Zugriff auf Deskriptoren von einem sicheren Speicherzugriffsverhalten abhängen, müssen sie die Deskriptorbereiche, die auf diese Deskriptoren zugreifen, als DESCRIPTORS \_ VOLATILE markieren.

### <a name="data_volatile"></a>DATA \_ VOLATILE

Wenn dieses Flag festgelegt ist, können die Daten, auf die Deskriptoren zeigen, jederzeit von der CPU geändert werden, es sei denn, die Befehlsliste/-bündel, die die Deskriptortabelle binden, wurden übermittelt und die Ausführung nicht abgeschlossen. Dies ist das einzige unterstützte Verhalten von Root Signature Version 1.0.

Das Flag ist sowohl in Deskriptorbereichsflags als auch in Stammdeskriptorflags verfügbar.

### <a name="data_static_while_set_at_execute"></a>DATA \_ STATIC \_ WHILE \_ SET \_ AT \_ EXECUTE

Wenn dieses Flag festgelegt ist, können sich die Daten, auf die von Deskriptoren verwiesen wird, nicht mehr ändern, wenn die zugrunde liegende Stammdeskriptor- oder Deskriptortabelle während der Ausführung auf der GPU-Zeitachse für eine Befehlsliste bzw. ein Bündel festgelegt ist und endet, wenn nachfolgende Striche/Dispatches nicht mehr auf die Daten verweisen.

Bevor eine Stammdeskriptor- oder Deskriptortabelle auf der  GPU festgelegt wurde, können diese Daten auch durch dieselbe Befehlsliste bzw. dasselbe Paket geändert werden. Die Daten können auch geändert werden, während eine Stammdeskriptor- oder Deskriptortabelle, die darauf zeigt, weiterhin für die Befehlsliste/das Bündel festgelegt ist, solange Draw/Dispatches, die darauf verweisen, abgeschlossen sind. Dies erfordert jedoch, dass die Deskriptortabelle erneut an die Befehlsliste zurückgebunden wird, bevor das nächste Mal die Stammdeskriptor- oder Deskriptortabelle dereferenziert wird. Dadurch kann der Treiber wissen, dass daten, auf die von einem Stammdeskriptor oder einer Deskriptortabelle verwiesen wird, geändert wurden.

Der wesentliche Unterschied zwischen DATA STATIC WHILE SET AT EXECUTE und DATA VOLATILE ist, dass ein Treiber bei DATA VOLATILE nicht erkennen kann, ob Datenkopien in einer Befehlsliste die Daten geändert haben, auf die ein \_ \_ \_ \_ \_ \_ \_ Deskriptor verweist, ohne eine zusätzliche Zustandsnachverfolgung auszuführen. Wenn ein Treiber z. B. eine beliebige Art von Datenvorabrufbefehlen in seine Befehlsliste einfügen kann (um den Shaderzugriff auf bekannte Daten effizienter zu gestalten, z. B. ), informiert data STATIC WHILE SET AT EXECUTE den Treiber darüber, dass er nur datenvorabrufen muss, wenn er über \_ \_ \_ \_ \_ [**SetGraphicsRootDescriptorTable,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) oder eine der Methoden zum Festlegen der konstanten Pufferansicht, Shaderressourcenansicht oder ungeordneten Zugriffsansicht festgelegt wird.

Bei Paketen gilt die Zusage, dass Daten statisch sind, während sie bei der Ausführung festgelegt werden, eindeutig für jede Ausführung des Pakets.

Das Flag ist sowohl in Deskriptorbereichsflags als auch in Stammdeskriptorflags verfügbar.

### <a name="data_static"></a>DATA \_ STATIC

Wenn dieses Flag festgelegt ist, wurden die Daten, auf die von Deskriptoren verwiesen wird, bis zu dem Zeitpunkt initialisiert, zu dem ein Stammdeskriptor oder eine Deskriptortabelle, die auf den Arbeitsspeicher verweist, für eine Befehlsliste/ein Paket während der Aufzeichnung festgelegt wurde, und die Daten können erst geändert werden, wenn die Befehlsliste bzw. das Paket zum letzten Mal ausgeführt wurde.

Bei Paketen beginnt die statische Dauer bei der Einstellung der Stammdeskriptor- oder Deskriptortabelle während der Aufzeichnung des Pakets, im Gegensatz zur Aufzeichnung einer aufrufenden Befehlsliste. Darüber hinaus muss eine Deskriptortabelle, die auf statische Daten verweist, im Bündel festgelegt und nicht geerbt werden. Es ist gültig, dass eine Befehlsliste eine Deskriptortabelle verwendet, die auf statische Daten verweist, die in einem Bündel festgelegt und an die Befehlsliste zurückgegeben wurden.

Das Flag ist sowohl in Deskriptorbereichsflags als auch in Stammdeskriptorflags verfügbar.

### <a name="combining-flags"></a>Kombinieren von Flags

Höchstens eines der DATA-Flags kann gleichzeitig angegeben werden, mit Ausnahme von Sampler-Deskriptorbereichen, die überhaupt keine DATA-Flags unterstützen, da Sampler nicht auf Daten verweisen.

Das Fehlen von DATA-Flags für SRV- und CBV-Deskriptorbereiche bedeutet, dass das Standardverhalten DATA \_ STATIC WHILE SET AT EXECUTE angenommen \_ \_ \_ \_ wird. Der Grund, warum dieser Standardwert anstelle von DATA STATIC ausgewählt \_ wird, ist, dass DATA \_ STATIC WHILE SET AT EXECUTE in den meisten Fällen viel \_ \_ \_ \_ wahrscheinlicher ein sicherer Standardwert ist, während dennoch einige Optimierungsmöglichkeiten besser sind als die Standardeinstellung DATA \_ VOLATILE.

Das Fehlen von DATA-Flags für UAV-Deskriptorbereiche bedeutet, dass ein Standardverhalten von DATA VOLATILE angenommen wird, da in der \_ Regel UAVs geschrieben werden.

DESCRIPTORS \_ VOLATILE kann *nicht* mit DATA \_ STATIC, aber mit den anderen DATA-Flags kombiniert werden.  Der Grund, warum DESCRIPTORS \_ VOLATILE mit DATA STATIC kombiniert werden \_ \_ kann, während SET AT EXECUTE \_ \_ festgelegt \_ ist, ist, dass flüchtige Deskriptoren während der Ausführung von Befehlsliste/Bündeln immer noch bereit sein müssen, und DATA \_ STATIC WHILE SET AT EXECUTE nur \_ \_ \_ \_ Zusagen zur statischen Ness innerhalb einer Teilmenge der Befehlsliste/Paketausführung macht.

### <a name="flag-summary"></a>Flagzusammenfassung

In den folgenden Tabellen werden die möglicherweise verwendeten Flagkombinationen zusammengefasst.



| Gültige D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS-Einstellungen                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine Flags festgelegt                                                   | Deskriptoren sind statisch (Standardeinstellung). Standardannahmen für Daten: für SRV/CBV: DATA \_ STATIC WHILE SET AT EXECUTE und für \_ \_ \_ \_ UAV: DATA \_ VOLATILE. Diese Standardwerte für SRV/CBV passen sicher zu den Verwendungsmustern für den Großteil der Stammsignaturen.                                                                                              |
| DATA \_ STATIC                                                   | Sowohl Deskriptoren als auch Daten sind statisch. Dadurch wird das Potenzial für die Treiberoptimierung maximiert.                                                                                                                                                                                                                                                          |
| DATA \_ VOLATILE                                                 | Deskriptoren sind statisch, und die Daten sind flüchtig.                                                                                                                                                                                                                                                                                                     |
| DATA \_ STATIC \_ WHILE \_ SET \_ AT \_ EXECUTE                          | Deskriptoren sind statisch, und Daten sind statisch, während sie bei der Ausführung festgelegt werden.                                                                                                                                                                                                                                                                                      |
| DESKRIPTOREN \_ VOLATILE                                          | Deskriptoren sind flüchtig, und es werden Standardannahmen zu Daten getroffen: für SRV/CBV: DATA \_ STATIC WHILE SET AT EXECUTE und für \_ \_ \_ \_ UAV: DATA \_ VOLATILE.                                                                                                                                                                                              |
| DESKRIPTOREN VOLATILE \_ \| DATA \_ VOLATILE                        | Sowohl Deskriptoren als auch Daten sind flüchtig, äquivalent zu Root Signature 1.0.                                                                                                                                                                                                                                                                            |
| DESKRIPTOREN VOLATILE \_ DATA STATIC WHILE SET AT \| \_ \_ \_ \_ \_ EXECUTE | Deskriptoren sind flüchtig, beachten Sie jedoch, dass sie sich während der Ausführung der Befehlsliste nicht ändern können. Daher ist es gültig, die zusätzliche Deklaration zu kombinieren, dass Daten statisch sind, während sie während der Ausführung über die Stammdeskriptortabelle festgelegt werden. Die zugrunde liegenden Deskriptoren sind effektiv statisch, solange die Daten nicht statisch sind. |



 



| Gültige D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS-Einstellungen                                                  |  BESCHREIBUNG                                                                                                                                                                                                                 |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine Flags festgelegt                                      | Standardannahmen für Daten: für SRV/CBV: DATA \_ STATIC WHILE SET AT EXECUTE und für \_ \_ \_ \_ UAV: DATA \_ VOLATILE. Diese Standardwerte für SRV/CBV passen sicher zu den Verwendungsmustern für den Großteil der Stammsignaturen. |
| DATA \_ STATIC                                      | Daten sind statisch, das beste Potenzial für die Treiberoptimierung.                                                                                                                                                       |
| \_DATA STATIC WÄHREND SET AT \_ \_ \_ \_ EXECUTE             | Daten sind statisch, während sie bei der Ausführung festgelegt werden.                                                                                                                                                                              |
| DATA \_ VOLATILE                                    | Entspricht stammsignatur 1.0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>API-Zusammenfassung der Version 1.1

Die folgenden API-Aufrufe ermöglichen Version 1.1.

### <a name="enums"></a>Enumerationen

Diese Enumerationen enthalten die Schlüsselflags zum Angeben von Deskriptor und Datenvolatilität.

-   [**D3D \_ ROOT \_ SIGNATURE \_ VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : Versions-IDs.
-   [**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) Ein Bereich von Flags, der bestimmt, ob Deskriptoren oder Daten flüchtig oder statisch sind.
-   [**D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Ein ähnlicher Bereich von Flags wie [**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags)mit der Ausnahme, dass nur Datenflags für Stammdeskriptoren gelten.

### <a name="structures"></a>Strukturen

Aktualisierte Strukturen (ab Version 1.0) enthalten Verweise auf die Flags "volatiley"/"static".

-   [**D3D12 \_ FEATURE \_ DATA \_ ROOT \_ SIGNATURE:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) Übergeben Sie diese Struktur an [**CheckFeatureSupport,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) um zu überprüfen, ob Root Signature Version 1.1 unterstützt wird.
-   [**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) kann eine beliebige Version einer Stammsignaturbeschreibung enthalten und ist für die Verwendung mit den unten aufgeführten Serialisierungs-/Deserialisierungsfunktionen konzipiert.
-   Diese Strukturen entsprechen denen, die in Version 1.0 verwendet werden, mit dem Hinzufügen neuer Flagfelder für Deskriptorbereiche und Stammdeskriptoren:

    -   [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**D3D12 \_ ROOT \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Functions

Die hier aufgeführten Methoden haben die ursprünglichen [**Funktionen D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) und [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) ersetzt, da sie für eine beliebige Version der Stammsignatur konzipiert sind. Das serialisierte Formular wird an die [**CreateRootSignature-API**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) übergeben. Wenn ein Shader mit einer Stammsignatur erstellt wurde, enthält der kompilierte Shader bereits eine serialisierte Stammsignatur.

-   [**D3D12SerializeVersionedRootSignature:**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) Wenn eine Anwendung die [**D3D12 \_ \_ VERSIONED ROOT \_ SIGNATURE-Datenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) prozedural generiert, muss sie das serialisierte Formular mit dieser Funktion erstellen.
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) : Generiert eine Schnittstelle, die die deserialisierte Datenstruktur über [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)zurückgeben kann.

### <a name="methods"></a>Methoden

Die [**ID3D12VersionedRootSignatureDeserializer-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) wird erstellt, um die Stammsignaturdatenstruktur zu deserialisieren.

-   [**GetRootSignatureDescAtVersion:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) Konvertiert Stammsignaturbeschreibungsstrukturen in eine angeforderte Version.
-   [**GetUnconvertedRootSignatureDesc:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) Gibt einen Zeiger auf eine [**D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) zurück.

### <a name="helper-structures"></a>Hilfsstrukturen

Hilfsstrukturen wurden hinzugefügt, um die Initialisierung einiger der Strukturen der Version 1.1 zu unterstützen.

-   CD3DX12 \_ DESCRIPTOR \_ RANGE1
-   CD3DX12 \_ ROOT \_ PARAMETER1
-   CD3DX12 \_ STATIC \_ SAMPLER1
-   STAMMSIGNATUR-DESC MIT \_ \_ CD3DX12-VERSION \_ \_

Weitere Informationen finden [Sie unter Hilfsstrukturen und -funktionen für D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="consequences-of-violating-static-ness-flags"></a>Folgen der Verletzung von Static-ness-Flags

Der oben beschriebene Deskriptor und die Datenflags (sowie die Standardwerte, die durch das Fehlen bestimmter Flags impliziert werden) definieren eine Zusage der Anwendung an den Treiber, wie sie sich verhält. Wenn eine Anwendung gegen die Zusage verstößt, ist dies ungültiges Verhalten: Ergebnisse sind nicht definiert und können sich über verschiedene Treiber und Hardware hinweg unterscheiden.

Die Debugebene verfügt über Optionen zum Überprüfen, dass Anwendungen ihre Zusagen einhalten, einschließlich der Standardzusicherungen, die mit der Verwendung von Root Signature Version 1.1 geliefert werden, ohne Flags festzulegen.

## <a name="version-management"></a>Versionsverwaltung

Beim Kompilieren von Stammsignaturen, die an Shader angefügt sind, kompilieren neuere HLSL-Compiler standardmäßig die Stammsignatur in Version 1.1, während alte HLSL-Compiler nur 1.0 unterstützen. Beachten Sie, dass 1.1-Stammsignaturen unter Betriebssystemen, die stammsignatur 1.1 nicht unterstützen, nicht funktionieren.

Die mit einem Shader kompilierte Stammsignaturversion kann mithilfe von auf eine bestimmte Version erzwungen `/force_rootsig_ver <version>` werden. Das Erzwingen der Version ist erfolgreich, wenn der Compiler das Verhalten der Stammsignatur, die bei der erzwungenen Version kompiliert wird, beibehalten kann, z. B. durch Löschen nicht unterstützter Flags in der Stammsignatur, die nur zu Optimierungszwecken dienen, sich aber nicht auf das Verhalten auswirken.

Auf diese Weise kann eine Anwendung z.B. eine 1.1-Stammsignatur für 1.0 und 1.1 kompilieren, wenn sie die Anwendung erstellt und die entsprechende Version zur Laufzeit abhängig vom Grad der Betriebssystemunterstützung auswählt. Es wäre jedoch am effizientesten, wenn eine Anwendung Stammsignaturen einzeln kompilieren würde (insbesondere, wenn mehrere Versionen benötigt werden), und zwar getrennt von Shadern. Auch wenn Shader anfänglich nicht mit einer angefügten Stammsignatur kompiliert werden, kann der Vorteil der Compilervalidierung der Stammsignaturkompatibilität mit einem Shader mithilfe der Compileroption beibehalten `/verifyrootsignature` werden. Später zur Laufzeit können PSOs mithilfe von Shadern erstellt werden, die keine Stammsignaturen enthalten, während die gewünschte Stammsignatur (möglicherweise die entsprechende Version, die vom Betriebssystem unterstützt wird) als separater Parameter übergeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Stammsignatur](creating-a-root-signature.md)
</dt> <dt>

[Stammsignaturen](root-signatures.md)
</dt> <dt>

[Festlegen von Stammsignaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




