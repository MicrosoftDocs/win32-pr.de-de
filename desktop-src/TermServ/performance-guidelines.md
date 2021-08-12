---
title: Leistungsrichtlinien
description: Richtlinien für die Entwicklung von Anwendungen, die in einer Remotedesktopdienste-Umgebung gut funktionieren.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a8211f12e4a89c5dfb309bb4e3c0f998159738b46185aeb5dcee7a5cd29f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605312"
---
# <a name="performance-guidelines"></a>Leistungsrichtlinien

Die folgenden Abschnitte enthalten Richtlinien für die Entwicklung von Anwendungen, die in einer Remotedesktopdienste-Umgebung gut funktionieren.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Grafische Effekte](graphic-effects.md)
</dt> <dd>

Eine Liste der Features, die deaktiviert werden sollten, wenn sie als Remotesitzung in einer Remotedesktopdienste-Umgebung ausgeführt werden.

</dd> <dt>

[Richtlinien für Hintergrundaufgaben in Remotedesktopdienste](background-tasks.md)
</dt> <dd>

Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben, wenn sie in einer Remotedesktopdienste-Umgebung ausgeführt werden, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.

</dd> <dt>

[Verwendung von Threads](thread-usage.md)
</dt> <dd>

Sie sollten die Verwendung von Anwendungsthreads für eine Multiuser-, Multiprozessor- Remotedesktopdienste-Umgebung optimieren und ausgleichen.

</dd> <dt>

[Erkennen der Remotedesktopdienste-Umgebung](detecting-the-terminal-services-environment.md)
</dt> <dd>

Um die Leistung zu optimieren, ist es eine bewährte Methode für Anwendungen, zu erkennen, ob sie in einer Remotedesktopdienste Clientsitzung ausgeführt werden.

</dd> </dl>

Überprüfen Sie Ihre Anwendung auf Speicherverluste, und beheben Sie alle Probleme. Dies ist natürlich ein guter Rat für jede Anwendung, aber in einer Remotedesktopdienste Umgebung kann eine Anwendung mehrmals von mehreren Benutzern ausgeführt werden, wodurch die Auswirkungen eines Speicherverlusts schnell vergrößert werden.

Animationen, große Bilder, Audio und andere bandbreitenintensive Dienste müssen konfigurierbar sein. Wenn diese Dienste nicht die primäre Funktion sind, können sie standardmäßig für Remotesitzungen deaktiviert sein, aber aktiviert, wenn eine Sitzung lokal oder über eine Verbindung mit hoher Bandbreite ausgeführt wird. Wenn der Zweck einer Anwendung darin besteht, Dienste mit hoher Bandbreite bereitzustellen, z. B. Streamingvideoübertragungen, muss der Dienst standardmäßig nicht deaktiviert sein.

 

 




