---
title: Neuerungen in Direct3D 12
description: In diesem Thema wird die wichtigste neue Direct3D 12-Dokumentation beschrieben, die für verschiedene Releases verfügbar ist.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548629"
---
# <a name="whats-new-in-direct3d-12"></a>Neuerungen in Direct3D 12

In diesem Thema wird die wichtigste neue Direct3D 12-Dokumentation beschrieben, die für verschiedene Releases verfügbar ist.

Informationen zum Abrufen und Installieren von Direct3D finden Sie unter [Direct3D 12 Programming Environment Setup](./directx-12-programming-environment-set-up.md).

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 unter Windows 7

- [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) ist jetzt für Entwickler verfügbar.

## <a name="windows-10-may-2019-update"></a>Windows 10-Update von Mai 2019

Diese Features und APIs wurden für Windows 10, Version 1903 (10,0;) hinzugefügt oder aktualisiert. Build 18362) &mdash; auch als Windows 10-Update vom Mai 2019 bezeichnet.

- [Schattierung der Variablen Rate (VRS)](./vrs.md). Ermöglicht das Zuordnen von Renderleistung/-Strom Sätzen, die sich in Ihrem gerenderten Bild unterscheiden.
- [HLSL-Shader-Modell 6,4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md). Beschreibt die Machine Learning-systeminternen Funktionen, die dem HLSL-Shadermodell 6,4 hinzugefügt werden.
- [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) Enumeration. Definiert Konstanten, die eine Version der entfernten erweiterten Daten (Dred) des Geräts angeben.
- [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) Struktur. Gibt den Grad der Unterstützung an, den der Adapter für Metacommands bereitstellt.
- [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) Struktur. Gibt den Grad der Unterstützung an, den der Adapter für Metacommands bereitstellt.
- [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) Enumeration. Definiert Konstanten, die eine Schattierungs Raten Ebene angeben (für Schattierung mit variabler Rate oder VRS).
- [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) -Schnittstelle und ihre Methoden. Wird verwendet, um den Modus für die Optimierung der Treiber Hintergrundverarbeitung festzulegen. Siehe auch [Optimierungen für den Hintergrund-Shader](https://devblogs.microsoft.com/directx/background-shader-optimizations/).
- [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) -Schnittstelle und ihre Methoden. Bietet Lauf Zeit Zugriff auf vom Gerät entfernte erweiterte Daten (Dred)-Daten.
- [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) -Schnittstelle und ihre Methoden. Steuert die entfernten erweiterten Daten Einstellungen (Dred) des Geräts.
- [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) -Schnittstelle und ihre Methoden. Unterstützung für Variablenraten Schattierung (VRS).

Die [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) Enumeration wurde mit dem Hinzufügen der **D3D_SHADER_MODEL_6_5** Konstante (einer Funktion auf experimentellen Ebene) aktualisiert.

Die [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) Enumeration wurde mit dem Hinzufügen der **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** Konstante aktualisiert.

Die [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) Enumeration wurde mit dem Hinzufügen der Konstanten **D3D12_FEATURE_D3D12_OPTIONS6** und **D3D12_FEATURE_QUERY_META_COMMAND** aktualisiert.

Die [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) Enumeration wurde mit dem Hinzufügen der **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** Konstante aktualisiert.

## <a name="windows-10-version-1809"></a>Windows 10, Version 1809

Diese Features und APIs wurden für Windows 10, Version 1809 (10,0;) hinzugefügt oder aktualisiert. Build 17763) &mdash; auch als Windows 10-Update vom Oktober 2018 bezeichnet.

- [Direct3D 12-Raytracing](./direct3d-12-raytracing.md)
- [Direct3D 12-Rendering-Verläufen](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10, Version 1709

Diese Schnittstellen wurden der Direct3D-Dokumentation für Windows 10, Version 1709, hinzugefügt.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) erweitert die Funktionalität zum Erstellen von Zäunen durch Unterstützung des Abrufens von Flags, die zum Erstellen des Fence übergebenen werden.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) erweitert die Liste der verfügbaren Grafikbefehle durch Unterstützung der direkten Schreibweise von unmittelbaren Werten in einen Puffer.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) erweitert die Funktionen des virtuellen Adapters durch das Erstellen von speziellen Diagnose Heaps im Systemspeicher, die auch im Fall eines GPU-Fehlers oder eines Geräts mit einem Gerät entfernt bleiben.

Die [**D3D \_ Shader- \_ modellenumeration**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) verfügt über einen neuen **D3D \_ Shader \_ Model \_ 6 \_ 1** -Wert, der zum Beschreiben des Shader-Modells 6,1 hinzugefügt wurde.

Die [**D3D12 \_ Feature**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) -Enumeration verfügt auch über das neue **D3D12 \_ Feature \_ D3D12 \_ OPTIONS3** und **D3D12 \_ Feature \_ vorhandene \_ Heaps** -Werte. Wie die Namen vermuten, können Sie mit diesen Werten nach zusätzlichen Direct3D12-Optionen suchen und die Unterstützung vorhandener Heaps überprüfen.

## <a name="windows-10-version-1703"></a>Windows 10, Version 1703

Diese Themen wurden der Direct3D-Dokumentation für Windows 10, Version 1703, hinzugefügt.

-   Die [**ID3D12Device2:: anatepipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) -Methode und die [**D3D12 \_ Pipeline \_ State \_ Stream- \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) -Struktur stellen eine neue und stabilere Methode zum Erstellen von PSOs dar und vereinheitlicht die ganze Zahl zum Erstellen von Grafiken und Compute-Pipelines.
-   Mit der [**ID3D12Device1:: CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) -Methode wird die Pipeline Bibliotheks Schnittstelle erweitert, um die mit der neuen, einheitlichen [**D3D12 \_ Pipeline \_ State \_ Stream \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) -Struktur erstellten PSOs zu akzeptieren.
-   Mit der [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) -Funktion können Entwickler mit bestimmten Entwicklungs Features experimentieren, die einen Computer im Entwicklermodus verwenden.
-   Es gibt fünf neue Schnittstellen (siehe [Schnittstellen Hierarchie](interface-hierarchy.md)):
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   Weitere Informationen finden Sie in der [Übersicht über das HLSL-Shader-Modell 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), in dem die systeminternen Wellen Vorgänge für Multithread-Pixel-und Compute-Shader beschrieben
-   Die Verwendung von [**ID3D12Device:: setstablepowerstate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) hat sich geändert.
-   Einige neue Features für Direct3D 11 werden unter [Direct3D 11,4 Features](../direct3d11/direct3d-11-4-features.md)beschrieben.
-   [**Atomiccopybufferuint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) und [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) aktivieren Sie den **spät Latch** , um die überarbeitete Latenz zu verringern.
-   [**ID3D12Device2:: kreatepipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) und [**omsetdepthbounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) ermöglichen das **Testen von tiefen Begrenzungen auf unterstützter** Hardware.
-   [**Resolvesubresourceregion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) ermöglicht **partielle Auflösung** von unter Ressourcen, um die Leistung zu optimieren.
-   [**Setsamplepositions**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) aktiviert **Programm fähige Beispiel Positionen** auf unterstützter Hardware.

## <a name="november-2016-documentation-update"></a>Dokumentations Update von November 2016

-   Revision der Hinweise für [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Erläuterung von "State Decay to Common" (Weitere Informationen finden [Sie unter Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)).
-   Die Header Datei "D3dx12. h", auf die in [Hilfsstrukturen und Funktionen für D3D12](helper-structures-and-functions-for-d3d12.md)verwiesen wird, kann direkt von [der D3D12-Hilfsbibliothek](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12)heruntergeladen werden.

## <a name="august-2016-documentation-update-2"></a>Dokumentations Update 2 August 2016

-   Ein neuer Leitfaden mit dem Titel [zum Verständnis der D3D12 Debug-Schicht](understanding-the-d3d12-debug-layer.md).

    Drei neue debugebenenschnittstellen (im Vorschaumodus) werden beschrieben: [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Dokumentations Update 1 August 2016

-   Revision der [Verwendung von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Revision des [Ressourcen Zugriffs für mehrere Warteschlangen](./user-mode-heap-synchronization.md#multi-queue-resource-access).

## <a name="windows-10-version-1607"></a>Windows 10, Version 1607

Diese Themen wurden der Direct3D-Dokumentation für Windows 10, Version 1607, hinzugefügt.

-   Stamm [Signatur Version 1,1](root-signature-version-1-1.md) : eine Übersicht über die aktualisierten Stamm Signaturen, die es apps ermöglichen, anzugeben, wie statische oder flüchtige Deskriptoren und Daten sind, wodurch Grafiktreiber Optimierungen unterstützen können.
-   Die [**ID3D12Device1:: kreatepipelinelibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) -Methode beschreibt die Vorteile der Erstellung einer Pipeline Bibliothek.
-   Es gibt drei neue Schnittstellen (siehe [Schnittstellen Hierarchie](interface-hierarchy.md)):
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   Weitere Informationen finden Sie in der [Übersicht über das HLSL-Shader-Modell 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), in dem die systeminternen Wellen Vorgänge für Multithread-Pixel-und Compute-Shader beschrieben
-   Die Verwendung von [**ID3D12Device:: setstablepowerstate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) hat sich geändert.
-   Einige neue Features für Direct3D 11 werden unter [Direct3D 11,4 Features](../direct3d11/direct3d-11-4-features.md)beschrieben.
-   Der Bereich der unterstützten Bibliotheken für Direct3D 12 wurde aktualisiert. Weitere Informationen finden Sie im Abschnitt " **unterstützte Tools und Bibliotheken" unter** [Direct3D 12 Programming Environment Setup](directx-12-programming-environment-set-up.md).
-   [Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe](../direct3darticles/high-dynamic-range.md)
-   [Variable Aktualisierungsrate anzeigen](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [DXGI 1,5-Verbesserungen](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Verwandte Themen

* [Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)