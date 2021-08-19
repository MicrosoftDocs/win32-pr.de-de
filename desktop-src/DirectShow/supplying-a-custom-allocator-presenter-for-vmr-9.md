---
description: Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e5f87aaecf0b2e8576b60a2d0f6a8c74e60fcf0759a123015ded9136c079bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951719"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9

Führen Sie die folgenden Schritte aus, um einen benutzerdefinierten Allocator-Presenter mit dem Filter Video Mixing Renderer 9 (VMR-9) zu verwenden:

1.  Implementieren Sie eine Klasse, die die Schnittstellen [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) und [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) unterstützt.
2.  Rufen Sie **QueryInterface** für den VMR-9-Filter für die [**IVMRFilterConfig9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) auf.
3.  Rufen Sie die [**IVMRFilterConfig9::SetRenderingMode-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) auf, und übergeben Sie das **FLAG VMR9Mode \_ Renderless.**
4.  **QueryInterface** für den VMR-9-Filter für die [**IVMRSurfaceAllocatorNotify9-Schnittstelle.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9)
5.  Rufen Sie die [**IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) auf, und übergeben Sie einen Zeiger auf die [**IVMRSurfaceAllocator9-Methode**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) Ihres Allocator-Presenters.
6.  Rufen Sie die [**IVMRSurfaceAllocator9::AdviseNotify-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) Ihres Allocator-Presenters auf, und übergeben Sie einen Zeiger auf die [**IVMRSurfaceAllocatorNotify9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) des VMR-9-Filters.
7.  Rufen Sie in Ihrer Implementierung von [**IVMRSurfaceAllocator9::AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) [**IVMRSurfaceAllocatorNotify9::SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) einen Zeiger auf das Direct3D-Gerät und ein Handle für den Monitor an, auf dem das Video angezeigt wird.
8.  Erstellen Sie in ihrer Implementierung der [**IVMRSurfaceAllocator9::InitializeDevice-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) Direct3D-Oberflächen, die den in der **InitializeDevice-Methode** angegebenen Parametern entsprechen. Optional können Sie die [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) des VMR-9-Filters verwenden, um diese Oberflächen zuzuordnen. Store die Oberflächenzeiger in einem Array.
    > [!Note]  
    > Wenn die Videoframes von VMR-9 auf eine Texturoberfläche gezeichnet werden sollen, fügen Sie der [**VMR9AllocationInfo-Struktur**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) das Flag **VMR9AllocFlag \_ TextureSurface** hinzu. Wenn das Gerät keine Texturen im nativen Videoformat unterstützt, müssen Sie möglicherweise eine separate Texturoberfläche erstellen und dann die Videoframes von der Videooberfläche in die Textur kopieren.

     

9.  Während des Streamings ruft vmR-9 Oberflächen vom allocator-presenter ab, indem die [**IVMRSurfaceAllocator9::GetSurface-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) aufgerufen wird. DIE VMR-9 gibt die Oberfläche nach ihrem Index im Surface-Array an (Schritt 8).
10. Zeigen Sie das Image an, wenn VMR-9 die [**IVMRImagePresenter9::P resentImage-Methode aufruft.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) Die Parameter enthalten einen Zeiger auf die Direct3D-Oberfläche, die das Videobild enthält.
11. Wenn das Direct3D-Gerät zu einem beliebigen Zeitpunkt verloren geht, muss der Allocator-Presenter das Gerät wiederherstellen und die Oberflächen neu erstellen. Beispielsweise kann das Gerät verlorengehen, wenn sich der Anzeigemodus ändert oder der Benutzer das Fenster auf einen anderen Monitor verschiebt. Wenn sich das Direct3D-Gerät ändert, rufen Sie die [**IVMRSurfaceAllocatorNotify9::ChangeD3DDevice-Methode des VMR-9-Filters**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) auf.
12. Wenn das Streaming beendet wird, ruft VMR-9 die [**IVMRSurfaceAllocator9::TerminateDevice-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) auf. Der Allocator-Presenter sollte alle Direct3D-Ressourcen freigeben.

Es gibt einige Unterschiede zwischen VMR-7 und VMR-9 in der Art und Weise, wie benutzerdefinierte Allocator-Presenter verwaltet werden:

-   Die [**AllocateSurfaceHelper-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) des VMR-9-Filters ist für den Allocator-Presenter verfügbar, der beim Zuordnen von Oberflächen verwendet werden kann. Diese Methode macht es für einen benutzerdefinierten Allocator-Presenter überflüssig, Aufrufe an die Standardzuweisungs-Presenter-Methode weiterzuleiten. Aus diesem Grund wird die CLSID des Standardzuweisungs-Presenters des VMR-9-Filters nicht veröffentlicht.
-   Im Gegensatz zu VMR-7 bietet VMR-9 keine spezielle Zuweisung im exklusiven DirectDraw-Modus allocator-presenter. Die [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) macht dieses Objekt überflüssig.
-   Bei Interlacingvideos wird das Video von VMR-9 immer getrennt, bevor es das Image präsentiert. Der Allocator-Presenter ist nicht mehr für das De-Interlacing des Bilds verantwortlich, bevor es angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VMR Renderless Playback Mode (Custom Allocator-Presenters)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



