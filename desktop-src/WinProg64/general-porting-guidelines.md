---
title: Allgemeine Richtlinien für die Portierung
description: Das Portieren von 32-Bit-Anwendungen auf 64-Bit-Microsoft Windows ist einfacher als das Portieren von 16-Bit-Anwendungen auf 32-Bit-Windows. Die Verschiebung wird jedoch mit einer sorgfältigen Planung reibungslos verlaufen. Im folgenden finden Sie einige allgemeine Richtlinien.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- Portieren von 32-Bit-Anwendungen auf eine 64-Bit-Windows 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Portieren von Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "104218926"
---
# <a name="general-porting-guidelines"></a>Allgemeine Richtlinien für die Portierung

Das Portieren von 32-Bit-Anwendungen auf 64-Bit-Microsoft Windows ist einfacher als das Portieren von 16-Bit-Anwendungen auf 32-Bit-Windows. Die Verschiebung wird jedoch mit einer sorgfältigen Planung reibungslos verlaufen. Im folgenden finden Sie einige allgemeine Richtlinien.

## <a name="planning"></a>Planung

-   Legen Sie die Größe des erforderlichen Aufwands für den Port fest. Messen Sie, wie viel Arbeit beteiligt ist, indem Sie die folgenden Elemente identifizieren:
    -   Problem 32-Bit-Code. Kompilieren Sie Ihren 32-Bit-Code mit dem 64-Bit-Compiler, und untersuchen Sie das Ausmaß der Fehler und Warnungen.
    -   Freigegebene Komponenten oder Abhängigkeiten. Bestimmen Sie, welche Komponenten in der Anwendung von anderen Teams stammen und ob diese Teams beabsichtigen, 64-Bit-Versionen Ihres Codes zu entwickeln.
    -   Legacy-oder Assemblycode. Windows-basierte 16-Bit-Anwendungen können nicht auf 64-Bit-Fenstern ausgeführt werden und müssen umgeschrieben werden. Während der x86-Assemblycode in WOW64 ausgeführt wird, können Sie diesen Code umschreiben, um die Geschwindigkeit der Intel Itanium-Architektur zu nutzen.
-   Portieren Sie die gesamte Anwendung, nicht nur Teile davon.

    Obwohl es möglich ist, Teile einer Anwendung zu portieren oder Code auf 2G mit/LARGEADDRESSAWARE: No einzuschränken, stellt diese Strategie kurzfristigen Aufwand für langfristige Probleme dar.

    > [!Note]  
    > /LARGEADDRESSAWARE: No wird für eine ARM64-Binärdatei ignoriert.

     

-   Suchen Sie Ersatz für Technologien, die nicht portiert werden.

    Einige Technologien, einschließlich DAO (Datenzugriffs Objekt) und der Jet Red Database Engine, werden nicht in 64-Bit-Windows portiert.

-   Behandeln Sie Ihre 64-Bit-Version als separate Produktversion.

    Auch wenn Ihr 64-Bit-Produkt die gleiche Codebasis wie Ihr 32-Bit gemeinsam nutzen kann, sind zusätzliche Tests erforderlich, und es können weitere Überlegungen zur Version vorliegen.

## <a name="development"></a>Entwicklung

-   Beginnen Sie jetzt mit der Entwicklung von kompatibler Code

    Entwickler können mit dem Schreiben von kompatibler Code beginnen, indem Sie die neuesten Windows-Header Dateien und die neuen Datentypen ohne negative Auswirkungen auf die 32-Bit-Produktentwicklung verwenden. Weitere Informationen finden Sie unter Vorbereiten [für 64-Bit-Windows](getting-ready-for-64-bit-windows.md).

-   Stellen Sie sicher, dass Ihr Code für 32-und 64-Bit-Fenster kompiliert werden kann.

    Das neue Datenmodell war so konzipiert, dass 32-und 64-Bit-Anwendungen aus einer einzelnen Codebasis mit wenigen Änderungen erstellt werden können. Das SQL Server-und das Windows-Entwicklungsteam entwickeln 32-und 64-Bit-Versionen ihrer Produkte aus der gleichen Codebasis.

-   Verwenden Sie die neuen Optimierungs Features des Compilers, um optimale Leistung zu erzielen.

    Die Code Optimierung für Intel Itanium-Prozessoren ist wichtiger als bei x86. Der Compiler geht von vielen der Optimierungs Funktionen aus, die zuvor vom Mikroprozessor verarbeitet wurden. Sie können die Leistung einer 64-Bit-Anwendung maximieren, indem Sie zwei neue Optimierungs Features des Compilers verwenden: *Profil gesteuerte Optimierung* und *Optimierung des gesamten Programms*. Beide Features führen zu längeren Buildzeiten und erfordern die frühe Entwicklung von guten Testszenarien.

    Die *Profil gesteuerte Optimierung* umfasst einen zweistufigen Kompilierungs Vorgang. Während der ersten Kompilierung wird der Code instrumentiert, um das Ausführungs Verhalten aufzuzeichnen. Diese Informationen werden während der zweiten Kompilierung verwendet, um alle Optimierungs Features zu unterstützen.

    Die *Optimierung des gesamten Programms* analysiert den Code in allen Anwendungs Dateien, nicht nur eine einzige. Diese Vorgehensweise erhöht die Leistung auf verschiedene Weise, z. a. eine bessere Inlining sowie verbesserte Nebeneffekte und benutzerdefinierte Aufruf Konventionen.

## <a name="testing"></a>Test

-   Bestimmen Sie, ob Sie 64-oder 32-Bit-Code testen, der in WOW64 ausgeführt wird.

    Einige Anwendungen enthalten sowohl systemeigenen 64-Bit-Code als auch 32-Bit-Code, der in WOW64 ausgeführt wird. Untersuchen Sie dies sehr gut, während Sie einen Testplan entwickeln, und entscheiden Sie, ob Ihre TestTools 64-Bit, 32-Bit oder eine Kombination sein sollten. Sie müssen häufig sowohl die 64-als auch die 32-Bit-Version der Anwendung auf 64-Bit-Windows testen.

-   Testen Sie häufig verwendete 32-Bit-Komponenten.

    Kompilieren Sie zunächst den Code in 64-Bit neu, und testen Sie. Zum anderen beheben Sie Probleme, kompilieren Sie in 32 Bits neu, und testen Sie dann. Als dritte Neukompilierung in 64-Bit und testen.

-   Testen Sie die com-und RPC-Komponenten.

    Stellen Sie sicher, dass die com-und RPC-Komponenten 32-und 64-Bit ordnungsgemäß kommunizieren. Sie müssen möglicherweise auch die Kommunikation mit 16-Bit-Komponenten über ein Netzwerk testen.

-   Testen Sie Ihre 32-Bit-Version auf 64-Bit-Fenstern.

    Kunden können weiterhin 32-Bit-Anwendungen auf 64-Bit-Windows verwenden, bei denen Leistungs-und Arbeitsspeicher Probleme keine wichtigen Aspekte sind.

-   Testen Sie verschiedene Speicherkonfigurationen.

    Wenn Sie große Mengen an Arbeitsspeicher auf dem Server hinzufügen, werden in der Anwendung oder im Betriebssystem manchmal nicht aufmerkte Probleme angezeigt.

 

 




