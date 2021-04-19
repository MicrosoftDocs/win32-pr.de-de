---
title: Kern Schnittstellen (Direct3D 12-Grafiken)
description: Die folgenden Schnittstellen werden in d3d12. h deklariert.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: a51e35fff74ab1d0251d64578de665ad4134a843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339492"
---
# <a name="core-interfaces"></a>Core-Schnittstellen

Die folgenden Schnittstellen werden in d3d12. h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Stellt die Speicher Belegungen für GPU-Befehle (Graphics Processing Unit) dar. |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Eine Schnittstelle, von der [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) erbt. Sie stellt einen geordneten Satz von Befehlen dar, den die GPU ausführt, und ermöglicht es, dass die Erweiterung andere Befehlslisten unterstützt als nur die für Grafiken (z. b. COMPUTE und Copy). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Stellt Methoden zum Übermitteln von Befehlslisten, zum Synchronisieren der Befehlslisten Ausführung, zum Instrumentieren der Befehls Warteschlange und zum Aktualisieren von Ressourcen Kachel Zuordnungen bereit. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Ein Befehls Signatur Objekt ermöglicht es apps, indirekte Zeichnungen anzugeben, einschließlich des zu verwendenden Puffer Formats, des Befehls Typs und der zu verwendenden Ressourcen Bindungen. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor. Deskriptorheaps enthalten viele Objekttypen, die nicht Teil eines Pipeline Zustands Objekts (PSO) sind, wie z. b. Shader-Ressourcen Sichten (Srvs), ungeordnete Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Stellt einen virtuellen Adapter dar. Es wird verwendet, um Befehls Zuweisungen, Befehlslisten, Befehls Warteschlangen, Zäune, Ressourcen, Pipeline Zustands Objekte, Heaps, Stamm Signaturen, Samplers und viele Ressourcen Sichten zu erstellen. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Stellt einen virtuellen Adapter dar und erweitert den von [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)bereitgestellten Bereich von Methoden. |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) , um Pipeline Zustands Objekte aus den Datenstrom Beschreibungen des Pipeline Zustands zu erstellen. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) , um die Erstellung von speziellen Diagnose Heaps im Systemspeicher zu unterstützen, die auch im Fall eines GPU-Fehlers oder eines von einem Gerät entfernten Szenarios beibehalten werden. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3). |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Stellt einen virtuellen Adapter dar. Diese Schnittstelle erweitert [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Eine Schnittstelle, von der andere Kern Schnittstellen erben, einschließlich [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary), [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist), [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)und [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Sie stellt eine Methode bereit, um zum Geräte Objekt zurückzukehren, für das es erstellt wurde. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Bietet Lauf Zeit Zugriff auf vom Gerät entfernte erweiterte Daten (Dred)-Daten. |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Diese Schnittstelle steuert vom Gerät entfernte erweiterte Daten Einstellungen (Dred). |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Stellt einen Fence dar, ein Objekt, das für die Synchronisierung der CPU und eines oder mehrerer GPUs verwendet wird.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Stellt einen Fence dar. Diese Schnittstelle erweitert [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)und unterstützt das Abrufen der Flags, die zum Erstellen des ursprünglichen Fence verwendet werden.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Kapselt eine Liste von Grafik Befehlen zum Rendern. Umfasst APIs zum Instrumentieren der Befehlslisten Ausführung und zum Festlegen und Löschen des Pipeline Zustands. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Kapselt eine Liste von Grafik Befehlen für das Rendering, erweitert die ganze Zahl, um programmierbare Beispiel Positionen zu unterstützen, unteilbare Kopien zum Implementieren späterer latchtechniken und optionale tiefen Begrenzungen. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Kapselt eine Liste von Grafik Befehlen zum Rendern und erweitert so die-Schnittstelle, um das direkte Schreiben von unmittelbaren Werten in einen Puffer zu unterstützen. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Kapselt eine Liste von Grafik Befehlen zum Rendern. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Kapselt eine Liste von Grafik Befehlen zum Rendern und erweitert die-Schnittstelle zur Unterstützung der Ray-Ablauf Verfolgung und renderingdurch |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Ein Heap ist eine Abstraktion der zusammenhängenden Speicher Belegung, die zur Verwaltung des physischen Speichers verwendet wird. Dieser Heap kann mit [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) -Objekten verwendet werden, um belegte Ressourcen oder reservierte Ressourcen zu unterstützen. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Stellt einen Anwendungs definierten Rückruf dar, der für die Benachrichtigung Überlebens Dauer Änderungen eines-Objekts verwendet wird. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Stellt Funktionen zum Steuern der Lebensdauer eines Objekts dar, das die Lebensdauer überwacht. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Stellt einen Meta-Befehl dar. Ein Meta-Befehl ist ein Direct3D 12-Objekt, das einen Algorithmus darstellt, der von unabhängigen Hardwareherstellern (IHVs) beschleunigt wird. Es handelt sich um einen nicht transparenten Verweis auf einen Befehls Generator, der vom Treiber implementiert wird. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Eine Schnittstelle, von der [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) und [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) erben. Es stellt Methoden bereit, um private Daten zuzuordnen und Objektnamen zu kommentieren. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Eine Schnittstelle, von der viele andere Kern Schnittstellen erben. Gibt an, dass der Objekttyp eine gewisse Menge an GPU-zugreif baren Arbeitsspeicher kapselt. gibt jedoch nicht unbedingt an, ob die Anwendung die Residenz des Objekts bearbeiten kann.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Verwaltet eine Pipeline Bibliothek, insbesondere das Laden und Abrufen einzelner PSOs. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Verwaltet eine Pipeline Bibliothek. Diese Schnittstelle erweitert [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) , um PSOs aus einer Pipeline Status-Datenstrom Beschreibung zu laden. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Stellt den Status aller aktuell festgelegten Shader sowie bestimmter fester Funktions Zustands Objekte dar. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Verwaltet einen Abfrage Heap. Ein Abfrage Heap enthält ein Array von Abfragen, auf das von Indizes verwiesen wird. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Kapselt eine verallgemeinerte Fähigkeit der CPU und GPU, Lese-und Schreibvorgänge in den physischen Speicher oder Heaps durchzusetzen. Sie enthält Abstraktionen zum organisieren und Bearbeiten von einfachen Arrays von Daten sowie Mehrdimensionale Daten, die für die Shader-Stichproben Optimierung optimiert sind. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | Die Stamm Signatur definiert, welche Ressourcen an die Grafik Pipeline gebunden werden. Eine Stamm Signatur wird von der APP und Verknüpfungen Befehlslisten mit den Ressourcen konfiguriert, die für die Shader erforderlich sind. Zurzeit gibt es eine Grafik und eine computestammsignatur pro app. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Enthält eine Methode zum Zurückgeben der deserialisierten [**D3D12-root-Signature-DESC-**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) Datenstruktur einer serialisierten Stamm Signatur Version 1,0.  |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Stellt eine Variable Menge an Konfigurations Zuständen, einschließlich Shader, dar, die von einer Anwendung als eine Einheit verwaltet werden und die einem Treiber atomisch zur Verarbeitung zugewiesen ist, z. b. kompilieren oder optimieren.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Stellt Methoden zum erhalten und Festlegen der Eigenschaften eines [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject)bereit.  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Diese Schnittstelle wird verwendet, um die Laufzeit für Tools wie pix zu konfigurieren. Es ist nicht beabsichtigt oder wird für ein anderes Szenario nicht unterstützt. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Enthält Methoden, mit denen die deserialisierte [**D3D12-root-Signature-DESC1-**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) Datenstruktur einer beliebigen Version einer serialisierten Stamm Signatur zurückgegeben werden kann.  |

## <a name="related-topics"></a>Zugehörige Themen

* [Core-Referenz](direct3d-12-core-reference.md)
* [Direct3D 12-Referenz](direct3d-12-reference.md)
* [Schnittstellenhierarchie](interface-hierarchy.md)