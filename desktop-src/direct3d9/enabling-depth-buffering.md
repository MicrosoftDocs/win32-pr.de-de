---
description: 'Nachdem Sie einen tiefen Puffer erstellt haben, wie unter Erstellen eines tiefen Puffers (Direct3D 9) beschrieben, aktivieren Sie die Tiefe Pufferung durch Aufrufen der Methode IDirect3DDevice9:: settrenderstate.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Aktivieren der tiefen Pufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341428"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Aktivieren der tiefen Pufferung (Direct3D 9)

Nachdem Sie einen tiefen Puffer erstellt haben, wie unter [Erstellen eines tiefen Puffers (Direct3D 9)](creating-a-depth-buffer.md)beschrieben, aktivieren Sie die Tiefe Pufferung durch Aufrufen der Methode [**IDirect3DDevice9:: settrenderstate**](/windows/desktop/api) . Legen Sie den D3DRS \_ zenable-renderzustand so fest, dass tiefe Pufferung aktiviert wird. Verwenden Sie den D3DZB \_ true-Member des [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) -Enumerationstyps (oder **true**), um z-Pufferung zu aktivieren, D3DZB \_ usew, um w-buffereing zu aktivieren, oder D3DZB \_ false (oder **false**), um die tiefen Pufferung zu deaktivieren.

> [!Note]  
> Um w-buffereing zu verwenden, muss die Anwendung eine konforme Projektions Matrix festlegen, auch wenn Sie die Direct3D-Transformations Pipeline nicht verwendet. Weitere Informationen zum Bereitstellen einer geeigneten Projektions Matrix finden Sie in der [W-freundlichen Projektions Matrix](projection-transform.md) .

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 
