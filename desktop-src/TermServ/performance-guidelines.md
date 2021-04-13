---
title: Leistungsrichtlinien
description: Richtlinien für die Entwicklung von Anwendungen, die in einer Remotedesktopdienste Umgebung eine gute Leistung erbringen.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388727"
---
# <a name="performance-guidelines"></a>Leistungsrichtlinien

In den folgenden Abschnitten finden Sie Richtlinien zum Entwickeln von Anwendungen, die in einer Remotedesktopdienste Umgebung eine gute Leistung bieten.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Grafische Effekte](graphic-effects.md)
</dt> <dd>

Eine Liste der Funktionen, die beim Ausführen als Remote Sitzung in einer Remotedesktopdienste Umgebung deaktiviert werden sollten.

</dd> <dt>

[Richtlinien für Hintergrundaufgaben in Remotedesktopdienste](background-tasks.md)
</dt> <dd>

Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben bei der Ausführung in einer Remotedesktopdienste Umgebung, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.

</dd> <dt>

[Verwendung von Threads](thread-usage.md)
</dt> <dd>

Sie sollten die Anwendungs Thread Verwendung für eine mehr Benutzer-, multiprozessorRemotedesktopdienste Umgebung optimieren und ausgleichen.

</dd> <dt>

[Erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md)
</dt> <dd>

Um die Leistung zu optimieren, empfiehlt es sich, Anwendungen zu erkennen, ob Sie in einer Remotedesktopdienste Client Sitzung ausgeführt werden.

</dd> </dl>

Überprüfen Sie die Anwendung auf Speicher Verluste, und beheben Sie etwaige Probleme. Dies ist natürlich ein guter Rat für jede Anwendung, aber in einer Remotedesktopdienste Umgebung kann eine Anwendung mehrmals von mehreren Benutzern ausgeführt werden, wodurch die Auswirkungen eines Speicherlecks schnell vergrößert werden.

Animationen, große Bilder, Audiodaten und andere bandbreitenintensive Dienste müssen konfiguriert werden können. Wenn diese Dienste nicht die primäre Funktion sind, können Sie für Remote Sitzungen standardmäßig deaktiviert sein. Sie können jedoch aktiviert werden, wenn eine Sitzung lokal oder über eine Verbindung mit hoher Bandbreite ausgeführt wird. Wenn der Zweck einer Anwendung darin besteht, Dienste mit hoher Bandbreite (z. b. Streaming-Videoübertragungen) bereitzustellen, muss der Dienst nicht standardmäßig deaktiviert sein.

 

 




