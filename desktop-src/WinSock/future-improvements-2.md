---
description: Zukünftige Verbesserungen am Winsock-Beispielanwendungscode.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Zukünftige Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384d5a4f4ee9a4d6cb4a0f258d63262930dc5a6636be8d0e7f709b0e4f04e152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132363"
---
# <a name="future-improvements"></a>Zukünftige Verbesserungen

Es gibt mehrere Verbesserungen, die an dieser Anwendung vorgenommen werden können, z. B.:

-   Eine einzelne, dauerhafte Verbindung kann von der Anwendung erstellt werden. Eine entsprechende Fehlerbehandlung müsste hinzugefügt werden. Dies würde den Mehraufwand reduzieren, der mit dem Start und der Abschaltung der Verbindung verbunden ist.
-   Der Antwortcode auf dem Server kann optimiert werden, um Antworten zu konsolidieren, wodurch die Anzahl der vom Server gesendeten Pakete reduziert wird.
-   Es können Verbesserungen am Protokoll vorgenommen werden. Beispielsweise könnte eine Updatebitmaske verwendet werden, um zu kennzeichnen, welche Zellen aktualisiert werden sollen und nur diese Zellendaten gesendet werden.
-   Updates können mithilfe verschiedener Threads überlappen, sodass sich das Netzwerk nicht im Leerlauf befindet, während die **ComputeNext-Funktion** ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)
</dt> <dt>

[Baselineversion: Eine Anwendung mit sehr schlechter Leistung](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revision 1: Bereinigen des Offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revision 2: Neugestaltung für weniger Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revision 3: Compressed Block Send](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



