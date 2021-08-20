---
title: COM-Clients und -Server
description: Ein wichtiger Aspekt von COM ist die Interaktion zwischen Clients und Servern.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d189b464c8e3a32ff378951067275ab29f5fbabc0b2777c2b2226d632a8bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048658"
---
# <a name="com-clients-and-servers"></a>COM-Clients und -Server

Ein wichtiger Aspekt von COM ist die Interaktion zwischen Clients und Servern. Ein *COM-Client* ist der Code oder das Objekt, der einen Zeiger auf einen COM-Server erhält und seine Dienste verwendet, indem er die Methoden seiner Schnittstellen aufruft. Ein *COM-Server* ist ein beliebiges Objekt, das Dienste für Clients bietet. Diese Dienste werden in Form von COM-Schnittstellenimplementierungen verwendet, die von jedem Client aufgerufen werden können, der einen Zeiger auf eine der Schnittstellen im Serverobjekt erhalten kann.

Es gibt zwei Haupttypen von Servern: *In-Process* und *Out-of-Process.* Prozessin-Process-Server werden in einer DLL (Dynamic Linked Library) implementiert, und Out-of-Process-Server werden in einer ausführbaren Datei (EXE) implementiert. Out-of-Process-Server können sich entweder auf dem lokalen Computer oder auf einem Remotecomputer befinden. Darüber hinaus bietet COM einen Mechanismus, der es einem Prozessserver (einer DLL) ermöglicht, in einem EXE-Ersatzprozess ausgeführt zu werden, um den Vorteil zu erhalten, dass der Prozess auf einem Remotecomputer ausgeführt werden kann. Weitere Informationen finden Sie unter [DLL-Ersatzzeichen.](dll-surrogates.md)

Das COM-Programmiermodell und die Konstrukte wurden nun erweitert, sodass COM-Clients und -Server nicht nur auf einem bestimmten Computer, sondern auch über das Netzwerk zusammenarbeiten können. Dies ermöglicht vorhandenen Anwendungen die Interaktion mit neuen Anwendungen und miteinander über Netzwerke hinweg mit ordnungsgemäßer Verwaltung, und neue Anwendungen können geschrieben werden, um netzwerkfeatures zu nutzen.

COM-Clientanwendungen müssen nicht wissen, wie Serverobjekte gepackt werden, unabhängig davon, ob sie als In-Process-Objekte (in DLLs) oder als lokale oder Remoteobjekte (in EXEs) gepackt sind. Verteiltes COM ermöglicht darüber hinaus das Packen von Objekten als Dienstanwendungen und synchronisiert COM mit den vielfältigen Verwaltungs- und Systemintegrationsfunktionen Windows.

> [!Note]  
> In dieser Dokumentation wird das Akronym COM vor DCOM verwendet. Dies liegt daran, dass DCOM nicht getrennt ist. Es handelt sich lediglich um COM mit einer längeren Leitung. In Fällen, in denen es sich bei der beschreibung speziell um einen Remotevorgang handelt, wird der Begriff *verteiltes COM* verwendet.

 

COM ist so konzipiert, dass es möglich ist, die Unterstützung für Standorttransparenz hinzuzufügen, die sich über ein Netzwerk erstreckt. Es ermöglicht anwendungen, die für einzelne Computer geschrieben wurden, über ein Netzwerk ausgeführt zu werden, und stellt Features bereit, die diese Funktionen erweitern und die in einem Netzwerk erforderliche Sicherheit erhöhen. (Weitere Informationen finden Sie unter [Sicherheit in COM.)](security-in-com.md)

COM gibt einen Mechanismus an, mit dem der Klassencode von vielen verschiedenen Anwendungen verwendet werden kann.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Abrufen eines Zeigers auf ein Objekt](getting-a-pointer-to-an-object.md)
-   [Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
-   [COM-Serveraufgaben](com-server-responsibilities.md)
-   [Persistenter Objektzustand](persistent-object-state.md)
-   [Bereitstellen von Klasseninformationen](providing-class-information.md)
-   [Objektübergreifende Kommunikation](inter-object-communication.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufsynchronisierung](call-synchronization.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




