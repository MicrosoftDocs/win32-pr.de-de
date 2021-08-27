---
title: Kernschnittstellen (Direct3D 12-Grafiken)
description: Die folgenden Schnittstellen werden in d3d12.h deklariert.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 0cc8fcecec2e2a0966ed34e23eb65ed9acd37e76
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812891"
---
# <a name="core-interfaces"></a>Core-Schnittstellen

Die folgenden Schnittstellen werden in d3d12.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Stellt die Speicherbelegungen für GPU-Befehle (Graphics Processing Unit) dar. |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Eine Schnittstelle, von der [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) erbt. Es stellt einen geordneten Satz von Befehlen dar, die von der GPU ausgeführt werden, während die Erweiterung andere Befehlslisten als nur die für Grafiken (z. B. Compute und Kopie) unterstützen kann. |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Stellt Methoden zum Übermitteln von Befehlslisten, Synchronisieren der Ausführung von Befehlslisten, Instrumentieren der Befehlswarteschlange und Aktualisieren von Ressourcenkachelzuordnungen bereit. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Ein Befehlssignaturobjekt ermöglicht Apps das Angeben indirekter Zeichnungen, einschließlich des Pufferformats, des Befehlstyps und der zu verwendenden Ressourcenbindungen. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Ein Deskriptorheap ist eine Auflistung zusammenhängender Zuordnungen von Deskriptoren, eine Zuordnung für jeden Deskriptor. Deskriptorheaps enthalten viele Objekttypen, die nicht Teil eines Pipelinezustandsobjekts (Pipeline State Object, PSO) sind, z. B. Shaderressourcenansichten (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs) und Samplers. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Stellt einen virtuellen Adapter dar. Sie wird zum Erstellen von Befehlszuweisungen, Befehlslisten, Befehlswarteschlangen, Umgrenzungen, Ressourcen, Pipelinezustandsobjekten, Heaps, Stammsignaturen, Samplern und vielen Ressourcenansichten verwendet. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Stellt einen virtuellen Adapter dar und erweitert den Von [**ID3D12Device bereitgestellten**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)Methodenbereich. |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [**ID3D12Device1,**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) um Pipelinezustandsobjekte aus Beschreibungen des Pipelinezustandsstreams zu erstellen. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [**ID3D12Device2,**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) um die Erstellung von speziellen Diagnoseheaps im Systemspeicher zu unterstützen, die auch im Falle eines GPU-Fehlers oder gerätefernen Szenarios beibehalten werden. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device3.](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12Device7**](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device6](/windows/win32/api/d3d12/nn-d3d12-id3d12device6). |
| [**ID3D12Device8**](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device7](/windows/win32/api/d3d12/nn-d3d12-id3d12device7). |
| [**ID3D12Device9**](/windows/win32/api/d3d12/nn-d3d12-id3d12device9) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device8,](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) um Methoden zum Verwalten von Shadercaches hinzuzufügen. |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Eine Schnittstelle, von der andere Kernschnittstellen erben, einschließlich [**ID3D12PipelineLibrary,**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) [**ID3D12CommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)und [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Sie stellt eine Methode bereit, um zum Geräteobjekt zurückzukehren, für das es erstellt wurde. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Stellt Laufzeitzugriff auf DRED-Daten (Device Removed Extended Data) bereit. |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Diese Schnittstelle steuert die Einstellungen für vom Gerät entfernte erweiterte Daten (DEVICE Removed Extended Data, DRED). |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Stellt einen Fence dar, ein Objekt, das für die Synchronisierung der CPU und mindestens einer GPUs verwendet wird.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Stellt einen Fence dar. Diese Schnittstelle erweitert [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)und unterstützt das Abrufen der Flags, die zum Erstellen des ursprünglichen Fences verwendet werden.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Kapselt eine Liste von Grafikbefehlen für das Rendering. Enthält APIs zum Instrumentieren der Befehlslistenausführung sowie zum Festlegen und Löschen des Pipelinezustands. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Kapselt eine Liste von Grafikbefehlen für das Rendering, die Erweiterung der Schriftart zur Unterstützung programmierbarer Beispielpositionen, atomische Kopien für die Implementierung von Spätlatchtechniken und optionale Tiefengrenzentests. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Kapselt eine Liste von Grafikbefehlen für das Rendering und erweitert die -Schnittstelle, um das direkte Schreiben von Werten direkt in einen Puffer zu unterstützen. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Kapselt eine Liste von Grafikbefehlen für das Rendering. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Kapselt eine Liste von Grafikbefehlen für das Rendering und erweitert die -Schnittstelle, um die Ray-Ablaufverfolgung und Renderdurchläufe zu unterstützen. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Ein Heap ist eine Abstraktion der zusammenhängenden Speicherbelegung, die zum Verwalten des physischen Speichers verwendet wird. Dieser Heap kann mit [**ID3D12Resource-Objekten**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) verwendet werden, um platzierte oder reservierte Ressourcen zu unterstützen. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Stellt einen anwendungsdefinierte Rückruf dar, der verwendet wird, um über Änderungen der Lebensdauer eines Objekts benachrichtigt zu werden. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Stellt Einrichtungen zum Steuern der Lebensdauer eines über die Lebensdauer nachverfolgten Objekts dar. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Stellt einen Metabefehl dar. Ein Metabefehl ist ein Direct3D 12-Objekt, das einen Algorithmus darstellt, der von unabhängigen Hardwareanbietern (IHVs) beschleunigt wird. Es handelt sich um einen nicht transparenten Verweis auf einen Befehlsgenerator, der vom Treiber implementiert wird. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Eine Schnittstelle, von der [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) und [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) erben. Sie stellt Methoden bereit, um private Daten zuzuordnen und Objektnamen zu kommentieren. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Eine Schnittstelle, von der viele andere Kernschnittstellen erben. Es gibt an, dass der Objekttyp eine gewisse Menge an GPU-zugänglichen Arbeitsspeicher kapselt. gibt jedoch nicht stark an, ob die Anwendung die Residency des Objekts bearbeiten kann.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Verwaltet eine Pipelinebibliothek, insbesondere das Laden und Abrufen einzelner PSOs. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Verwaltet eine Pipelinebibliothek. Diese Schnittstelle erweitert [**ID3D12PipelineLibrary,**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) um PSOs aus einer Beschreibung des Pipelinezustandsstreams zu laden. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Stellt den Zustand aller derzeit festgelegten Shader sowie bestimmter fester Funktionszustandsobjekte dar. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Verwaltet einen Abfrageheap. Ein Abfrageheap enthält ein Array von Abfragen, auf das von Indizes verwiesen wird. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Kapselt eine generalisierte Fähigkeit der CPU und GPU zum Lesen und Schreiben in den physischen Arbeitsspeicher oder Heaps. Sie enthält Abstraktionen zum Organisieren und Bearbeiten einfacher Datenarrays sowie mehrdimensionale Daten, die für die Shader-Stichprobenentnahme optimiert sind. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | Die Stammsignatur definiert, welche Ressourcen an die Grafikpipeline gebunden sind. Eine Stammsignatur wird von der App konfiguriert und verknüpft Befehlslisten mit den Ressourcen, die shaders benötigen. Derzeit gibt es eine Grafik und eine Computestammsignatur pro App. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Enthält eine Methode zum Zurückgeben der deserialisierten [**D3D12-ROOT-SIGNATURE-DESC-Datenstruktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) einer serialisierten Stammsignaturversion 1.0.  |
| [**ID3D12ShaderCacheSession**](/windows/win32/api/d3d12/nn-d3d12-id3d12shadercachesession) | Stellt eine Shadercachesitzung dar. |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Stellt eine variable Menge des Konfigurationszustands dar, einschließlich Shadern, die eine Anwendung als einzelne Einheit verwaltet und die einem Treiber atomisch zur Verarbeitung zugewiesen wird, z. B. kompilieren oder optimieren.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Stellt Methoden zum Abrufen und Festlegen der Eigenschaften eines [**ID3D12StateObject-Objekts zur**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject)  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Diese Schnittstelle wird verwendet, um die Laufzeit für Tools wie PIX zu konfigurieren. Dies ist nicht beabsichtigt oder wird für ein anderes Szenario unterstützt. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Enthält Methoden zum Zurückgeben der deserialisierten [**D3D12-ROOT-SIGNATURE-DESC1-Datenstruktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) einer beliebigen Version einer serialisierten Stammsignatur.  |

## <a name="related-topics"></a>Zugehörige Themen

* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz zu Direct3D 12](direct3d-12-reference.md)
* [Schnittstellenhierarchie](interface-hierarchy.md)