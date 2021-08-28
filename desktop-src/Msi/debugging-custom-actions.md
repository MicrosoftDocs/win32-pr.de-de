---
description: Sie können benutzerdefinierte Aktionen debuggen, die auf Dynamic Link-Bibliotheken basieren, indem Sie Debugtools für Windows. Es ist nicht möglich, dynamisches Debuggen mit benutzerdefinierten Aktionen zu verwenden, die auf ausführbaren Dateien oder Skripts basieren.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Debuggen von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781aaa5bfc8303175e7addfee730908c581575fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887021"
---
# <a name="debugging-custom-actions"></a>Debuggen von benutzerdefinierten Aktionen

Sie können benutzerdefinierte Aktionen debuggen, die auf Dynamic [Link-Bibliotheken](dynamic-link-libraries.md) basieren, indem Sie [Debugtools für Windows.](https://www.microsoft.com/?ref=go) Es ist nicht möglich, dynamisches Debuggen mit benutzerdefinierten Aktionen zu verwenden, die auf [ausführbaren Dateien oder](executable-files.md) Skripts [basieren.](scripts.md)

Die in diesem Abschnitt beschriebenen Techniken können Sie beim Debuggen Windows benutzerdefinierten Aktionen des Installers unterstützen. Informationen zu Debugtools für Windows finden Sie im Abschnitt Treiberentwicklungstools des Windows Driver Kit (WD [Windows K).](https://www.microsoft.com/?ref=go)

Windows Das Installationsprogramm verwendet die MsiBreak-Umgebungsvariable, um zu bestimmen, welche benutzerdefinierte Aktion debuggt werden soll. Wenn Sie Zugriff auf den Quellcode der benutzerdefinierten Aktion haben, können Sie das Debuggen möglicherweise ohne MsiBreak verwenden. Um mit dem Debuggen ohne MsiBreak zu beginnen, setzen Sie am Anfang des Aktionscodes ein temporäres Meldungsfeld. Wenn das Meldungsfeld während der Installation angezeigt wird, fügen Sie den Debugger an den Prozess an, der das Meldungsfeld besitzt. Sie können dann alle erforderlichen Haltepunkte festlegen und das Meldungsfeld schließen, um die Ausführung wieder aufzunehmen. Es ist nicht möglich, die früheren Teile der benutzerdefinierten Aktion mit dieser Methode zu debuggen.

Um die MsiBreak-Umgebungsvariable zum Debuggen der benutzerdefinierten Aktion zu verwenden, legen Sie MsiBreak auf den Namen der benutzerdefinierten Aktion in der [CustomAction-Tabelle fest.](customaction-table.md) MsiBreak kann entweder eine System- oder eine Benutzerumgebungsvariable sein. Wenn die Variable als Systemvariable festgelegt ist, ist möglicherweise ein Neustart des Systems erforderlich, wenn der Wert geändert wird, um den neuen Wert zu erkennen.

Um die MsiBreak-Umgebungsvariable zum Debuggen einer eingebetteten Benutzeroberfläche zu verwenden, legen Sie den Wert von MsiBreak auf MsiEmbeddedUI fest.

Windows Das Installationsprogramm überprüft die MsiBreak-Umgebungsvariable nur, wenn der Benutzer Administrator ist. Das Installationsprogramm ignoriert den Wert von MsiBreak, wenn der Benutzer kein Administrator ist, auch wenn es sich um eine verwaltete [*Anwendung handelt.*](m-gly.md)

Wenn Sie eine benutzerdefinierte Aktion debuggen, die mit erhöhten Rechten (System) in der Ausführungssequenz ausgeführt wird, fügen Sie den Debugger an den Windows Installer-Dienst an. Beim Debuggen einer benutzerdefinierten Aktion, die mit Identitätswechselberechtigungen in der Ausführungssequenz ausgeführt wird, fordert das System ein Dialogfeld an, das angibt, welcher Prozess debuggt werden soll. Der Benutzer wird mit einem Dialogfeld aufgefordert, das angibt, welcher Prozess debuggt werden soll. Weitere Informationen zu benutzerdefinierten Aktionen mit erhöhten Rechten finden Sie unter [Custom Action Security](custom-action-security.md).

Sobald der Debugger an den richtigen Prozess angefügt wurde, löst das Installationsprogramm unmittelbar vor dem Aufrufen des Einstiegspunkts der DLL einen Debugger-Haltepunkt aus. Am Haltepunkt ist die DLL bereits in den Prozess geladen, und die Einstiegspunktadresse wurde bestimmt. Wenn die DLL für benutzerdefinierte Aktionen nicht geladen werden konnte oder der Einstiegspunkt für die benutzerdefinierte Aktion nicht vorhanden war, wird kein Haltepunkt ausgelöst. Da der Haltepunkt vor dem Aufrufen der DLL-Funktion ausgelöst wird, sollten Sie nach dem Auslösen des Haltepunkts den Debugger verwenden, um vorwärts zu gehen, bis der Einstiegspunkt für die benutzerdefinierte Aktion aufgerufen wird. Alternativ können Sie einen Haltepunkt an einer beliebigen Stelle in Ihrer benutzerdefinierten Aktion festlegen und die normale Ausführung fortsetzen.

Der Windows Installer führt DLLs aus, die nicht direkt am DLL-Speicherort in der [Binärtabelle](binary-table.md) gespeichert sind. Das Installationsprogramm kennt den ursprünglichen Namen einer in der Binärtabelle gespeicherten DLL nicht und führt die benutzerdefinierte DLL-Aktion unter einem temporären Dateinamen aus. Die Form des temporären Dateinamens ist MSI?????. TMP. Auf Windows XP wird diese temporäre Datei an einem sicheren Speicherort gespeichert, in der Regel &lt; an einem WindowFolder-Installer. &gt; \\

Beachten Sie, dass viele DLLs, die für das Debuggen erstellt wurden, den Namen und Pfad der entsprechenden PDB-Datei als Teil der DLL selbst enthalten. Beim Debuggen dieser Art von DLL auf einem System, in dem sich die PDB-Datei an dem in der DLL gespeicherten Speicherort befindet, können Symbole automatisch vom Debuggertool geladen werden. In Situationen, in denen die PDB nicht am gespeicherten Speicherort gefunden werden kann, der Debugger das Laden von Symbolen vom gespeicherten Speicherort nicht unterstützt oder die DLL nicht mit Debuginformationen erstellt wurde, müssen Sie die Symboldateien möglicherweise im Ordner mit der temporären DLL-Datei platzieren.

Das Installationsprogramm fügt der Installationsprotokolldatei Debuginformationen für benutzerdefinierte Aktionsskripts hinzu.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



