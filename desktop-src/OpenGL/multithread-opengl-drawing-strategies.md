---
title: Multithread-OpenGL-Zeichnungs Strategien
description: Der GDI unterstützt nicht mehrere Threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL unter Windows, multithreadzeichnung
- Multithread-OpenGL-Zeichen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309792"
---
# <a name="multithread-opengl-drawing-strategies"></a>Multithread-OpenGL-Zeichnungs Strategien

Der GDI unterstützt nicht mehrere Threads. Sie müssen für jeden Thread einen eindeutigen Gerätekontext und einen eindeutigen renderingkontext verwenden. Dadurch werden die Leistungsvorteile der Verwendung mehrerer Threads bei Systemen mit nur einem Prozessor, auf denen OpenGL-Anwendungen ausgeführt werden, eingeschränkt. Es gibt jedoch Möglichkeiten, Threads mit einem einzelnen Prozessor System zu verwenden, um die Leistung erheblich zu steigern. Beispielsweise können Sie einen separaten Thread verwenden, um OpenGL-renderingaufrufe an dedizierte 3D-Hardware zu übergeben.

Symmetrische Multiprozessorsysteme (Symmetric Multiprocessing, SMP) können von der Verwendung mehrerer Threads profitieren. Eine offensichtliche Strategie besteht darin, einen separaten Thread für jeden Prozessor zu verwenden, um das OpenGL-Rendering in separaten Fenstern zu verarbeiten. Beispielsweise können Sie in einer Anwendung für die Flugsimulation separate Prozessoren und Threads verwenden, um die Front-, rückwärts-und Seitenansichten zu erzeugen.

Ein Thread kann nur über einen aktuellen aktiven renderingkontext verfügen. Wenn Sie mehrere Threads und mehrere renderingkontexte verwenden, müssen Sie Ihre Verwendung sorgfältig synchronisieren. Verwenden Sie z. b. nur einen Thread, um " [**Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) " aufzurufen, nachdem alle Threads gezeichnet wurden.

 

 




