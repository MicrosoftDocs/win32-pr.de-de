---
title: Allgemeine Portierungsrichtlinien
description: Das Portieren von 32-Bit-Anwendungen auf 64-Bit-Microsoft Windows ist einfacher als das Portieren von 16-Bit-Anwendungen in 32-Bit-Windows. Die Verschiebung verläuft jedoch mit einer sorgfältigen Planung reibungsloser. Im Folgenden sind einige allgemeine Richtlinien enthalten.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- Portieren von 32-Bit-Anwendungen auf 64-Bit-Windows 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmierhandbuch 64-Bit-Windows Programmieren, Portierungsrichtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a586318ecc6ec8852077052cbcff41bffacff6c35c36d23de4b020ce19f12af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680240"
---
# <a name="general-porting-guidelines"></a>Allgemeine Portierungsrichtlinien

Das Portieren von 32-Bit-Anwendungen auf 64-Bit-Microsoft Windows ist einfacher als das Portieren von 16-Bit-Anwendungen in 32-Bit-Windows. Die Verschiebung verläuft jedoch mit einer sorgfältigen Planung reibungsloser. Im Folgenden sind einige allgemeine Richtlinien enthalten.

## <a name="planning"></a>Planung

-   Bestimmen Sie die Größe des Aufwands, der für den Port erforderlich ist. Messen Sie, wie viel Arbeit erforderlich ist, indem Sie die folgenden Elemente identifizieren:
    -   Problem mit 32-Bit-Code. Kompilieren Sie Ihren 32-Bit-Code mit dem 64-Bit-Compiler, und untersuchen Sie das Ausmaß der Fehler und Warnungen.
    -   Freigegebene Komponenten oder Abhängigkeiten. Bestimmen Sie, welche Komponenten in Ihrer Anwendung von anderen Teams stammen und ob diese Teams planen, 64-Bit-Versionen ihres Codes zu entwickeln.
    -   Legacy- oder Assemblycode. 16-Bit-Windows-basierte Anwendungen werden nicht auf 64-Bit-Windows ausgeführt und müssen neu geschrieben werden. Während x86-Assemblycode in WOW64 ausgeführt wird, können Sie diesen Code umschreiben, um die Geschwindigkeit der Intel Itanium-Architektur zu nutzen.
-   Portiert die gesamte Anwendung, nicht nur Teile davon.

    Obwohl es möglich ist, Teile einer Anwendung zu porten oder Code mit /LARGEADDRESSAWARE:NO auf 2G zu beschränken, handelt diese Strategie kurzfristigen Gewinn gegen langfristige Probleme.

    > [!Note]  
    > /LARGEADDRESSAWARE:NO wird für eine ARM64-Binärdatei ignoriert.

     

-   Suchen Sie nach Ersatztechnologien, die nicht portiert werden.

    Einige Technologien, einschließlich DAO (Data Access Object) und der Jet Red-Datenbank-Engine, werden nicht auf 64-Bit-Windows portiert.

-   Behandeln Sie Ihre 64-Bit-Version als separate Produktversion.

    Auch wenn Ihr 64-Bit-Produkt die gleiche Codebasis wie Ihr 32-Bit-Produkt nutzen kann, sind zusätzliche Tests erforderlich, und möglicherweise sind weitere Überlegungen zur Veröffentlichung erforderlich.

## <a name="development"></a>Entwicklung

-   Beginnen Sie jetzt mit der Entwicklung von kompatiblem Code.

    Entwickler können mit dem Schreiben von kompatiblem Code beginnen, indem sie die neuesten Windows Headerdateien und die neuen Datentypen ohne negative Auswirkungen auf die 32-Bit-Produktentwicklung verwenden. Weitere Informationen finden Sie unter [Getting Ready for 64-Bit Windows](getting-ready-for-64-bit-windows.md).

-   Stellen Sie sicher, dass Ihr Code sowohl für 32- als auch für 64-Bit-Windows kompiliert werden kann.

    Das neue Datenmodell wurde so konzipiert, dass 32- und 64-Bit-Anwendungen aus einer einzelnen Codebasis mit wenigen Änderungen erstellt werden können. Die Entwicklungsteams für SQL Server und Windows entwickeln 32- und 64-Bit-Versionen ihrer Produkte aus derselben Codebasis.

-   Verwenden Sie die neuen Optimierungsfeatures des Compilers, um eine optimale Leistung zu erzielen.

    Codeoptimierung für Intel Itanium-Prozessoren ist wichtiger als für x86. Der Compiler geht von vielen Optimierungsfunktionen aus, die zuvor vom Mikroprozessor verarbeitet wurden. Sie können die Leistung einer 64-Bit-Anwendung maximieren, indem Sie zwei neue Optimierungsfeatures des Compilers verwenden: *Profilgesteuerte Optimierung* und Optimierung des *gesamten Programms.* Beide Features führen zu längeren Buildzeiten und erfordern die frühe Entwicklung guter Testszenarien.

    *Die profilgesteuerte Optimierung* umfasst einen zweistufigen Kompilierungsprozess. Während der ersten Kompilierung wird der Code instrumentiert, um das Ausführungsverhalten zu erfassen. Diese Informationen werden während der zweiten Kompilierung verwendet, um alle Optimierungsfeatures zu steuern.

    *Die Optimierung* des gesamten Programms analysiert den Code in allen Anwendungsdateien, nicht nur in einer einzigen. Dieser Ansatz erhöht die Leistung auf verschiedene Weise, einschließlich besserem Inlining sowie verbesserter Nebeneffektanalyse und benutzerdefinierten Aufrufkonventionen.

## <a name="testing"></a>Testen

-   Bestimmen Sie, ob Sie 64- oder 32-Bit-Code testen, der in WOW64 ausgeführt wird.

    Einige Anwendungen enthalten sowohl nativen 64-Bit-Code als auch 32-Bit-Code, der in WOW64 ausgeführt wird. Untersuchen Sie dies beim Entwickeln eines Testplans genau, und entscheiden Sie, ob Ihre Testtools 64-Bit, 32-Bit oder eine Kombination sein sollen. Häufig müssen Sie die 64- und 32-Bit-Versionen Ihrer Anwendung auf 64-Bit-Windows testen.

-   Testen sie häufig verwendete 32-Bit-Komponenten.

    Kompilieren Sie zunächst Ihren Code erneut in 64-Bit, und testen Sie den Code. Beheben Sie zweitens Probleme, kompilieren Sie sie in 32 Bits neu, und testen Sie dann. Drittens: Kompilieren Sie die Kompilierung in 64-Bit neu, und testen Sie sie.

-   Testen sie COM- und RPC-Komponenten.

    Stellen Sie sicher, dass sowohl 32- als auch 64-Bit-COM- und RPC-Komponenten ordnungsgemäß kommunizieren. Möglicherweise müssen Sie auch die Kommunikation mit 16-Bit-Komponenten über ein Netzwerk testen.

-   Testen Sie Ihre 32-Bit-Version mit 64-Bit-Windows.

    Kunden können weiterhin 32-Bit-Anwendungen auf 64-Bit-Windows verwenden, bei denen Leistungs- und Arbeitsspeicherprobleme keine wichtigen Überlegungen sind.

-   Testen Sie verschiedene Speicherkonfigurationen.

    Das Hinzufügen großer Mengen an Arbeitsspeicher auf dem Server macht manchmal zuvor unbemerkte Probleme in der Anwendung oder im Betriebssystem verfügbar.

 

 




