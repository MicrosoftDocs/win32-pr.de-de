---
title: Threading Unterschiede zwischen Direct3D-Versionen
description: Viele multithreadprogrammierungs-Modelle verwenden Synchronisierungs primitive (z. b. Mutexen), um kritische Abschnitte zu erstellen und zu verhindern, dass der Zugriff auf Code von mehreren Threads gleichzeitig erfolgt.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e99c68dbdba1d6f0cdd789f6ccac8b81d4ac03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390645"
---
# <a name="threading-differences-between-direct3d-versions"></a>Threading Unterschiede zwischen Direct3D-Versionen

Viele multithreadprogrammierungs-Modelle verwenden Synchronisierungs primitive (z. b. Mutexen), um kritische Abschnitte zu erstellen und zu verhindern, dass der Zugriff auf Code von mehreren Threads gleichzeitig erfolgt.

Die Methoden zum Erstellen von Ressourcen der [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle wurden jedoch so konzipiert, dass Sie Wiedereintritts fähig werden, ohne dass Synchronisierungs primitive und kritische Abschnitte erforderlich sind. Folglich sind die Methoden zum Erstellen von Ressourcen effizient und leicht zu verwenden.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 11, 10 und 9:<br/> Direct3D 11 ist standardmäßig größtenteils Thread sicher und ermöglicht es den Anwendungen weiterhin, die Verwendung von D3D11 \_ Create \_ Device \_ Singlethreaded zu abonnieren. Wenn Anwendungen nicht Thread sicher sind, müssen Sie Threading Regeln einhalten. Die Laufzeit synchronisiert Threads für die Anwendung, sodass gleichzeitige Threads ausgeführt werden können. Tatsächlich ist die Synchronisierung in Direct3D 11 effizienter als die Verwendung der Thread sicheren Schicht in Direct3D 10.<br/> Direct3D 10 unterstützt die gleichzeitig Ausführung von nur einem Thread. Direct3D 10 ist vollständig Thread sicher und ermöglicht es einer Anwendung, dieses Verhalten mithilfe von d3d10 \_ Create \_ Device \_ Single Thread abzumelden \_ . <br/> Direct3D 9 ist nicht standardmäßig Thread sicher. Wenn Sie jedoch " [**devatedevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) " oder " [**foratedeviceex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) " aufrufen, um ein Gerät zu erstellen, können Sie das D3DCREATE- \_ multithreadflag angeben, um den Direct3D 9-API-Thread sicher zu machen. Dies verursacht einen erheblichen Synchronisierungs Aufwand. Daher wird empfohlen, den Direct3D 9-API-Thread sicher zu gestalten, da die Leistung beeinträchtigt werden kann.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

