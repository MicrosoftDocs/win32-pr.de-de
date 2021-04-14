---
description: Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568758"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a>Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7

Der Zuweisungs Presenter ist für das Zuordnen von DirectDraw-Oberflächen und das darstellen der Video Frames zum Rendern verantwortlich. In den meisten Szenarios ist die Funktionalität des standardzuordnerpräsentators für die Anforderungen einer Anwendung mehr als ausreichend. Durch das Plug eines benutzerdefinierten zuordnerbildrors kann eine Anwendung jedoch direkten Zugriff auf die Video Bits erhalten und den Renderingprozess vollständig steuern. Der Nachteil dieser verbesserten Leistung besteht darin, dass die Anwendung die zusätzliche Komplexität der DirectDraw-Oberflächen Verwaltung bewältigen muss.

![Verwenden eines benutzerdefinierten zuordcators (Presenter)](images/custom-ap.png)

Die obige Abbildung zeigt die Kommunikationsschnittstellen, die von VMR und der Zuweisung-Presenter verwendet werden. Ein benutzerdefinierter Allocator-Presenter, der alle standardmäßigen Zuordnungs-und Präsentations Funktionen überschreibt, muss die [**ivmrimagepresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) -Schnittstelle und die [**ivmrsurfaceallocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) -Schnittstelle implementieren und optional [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol).

Um den standardzuordnerpräsentator zu ersetzen, ruft eine Anwendung die [**ivmrsurfaceverteilcatornotify:: advisesurfacedepcator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) -Methode auf und übergibt einen Zeiger auf den neuen zuordnerpräsentator. Als Reaktion auf diesen-Befehl ruft der VMR die [**ivmrsurfacedepcator:: advisenotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) -Methode des zugriffspräsentators auf, um den Zeiger auf die [**ivmrsurfaceverteilcatornotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) -Schnittstelle von VMR bereitzustellen. Der zuordnerpresenter verwendet diesen Schnittstellen Zeiger, wenn Ereignisse mit der [**ivmrsurfacezucatornotify:: notifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) -Methode an den VMR übergeben werden.

Als alternative Lösung kann eine Anwendung sowohl Ihren eigenen zuordnerpresenter als auch den standardzuordnerpresenter verwenden. In diesem Szenario verarbeitet der Custom-zuordnerpräsentator nur die Aufrufe, bei denen eine benutzerdefinierte Funktionalität benötigt wird, und übergibt die restlichen Aufrufe von VMR an den standardzuordcator-Presenter. In vielen Fällen ist es nur erforderlich, die [**ivmrimagepresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) -Schnittstelle zu überschreiben.

![Verwenden von zwei zuordnermoderatorpresenter](images/custom-ap2.png)

Um sowohl einen benutzerdefinierten zuordnerpresenter als auch den standardzuordnerpräsentator zu verwenden, ruft eine Anwendung zunächst [**ivmrsurfacedepcatornotify:: advisesurfacedepcator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) auf, um einen Zeiger auf den neuen zuordnerpräsentator bereitzustellen. Dies bewirkt, dass der standardzuordnerpresenter zerstört wird, sodass die Anwendung eine andere Instanz dieser Instanz erstellen muss, indem **QueryInterface** für den VMR aufgerufen und die [**ivmrsurfaceverteilcator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) -Schnittstelle angefordert wird. Wie in der obigen Abbildung gezeigt, überschreibt der Custom- [**zuordnerpräsentator die ivmrimagepresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) -Schnittstellen Methoden und übergibt einfach alle Aufrufe an die **ivmrsurfacediskcator** -Schnittstelle an die Standard Implementierung. Die Abbildung zeigt auch die [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle, die auf der "zuordcator-Presenter" implementiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



