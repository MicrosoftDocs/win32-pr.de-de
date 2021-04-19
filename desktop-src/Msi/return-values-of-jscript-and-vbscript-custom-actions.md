---
description: In JScript oder Visual Basic geschriebene benutzerdefinierte Aktionen, Scripting Edition (VBScript) können eine optionale Funktion aufzurufen. Diese Funktionen müssen einen der in der folgenden Tabelle dargestellten Werte zurückgeben.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Rückgabewerte von benutzerdefinierten JScript-und VBScript-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355592"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Rückgabewerte von benutzerdefinierten JScript-und VBScript-Aktionen

In JScript oder Visual Basic geschriebene benutzerdefinierte Aktionen, Scripting Edition (VBScript) können eine optionale Funktion aufzurufen. Diese Funktionen müssen einen der in der folgenden Tabelle dargestellten Werte zurückgeben.



| Rückgabewert              | Wert        | BESCHREIBUNG                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msidoaction Status-NoAction | 0            | Die Aktion wurde nicht ausgeführt.                                                                                       |
| msidoaktionstatus-Erfolg  | IDOK = 1     | Die Aktion wurde erfolgreich abgeschlossen.                                                                             |
| msidoaktionstatus ususerexit | IDCANCEL = 2 | Vorzeitige Beendigung durch den Benutzer.                                                                             |
| msidoaktionstatus-Fehler  | Idabort = 3  | Nicht BEHEB barer Fehler. Wird zurückgegeben, wenn während der Verarbeitung oder Ausführung von JScript oder VBScript ein Fehler aufgetreten ist. |
| msidoaktionstatus-Suspend  | Idretry = 4  | Angehaltene Sequenz, die später fortgesetzt werden soll.                                                                    |
| msidoaktionstatus "beendet" | IDIGNORE = 5 | Verbleibende Aktionen überspringen. Kein Fehler.                                                                      |



 

Beachten Sie, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn der Rückgabewert der Aktion z. b. als 1 (eins) in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion msidoaction Status-Success zurückgegeben hat. Weitere Informationen zu dieser Übersetzung finden Sie [unter Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).

Wenn Sie einen anderen Wert als Success aus einer benutzerdefinierten Skript Aktion zurückgeben möchten, müssen Sie für die benutzerdefinierte Aktion ein Funktions Ziel verwenden. Die Zielfunktion wird in der Ziel Spalte der [CustomAction-Tabelle](customaction-table.md)angegeben.

Im folgenden Skript Beispiel wird gezeigt, wie Sie Erfolg oder Fehler von einer benutzerdefinierten VBScript-Aktion zurückgeben.


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



Wenn dieses VBScript als MyCA.vbs in die [binäre Tabelle](binary-table.md) des Installationspakets eingebettet wurde, lautet der [CustomAction-Tabellen](customaction-table.md) Eintrag für das Skript wie folgt:



| Aktion         | type | `Source`   | Ziel       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | Myvbscriptca |



 

 

 



