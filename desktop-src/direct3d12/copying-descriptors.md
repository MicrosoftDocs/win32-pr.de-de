---
title: Kopieren von Deskriptoren
description: Die Methoden ID3D12Device CopyDescriptors und ID3D12Device CopyDescriptorsSimple auf der Geräteschnittstelle verwenden die CPU, um Deskriptoren sofort zu kopieren.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02abfb433b36738de0fd62285e44b2f065ac017217a1e61f8c305e8ca76228
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069700"
---
# <a name="copying-descriptors"></a>Kopieren von Deskriptoren

Die [**Methoden ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) und [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) auf der Geräteschnittstelle verwenden die CPU, um Deskriptoren sofort zu kopieren. Sie können als free threaded bezeichnet werden, solange mehrere Threads auf der CPU oder GPU keine potenziell in Konflikt stehenden Schreibvorgänge ausführen.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Sofortiges Kopieren von Deskriptoren (CPU-Zeitachse)

Die Anzahl der Quelldeskriptoren (aus der kopiert werden soll), die als Satz von Deskriptorbereichen angegeben werden, muss der Anzahl der Zieldeskriptoren (in die kopiert werden soll) und als separater Satz von Deskriptorbereichen angegeben sein. Die Quell- und Zielbereiche müssen andernfalls nicht in der Reihe stehen. Beispielsweise könnte ein Sparsesatz von Deskriptoren in ein zusammenhängendes Ziel kopiert werden (umgekehrt) oder in einer Kombination.

Am Kopiervorgang können mehrere Deskriptor-Heaps beteiligt sein, sowohl als Quelle als auch als Ziel. Die Verwendung von Deskriptorhandles als Parameter bedeutet, dass die Kopiermethoden sich nicht darum kümmern, in welchen Heaps ein deskriptor liegt– sie sind alle nur Arbeitsspeicher.

Die Deskriptor-Heaptypen, die aus und kopiert werden, müssen übereinstimmen, sodass die Methoden einen einzelnen Deskriptor-Heaptyp als Eingabe verwenden. Der Treiber muss den Heaptyp aller Deskriptoren im angegebenen Kopiervorgang kennen, damit er weiß, welche Datengröße am Kopiervorgang beteiligt ist. Der Treiber muss möglicherweise auch benutzerdefinierte Kopierarbeiten tun, wenn ein angegebener Deskriptorhaptyp dies zusichert – ein Implementierungsdetail. Beachten Sie, dass Deskriptorhandles nicht anderweitig identifizieren, auf welchen Typ sie verweisen. daher ist ein zusätzlicher Parameter für den Kopiervorgang erforderlich.

Eine alternative API zu [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) wird für den einfachen Fall bereitgestellt, dass ein einzelner Bereich von Deskriptoren von einem Speicherort an einen anderen kopiert wird : [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).

Für diese gerätebasierten Deskriptorkopiemethoden (CPU-Zeitachse) müssen Quelldeskriptoren von einem nicht shader sichtbaren Deskriptor-Heap stammen. Die Zieldeskriptoren können sich in jedem deskriptor-Heap befindet, der cpu-sichtbar (Shader sichtbar oder nicht) ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptoren](descriptors.md)
</dt> </dl>

 

 




