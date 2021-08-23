---
description: Der Formatierte Datentyp ist eine Textzeichenfolge, die verarbeitet wird, um eingebettete Eigenschaftsnamen, Tabellenschlüssel, Verweise auf Umgebungsvariablen und andere spezielle Teilzeichenfolgen aufzulösen.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formatiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58cd21a53a3f77a646d6da0fac04480bd709ab8f1d7ddcb918d5362a0a366c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649641"
---
# <a name="formatted"></a>Formatiert

Der Formatierte Datentyp ist eine Textzeichenfolge, die verarbeitet wird, um eingebettete Eigenschaftsnamen, Tabellenschlüssel, Verweise auf Umgebungsvariablen und andere spezielle Teilzeichenfolgen aufzulösen. Die folgenden Konventionen werden zum Auflösen der Zeichenfolge erkannt:

-   Eckige Klammern \[ \] () oder geschweifte Klammern ({ }) ohne übereinstimmendes Paar bleiben im Text erhalten.
-   Wenn eine Teilzeichenfolge des \[ *Formulareigenschaftennamens* \] gefunden wird, wird sie durch den Wert der Eigenschaft ersetzt. Wenn *propertyname* kein gültiger Eigenschaftenname ist, wird die Teilzeichenfolge als leer aufgelöst. Beispielsweise nimmt die Spalte Description der [LaunchCondition-Tabelle](launchcondition-table.md) eine formatierte Zeichenfolge an. Wenn ERRORTXT auf "Please contact your support personnel" festgelegt wurde. dann enthält der Text, der für einen Fehler bei der Startbedingung angezeigt wird, diese Zeichenfolge. Wenn ERRORTXT nicht festgelegt ist, lautet der Text, der für einen Fehler bei der Startbedingung angezeigt wird, einfach "System erfüllt die Installationsanforderungen nicht."

    

    | Bedingung | Beschreibung                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9x | Das System erfüllt die Installationsanforderungen nicht. \[ERRORTXT\] |

    

     

-   Die eckigen Klammern können iteriert werden, und die Eigenschaftennamen werden von innen nach außen aufgelöst. Angenommen, die Teilzeichenfolge \[ \[ PropertyA \] \] wird im Text angezeigt. Zuerst wird der Wert der Eigenschaft PropertyA abgerufen. Wenn der Wert ein gültiger Eigenschaftenname ist, z. B. PropertyB, wird der Wert von PropertyB abgerufen, und die gesamte Teilzeichenfolge \[ \[ PropertyA \] \] wird durch den Wert von PropertyB ersetzt. Wenn PropertyA kein gültiger Eigenschaftenname ist oder der Wert von PropertyA kein gültiger Eigenschaftenname ist, ist die Teilzeichenfolge leer.
-   Wenn eine Teilzeichenfolge der Form \[ % *environmentvariable* \] gefunden wird, wird der Wert der Umgebungsvariablen durch die Teilzeichenfolge ersetzt.
-   Wenn eine Teilzeichenfolge des Formulars \[ \\ *x* \] gefunden wird, wird sie durch das Zeichen *x* ersetzt, wobei *x* ein Zeichen ohne weitere Verarbeitung ist. Nur das erste Zeichen nach dem umgekehrten Schrägstrich wird beibehalten. alles andere wird entfernt. Verwenden Sie beispielsweise , um eine literale linke Klammer \[ () \[ \\ \[ \] einzufügen. Der Text \[ \\ \[ \] Klammertext \[ \\ \] \] wird in \[ Klammertext \] aufgelöst.
-   Wenn eine Teilzeichenfolge in geschweifte Klammern ({ }) eingeschlossen ist und keine Eigenschaftsnamen enthält, die in eckige Klammern () eingeschlossen \[ \] sind, bleibt die Teilzeichenfolge unverändert, einschließlich der geschweiften Klammern.
-   Wenn eine Teilzeichenfolge in geschweifte Klammern ({ }) eingeschlossen ist und einen oder mehrere Eigenschaftsnamen enthält, die in eckige Klammern () eingeschlossen \[ \] sind, wird der Text (mit den aufgelösten Ersetzungen) ohne die geschweiften Klammern angezeigt, wenn alle Eigenschaftsnamen gültig sind.
-   Wenn eine Teilzeichenfolge des Formulars \[ ~ \] gefunden wird, wird sie durch das NULL-Zeichen ersetzt. Dies wird verwendet, um **REG \_ MULTI \_ SZ-Zeichenfolgen** in der [Registrierungstabelle](registry-table.md)zu erstellen. Beachten Sie, dass \[ ~ \] auch zum Anfügen oder Präfixen von Werten an Umgebungsvariablen mithilfe der [Umgebungstabelle](environment-table.md)verwendet wird.
-   Wenn eine Teilzeichenfolge des \[ \# *Formdateischlüssels* \] gefunden wird, wird sie durch den vollständigen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in der [Dateitabelle](file-table.md)verwendet wird. Der Wert von \[ \# *filekey* \] bleibt leer und wird erst durch einen Pfad ersetzt, wenn das Installationsprogramm die Aktion [CostInitialize,](costinitialize-action.md)die [FileCost-Aktion](filecost-action.md)und die [CostFinalize-Aktion](costfinalize-action.md)ausführt. Der Wert von \[ \# *filekey* \] hängt vom Installationsstatus der Komponente ab, zu der die Datei gehört. Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert der Pfad zum Quellspeicherort der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert der Pfad zum Zielspeicherort der Datei nach der Installation. Wenn die Komponente den Aktionsstatus fehlt, wird der installierte Zustand der Komponente verwendet, um den zu \[ \) bestimmen.
-   Wenn eine Teilzeichenfolge des \[ $ *Formkomponentenschlüssels* \] gefunden wird, wird sie durch das Installationsverzeichnis der Komponente durch den Wert *componentkey* ersetzt, der als Schlüssel in der [Komponententabelle](component-table.md)verwendet wird. Der Wert von \[ $ *componentkey* \] bleibt leer und wird erst durch ein Verzeichnis ersetzt, wenn das Installationsprogramm die Aktion [CostInitialize,](costinitialize-action.md)die [FileCost-Aktion](filecost-action.md)und die [CostFinalize-Aktion](costfinalize-action.md)ausführt. Der Wert von \[ $ *componentkey* \] hängt vom Installationsstatus der Komponente und dem Ort ab, an dem sie auftritt. In der Spalte Wert der [Registrierungstabelle](registry-table.md)kann diese Teilzeichenfolge auf den Aktionszustand oder den angeforderten Aktionszustand der Komponente verweisen. In allen anderen Fällen bezieht sich diese Teilzeichenfolge auf den Aktionszustand der Komponente. Wenn die Komponente beispielsweise aus der Quelle ausgeführt wird, ist der Wert das Quellverzeichnis der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert das Zielverzeichnis nach der Installation. Wenn die Komponente nicht vorhanden ist, wird der Wert leer gelassen. Windows Das Installationsprogramm verfolgt sowohl die Aktion als auch die angeforderten Installationszustände von Komponenten nach. Wenn beispielsweise eine Komponente bereits installiert ist, kann sie den angeforderten Zustand local und den Aktionsstatus NULL aufweisen. Weitere Informationen zum Überprüfen des Installationsstatus von Komponenten finden Sie unter [Überprüfen der Installation von Features, Komponenten und Dateien.](checking-the-installation-of-features-components-files.md)
-   Beachten Sie Folgendes: Wenn eine Komponente bereits installiert ist und während der aktuellen Installation nicht neu installiert, entfernt oder verschoben wird, ist der Aktionsstatus der Komponente NULL, und der String \[ $ *componentkey* \] wird als NULL ausgewertet.
-   Wenn eine Teilzeichenfolge des Formulars \[ !*filekey* wurde gefunden. Er \] wird durch den vollständigen kurzen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in der [Dateitabelle](file-table.md)verwendet wird.

    Diese Syntax ist nur gültig, wenn sie in der Spalte Wert der Registry- oder IniFile-Tabellen verwendet wird. Bei Verwendung in anderen Spalten wird diese Syntax genauso behandelt wie \[ \# *der Dateischlüssel* \] .

 

 



