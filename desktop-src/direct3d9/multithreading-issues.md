---
description: Vollbild Direct3D-Anwendungen stellen ein Fenster Handle für die Direct3D-Laufzeit bereit.
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: Probleme beim Multithreading (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d163698e6cc1b4855668d255ed46fd28700d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392425"
---
# <a name="multithreading-issues-direct3d-9"></a>Probleme beim Multithreading (Direct3D 9)

Vollbild Direct3D-Anwendungen stellen ein Fenster Handle für die Direct3D-Laufzeit bereit. Das Fenster wird von der Laufzeit angehängten. Dies bedeutet, dass alle Nachrichten, die an die Fenster Nachrichten Prozedur der Anwendung übermittelt wurden, zuerst von der eigenen Nachrichten Behandlung der Direct3D-Laufzeit untersucht wurden.

Änderungen im Anzeigemodus sind von in das zugrunde liegenden Betriebssystem integrierten Unterstützungs Routinen betroffen. Wenn Modusänderungen auftreten, überträgt das System mehrere Nachrichten an alle Anwendungen. In Direct3D-Anwendungen werden die Nachrichten im Fenster Prozedur Thread empfangen, bei dem es sich nicht unbedingt um denselben Thread handelt, der " [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) " oder " [**IDirect3D9:: foratedevice**](/windows/desktop/api) " aufgerufen hat (oder die endgültige Version von [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9), was zu einer Änderung des Anzeigemodus führen kann). Die Direct3D-Laufzeit verwaltet mehrere kritische Abschnitte intern. Da mindestens einer dieser kritischen Abschnitte über den von **IDirect3DDevice9:: Reset** oder **IDirect3D9:: kreatedevice** verursachten Modusschalter hinweg gehalten wird, werden diese kritischen Abschnitte weiterhin beibehalten, wenn die Anwendung die Fenster Meldungen im Fenstermodus-Änderungen empfängt.

Dieser Entwurf hat einige Auswirkungen auf Multithreadanwendungen. Insbesondere muss eine Anwendung sicher sein, dass Ihre Fenster Meldungs Behandlungs Threads von ihren Direct3D-Threads stark getrennt werden. Eine Anwendung, die eine Modusänderung in einem Thread bewirkt, aber Direct3D-Aufrufe in einem anderen Thread in der Fenster Prozedur durchführt, besteht in der Gefahr eines Deadlocks.

Aus diesen Gründen ist Direct3D so konzipiert, dass die Methoden [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), [**IDirect3D9:: foratedevice**](/windows/desktop/api), [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)oder die endgültige Version von [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) nur aus demselben Thread aufgerufen werden können, der Fenster Meldungen verarbeitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
