---
description: Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f004e119fc1cbfc167c2130852a4f59700706fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369064"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9

Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Zuordnung mit dem Filter Video Mischungs-Renderer 9 (VMR-9) zu verwenden:

1.  Implementieren Sie eine Klasse, die die Schnittstellen [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) und [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) unterstützt.
2.  Ruft **QueryInterface** für den VMR-9-Filter für die [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) -Schnittstelle auf.
3.  Nennen Sie die [**IVMRFilterConfig9:: setrenderingmode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) -Methode, und übergeben Sie das **VMR9Mode \_ Renderless** -Flag.
4.  **QueryInterface** für den VMR-9-Filter für die [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) -Schnittstelle.
5.  Nennen Sie die [**IVMRSurfaceAllocatorNotify9:: advisesurfacezuweisung**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) -Methode, und übergeben Sie einen Zeiger auf die [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) -Methode Ihres Zuordners.
6.  Nennen Sie die [**IVMRSurfaceAllocator9:: advisenotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) -Methode Ihres Zuordners und übergeben Sie einen Zeiger auf die [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) -Schnittstelle des VMR-9-Filters.
7.  Geben Sie in ihrer Implementierung von [**IVMRSurfaceAllocator9:: advisenotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify)den Befehl [**IVMRSurfaceAllocatorNotify9:: SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) Pass an einen Zeiger auf das Direct3D-Gerät und ein Handle für den Monitor an, in dem das Video angezeigt wird.
8.  Erstellen Sie in ihrer Implementierung der [**IVMRSurfaceAllocator9:: initializedevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) -Methode Direct3D-Oberflächen, die den in der **initializedevice** -Methode angegebenen Parametern entsprechen. Optional können Sie die [**IVMRSurfaceAllocatorNotify9:: alloskiesurfacehelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) -Methode des VMR-9-Filters verwenden, um diese Oberflächen zuzuordnen. Speichert die Oberflächen Zeiger in einem Array.
    > [!Note]  
    > Wenn die Video Frames von VMR-9 auf eine Textur Oberfläche gezeichnet werden sollen, fügen Sie der [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) -Struktur das **VMR9AllocFlag \_ texturesurface** -Flag hinzu. Wenn das Gerät keine Texturen im systemeigenen Videoformat unterstützt, müssen Sie möglicherweise eine separate Textur Oberfläche erstellen und dann die Video Frames von der Video Oberfläche in die Textur kopieren.

     

9.  Während des Streamings ruft VMR-9 Oberflächen aus dem zuordnerpresenter ab, indem die [**IVMRSurfaceAllocator9:: getSurface**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) -Methode aufgerufen wird. VMR-9 gibt die Oberfläche nach dem Index innerhalb des Oberflächen Arrays an (Schritt 8).
10. Präsentieren Sie das Bild, wenn VMR-9 die [**IVMRImagePresenter9::P resentimage**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) -Methode aufruft. Die Parameter enthalten einen Zeiger auf die Direct3D-Oberfläche, die das Video Bild enthält.
11. Wenn das Direct3D-Gerät zu einem beliebigen Zeitpunkt verloren geht, muss der zuordnerpresenter das Gerät wiederherstellen und die Oberflächen neu erstellen. Beispielsweise kann das Gerät verloren gehen, wenn sich der Anzeigemodus ändert oder der Benutzer das Fenster auf einen anderen Monitor verschiebt. Wenn das Direct3D-Gerät geändert wird, wird die [**IVMRSurfaceAllocatorNotify9:: ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) -Methode des VMR-9-Filters aufgerufen.
12. Wenn das Streaming beendet wird, ruft VMR-9 die [**IVMRSurfaceAllocator9:: terminatedevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) -Methode auf. Der Zuweiser-Presenter sollte alle seine Direct3D-Ressourcen freigeben.

Es gibt einige Unterschiede zwischen VMR-7 und VMR-9 in der Art und Weise, wie benutzerdefinierte zuordcator-Moderatoren verwaltet werden:

-   Die [**Zuweisungs Methode "Zuweisungs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) Methode" des VMR-9-Filters ist für die Zuweisung von Oberflächen verfügbar. Diese Methode macht es unnötig, dass ein benutzerdefinierter zuordnerpresenter alle Aufrufe an den standardzuweicator-Presenter weitergibt. Aus diesem Grund wird die CLSID des standardmäßigen "zuordcators-Presenter" des VMR-9-Filters nicht veröffentlicht.
-   Anders als bei VMR-7 bietet VMR-9 keinen speziellen DirectDraw Exclusive Mode-Zuweiser. Mit der [**IVMRSurfaceAllocatorNotify9:: depingesurfacehelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) -Methode ist dieses Objekt unnötig.
-   Bei einem Video mit Zeilen Sprung wird das Video von VMR-9 immer deformatiert, bevor es dargestellt wird. Der zuordnerpräsentator ist nicht mehr für die Deaktivierung des Bilds verantwortlich, bevor es angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



