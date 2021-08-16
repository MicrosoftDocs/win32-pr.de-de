---
title: Multithread-OpenGL-Zeichnungsstrategien
description: Die GDI unterstützt nicht mehrere Threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL für Windows, Multithreadzeichnung
- Multithread-OpenGL-Zeichnung von OpenGL
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

Die GDI unterstützt nicht mehrere Threads. Sie müssen einen unterschiedlichen Gerätekontext und einen eindeutigen Renderingkontext für jeden Thread verwenden. Dies führt dazu, dass die Leistungsvorteile durch die Verwendung mehrerer Threads mit Einzelprozessorsystemen, auf denen OpenGL-Anwendungen ausgeführt werden, eingeschränkt werden. Es gibt jedoch Möglichkeiten, Threads mit einem einzelnen Prozessorsystem zu verwenden, um die Leistung erheblich zu steigern. Beispielsweise können Sie einen separaten Thread verwenden, um OpenGL-Renderingaufrufe an dedizierte 3D-Hardware zu übergeben.

SMP-Systeme (Symmetric Multiprocessing) können von der Verwendung mehrerer Threads erheblich profitieren. Eine offensichtliche Strategie ist die Verwendung eines separaten Threads für jeden Prozessor, um OpenGL-Rendering in separaten Fenstern zu verarbeiten. In einer Flugsimulationsanwendung können Sie beispielsweise separate Prozessoren und Threads verwenden, um die Front-, Back- und Seitenansichten zu rendern.

Ein Thread kann nur einen aktuellen, aktiven Renderingkontext aufweisen. Wenn Sie mehrere Threads und mehrere Renderingkontexte verwenden, müssen Sie darauf achten, ihre Verwendung zu synchronisieren. Verwenden Sie beispielsweise nur einen Thread, um [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) aufzurufen, nachdem alle Threads das Zeichnen abgeschlossen haben.

 

 




