---
title: Deskriptorheaps
description: Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104241"
---
# <a name="descriptor-heaps"></a>Deskriptorheaps

Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | Beschreibung                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über deskriptorheaps](descriptor-heaps-overview.md)<br/>                             | Deskriptorheaps enthalten viele Objekttypen, die nicht Teil eines Pipeline Zustands Objekts (PSO) sind, wie z. b. Shader-Ressourcen Sichten (Srvs), ungeordnete Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers. <br/>                |
| [Hardware Tarife](hardware-support.md)<br/>                                                 | Die Hardware Ebenen von Ebene 1 bis Ebene 3 verbessern die Ressourcen, die für die Pipeline verfügbar sind. <br/>                                                                                                                              |
| [Shader sichtbare deskriptorheaps](shader-visible-descriptor-heaps.md)<br/>                 | Shader sichtbare deskriptorheaps, sind deskriptorheaps, auf die Shader durch deskriptortabellen verweisen können.<br/>                                                                                                              |
| [Nicht Shader sichtbare deskriptorheaps](non-shader-visible-descriptor-heaps.md)<br/>         | Auf einige deskriptorheaps kann nicht durch Shader durch deskriptortabellen verwiesen werden. Sie ist jedoch entweder vorhanden, um der APP das Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein Shader-sichtbarer Heap erforderlich ist.<br/> |
| [Erstellen von deskriptorheaps](creating-descriptor-heaps.md)<br/>                             | Zum Erstellen und Konfigurieren eines deskriptorheaps müssen Sie einen deskriptorheap auswählen, die Anzahl der enthaltenen Deskriptoren bestimmen und Flags festlegen, die angeben, ob CPU-sichtbar und/oder Shader sichtbar sind. <br/>                    |
| [Festlegen und Auffüllen von deskriptorheaps](setting-descriptor-heaps.md)<br/>                | Die deskriptorheap-Typen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die deskriptortabellen verwendet werden können (höchstens jeweils jeweils jeweils). <br/>                                                        |
| [Deskriptorheap-Konfigurations Zusammenfassung](descriptor-heap-configurability-summary.md)<br/> | In der folgenden Tabelle werden Informationen zur Unterstützung von Shader und nicht-Shader-sichtbarem Heap zusammengefasst.<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptoren](descriptors.md)
</dt> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 





