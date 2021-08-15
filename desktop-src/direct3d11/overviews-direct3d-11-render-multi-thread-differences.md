---
title: Threadingunterschiede zwischen Direct3D-Versionen
description: Viele Multithread-Programmiermodelle verwenden Synchronisierungsprimitiven (z. B. Mutexe), um kritische Abschnitte zu erstellen und zu verhindern, dass von mehreren Threads gleichzeitig auf Code zugegriffen wird.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9b53e53ad10dc662bfb57dc880c6423b3df0f320d109f212e54c10f3b9f314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913057"
---
# <a name="threading-differences-between-direct3d-versions"></a>Threadingunterschiede zwischen Direct3D-Versionen

Viele Multithread-Programmiermodelle verwenden Synchronisierungsprimitiven (z. B. Mutexe), um kritische Abschnitte zu erstellen und zu verhindern, dass von mehreren Threads gleichzeitig auf Code zugegriffen wird.

Die Methoden zum Erstellen von Ressourcen der [**ID3D11Device-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) wurden jedoch so entworfen, dass sie erneut in die Lage sind, ohne Synchronisierungsprimitiven und kritische Abschnitte zu erfordern. Daher sind die Ressourcenerstellungsmethoden effizient und einfach zu verwenden.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 11, 10 und 9:<br/> Direct3D 11 ist standardmäßig größtenteils threadsicher und lässt weiterhin zu, dass Anwendungen die Verwendung von D3D11 \_ CREATE \_ DEVICE \_ SINGLETHREADED deaktivieren. Wenn Anwendungen nicht threadsicher sind, müssen sie Threadingregeln einhalten. Die Runtime synchronisiert Threads im Namen der Anwendung, sodass gleichzeitige Threads ausgeführt werden können. Tatsächlich ist die Synchronisierung in Direct3D 11 effizienter als die Verwendung der threadsicheren Schicht in Direct3D 10.<br/> Direct3D 10 kann die Ausführung von nur einem Thread gleichzeitig unterstützen. Direct3D 10 ist vollständig threadsicher und ermöglicht es einer Anwendung, dieses Verhalten mithilfe von D3D10 \_ CREATE \_ DEVICE SINGLE \_ \_ THREADED zu deaktivieren. <br/> Direct3D 9 ist standardmäßig nicht threadsicher. Wenn Sie jedoch [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) oder [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) aufrufen, um ein Gerät zu erstellen, können Sie das Flag D3DCREATE MULTITHREADED angeben, um den \_ Direct3D 9-API-Thread sicher zu machen. Dies verursacht einen erheblichen Synchronisierungsaufwand. Daher wird nicht empfohlen, den Direct3D 9-API-Thread sicher zu machen, da die Leistung beeinträchtigt werden kann.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

