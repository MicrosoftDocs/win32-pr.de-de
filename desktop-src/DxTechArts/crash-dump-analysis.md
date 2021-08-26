---
title: Absturzabbildanalyse
description: Dieser technische Artikel enthält Informationen zum Schreiben und Verwenden eines Minidumps.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c68891e2e20938036bd016e6e786a2cdad0096ae44af0e8974a88052963be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075520"
---
# <a name="crash-dump-analysis"></a>Absturzabbildanalyse

Nicht alle Fehler können vor der Veröffentlichung gefunden werden. Das bedeutet, dass nicht alle Fehler, die Ausnahmen auslösen, vor dem Release gefunden werden können. Glücklicherweise hat Microsoft eine Funktion in das Platform SDK integriert, mit der Entwickler Informationen zu Ausnahmen sammeln können, die von Benutzern erkannt werden. Die [**MiniDumpWriteDump-Funktion**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) schreibt die erforderlichen Absturzabbildinformationen in eine Datei, ohne den gesamten Prozessspeicherplatz zu sparen. Diese Absturzabbild-Informationsdatei wird als Minidump bezeichnet. Dieser technische Artikel enthält Informationen zum Schreiben und Verwenden eines Minidumps.

-   [Schreiben eines Minidumps](#writing-a-minidump)
-   [Threadsicherheit](#thread-safety)
-   [Schreiben eines Minidumps mit Code](#writing-a-minidump-with-code)
-   [Verwenden von Dumpchk.exe](#using-dumpchkexe)
-   [Analysieren eines Minidumps](#analyzing-a-minidump)
    -   [Verwenden des öffentlichen Microsoft-Symbolservers](#using-the-microsoft-public-symbol-server)
    -   [Debuggen eines Minidumps mit WinDbg](#debugging-a-minidump-with-windbg)
    -   [Verwenden von Copy-Protection Tools mit Minidumps](#using-copy-protection-tools-with-minidumps)
-   [Zusammenfassung](#summary)

## <a name="writing-a-minidump"></a>Schreiben eines Minidumps

Die grundlegenden Optionen zum Schreiben eines Minidumps sind wie folgt:

-   Sie unternehmen nichts. Windows generiert automatisch einen Minidump, wenn ein Programm eine nicht behandelte Ausnahme auslöst. Die automatische Generierung eines Minidumps ist seit Windows XP verfügbar. Wenn der Benutzer dies zulässt, wird der Minidump über Windows-Fehlerberichterstattung (WER) an Microsoft und nicht an den Entwickler gesendet. Entwickler können über das [Windows Desktopanwendungsprogramm](../appxpkg/windows-desktop-application-program.md)auf diese Minidumps zugreifen.

    Die Verwendung von WER erfordert:

    -   Entwickler zum Signieren ihrer Anwendungen mit Authenticode
    -   Anwendungen verfügen in jeder ausführbaren Datei und DLL über eine gültige VERSIONINFO-Ressource.

    Wenn Sie eine benutzerdefinierte Routine für nicht behandelte Ausnahmen implementieren, werden Sie dringend aufgefordert, die [**ReportFault-Funktion**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) im Ausnahmehandler zu verwenden, um auch einen automatisierten Minidump an WER zu senden. Die **ReportFault-Funktion** behandelt alle Probleme beim Herstellen einer Verbindung mit und dem Senden des Minidumps an WER. Das Senden von Minidumps an WER verstößt gegen die Anforderungen von Games for Windows.

    Weitere Informationen zur Funktionsweise von WER finden Sie unter [Funktionsweise von Windows-Fehlerberichterstattung](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). Eine Erläuterung der Registrierungsdetails finden Sie unter Introducing Windows-Fehlerberichterstattung on MSDN es ISV Zone [(Einführung in Windows-Fehlerberichterstattung](https://msdn.microsoft.com/) in der [ISV-Zone](https://msdn.microsoft.com/)von MSDN).

-   Verwenden Sie ein Produkt aus dem Microsoft Visual Studio Team System. Klicken Sie im Menü **Debuggen** auf **Speicherabbild speichern unter** , um eine Kopie eines Speicherabbilds zu speichern. Die Verwendung eines lokal gespeicherten Speicherabbilds ist nur eine Option für das lokale Testen und Debuggen.
-   Fügen Sie Code zu Ihrem Projekt hinzu. Fügen Sie die [**MiniDumpWriteDump-Funktion**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) und den entsprechenden Ausnahmebehandlungscode hinzu, um einen Minidump direkt an den Entwickler zu speichern und zu senden. In diesem Artikel wird veranschaulicht, wie Diese Option implementiert wird. Beachten Sie jedoch, dass **MiniDumpWriteDump** derzeit nicht mit verwaltetem Code funktioniert und nur auf Windows XP, Windows Vista Windows 7 verfügbar ist.

## <a name="thread-safety"></a>Threadsicherheit

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) ist Teil der DBGHELP-Bibliothek. Diese Bibliothek ist nicht threadsicher, daher sollte jedes Programm, das **MiniDumpWriteDump** verwendet, alle Threads synchronisieren, bevor versucht **wird, MiniDumpWriteDump** aufzurufen.

## <a name="writing-a-minidump-with-code"></a>Schreiben eines Minidumps mit Code

Die tatsächliche Implementierung ist einfach. Im Folgenden wird ein einfaches Beispiel für die Verwendung von [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)veranschaulicht.


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



In diesem Beispiel werden die grundlegende Verwendung von [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) und die für den Aufruf erforderlichen Mindestinformationen veranschaulicht. Der Name der Speicherabbilddatei liegt beim Entwickler. Um Dateinamenkonflikte zu vermeiden, empfiehlt es sich jedoch, den Dateinamen aus dem Namen und der Versionsnummer der Anwendung, den Prozess- und Thread-IDs sowie dem Datum und der Uhrzeit zu generieren. Dies hilft auch dabei, die Minidumps nach Anwendung und Version gruppiert zu halten. Der Entwickler muss entscheiden, wie viele Informationen zur Unterscheidung von Minidump-Dateinamen verwendet werden.

Beachten Sie, dass der Pfadname im vorherigen Beispiel durch Aufrufen der [**GetTempPath-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) generiert wurde, um den Pfad des Verzeichnisses abzurufen, das für temporäre Dateien festgelegt ist. Die Verwendung dieses Verzeichnisses funktioniert auch bei Benutzerkonten mit den geringsten Berechtigungen und verhindert außerdem, dass der Minidump Festplattenspeicher einnimmt, nachdem er nicht mehr benötigt wird.

Wenn Sie das Produkt während des täglichen Buildprozesses archivieren, stellen Sie außerdem sicher, dass Sie Symbole für den Build einschließen, damit Sie bei Bedarf eine alte Version des Produkts debuggen können. Sie müssen auch Schritte ausführen, um vollständige Compileroptimierungen beim Generieren von Symbolen beizubehalten. Öffnen Sie hierzu die Eigenschaften Ihres Projekts in der Entwicklungsumgebung, und gehen Sie für die Releasekonfiguration wie folgt vor:

1.  Klicken Sie links auf der Eigenschaftenseite des Projekts auf C/C++. Standardmäßig werden hier **allgemeine** Einstellungen angezeigt. Legen Sie rechts auf der Eigenschaftenseite des Projekts **Debuginformationsformat** auf **Programmdatenbank (/Zi)** fest.
2.  Erweitern Sie links auf der Eigenschaftenseite **linker**, und klicken Sie dann auf **Debuggen.** Legen Sie auf der rechten Seite der Eigenschaftenseite **Debuginformationen generieren** auf **Ja (/DEBUG)** fest.
3.  Klicken Sie auf **Optimierung**, und legen Sie **Verweise** auf Nicht **referenzierte Daten (/OPT:REF)** fest.
4.  Legen **Sie COMDAT Folding aktivieren** fest, um **redundante COMDATs (/OPT:ICF)** zu entfernen.

MSDN enthält ausführlichere Informationen zur [**MINIDUMP \_ EXCEPTION \_ INFORMATION-Struktur**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) und zur [**MiniDumpWriteDump-Funktion.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)

## <a name="using-dumpchkexe"></a>Verwenden von Dumpchk.exe

Dumpchk.exe ist ein Befehlszeilenprogramm, mit dem überprüft werden kann, ob eine Sicherungsdatei ordnungsgemäß erstellt wurde. Wenn Dumpchk.exe einen Fehler generiert, ist die Dumpdatei beschädigt und kann nicht analysiert werden. Informationen zur Verwendung von Dumpchk.exe finden Sie unter [Verwenden von Dumpchk.exe zum Überprüfen einer Speicherabbilddatei.](https://support.microsoft.com/kb/315271/)

Dumpchk.exe ist auf der Windows XP-Produkt-CD enthalten und kann in den Supporttools für Systemlaufwerkprogrammdateien installiert werden, \\ indem Setup.exe im Ordner \\ \\ \\ Supporttools auf der \\ produkt-CD Windows XP ausgeführt wird. Sie können auch die neueste Version von Dumpchk.exe abrufen, indem Sie die Debugtools herunterladen und installieren, die über [Windows Debugtools](https://www.microsoft.com/whdc/devtools/debugging/) auf [Windows Hardware Developer Central](https://www.microsoft.com/whdc/)verfügbar sind.

## <a name="analyzing-a-minidump"></a>Analysieren eines Minidumps

Das Öffnen eines Minidumps für die Analyse ist so einfach wie das Erstellen eines Minidumps.

**So analysieren Sie einen Minidump**

1.  Öffnen Sie Visual Studio.
2.  Klicken Sie im Menü **Datei** auf **Project öffnen.**
3.  Legen Sie **Dateien vom Typ** auf **Dumpdateien** fest, navigieren Sie zur Dumpdatei, wählen Sie sie aus, und klicken Sie auf **Öffnen.**
4.  Führen Sie den Debugger aus.

Der Debugger erstellt einen simulierten Prozess. Der simulierte Prozess wird bei der Anweisung angehalten, die den Absturz verursacht hat.

### <a name="using-the-microsoft-public-symbol-server"></a>Verwenden des öffentlichen Microsoft-Symbolservers

Um den Stapel für Abstürze auf Treiber- oder Systemebene abzurufen, ist es möglicherweise erforderlich, Visual Studio so zu konfigurieren, dass er auf den öffentlichen Microsoft-Symbolserver verweist.

**So legen Sie einen Pfad zum Microsoft-Symbolserver fest**

1.  Klicken Sie im Menü **Debuggen** auf **Optionen**.
2.  Öffnen **Sie** im Dialogfeld Optionen den Knoten **Debuggen,** und klicken Sie auf **Symbole.**
3.  Stellen Sie sicher, dass **Die oben genannten Speicherorte nur dann suchen, wenn Symbole manuell geladen werden** nicht ausgewählt ist, es sei denn, Sie möchten Symbole beim Debuggen manuell laden.
4.  Wenn Sie Symbole auf einem Remotesymbolserver verwenden, können Sie die Leistung verbessern, indem Sie ein lokales Verzeichnis angeben, in das Symbole kopiert werden können. Geben Sie hierzu einen Pfad für **Symbole zwischenspeichern vom Symbolserver zu diesem Verzeichnis** ein. Um eine Verbindung mit dem öffentlichen Microsoft-Symbolserver herzustellen, müssen Sie diese Einstellung aktivieren. Beachten Sie, dass sich das Cacheverzeichnis beim Debuggen eines Programms auf einem Remotecomputer auf ein Verzeichnis auf dem Remotecomputer bezieht.
5.  Klicken Sie auf **OK**.
6.  Da Sie den öffentlichen Microsoft-Symbolserver verwenden, wird das Dialogfeld Endbenutzer-Lizenzvertrag angezeigt. Klicken Sie auf **Ja,** um die Vereinbarung zu akzeptieren und Symbole in Ihren lokalen Cache herunterzuladen.

### <a name="debugging-a-minidump-with-windbg"></a>Debuggen eines Minidumps mit WinDbg

Sie können auch WinDbg verwenden, einen Debugger, der Teil der Windows Debugtools ist, um einen Minidump zu debuggen. Mit WinDbg können Sie debuggen, ohne Visual Studio verwenden zu müssen. Informationen zum Herunterladen Windows Debugtools finden Sie unter [Windows Debugtools](https://www.microsoft.com/whdc/devtools/debugging/) auf [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

Nach der Installation Windows Debugtools müssen Sie den Symbolpfad in WinDbg eingeben.

**So geben Sie einen Symbolpfad in WinDbg ein**

1.  Klicken Sie im Menü **Datei** auf **Symbolpfad**.
2.  Geben Sie im Fenster **Symbolsuchepfad** Folgendes ein:

    "srv \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Verwenden von Copy-Protection Tools mit Minidumps

Entwickler müssen auch wissen, wie sich ihr Kopierschutzschema auf den Minidump auswirken kann. Die meisten Kopierschutzschemas verfügen über eigene Descramble-Tools, und der Entwickler muss lernen, wie diese Tools mit [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)verwendet werden.

## <a name="summary"></a>Zusammenfassung

Die [**MiniDumpWriteDump-Funktion**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) kann ein äußerst nützliches Tool zum Sammeln und Beheben von Fehlern sein, nachdem das Produkt veröffentlicht wurde. Durch das Schreiben eines benutzerdefinierten Ausnahmehandlers, der **MiniDumpWriteDump** verwendet, kann der Entwickler die Informationssammlung anpassen und den Debugprozess verbessern. Die Funktion ist flexibel genug, um in jedem C++-basierten Projekt verwendet zu werden und sollte als Teil des Stabilitätsprozesses jedes Projekts betrachtet werden.

 

 