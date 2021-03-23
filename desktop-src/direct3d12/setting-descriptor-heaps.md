---
title: Festlegen und Auffüllen von deskriptorheaps
description: Die deskriptorheap-Typen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die deskriptortabellen verwendet werden können (höchstens jeweils jeweils jeweils).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548669"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Festlegen und Auffüllen von deskriptorheaps

Die deskriptorheap-Typen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die deskriptortabellen verwendet werden können (höchstens jeweils jeweils jeweils).

-   [Festlegen von deskriptorheaps](#setting-and-populating-descriptor-heaps)
-   [Auffüllen von deskriptorheaps](#populating-descriptor-heaps)
-   [Verwandte Themen](#related-topics)

## <a name="setting-descriptor-heaps"></a>Festlegen von deskriptorheaps

Die Typen des deskriptorheaps, die in einer Befehlsliste festgelegt werden können, sind:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Die Heaps, die in der Befehlsliste festgelegt werden, müssen auch als Shader-sichtbar erstellt worden sein. Es gibt drei Typen von Befehlslisten: Direct, Bundle und Compute.

Nachdem ein deskriptorheap in einer Befehlsliste festgelegt wurde, verweisen nachfolgende Aufrufe, die deskriptortabellen definieren, auf den aktuellen deskriptorheap. Der deskriptortabellenstatus ist am Anfang einer Befehlsliste nicht definiert, und nach dem Ändern der deskriptorheaps in einer Befehlsliste. Das redundanter festlegen desselben deskriptorheaps führt nicht dazu, dass deskriptortabelleneinstellungen nicht definiert sind.

In einem Bündel können die deskriptorheaps dagegen nur einmal festgelegt werden (redundante Aufrufe, die zweimal denselben Heap festlegen, verursachen keinen Fehler); Andernfalls ist das Verhalten nicht definiert. Die festgelegten deskriptorheaps müssen dem Status entsprechen, wenn eine Befehlsliste das Paket aufruft. Andernfalls ist das Verhalten nicht definiert. Dadurch können Pakete die deskriptortabelleneinstellungen der Befehlsliste erben und bearbeiten. Bündel, die keine deskriptortabellen ändern (nur erben), müssen überhaupt keinen deskriptorheap festlegen, und Sie erben nur von der aufrufenden Befehlsliste.

Wenn deskriptorheaps festgelegt werden (mithilfe von [**ID3D12GraphicsCommandList:: setdescriptorheaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), werden alle verwendeten Heaps in einem einzelnen-Befehl festgelegt (und alle zuvor festgelegten Heaps werden durch den-Befehl nicht festgelegt). Höchstens ein Heap jedes oben aufgeführten Typs kann im-Befehl festgelegt werden.

## <a name="populating-descriptor-heaps"></a>Auffüllen von deskriptorheaps

Nachdem eine Anwendung einen deskriptorheap erstellt hat, kann Sie Methoden auf dem Gerät verwenden, um entweder Deskriptoren direkt in den Heap zu generieren oder Deskriptoren von einem Ort in einen anderen zu kopieren.

Der anfängliche Inhalt des deskriptorheap-Speichers ist nicht definiert. Daher kann die GPU oder der Treiber zum Verweisen auf nicht initialisierten Speicher für das Rendering zu nicht definierten Ergebnissen führen, z. b. zum Zurücksetzen des Geräts.

Wenn die Anwendung einen deskriptorheap für die CPU-Sicht konfiguriert, kann die CPU Methoden zum Erstellen von Deskriptoren im Heap und zum Kopieren von Ort zu Ort (einschließlich Heaps) in einem unmittelbaren, kostenlosen Thread aufzurufen. Wenn der Heap als SHADER_VISIBLE konfiguriert wurde, ist das Lesen der CPU nicht zulässig.



## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




