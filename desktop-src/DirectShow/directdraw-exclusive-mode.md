---
description: Exklusiver DirectDraw-Modus
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Exklusiver DirectDraw-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344935"
---
# <a name="directdraw-exclusive-mode"></a>Exklusiver DirectDraw-Modus

> [!Note]  
> Dieses Thema gilt nur für VMR-7. In VMR-9 aktivieren Sie den exklusiven Modus, indem Sie Ihren eigenen exklusiven moduszuordnerpräsentator bereitstellen. Dies ist relativ unkompliziert, wenn Sie die [**IVMRSurfaceAllocatorNotify9:: depingesurfacehelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) -Methode verwenden. Das VMR9Allocator-Beispiel zeigt, wie ein benutzerdefinierter Zuweiser zukator implementiert wird.

 

Im exklusiven DirectDraw-Modus übernimmt eine Anwendung die exklusive Kontrolle über die Grafikhardware. Dies ist nützlich für Anwendungen, wie z. b. Spiele oder für Vollbild-Videoanwendungen. Normalerweise erstellt VMR die DirectDraw-Objekte und legt die kooperative Ebene auf Normal fest. Um jedoch VMR im exklusiven DirectDraw-Modus auszuführen, muss die Anwendung selbst das DirectDraw-Objekt und die primäre Oberfläche erstellen und **setkooperativelevel** aufrufen, um den exklusiven Modus anzugeben.

VMR verfügt über einen speziellen zuordnerpräsentator, der es ermöglicht, im exklusiven DirectDraw-Modus auszuführen. So konfigurieren Sie VMR für die Verwendung dieses zuordnerstellers:

1.  Erstellen Sie das Filter Diagramm, und fügen Sie das VMR mithilfe der [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode hinzu. Ein Codebeispiel finden Sie unter [VMR (fensterlose Modus](vmr-windowless-mode.md)).
2.  Erstellen Sie den exklusiven Modus "zuordcator-Presenter":
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

    

3.  Konfigurieren Sie den neuen zuordcator-Presenter:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Verbinden Sie die neue Zuweisung-Presenter mit der VMR.
5.  Erstellen Sie den Rest des Filter Diagramms auf die übliche Weise.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VMR-Betriebsmodi](vmr-modes-of-operation.md)
</dt> </dl>

 

 



