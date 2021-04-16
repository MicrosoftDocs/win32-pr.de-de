---
title: Die wichtigsten Tools und Techniken zum Erstellen robuster Windows-Spiele
description: In diesem Artikel werden Tools und Techniken beschrieben, die Sie verwenden können, um die Anzahl der empfangenen Support Anrufe zu verringern.
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76b49c228af6a932c453b11e92f612d3419a4af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473661"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>Die wichtigsten Tools und Techniken zum Erstellen robuster Windows-Spiele

Eine der unerwünschteren Kosten bei der Spieleproduktion sind Support Anrufe. Jedes Mal, wenn ein Benutzer den Kundensupport kontaktiert, wird der Gewinn aus dem Spiel reduziert. Einige Aufrufe des Kunden Supports sind nicht vermeidbar, andere können durch die Verwendung von guten Entwicklungsverfahren eliminiert oder verringert werden. In diesem Artikel werden Tools und Techniken beschrieben, die Sie verwenden können, um die Anzahl der empfangenen Support Anrufe zu verringern.

Alle hier beschriebenen Tools sind kostenlos, und die Techniken sind einfach genug, um den meisten Entwicklungsmethoden hinzuzufügen.

Tools und Techniken:

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Microsoft Anwendungskompatibilitäts-Toolkit](#microsoft-application-compatibility-toolkit)
-   [Test zum Schutz von Benutzerkonten](#user-account-protection-testing)
-   [Pix für Windows](#pix-for-windows)
-   [Konfigurations Erkennung](#configuration-detection)
-   [Vollständige Compilerwarnungen aktivieren](#enable-full-compiler-warnings)
-   [Microsoft-Symbol Server](#microsoft-symbol-server)
-   [Windows-Fehlerberichterstattung](#windows-error-reporting)
-   [Tools zur Leistungsoptimierung](#performance-tuning-tools)
-   [Zusammenfassung](#summary)

## <a name="prefast"></a>PREfast

PREfast for Drivers ist ein Tool von Microsoft, mit dem Ausführungs Pfade in kompiliertem C oder C++ analysiert werden, um Laufzeitfehler zu finden. Vorfast funktioniert, indem alle Ausführungs Pfade in allen Funktionen durchlaufen und die einzelnen Pfade auf Probleme bewertet werden. Dieses Tool wird normalerweise verwendet, um Treiber und anderen Kernel-Code zu entwickeln. es kann Spiel Entwicklern dabei helfen, Zeit zu sparen, indem einige Fehler vermieden werden, die schwer zu finden sind oder vom Compiler ignoriert werden. Die Verwendung von PREfast ist eine hervorragende Möglichkeit, ihre Workloads nach der Freigabe und Supportkosten zu reduzieren.

In Visual Studio Team System und als Teil des [Windows-treiberkits](https://www.microsoft.com/whdc/devtools/WDK/)ist eine vorab Bereitstellung enthalten. Weitere Informationen zu PREfast finden Sie unter [PREfast for Drivers](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx).

## <a name="appverifier"></a>AppVerifier

Das Microsoft Application Verifier oder AppVerifier ist ein Tool, das Tester bei der Bereitstellung mehrerer Funktionen in einem Tool helfen kann. AppVerifier wurde entwickelt, um die Tests auf häufige Programmierfehler zu vereinfachen. AppVerifier kann die in API-aufrufen übergebenen Parameter überprüfen, falsche Eingaben einfügen, um die Fehler behandlungsfähigkeit zu überprüfen und Änderungen an der Registrierung und im Dateisystem zu protokollieren. AppVerifier kann auch Pufferüberläufe im Heap erkennen, überprüfen, ob eine Zugriffs Steuerungs Liste (ACL) ordnungsgemäß definiert wurde, und erzwingt die sichere Verwendung von Sockets-APIs.

Obwohl es nicht vollständig ist, kann AppVerifier eine weitere Komponente der Toolbox eines Tester sein, um Entwicklungsstudio bei der Veröffentlichung eines Qualitätsprodukts zu unterstützen und die potenziellen Kosten nach der Freigabe zu verringern.

Weitere Informationen zu Application Verifier finden Sie unter [Application Verifier](/previous-versions/ms220948(v=vs.80)) und [Verwenden von Application Verifier in Ihrem Lebenszyklus der Software Entwicklung](/previous-versions/aa480483(v=msdn.10)) auf MSDN. Sie können Application Verifier von den [Download Details herunterladen: Application Verifier](https://www.microsoft.com/download/details.aspx?id=20028) im Microsoft Download Center.

Ein ähnliches Tool für Treiber, Treiber Überprüfung, ist ebenfalls verfügbar. Weitere Informationen finden Sie unter [Verwenden der Treiber Überprüfung zum Identifizieren von Problemen mit Windows-Treibern für fortgeschrittene Benutzer](https://support.microsoft.com/Default.aspx?kbid=244617) in der Hilfe und Unterstützung von Microsoft.

## <a name="microsoft-application-compatibility-toolkit"></a>Microsoft Anwendungskompatibilitäts-Toolkit

Das Microsoft-Anwendungskompatibilitäts-Toolkit ist eine Reihe von kostenlosen Tools, mit denen Entwickler schnell überprüfen können, wie Ihre Releases für neu veröffentlichte Service Packs für Microsoft Windows durchgeführt werden. Wenn Sie für neue Service Packs bereit sind, können Entwickler Probleme verhindern oder bereitstellen.

Das Anwendungskompatibilitäts-Toolkit und weitere Informationen finden Sie unter [Windows-Anwendungs Kompatibilität](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx).

## <a name="user-account-protection-testing"></a>Test zum Schutz von Benutzerkonten

Windows Vista und Windows 7 verfügen über zwei primäre Arten von Benutzerkonten: Standard Benutzer und Administrator. Standard Benutzerkonten sind der bevorzugte Typ für alle Benutzer, da Sie das Risiko einer Beschädigung des Systems durch böswillige Anwendungen verringern. Da Standard Benutzer Zugriffsbeschränkungen haben – beispielsweise nicht in der Lage sind, in den Ordner "Programme" oder \_ \_ HKLM (HKEY Local Machine) in der Registrierung zu schreiben – ist es wichtig, dass Spiele entworfen und getestet werden, um mit einem Standard Benutzerkonto zu arbeiten.

Weitere Informationen zu diesem Thema finden Sie in den Artikeln [Patching Game Software in Windows XP, Windows Vista und Windows 7](./patching-methods-in-windows-xp-and-vista.md) und [Benutzerkontensteuerung für Spieleentwickler](./user-account-control-for-game-developers.md).

## <a name="pix-for-windows"></a>Pix für Windows

PIX ist ein Tool zum Erfassen und Analysieren von Leistungsinformationen aus einer laufenden Anwendung. Pix kann statistische Daten sammeln, warum einige Frames langsamer als andere werden und eine schlechte API-Auslastung identifizieren können. Pix kann auch automatisiert werden, um den täglichen Build zu testen und plötzliche Änderungen an der Anwendungsleistung zu kennzeichnen. Durch die Verwendung von Pix für eine Vielzahl von Hardware Konfigurationen können Tester und Entwickler helfen, Support Anrufe im Zusammenhang mit der Spielleistung zu minimieren.

## <a name="configuration-detection"></a>Konfigurations Erkennung

Gerätefunktionen, die von Treibern verfügbar gemacht werden, sind nicht immer korrekt. Eine Lösung ist die Verwendung eines datenbankgesteuerten Systems für die Konfiguration von Anwendungen, wie z. b. das im DirectX SDK enthaltene System, das im Beispiel configsystem veranschaulicht wird. Ein Erkennungs Modell, das dem System in diesem Beispiel ähnelt, kann dabei helfen, Gerätefunktionen zu identifizieren, die die Leistung des Spiels beeinträchtigen, und somit die Anzahl von Support aufrufen für die Leistung zu reduzieren.

## <a name="enable-full-compiler-warnings"></a>Vollständige Compilerwarnungen aktivieren

Es empfiehlt sich, alle Compilerwarnungen wiederherzustellen, die von der **\# pragma-Warnung** deaktiviert wurden, sobald ein Projekt stabil geworden ist. Entwickler sollten versuchen, alle Warnungen vor der Freigabe eines Produkts auszuschließen. Selbst wenn eine Warnung keinen Absturz oder Fehler auf dem System eines Entwicklers verursacht, kann dies zu einem Problem im System eines Benutzers führen. Wenn eine Warnung nicht gelöscht werden kann, muss das Testteam ermitteln, ob die Warnung wenige oder gar keine Fehler auf dem System eines Benutzers verursacht.

## <a name="microsoft-symbol-server"></a>Microsoft-Symbol Server

Microsoft stellt einen Server mit Internet Zugriff bereit, der Symbol Dateien für die Microsoft Windows-Betriebssysteme sowie andere Microsoft-Produkte bereitstellt. Symbole sind auch auf dem Server für die aktuellen Beta Versionen und Releasekandidaten von Windows-Produkten sowie Hotfixes und Service Packs verfügbar. Sie können den Debugger so konfigurieren, dass während einer Debugsitzung erforderliche Symbole heruntergeladen werden, anstatt Symbol Dateien vor einer Debugsitzung separat herunterzuladen. Die Symbole werden an einen Verzeichnis Speicherort heruntergeladen, den Sie angeben, und der Debugger lädt Sie von dort.

Weitere Informationen zum Microsoft-Symbol Server finden Sie unter [Debugtools und-Symbole: Getting Started](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx).

## <a name="windows-error-reporting"></a>Windows-Fehlerberichterstattung

Windows-Fehlerberichterstattung (wer) ist ein von Microsoft bereitgestellter Dienst, mit dem Entwickler Fehlerinformationen aus Anwendungen einheitlich und organisiert erfassen können. Obwohl es vollständig freiwillig ist, sollten Entwickler diesen Dienst nutzen, um zu bestimmen, welche Fehler am häufigsten auftreten. Die Verwendung von Wer kann beim Debuggen häufig gemeldeter Probleme hilfreich sein, um die Unterstützung von Support aufrufen für die meisten Commons-Fehler zu beseitigen.

Weitere Informationen zu wer finden Sie unter [Absturz](./crash-dump-analysis.md)Abbild Analyse.

## <a name="performance-tuning-tools"></a>Tools zur Leistungsoptimierung

Entwickler können Leistungsanalyse Tools verwenden, um die Leistung Ihres Spiels zu optimieren. Zusätzlich zu pix gibt es eine Reihe beliebter Leistungsanalysen für Windows, wie z. b. [Intel VTune Performance Analyzer](https://software.intel.com/intel-vtune/) und [AMD CodeAnalyst Performance Analyzer](https://developer.amd.com/cpu/CodeAnalyst/). Diese Tools unterstützen Sie bei der Identifizierung von Engpässen und bei der Entscheidung, wie die Gesamtleistung einer Anwendung verbessert werden soll. Das verbessern von Leistungs Engpässen vor der Freigabe führt zu einer Senkung der Kosten nach der Freigabe.

## <a name="summary"></a>Zusammenfassung

Alle Benutzer, die an Entwurf, Entwicklung und Tests beteiligt sind, müssen in Erwägung gezogen werden, wie sich Ihre Arbeit auf die Kosten eines Produkts nach der Freigabe auswirkt. Durch die Verwendung der oben erwähnten Tools und Methoden im Produktionsprozess kann die Menge der Support Anrufe reduziert werden. Dies wiederum steigert den Gewinn, indem die Kosten für die Spieleentwicklung gesenkt werden.

 

 