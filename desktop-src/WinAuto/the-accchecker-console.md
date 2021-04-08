---
title: Die accchecker-Konsole
description: Die accchecker-Konsole (AccCheckConsole.exe) ist ein Befehlszeilen Tool zum Überprüfen der Barrierefreiheits Implementierung der Benutzeroberfläche Ihrer Anwendung.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Accchecker-Konsole
- Accchecker-Befehlszeilen Tool
- Befehlszeile, Zugriffs Prüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855556"
---
# <a name="the-accchecker-console"></a>Die accchecker-Konsole

Die accchecker-Konsole (AccCheckConsole.exe) ist ein Befehlszeilen Tool zum Überprüfen der Barrierefreiheits Implementierung der Benutzeroberfläche Ihrer Anwendung. Die Befehlszeile akzeptiert eine Vielzahl von Eingaben (z. b. HWND, Fenstertitel und Überprüfungs Routine) und liefert einen Exitcode, der der Anzahl der Fehlerprotokolle entspricht.

-   [Befehlszeilen Syntax](#command-line-syntax)
-   [Befehlszeilen-Fehler Codes](#command-line-error-codes)
-   [Befehlszeilen Beispiele](#command-line-examples)
-   [Zugehörige Themen](#related-topics)

![Befehlszeilen Tool der accchecker-Konsole](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die accchecker-Konsole weist die folgende Befehlszeilen Syntax auf.

**Acccheckconsole \[ \] -Optionen (-HWND <hwnd> \| -Process <name> ) \[<dlls>\]**

Die Befehlszeilenoptionen lauten wie folgt.



| Optionen                                                                                                                                                         | BESCHREIBUNG                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd><br/>                                                                     | Überprüft das Fenster, das über das angegebene Handle (HWND) verfügt. Das Handle kann in einem Hexadezimal-oder Dezimaltrennzeichen angegeben werden.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-Fenster <title><br/>                                                            | Überprüft das Fenster, das über den angegebenen Titel verfügt.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -Prozess <name><br/>                       | Überprüft das Hauptfenster des Prozesses, der über den angegebenen Namen verfügt.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -Liste<br/>                                       | Listet alle verfügbaren Überprüfungs Routinen auf.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -Aktivieren <name><br/>                          | Führt die angegebene Überprüfungs Routine aus. Diese Option kann mehrmals angegeben werden.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -Deaktivieren <name><br/> | Führt alle außer der angegebenen Überprüfungs Routine aus. Diese Option kann mehrmals angegeben werden.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -Log (Info \| Warnung \| Err)<br/>                          | Die niedrigste Ereignis Bewertung, die protokolliert wird.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -Logfile <file><br/>                       | Schreibt die Ausgabe in die angegebene Protokolldatei. Diese Option kann mehrmals angegeben werden.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-unterdrücken <file><br/>                                                         | Verwenden Sie die angegebene XML-Datei, um Fehler zu unterdrücken. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-Quiet<br/>                                                                                             | Schreiben Sie die Protokollierungs Ausgabe nicht in stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Hilfe <br/>                           | Zeigt eine schnelle Hilfe an. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Befehlszeilen-Fehler Codes

Die folgenden Fehlercodes werden von der acccheckconsole bei Verwendung von "Echo% ERRORLEVEL%" zurückgegeben.



| Fehlercode                       | BESCHREIBUNG                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Keine Fehler und keine Warnungen.<br/>       |
| <span id="1"></span>1<br/> | Die Verwendung der-Anweisung wurde angefordert. <br/> |
| <span id="2"></span>2<br/> | Fehler und keine Warnungen.<br/>          |
| <span id="3"></span>€<br/> | Fehler und Warnungen.<br/>             |
| <span id="4"></span>4<br/> | Warnungen, aber keine Fehler.<br/>          |
| <span id="5"></span>5@@<br/> | Ungültige Befehlszeile. <br/>           |



 

## <a name="command-line-examples"></a>Befehlszeilen Beispiele

Im folgenden finden Sie einige Beispiele für die Befehlszeile für die Zugriffs Steuerung.

-   Führt alle Überprüfungen in einem Fenster mit einem angegebenen Namen aus.

    **Acccheckconsole-Window "unbenannt-Notepad"**

-   Führen Sie eine Teilmenge der Überprüfungen für ein HWND aus, und geben Sie eine Unterdrückungs Datei an.

    **Acccheckconsole-HWND 0x00382f-enable checktabp-enable checkname-SUPsuppress.xml**

-   Führt alle Überprüfungen aus einer neuen Überprüfungs-dll aus.

    **Acccheckconsole-Window "unbenannt-Notepad" VerificationRoutine1.dll**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





