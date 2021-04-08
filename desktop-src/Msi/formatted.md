---
description: Der formatierte Datentyp ist eine Text Zeichenfolge, die zum Auflösen von eingebetteten Eigenschaftsnamen, Tabellen Schlüsseln, Umgebungsvariablen verweisen und anderen speziellen Teil Zeichenfolgen verarbeitet wird.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formatiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd15dca46839b25dbf186d8a741b7a5c37c05f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960053"
---
# <a name="formatted"></a>Formatiert

Der formatierte Datentyp ist eine Text Zeichenfolge, die zum Auflösen von eingebetteten Eigenschaftsnamen, Tabellen Schlüsseln, Umgebungsvariablen verweisen und anderen speziellen Teil Zeichenfolgen verarbeitet wird. Die folgenden Konventionen werden erkannt, um die Zeichenfolge aufzulösen:

-   Eckige Klammern ( \[ \] ) oder geschweifte Klammern ({}) ohne übereinstimmendes Paar verbleiben im Text.
-   Wenn eine Teil Zeichenfolge der Form \[ *propertyName* gefunden \] wird, wird Sie durch den Wert der-Eigenschaft ersetzt. Wenn *propertyName* kein gültiger Eigenschaftsname ist, wird die Teil Zeichenfolge als leer aufgelöst. Beispielsweise nimmt die Beschreibungs Spalte der [LaunchCondition-Tabelle](launchcondition-table.md) eine formatierte Zeichenfolge an. Wenn errortxt auf "wenden Sie sich an den Support. der Text, der für das Fehlschlagen der Startbedingung angezeigt wird, würde diese Zeichenfolge enthalten. Wenn errorxt nicht festgelegt ist, ist der Text, der zum Fehlschlagen der Startbedingung angezeigt wird, einfach "System erfüllt nicht die Installationsanforderungen".

    

    | Bedingung | BESCHREIBUNG                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | Das System erfüllt die Installationsanforderungen nicht. \[Errorxt\] |

    

     

-   Die eckigen Klammern können iteriert werden, und die Eigenschaftsnamen werden von innen nach oben aufgelöst. Angenommen, die Teil Zeichenfolge \[ \[ PropertyA wird \] \] im Text angezeigt. Zuerst wird der Wert der PropertyA-Eigenschaft abgerufen. Wenn der Wert ein gültiger Eigenschaftsname ist, z. b. propertyb, wird der Wert von propertyb abgerufen, und die gesamte Teil Zeichenfolge \[ \[ PropertyA \] \] wird durch den Wert von propertyb ersetzt. Wenn PropertyA kein gültiger Eigenschaftsname ist oder wenn der Wert von PropertyA kein gültiger Eigenschaftsname ist, dann ist die Teil Zeichenfolge leer.
-   Wenn eine Teil Zeichenfolge der Form \[ % *Umgebungsvariable* \] gefunden wird, wird der Wert der Umgebungsvariablen für die Teil Zeichenfolge ersetzt.
-   Wenn eine Teil Zeichenfolge in der Form " \[ \\ *x* " \] gefunden wird, wird Sie durch das Zeichen *x* ersetzt, wobei *x* ein Zeichen ist, ohne dass eine weitere Verarbeitung erfolgt. Nur das erste Zeichen nach dem umgekehrten Schrägstrich wird beibehalten. alles andere wird entfernt. Um z. b. eine Literale linke eckige Klammer () einzuschließen \[ , verwenden Sie \[ \\ \[ \] . Der Text Klammer Text wird \[ \\ \[ \] \[ \\ \] \] in den \[ Klammer Text aufgelöst \] .
-   Wenn eine Teil Zeichenfolge in geschweiften Klammern ({}) eingeschlossen ist und keine Eigenschaftsnamen in eckigen Klammern () enthalten sind \[ \] , bleibt die Teil Zeichenfolge unverändert, einschließlich der geschweiften Klammern.
-   Wenn eine Teil Zeichenfolge in geschweiften Klammern ({}) eingeschlossen ist und einen oder mehrere Eigenschaftsnamen enthält, die in eckigen Klammern ( \[ \] ) enthalten sind, wird der Text (mit den aufgelösten Ersetzungen) ohne geschweifte Klammern angezeigt, wenn alle Eigenschaftsnamen gültig sind.
-   Wenn eine Teil Zeichenfolge des Formulars \[ ~ \] gefunden wird, wird Sie durch das NULL-Zeichen ersetzt. Wird verwendet, um **reg \_ \_ MultiSZ** -Zeichen folgen in der [Registrierungs Tabelle](registry-table.md)zu erstellen. Beachten Sie, dass \[ ~ \] auch verwendet wird, um Umgebungsvariablen mithilfe der [Umgebungs Tabelle](environment-table.md)Werte anzufügen oder zu versehen.
-   Wenn eine Teil Zeichenfolge der Form \[ \# *filekey* \] gefunden wird, wird Sie durch den vollständigen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in die [Dateitabelle](file-table.md)verwendet wird. Der Wert von \[ \# *filekey* \] bleibt leer und wird nicht durch einen Pfad ersetzt, bis der Installer die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführt. Der Wert von \[ \# *filekey* \] hängt vom Installationsstatus der Komponente ab, zu der die Datei gehört. Wenn die Komponente von der Quelle ausgeführt wird, ist der Wert der Pfad zum Quell Speicherort der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert der Pfad zum Zielort der Datei nach der Installation. Wenn die Komponente den Aktionszustand Missing aufweist, wird der installierte Zustand der Komponente verwendet, um zu bestimmen \[ \) .
-   Wenn eine Teil Zeichenfolge der Form \[ $ *componentkey* \] gefunden wird, wird Sie durch das Installationsverzeichnis der Komponente ersetzt, wobei der Wert *componentkey* als Schlüssel in der [Komponenten Tabelle](component-table.md)verwendet wird. Der Wert von \[ $ *componentkey* \] bleibt leer und wird erst durch ein Verzeichnis ersetzt, wenn das Installationsprogramm die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführt. Der Wert von \[ $ *componentkey* \] hängt vom Installationsstatus der Komponente und der Stelle ab, an der Sie auftritt. In der Spalte Wert der [Registrierungs Tabelle](registry-table.md)bezieht sich diese Teil Zeichenfolge möglicherweise auf den Aktions Status oder den angeforderten Aktions Status der Komponente. In allen anderen Fällen verweist diese Teil Zeichenfolge auf den Aktionszustand der Komponente. Wenn die Komponente z. b. aus der Quelle ausgeführt wird, ist der Wert das Quellverzeichnis der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert das Zielverzeichnis nach der Installation. Wenn die Komponente nicht vorhanden ist, wird der Wert leer gelassen. Windows Installer verfolgt sowohl die Aktion als auch den angeforderten Installationsstatus von-Komponenten. Wenn z. b. eine Komponente bereits installiert ist, kann Sie den angeforderten Zustand local und den Aktions Status NULL aufweisen. Weitere Informationen zum Überprüfen des Installationsstatus von-Komponenten finden Sie unter über [Prüfen der Installation von Features, Komponenten und Dateien](checking-the-installation-of-features-components-files.md).
-   Beachten Sie Folgendes: Wenn eine Komponente bereits installiert ist und während der aktuellen Installation nicht neu installiert, entfernt oder verschoben wird, ist der Aktions Status der Komponente NULL, und die Zeichenfolge \[ $ *componentkey* ergibt \] NULL.
-   Wenn eine Teil Zeichenfolge des Formulars ist \[ .*filekey* \] wurde gefunden und wird durch den vollständigen kurzen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in die [Dateitabelle](file-table.md)verwendet wird.

    Diese Syntax ist nur gültig, wenn Sie in der Value-Spalte der Registrierungs-oder der IniFile-Tabelle verwendet wird. Wenn diese Syntax in anderen Spalten verwendet wird, wird Sie wie \[ \# *filekey* behandelt \] .

 

 



