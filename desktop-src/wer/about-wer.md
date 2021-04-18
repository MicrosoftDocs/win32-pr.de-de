---
title: Informationen zu wer
description: Windows-Fehlerberichterstattung (wer) ist eine flexible ereignisbasierte Feedback Infrastruktur, die für die Erfassung von Informationen zu den Hardware-und Softwareproblemen konzipiert ist, die von Windows erkannt werden können, die Informationen an Microsoft zu melden und Benutzern alle verfügbaren Lösungen bereitzustellen. Informationen zu den Verbesserungen an wer finden Sie unter What es New in Wer.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Windows-Fehlerberichterstattung für die Windows-Fehlerberichterstattung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310492"
---
# <a name="about-wer"></a>Informationen zu wer

Windows-Fehlerberichterstattung (wer) ist eine flexible ereignisbasierte Feedback Infrastruktur, die für die Erfassung von Informationen zu den Hardware-und Softwareproblemen konzipiert ist, die von Windows erkannt werden können, die Informationen an Microsoft zu melden und Benutzern alle verfügbaren Lösungen bereitzustellen. Informationen zu den Verbesserungen an wer finden Sie unter [What es New in Wer](what-s-new-in-wer.md).

Ab Windows Vista stellt Windows Absturz-, nicht-Antwort-und Kernel Fehler-Fehlerberichterstattung standardmäßig bereit, ohne dass Änderungen an der Anwendung erforderlich sind. Anwendungen verwenden stattdessen die wer-API, um Fehlerberichte für anwendungsspezifische Probleme zu generieren, die nicht mit Abstürzen, nicht-Antworten oder Kernel Fehlern zusammenhängen.

Um Fehlerberichte für anwendungsspezifische Probleme zu generieren, muss die Anwendung eine kurze Beschreibung des Problems mithilfe einiger grundlegender Informationen erstellen, die als *Berichts Parameter* bezeichnet werden. Berichts Parameter enthalten Informationen wie den Anwendungsnamen, die Anwendungs Version, den Modulnamen, die Modulversion und den Fehlercode. Durch die Kombination dieser Berichts Parameter wird ein eindeutiges Problem beschrieben.

Wenn wer auf eine Lösung prüft, kommuniziert er mit dem wer-Server bei Microsoft, indem er zunächst fragt, ob das Problem bereits bekannt ist. Der Server antwortet auf eine der folgenden Arten:

-   Wenn das Problem bekannt ist und eine Lösung vorhanden ist, sendet der Server die Lösung an den Client Computer, und wer zeigt diese Informationen dem Benutzer an.
-   Wenn das Problem untersucht wird, sendet der Server möglicherweise eine Antwort, die den Status angibt. Wenn der Entwickler Weitere Informationen benötigt, um das Problem zu beheben, fordert der Server zusätzliche Informationen von wer an und fordert den Benutzer auf, die Berechtigung zum Senden dieser Informationen zu erhalten.
-   Wenn das Problem nicht bekannt ist, erstellt der Server ein Problem, das ein Entwickler untersuchen und eine Antwort sendet, die den Status angibt.

Wenn Sie diesen Prozess verwenden, sammelt er bei Bedarf weitere Informationen oder sendet eine Lösung an den Benutzer, sofern verfügbar. Unter Windows Vista kann der Benutzer jederzeit zu **Problem berichten und-Lösungen** wechseln, um verfügbare Lösungen anzuzeigen, zu überprüfen, ob neue Lösungen verfügbar sind, oder andere wer-Berichte und-Einstellungen verwalten. Unter Windows 7 werden die **Problem Berichte und-Lösungen** jetzt als " **Aktions Center**" bezeichnet. Klicken Sie auf **Start** , und geben Sie "View" in **Programme/Dateien durchsuchen** ein, und wählen Sie dann **Alle Problemberichte anzeigen**, **Zuverlässigkeits Verlauf anzeigen** oder **Lösungen für Probleme anzeigen** aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Fehlerberichterstattung](windows-error-reporting.md)
</dt> </dl>

 

 




