---
description: Benutzerdefinierte Aktionen, die in JScript oder Visual Basic, Scripting Edition (VBScript) geschrieben wurden, können eine optionale Funktion aufrufen. Diese Funktionen müssen einen der in der folgenden Tabelle gezeigten Werte zurückgeben.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Rückgabewerte von JScript und benutzerdefinierten VBScript-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50a2b225c59b0e4d1787f2eaceeb094d6fb2abe7f9d9600822b6295ef2dd273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626090"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Rückgabewerte von JScript und benutzerdefinierten VBScript-Aktionen

Benutzerdefinierte Aktionen, die in JScript oder Visual Basic, Scripting Edition (VBScript) geschrieben wurden, können eine optionale Funktion aufrufen. Diese Funktionen müssen einen der in der folgenden Tabelle gezeigten Werte zurückgeben.



| Rückgabewert              | Wert        | Beschreibung                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Die Aktion wurde nicht ausgeführt.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | Die Aktion wurde erfolgreich abgeschlossen.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Vorzeitige Beendigung durch den Benutzer.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Nicht behebbarer Fehler. Wird zurückgegeben, wenn während der Analyse oder Ausführung des -JScript VBScript ein Fehler auftritt. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Angehaltene Sequenz, die später fortgesetzt werden soll.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Überspringen Sie die verbleibenden Aktionen. Kein Fehler.                                                                      |



 

Beachten Sie, Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn der Rückgabewert der Aktion beispielsweise als 1 (eins) in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion msiDoActionStatusSuccess zurückgegeben hat. Weitere Informationen zu dieser Übersetzung finden Sie unter [Protokollierung von Aktions-Rückgabewerten.](logging-of-action-return-values.md)

Sie müssen ein Funktionsziel für die benutzerdefinierte Aktion verwenden, um einen anderen Wert als erfolgreich aus einer benutzerdefinierten Skriptaktion zurück zu geben. Die Zielfunktion wird in der Spalte Target der [CustomAction-Tabelle angegeben.](customaction-table.md)

Im folgenden Skriptbeispiel wird gezeigt, wie Sie eine erfolgreiche oder nicht erfolgreiche Aktion einer benutzerdefinierten VBScript-Aktion zurückgeben.


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



Wenn dieses VBScript in die [Binärtabelle](binary-table.md) des Installationspakets als MyCA.vbs eingebettet wäre, würde der [CustomAction-Tabelleneintrag](customaction-table.md) für das Skript wie folgt sein:



| Aktion         | type | `Source`   | Ziel       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



