---
title: Die AccChecker-Konsole
description: AccChecker Console (AccCheckConsole.exe) ist ein Befehlszeilentool zum Überprüfen der Implementierung der Barrierefreiheit der Benutzeroberfläche Ihrer Anwendung.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- AccChecker-Konsole
- AccChecker-Befehlszeilentool
- Befehlszeile, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272447e2513f109206af6fedaaf6adffe665e8b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887035"
---
# <a name="the-accchecker-console"></a>Die AccChecker-Konsole

AccChecker Console (AccCheckConsole.exe) ist ein Befehlszeilentool zum Überprüfen der Implementierung der Barrierefreiheit der Benutzeroberfläche Ihrer Anwendung. Die Befehlszeile akzeptiert eine Vielzahl von Eingaben (z. B. HWND, Fenstertitel und Überprüfungsroutine) und stellt einen Exitcode bereit, der der Fehlerprotokollanzahl entspricht.

-   [Befehlszeilensyntax](#command-line-syntax)
-   [Befehlszeilenfehlercodes](#command-line-error-codes)
-   [Befehlszeilenbeispiele](#command-line-examples)
-   [Zugehörige Themen](#related-topics)

![Befehlszeilentool der Accchecker-Konsole](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die AccChecker-Konsole verfügt über die folgende Befehlszeilensyntax.

**AccCheckConsole-Optionen \[ \] (-hwnd &lt; hwnd &gt; \| -process &lt; name ) &gt; \[ &lt; dlls&gt;\]**

Die Befehlszeilenoptionen sind wie folgt.



| Optionen                                                                                                                                                         | Beschreibung                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd &lt; hwnd&gt;<br/>                                                                     | Überprüft das Fenster mit dem angegebenen Handle (HWND). Das Handle kann in hexidecimal oder decimal angegeben werden.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window &lt; title&gt;<br/>                                                            | Überprüft das Fenster mit dem angegebenen Titel.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process &lt; name&gt;<br/>                       | Überprüft das Hauptfenster des Prozesses mit dem angegebenen Namen.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list<br/>                                       | Listet alle verfügbaren Überprüfungsroutinen auf.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable &lt; name&gt;<br/>                          | Führt die angegebene Überprüfungsroutine aus. Diese Option kann mehr als einmal angegeben werden.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable &lt; name&gt;<br/> | Führt alle bis auf die angegebene Überprüfungsroutine aus. Diese Option kann mehr als einmal angegeben werden.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| warn \| err)<br/>                          | Die niedrigste Ereignisbewertung, die protokolliert wird.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span>&lt;-protokolldatei-Datei&gt;<br/>                       | Schreiben Sie die Ausgabe in die angegebene Protokolldatei. Diese Option kann mehr als einmal angegeben werden.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress &lt; file&gt;<br/>                                                         | Verwenden Sie die angegebene XML-Datei, um Fehler zu unterdrücken. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-quiet<br/>                                                                                             | Schreiben Sie die Protokollierungsausgabe nicht in stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help <br/>                           | Zeigt schnelle Hilfe an. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Befehlszeilenfehlercodes

Im Folgenden finden Sie Fehlercodes, die von AccCheckConsole zurückgegeben werden, wenn "echo %errorlevel%" verwendet wird.



| Fehlercode                       | BESCHREIBUNG                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Keine Fehler und keine Warnungen.<br/>       |
| <span id="1"></span>1<br/> | Die Usages-Anweisung wurde angefordert. <br/> |
| <span id="2"></span>2<br/> | Fehler und keine Warnungen.<br/>          |
| <span id="3"></span>3<br/> | Fehler und Warnungen.<br/>             |
| <span id="4"></span>4<br/> | Warnungen, aber keine Fehler.<br/>          |
| <span id="5"></span>5<br/> | Ungültige Befehlszeile. <br/>           |



 

## <a name="command-line-examples"></a>Befehlszeilenbeispiele

Im Folgenden sind einige Beispiele für die AccChecker-Konsolenbefehlszeile aufgeführt.

-   Führen Sie alle Überprüfungen in einem Fenster mit einem angegebenen Namen aus.

    **AccCheckConsole -window "Untitled - Editor"**

-   Führen Sie eine Teilmenge der Überprüfungen für ein HWND aus, und geben Sie dabei eine Unterdrückungsdatei an.

    **AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**

-   Führen Sie alle Überprüfungen über eine neue Überprüfungs-DLL aus.

    **AccCheckConsole -window "Untitled - Editor" VerificationRoutine1.dll**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





