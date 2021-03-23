---
title: Kopieren von Deskriptoren
description: Die ID3D12Device copydescriptors-Methode und die ID3D12Device copydescriptorssimple-Methode auf der Geräteschnittstelle verwenden die CPU, um die Deskriptoren sofort zu kopieren.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104555"
---
# <a name="copying-descriptors"></a>Kopieren von Deskriptoren

Die [**ID3D12Device:: copydescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) -Methode und die [**ID3D12Device:: copydescriptorssimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) -Methode auf der Geräteschnittstelle verwenden die CPU zum sofortigen Kopieren von Deskriptoren. Sie können als frei Thread bezeichnet werden, solange mehrere Threads auf der CPU oder GPU keine potenziell in Konflikt stehenden Schreibvorgänge durchführen.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Sofortiges Kopieren von Deskriptoren (CPU-Zeitachse)

Die Anzahl der Quell Deskriptoren (aus der kopiert werden soll), die als Satz von Deskriptorbereichen angegeben werden, muss gleich der Anzahl der Ziel Deskriptoren (zum Kopieren in) sein, die als separater Satz von Deskriptorbereichen angegeben werden. Die Quell-und Zielbereiche müssen andernfalls nicht in der Zeile angezeigt werden. Beispielsweise könnte eine Reihe von Deskriptoren mit geringer Dichte in ein zusammenhängendes Ziel kopiert werden, umgekehrt oder in einer Kombination.

Es können mehrere deskriptorheaps an dem Kopiervorgang beteiligt sein, sowohl als Quelle als auch als Ziel. Die Verwendung von Deskriptorhandles als Parameter bedeutet, dass die Kopiermethoden nicht darauf achten, welche Heaps ein bestimmter Deskriptor ist – es handelt sich lediglich um Arbeitsspeicher.

Die deskriptorheap-Typen, von denen und in kopiert werden, müssen abgeglichen werden, sodass die-Methoden einen einzelnen deskriptorheap als Eingabe verwenden. Der Treiber muss den heaptyp aller Deskriptoren im angegebenen Kopiervorgang kennen, damit er weiß, welche Datenmenge an dem Kopiervorgang beteiligt ist. Der Treiber muss möglicherweise auch benutzerdefinierte Kopiervorgänge durchführen, wenn er von einem bestimmten deskriptorheap verlangt wird – ein Implementierungsdetail. Beachten Sie, dass die Deskriptorhandles selbst nicht ermitteln, auf welchen Typ Sie verweisen. Daher ist ein zusätzlicher Parameter für den Kopiervorgang erforderlich.

Eine Alternative API zu [**copydescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) wird für den einfachen Fall bereitgestellt, dass ein einzelner Bereich von Deskriptoren von einem Speicherort in einen anderen kopiert wird – [**copydescriptorssimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).

Für diese gerätebasierten Methoden zum Kopieren von Deskriptoren (CPU-Zeitachse) müssen Quell Deskriptoren von einem sichtbaren deskriptorheap für nicht-Shader stammen. Die Ziel Deskriptoren können sich in jedem deskriptorheap befinden, der CPU-sichtbar ist (Shader ist sichtbar oder nicht).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptoren](descriptors.md)
</dt> </dl>

 

 




