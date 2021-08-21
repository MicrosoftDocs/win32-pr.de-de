---
description: Exklusiver DirectDraw-Modus
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Exklusiver DirectDraw-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09199e04a221299676c21fbc2876af4b8149943a743101d34893d5563ed42482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016179"
---
# <a name="directdraw-exclusive-mode"></a>Exklusiver DirectDraw-Modus

> [!Note]  
> Dieses Thema gilt nur für VMR-7. In VMR-9 aktivieren Sie den exklusiven Modus, indem Sie Einen eigenen Allocator-Presenter im exklusiven Modus bereitstellen. Dies ist relativ einfach, wenn Sie die [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) verwenden. Das VMR9Allocator-Beispiel zeigt, wie ein benutzerdefinierter Allocator-Presenter implementiert wird.

 

Im exklusiven DirectDraw-Modus übernimmt eine Anwendung die exklusive Kontrolle über die Grafikhardware. Dies ist nützlich für Anwendungen wie Spiele oder möglicherweise Vollbildvideoanwendungen. Normalerweise erstellt die VMR die DirectDraw-Objekte und legt die kooperative Ebene auf normal fest. Um die VMR jedoch im exklusiven DirectDraw-Modus auszuführen, muss die Anwendung selbst das DirectDraw-Objekt und die primäre Oberfläche erstellen und **SetCooperativeLevel** aufrufen, um den exklusiven Modus anzugeben.

Die VMR verfügt über einen speziellen Allocator-Presenter, mit dem sie im exklusiven DirectDraw-Modus ausgeführt werden kann. So konfigurieren Sie die VMR für die Verwendung dieses Allocator-Presenters:

1.  Erstellen Sie den filter-Graph, und fügen Sie ihm die VMR mithilfe der [**IFilterGraph::AddFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) hinzu. Ein Codebeispiel finden Sie unter [VMR-Fensterloser Modus.](vmr-windowless-mode.md)
2.  Erstellen Sie allocator-presenter im exklusiven Modus:
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  Konfigurieren Sie den neuen allocator-presenter:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Schließen Sie die neue allocator-presenter in die VMR ein.
5.  Erstellen Sie den Rest des Filterdiagramms auf die übliche Weise.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VMR-Betriebsmodi](vmr-modes-of-operation.md)
</dt> </dl>

 

 



