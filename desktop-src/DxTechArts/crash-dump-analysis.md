---
title: Absturz Abbild Analyse
description: Dieser technische Artikel enthält Informationen zum Schreiben und Verwenden eines minidumpdiensts.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039243"
---
# <a name="crash-dump-analysis"></a>Absturz Abbild Analyse

Vor der Freigabe können nicht alle Fehler gefunden werden. Dies bedeutet, dass nicht alle Fehler, die Ausnahmen auslösen, vor der Freigabe gefunden werden können. Glücklicherweise hat Microsoft in das Platform SDK eine Funktion integriert, um Entwicklern bei der Erfassung von Informationen zu Ausnahmen zu helfen, die von Benutzern erkannt werden. Die [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion schreibt die erforderlichen Absturz Abbild Informationen in eine Datei, ohne den gesamten Prozessbereich zu speichern. Diese Datei mit Absturz Abbild Informationen wird als Minidump bezeichnet. Dieser technische Artikel enthält Informationen zum Schreiben und Verwenden eines minidumpdiensts.

-   [Schreiben eines Minidumps](#writing-a-minidump)
-   [Thread Sicherheit](#thread-safety)
-   [Schreiben eines minidumpcodes mit Code](#writing-a-minidump-with-code)
-   [Verwenden von Dumpchk.exe](#using-dumpchkexe)
-   [Analysieren eines minidumpdiensts](#analyzing-a-minidump)
    -   [Verwenden des öffentlichen Symbol Servers von Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Debuggen eines Minidumps mit WinDbg](#debugging-a-minidump-with-windbg)
    -   [Verwenden von Copy-Protection Tools mit Minidumps](#using-copy-protection-tools-with-minidumps)
-   [Zusammenfassung](#summary)

## <a name="writing-a-minidump"></a>Schreiben eines Minidumps

Die grundlegenden Optionen zum Schreiben eines Minidumps lauten wie folgt:

-   Sie unternehmen nichts. Windows generiert automatisch ein Minidump, wenn ein Programm eine nicht behandelte Ausnahme auslöst. Die automatische Generierung eines minidumpdiensts ist seit Windows XP verfügbar. Wenn der Benutzer dies zulässt, wird das Minidump über Windows-Fehlerberichterstattung (wer) an Microsoft gesendet und nicht an den Entwickler. Entwickler können über das [Windows-Desktop Anwendungsprogramm](../appxpkg/windows-desktop-application-program.md)auf diese Minidumps zugreifen.

    Die Verwendung von wer erfordert Folgendes:

    -   Entwickler zum Signieren Ihrer Anwendungen mit Authenticode
    -   Anwendungen verfügen über eine gültige VERSIONINFO-Ressource in jeder ausführbaren Datei und dll.

    Wenn Sie eine benutzerdefinierte Routine für nicht behandelte Ausnahmen implementieren, werden Sie nachdrücklich aufgefordert, die [**Report Fault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) -Funktion im Ausnahmehandler zu verwenden, um auch einen automatisierten Minidump an wer zu senden. Die Funktion **Report Fault** behandelt alle Probleme, die beim Herstellen einer Verbindung mit und dem Senden des Minidump an wer auftreten. Das Senden von Minidumps an wer verstößt gegen die Anforderungen von Spielen für Windows.

    Weitere Informationen zur Funktionsweise von wer finden Sie unter [Funktionsweise von Windows-Fehlerberichterstattung](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). Eine Erläuterung der Registrierungsdetails finden Sie unter [Introducing Windows-Fehlerberichterstattung](https://msdn.microsoft.com/) in der MSDN- [ISV-Zone](https://msdn.microsoft.com/).

-   Verwenden Sie ein Produkt aus dem Microsoft Visual Studio Team System. Klicken Sie im Menü **Debuggen** auf **Dump speichern** unter, um eine Kopie eines dumpspeichers zu speichern. Die Verwendung eines lokal gespeicherten dumpdiensts ist nur eine Option für internes testen und Debuggen.
-   Fügen Sie Ihrem Projekt Code hinzu. Fügen Sie die [**minidumpbeschreib tedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion und den entsprechenden Code für die Ausnahmebehandlung hinzu, um ein Minidump direkt an den Entwickler zu speichern und zu senden. In diesem Artikel wird veranschaulicht, wie diese Option implementiert wird. Beachten Sie jedoch, dass **minidumpbeschreib tedump** derzeit nicht mit verwaltetem Code funktioniert und nur unter Windows XP, Windows Vista, Windows 7 verfügbar ist.

## <a name="thread-safety"></a>Threadsicherheit

[**Minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) ist Teil der DbgHelp-Bibliothek. Diese Bibliothek ist nicht Thread sicher, daher sollte jedes Programm, das **minidumpschreitedump** verwendet, alle Threads synchronisieren, bevor versucht wird, **minidumpschreitedump** aufzurufen.

## <a name="writing-a-minidump-with-code"></a>Schreiben eines minidumpcodes mit Code

Die tatsächliche Implementierung ist einfach. Im folgenden finden Sie ein einfaches Beispiel für die Verwendung von [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



Dieses Beispiel veranschaulicht die grundlegende Verwendung von [**minidumpbeschreib tedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) und die minimalen Informationen, die erforderlich sind, um es aufzurufen. Der Name der Dumpdatei ist für den Entwickler. um Dateinamen Konflikte zu vermeiden, empfiehlt es sich jedoch, den Dateinamen aus dem Namen und der Versionsnummer der Anwendung, die Prozess-und Thread-IDs sowie das Datum und die Uhrzeit zu generieren. Dies trägt auch dazu bei, dass die Minidumps nach Anwendung und Version gruppiert bleiben. Der Entwickler kann entscheiden, wie viele Informationen zur Unterscheidung von Minidump-Dateinamen verwendet werden.

Beachten Sie, dass der Pfadname im vorangehenden Beispiel durch Aufrufen der [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) -Funktion generiert wurde, um den Pfad des für temporäre Dateien vorgesehenen Verzeichnisses abzurufen. Die Verwendung dieses Verzeichnisses funktioniert auch mit Benutzerkonten mit den geringsten Rechten. Außerdem wird verhindert, dass der Minidump Festplattenspeicher belegt, wenn er nicht mehr benötigt wird.

Wenn Sie das Produkt während des täglichen Buildvorgangs archivieren, achten Sie auch darauf, dass Sie Symbole für den Build einschließen, damit Sie ggf. eine alte Version des Produkts Debuggen können. Außerdem müssen Sie Maßnahmen ergreifen, um bei der Erstellung von Symbolen vollständige Compileroptimierungen zu erhalten. Dies können Sie erreichen, indem Sie die Eigenschaften des Projekts in der Entwicklungsumgebung öffnen und für die Releasekonfiguration Folgendes ausführen:

1.  Klicken Sie auf der linken Seite der Eigenschaften Seite des Projekts auf C/C++. In der Standardeinstellung werden **Allgemeine** Einstellungen angezeigt. Legen Sie auf der rechten Seite der Eigenschaften Seite des Projekts **Debug-Informations Format** auf **Programmdatenbank (/Zi)** fest.
2.  Erweitern Sie auf der linken Seite der Eigenschaften Seite **Linker**, und klicken Sie dann auf **Debuggen**. Legen Sie auf der rechten Seite der Eigenschaften Seite **Debuginformationen generieren** auf **Ja (/Debug)** fest.
3.  Klicken Sie auf **Optimierung**, und legen Sie **Verweise** auf **nicht referenzierte Daten (/opt: Ref)** fest.
4.  Legen Sie **COMDAT-Faltung aktivieren** fest, um **Redundante COMDATs (/opt: ICF) zu entfernen**.

MSDN enthält ausführlichere Informationen zur [**Minidump- \_ Ausnahme \_ Informations**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) Struktur und der [**minidumpbeschreib tedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion.

## <a name="using-dumpchkexe"></a>Verwenden von Dumpchk.exe

Dumpchk.exe ist ein Befehlszeilenprogramm, das verwendet werden kann, um zu überprüfen, ob eine Dumpdatei ordnungsgemäß erstellt wurde. Wenn Dumpchk.exe einen Fehler generiert, ist die Dumpdatei beschädigt und kann nicht analysiert werden. Weitere Informationen zur Verwendung von Dumpchk.exe finden [Sie unter Verwenden von Dumpchk.exe zum Überprüfen einer Speicher](https://support.microsoft.com/kb/315271/)Abbild Datei.

Dumpchk.exe ist auf der Windows XP-Produkt-CD enthalten und kann auf System Drive \\ Program Files-Support Tools installiert werden, \\ \\ indem Setup.exe im Ordner "Support \\ Tools" \\ auf der Windows XP-Produkt-CD ausgeführt wird. Sie können auch die neueste Version von Dumpchk.exe herunterladen, indem Sie die Debugtools herunterladen und installieren, die in den [Windows-Debugtools](https://www.microsoft.com/whdc/devtools/debugging/) unter [Windows Hardware Developer Central](https://www.microsoft.com/whdc/)verfügbar

## <a name="analyzing-a-minidump"></a>Analysieren eines minidumpdiensts

Das Öffnen eines Minidump für die Analyse ist so einfach wie das Erstellen eines Minidump.

**So analysieren Sie ein Minidump**

1.  Öffnen Sie Visual Studio.
2.  Klicken Sie im Menü **Datei** auf **Projekt öffnen**.
3.  Legen Sie **Dateityp** auf **Dumpdateien** fest, navigieren Sie zu der Dumpdatei, wählen Sie Sie aus, und klicken Sie auf **Öffnen.**
4.  Führen Sie den Debugger aus.

Der Debugger erstellt einen simulierten Prozess. Der simulierte Prozess wird bei der Anweisung angehalten, die den Absturz verursacht hat.

### <a name="using-the-microsoft-public-symbol-server"></a>Verwenden des öffentlichen Symbol Servers von Microsoft

Um den Stapel für Abstürze auf Treiber-oder Systemebene zu erhalten, kann es erforderlich sein, Visual Studio so zu konfigurieren, dass er auf den öffentlichen Microsoft-Symbol Server verweist.

**So legen Sie einen Pfad zum Microsoft-Symbol Server fest**

1.  Klicken Sie im Menü **Debuggen** auf **Optionen**.
2.  Öffnen Sie im Dialogfeld **Optionen** den Knoten **Debuggen** , und klicken Sie auf **Symbole**.
3.  Stellen Sie sicher, dass Sie **die obigen Speicherorte nur durchsuchen, wenn Symbole manuell geladen werden** nicht ausgewählt ist, es sei denn, Sie möchten Symbole beim Debuggen manuell laden
4.  Wenn Sie Symbole auf einem Remote Symbol Server verwenden, können Sie die Leistung verbessern, indem Sie ein lokales Verzeichnis angeben, in das Symbole kopiert werden können. Geben Sie hierzu einen Pfad für **das Zwischenspeichern von Symbolen von Symbol Server zu diesem Verzeichnis** ein. Zum Herstellen einer Verbindung mit dem öffentlichen Symbol Server von Microsoft müssen Sie diese Einstellung aktivieren. Beachten Sie Folgendes: Wenn Sie ein Programm auf einem Remote Computer Debuggen, verweist das Cache Verzeichnis auf ein Verzeichnis auf dem Remote Computer.
5.  Klicken Sie auf **OK**.
6.  Da Sie den öffentlichen Microsoft-Symbol Server verwenden, wird das Dialogfeld Endbenutzer-Lizenzvertrag angezeigt. Klicken Sie auf **Ja** , um die Vereinbarung zu akzeptieren und Symbole in Ihren lokalen Cache herunterzuladen.

### <a name="debugging-a-minidump-with-windbg"></a>Debuggen eines Minidumps mit WinDbg

Sie können auch WinDbg verwenden, einen Debugger, der Teil der Windows-Debuggingtools ist, um ein Minidump zu debuggen. WinDbg ermöglicht das Debuggen, ohne Visual Studio verwenden zu müssen. Informationen zum Herunterladen der Windows-Debuggingtools finden Sie unter Windows- [Debugtools](https://www.microsoft.com/whdc/devtools/debugging/) unter [Windows Hardware](https://www.microsoft.com/whdc/)

Nachdem Sie die Windows-Debuggingtools installiert haben, müssen Sie den Symbol Pfad in WinDbg eingeben.

**So geben Sie einen Symbol Pfad in WinDbg ein**

1.  Klicken Sie im Menü **Datei** auf **Symbol Pfad**.
2.  Geben Sie im Fenster **Symbol Suchpfad** Folgendes ein:

    "SRV \* c: \\ Cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Verwenden von Copy-Protection Tools mit Minidumps

Entwickler müssen auch wissen, wie sich das Kopierschutz Schema auf das Minidump auswirken könnte. Die meisten Kopierschutz Schemas verfügen über eigene, abzurufbare Tools, und es ist für den Entwickler zu erfahren, wie diese Tools mit [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)verwendet werden.

## <a name="summary"></a>Zusammenfassung

Die [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion kann ein äußerst nützliches Tool zum Erfassen und lösen von Fehlern sein, nachdem das Produkt veröffentlicht wurde. Durch das Schreiben eines benutzerdefinierten Ausnahme Handlers, der **MiniDumpWriteDump** verwendet, kann der Entwickler die Informationssammlung anpassen und den Debugprozess verbessern. Die-Funktion ist flexibel genug, um in jedem C++ basierten Projekt verwendet zu werden, und sollte als Teil des Stabilitäts Prozesses eines beliebigen Projekts betrachtet werden.

 

 