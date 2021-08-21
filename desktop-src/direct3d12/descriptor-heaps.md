---
title: Deskriptorheaps
description: Ein Deskriptor-Heap ist eine Sammlung zusammenhängender Zuordnungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd883436954cb6e1f0270646f1a57d564f3d51d29b6023bec749d1728fda40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807552"
---
# <a name="descriptor-heaps"></a>Deskriptorheaps

Ein Deskriptor-Heap ist eine Sammlung zusammenhängender Zuordnungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | Beschreibung                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über Deskriptorheaps](descriptor-heaps-overview.md)<br/>                             | Deskriptor-Heaps enthalten viele Objekttypen, die nicht Teil eines Pipelinezustandsobjekts (Pipeline State Object, PSO) sind, z. B. Shader-Ressourcenansichten (SRVs), ungeordnete Zugriffsansichten (Unordered Access Views, UAVs), Konstantenpufferansichten (Constant Buffer Views, CBVs) und Sampler. <br/>                |
| [Hardwaretarife](hardware-support.md)<br/>                                                 | Die Hardwareebenen von Ebene 1 bis Ebene 3 verfügen über steigende Ressourcen, die für die Pipeline verfügbar sind. <br/>                                                                                                                              |
| [Für den Shader sichtbare Deskriptorheaps](shader-visible-descriptor-heaps.md)<br/>                 | Shader-sichtbare Deskriptor-Heaps sind Deskriptorhaps, auf die von Shadern über Deskriptortabellen verwiesen werden kann.<br/>                                                                                                              |
| [Für den Shader nicht sichtbare Deskriptorheaps](non-shader-visible-descriptor-heaps.md)<br/>         | Auf einige Deskriptor-Heaps kann nicht von Shadern über Deskriptortabellen verwiesen werden, sondern sie sind entweder vorhanden, um die App beim Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein für Shader sichtbarer Heap erforderlich ist.<br/> |
| [Erstellen von Deskriptorheaps](creating-descriptor-heaps.md)<br/>                             | Zum Erstellen und Konfigurieren eines Deskriptor-Heaps müssen Sie einen Deskriptor-Heaptyp auswählen, bestimmen, wie viele Deskriptoren er enthält, und Flags festlegen, die angeben, ob er cpu- und/oder shader sichtbar ist. <br/>                    |
| [Festlegen und Auffüllen von Deskriptorheaps](setting-descriptor-heaps.md)<br/>                | Die Deskriptor-Heaptypen, die für eine Befehlsliste festgelegt werden können, sind solche, die Deskriptoren enthalten, für die Deskriptortabellen verwendet werden können (jeweils mindestens eine). <br/>                                                        |
| [Zusammenfassung der Deskriptorheap-Konfigurierbarkeit](descriptor-heap-configurability-summary.md)<br/> | In der folgenden Tabelle sind Informationen zur Unterstützung von shader- und nicht shader-sichtbaren Heaps zusammengefasst.<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptoren](descriptors.md)
</dt> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> <dt>

[Stammsignaturen](root-signatures.md)
</dt> </dl>

 

 





