---
title: Multithread-OpenGL-Zeichnungsstrategien
description: Die GDI unterstützt nicht mehrere Threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL auf Windows,Multithread-Zeichnung
- OpenGL-Multithreadzeichnung openGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d928a481e4334f97cad2f7009f008c899ad8378f3fd15cf9e117e6b9599393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937255"
---
# <a name="multithread-opengl-drawing-strategies"></a>Multithread-OpenGL-Zeichnungsstrategien

Die GDI unterstützt nicht mehrere Threads. Sie müssen für jeden Thread einen eindeutigen Gerätekontext und einen eindeutigen Renderingkontext verwenden. Dies schränkt tendenziell die Leistungsvorteile der Verwendung mehrerer Threads mit Einzelprozessorsystemen ein, auf denen OpenGL-Anwendungen ausgeführt werden. Es gibt jedoch Möglichkeiten, Threads mit einem einzelnen Prozessorsystem zu verwenden, um die Leistung deutlich zu steigern. Beispielsweise können Sie einen separaten Thread verwenden, um OpenGL-Renderingaufrufe an dedizierte 3D-Hardware zu übergeben.

Symmetrische Multiprocessingsysteme (SMP) können von der Verwendung mehrerer Threads stark profitieren. Eine offensichtliche Strategie besteht in der Verwendung eines separaten Threads für jeden Prozessor, um OpenGL-Rendering in separaten Fenstern zu verarbeiten. Beispielsweise können Sie in einer Flight-Simulation-Anwendung separate Prozessoren und Threads verwenden, um die Front-, Back- und Seitenansichten zu rendern.

Ein Thread kann nur einen aktuellen, aktiven Renderingkontext haben. Wenn Sie mehrere Threads und mehrere Renderingkontexte verwenden, müssen Sie darauf achten, deren Verwendung zu synchronisieren. Verwenden Sie beispielsweise nur einen Thread, um [**SwapBuffers auf aufruft,**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) nachdem alle Threads das Zeichnen abgeschlossen haben.

 

 




