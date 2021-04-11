---
description: Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218210"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors

In seltenen Fällen möchten Sie möglicherweise das Video Rendering mit der Aktualisierungsrate des Monitors genau synchronisieren, damit jedes Mal, wenn der Monitor aktualisiert wird, genau ein neuer Frame angezeigt wird. Die zuverlässigste Methode hierfür ist das Erstellen eines benutzerdefinierten zuordcators, der einen Flip-Vorgang anstelle eines Blit-Vorgangs verwendet, um die Video Bits in die primäre Oberfläche zu schreiben. "Kippen" wird bei jeder Aktualisierung des Monitors aufgerufen. wenn der Videostream also keine Zeitstempel enthält, wird der VMR so schnell wie möglich auf die primäre Oberfläche rendern, aber die Oberfläche blockiert den Stream, bis der Flip-Vorgang abgeschlossen ist. Dies bedeutet, dass der nächste Frame immer auf die primäre Oberfläche wartet, wenn der Monitor aktualisiert wird, solange die CPU nicht überlastet ist. Wenn jedoch ein anderer CPU-intensiver Prozess ausgeführt wird, kann es passieren, dass der DirectShow-streamingingthread nicht schnell genug an die primäre Oberfläche geliefert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



