---
description: Sie können benutzerdefinierte Aktionen, die auf Dynamic Link Libraries basieren, mithilfe von Debugtools für Windows Debuggen. Das dynamische Debuggen kann nicht mit benutzerdefinierten Aktionen auf der Grundlage von ausführbaren Dateien oder Skripts verwendet werden.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Debugging von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ddfbc9952f0dd7fc1b85b5c64fa6a23381ceafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368851"
---
# <a name="debugging-custom-actions"></a>Debugging von benutzerdefinierten Aktionen

Sie können benutzerdefinierte Aktionen, die auf [Dynamic Link Libraries](dynamic-link-libraries.md) basieren, mithilfe von [Debugtools für Windows Debuggen](https://www.microsoft.com/?ref=go). Das dynamische Debuggen kann nicht mit benutzerdefinierten Aktionen auf der Grundlage von [ausführbaren Dateien](executable-files.md) oder [Skripts](scripts.md)verwendet werden.

Die in diesem Abschnitt beschriebenen Verfahren können Sie beim Debuggen von Windows Installer benutzerdefinierten Aktionen unterstützen. Weitere Informationen zu [Debuggingtools für Windows](https://www.microsoft.com/?ref=go)finden Sie im Abschnitt Treiber Entwicklungs Tools im Windows-Treiberkit (WDK).

In Windows Installer wird die msibreak-Umgebungsvariable verwendet, um zu bestimmen, welche benutzerdefinierte Aktion deentschlbelt werden soll. Wenn Sie Zugriff auf den Quellcode der benutzerdefinierten Aktion haben, können Sie möglicherweise das Debuggen ohne msibreak verwenden. Wenn Sie das Debuggen ohne msibreak starten möchten, legen Sie am Anfang des Aktionscodes ein temporäres Meldungs Feld ab. Wenn das Meldungs Feld während der Installation angezeigt wird, fügen Sie den Debugger an den Prozess an, der das Meldungs Feld besitzt. Sie können dann alle notwendigen Breakpoints festlegen und das Meldungs Feld schließen, um die Ausführung fortzusetzen. Es ist nicht möglich, die früheren Teile der benutzerdefinierten Aktion mit dieser Methode zu debuggen.

Um die msibreak-Umgebungsvariable zum Debuggen der benutzerdefinierten Aktion zu verwenden, legen Sie msibreak auf den Namen der benutzerdefinierten Aktion in der [Tabelle CustomAction](customaction-table.md)fest. Msibreak kann entweder eine System-oder eine Benutzer Umgebungsvariable sein. Wenn die Variable als Systemvariable festgelegt wird, ist möglicherweise ein Neustart des Systems erforderlich, wenn der Wert geändert wird, um den neuen Wert zu ermitteln.

Um die msibreak-Umgebungsvariable zum Debuggen einer eingebetteten Benutzeroberfläche zu verwenden, legen Sie den Wert von msibreak auf msiembeddedui fest.

Windows Installer überprüft nur die msibreak-Umgebungsvariable, wenn der Benutzer ein Administrator ist. Das Installationsprogramm ignoriert den Wert von "msibreak", wenn der Benutzer kein Administrator ist, auch wenn es sich um eine [*verwaltete Anwendung*](m-gly.md)handelt.

Wenn Sie eine benutzerdefinierte Aktion Debuggen, die mit erhöhten Rechten (System Berechtigungen) in der Ausführungssequenz ausgeführt wird, fügen Sie den Debugger an den Windows Installer-Dienst an. Beim Debuggen einer benutzerdefinierten Aktion, die mit den Berechtigungen mit Identitätswechsel in der Ausführungssequenz ausgeführt wird, fordert das System ein Dialogfeld an, das angibt, welcher Prozess gedebuggt werden soll. Der Benutzer wird in einem Dialogfeld aufgefordert, den zu debuggenden Prozess anzugeben. Weitere Informationen zu erweiterten benutzerdefinierten Aktionen finden Sie unter [Sicherheit für benutzerdefinierte](custom-action-security.md)Aktionen.

Nachdem der Debugger an den korrekten Prozess angefügt wurde, löst das Installationsprogramm unmittelbar vor dem Aufrufen des Einstiegs Punkts der dll einen Debugger-Breakpoint aus. Am Haltepunkt ist die DLL bereits in den Prozess geladen und die Einstiegspunkt Adresse wurde festgelegt. Wenn die DLL für die benutzerdefinierte Aktion nicht geladen werden konnte oder der Einstiegspunkt für die benutzerdefinierte Aktion nicht vorhanden ist, wird kein Haltepunkt ausgelöst. Da der Haltepunkt vor dem Aufrufen der DLL-Funktion ausgelöst wird, sollten Sie nach dem Auslösen des Breakpoints den Debugger verwenden, um den Schritt fortzusetzen, bis der Einstiegspunkt für die benutzerdefinierte Aktion aufgerufen wird. Alternativ können Sie einen Haltepunkt an einer beliebigen Stelle in der benutzerdefinierten Aktion festlegen und die normale Ausführung fortsetzen.

Der Windows Installer führt DLLs aus, die nicht direkt aus dem dll-Speicherort in der [binären Tabelle](binary-table.md) gespeichert sind. Das Installationsprogramm kennt den ursprünglichen Namen einer in der binären Tabelle gespeicherten dll nicht und führt die benutzerdefinierte DLL-Aktion unter einem temporären Dateinamen aus. Die Form des temporären Datei namens lautet MSI-?????. TMP. Unter Windows XP wird diese temporäre Datei an einem sicheren Speicherort gespeichert, üblicherweise im <WindowFolder> \\ Installationsprogramm.

Beachten Sie, dass viele DLLs, die für das Debuggen erstellt wurden, den Namen und den Pfad der entsprechenden PDB-Datei als Teil der DLL selbst enthalten. Beim Debuggen dieses dll-Typs in einem System, auf dem sich die PDB an dem Speicherort befindet, der in der dll gespeichert ist, können Symbole automatisch vom debuggertool geladen werden. In Fällen, in denen die PDB an der gespeicherten Position nicht gefunden werden kann, in der der Debugger das Laden von Symbolen aus dem gespeicherten Speicherort nicht unterstützt, oder wenn die dll nicht mit Debuginformationen erstellt wurde, müssen Sie Ihre Symbol Dateien möglicherweise mit der temporären dll-Datei im Ordner platzieren.

Das Installationsprogramm fügt der Installationsprotokoll Datei Debuginformationen für benutzerdefinierte Aktions Skripts hinzu.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



