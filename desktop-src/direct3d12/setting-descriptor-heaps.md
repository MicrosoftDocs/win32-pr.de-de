---
title: Festlegen und Auffüllen von Deskriptorheaps
description: Die Deskriptorheaptypen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die Deskriptortabellen verwendet werden können (höchstens jeweils einer).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e2fcb7143b097709cb7a3c98669a7d20331bfa9553f4eac5f2cf45a1a90797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119450"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Festlegen und Auffüllen von Deskriptorheaps

Die Deskriptorheaptypen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die Deskriptortabellen verwendet werden können (höchstens jeweils einer).

-   [Festlegen von Deskriptorheaps](#setting-and-populating-descriptor-heaps)
-   [Auffüllen von Deskriptorheaps](#populating-descriptor-heaps)
-   [Zugehörige Themen](#related-topics)

## <a name="setting-descriptor-heaps"></a>Festlegen von Deskriptorheaps

Die Typen von Deskriptorheaps, die in einer Befehlsliste festgelegt werden können, sind:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Die Heaps, die in der Befehlsliste festgelegt werden, müssen ebenfalls als sichtbarer Shader erstellt worden sein. Es gibt drei Arten von Befehlslisten: DIRECT, BUNDLE und COMPUTE.

Nachdem ein Deskriptorheap für eine Befehlsliste festgelegt wurde, verweisen nachfolgende Aufrufe, die Deskriptortabellen definieren, auf den aktuellen Deskriptorheap. Der Deskriptortabellenzustand ist am Anfang einer Befehlsliste und nach dem Ändern von Deskriptorheaps in einer Befehlsliste nicht definiert. Das redundante Festlegen desselben Deskriptorheaps führt nicht dazu, dass deskriptortabelleneinstellungen nicht definiert sind.

Im Gegensatz dazu können die Deskriptorheaps in einem Bündel nur einmal festgelegt werden (redundante Aufrufe, die den gleichen Heap zweimal festlegen, erzeugen keinen Fehler). Andernfalls ist das Verhalten nicht definiert. Die festgelegten Deskriptorheaps müssen mit dem Zustand übereinstimmen, wenn eine Befehlsliste das Paket aufruft. Andernfalls ist das Verhalten nicht definiert. Dadurch können Bundles die Deskriptortabelleneinstellungen der Befehlsliste erben und bearbeiten. Bundles, die keine Deskriptortabellen ändern (nur sie erben), müssen überhaupt keinen Deskriptorheap festlegen und erben nur von der Aufrufenden Befehlsliste.

Wenn Deskriptorheaps festgelegt werden (mit [**ID3D12GraphicsCommandList::SetDescriptorHeaps),**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)werden alle verwendeten Heaps in einem einzigen Aufruf festgelegt (und alle zuvor festgelegten Heaps werden durch den Aufruf nicht festgelegt). Im Aufruf kann höchstens ein Heap jedes oben aufgeführten Typs festgelegt werden.

## <a name="populating-descriptor-heaps"></a>Auffüllen von Deskriptorheaps

Nachdem eine Anwendung einen Deskriptorheap erstellt hat, kann sie methoden auf dem Gerät verwenden, um Deskriptoren direkt in den Heap zu generieren oder Deskriptoren von einem Ort an einen anderen zu kopieren.

Der anfängliche Inhalt des Deskriptorheapspeichers ist nicht definiert. Daher kann die Aufforderung der GPU oder des Treibers, zum Rendern auf nicht initialisierten Speicher zu verweisen, zu nicht definierten Ergebnissen führen, z. B. zum Zurücksetzen des Geräts.

Wenn die Anwendung einen Deskriptorheap so konfiguriert, dass er von der CPU sichtbar ist, kann die CPU Methoden aufrufen, um Deskriptoren im Heap zu erstellen und von Ort zu Ort (einschließlich heapübergreifender) sofort und ohne Threading zu kopieren. Wenn der Heap als SHADER_VISIBLE konfiguriert wurde, ist das Lesen durch die CPU nicht zulässig.



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




