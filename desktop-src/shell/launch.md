---
description: Nachdem die Anwendung ein Datei Objekt gefunden hat, besteht der nächste Schritt häufig darin, auf irgendeine Weise darauf zu reagieren.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Starten von Anwendungen (ShellExecute, ShellExecuteEx, shellexecuteinfo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864127"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Starten von Anwendungen (ShellExecute, ShellExecuteEx, shellexecuteinfo)

Nachdem die Anwendung ein Datei Objekt gefunden hat, besteht der nächste Schritt häufig darin, auf irgendeine Weise darauf zu reagieren. Beispielsweise kann Ihre Anwendung eine andere Anwendung starten, die es dem Benutzer ermöglicht, eine Datendatei zu ändern. Wenn es sich bei der gewünschten Datei um eine ausführbare Datei handelt, kann Sie von Ihrer Anwendung einfach gestartet werden. In diesem Dokument wird erläutert, wie [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Ausführen dieser Aufgaben verwendet wird.

-   [Verwenden von ShellExecute und ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Objekt Verben](#object-verbs)
    -   [Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungs Diensten von einem Standort](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Verwenden von ShellExecute zum Starten des Dialog Felds "suchen"](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Ein einfaches Beispiel für die Verwendung von ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Verwenden von ShellExecute und ShellExecuteEx

Um [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)verwenden zu können, muss Ihre Anwendung das Datei-oder Ordner Objekt angeben, für das die Aktion durchgeführt werden soll, und ein *Verb* , das den Vorgang angibt. Weisen Sie diese Werte für **ShellExecute** den entsprechenden Parametern zu. Füllen Sie für **ShellExecuteEx** die entsprechenden Member einer [**shellexecuteinfo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) -Struktur aus. Es gibt auch mehrere andere Member oder Parameter, die verwendet werden können, um das Verhalten der beiden Funktionen zu optimieren.

Datei-und Ordner Objekte können Teil des Dateisystems oder der virtuellen Objekte sein. Sie können entweder durch Pfade oder Zeiger auf elementbezeichnerlisten (pidls) identifiziert werden.

### <a name="object-verbs"></a>Objekt Verben

Die für ein Objekt verfügbaren Verben sind im Wesentlichen die Elemente, die im Kontextmenü eines Objekts gefunden werden. Um zu ermitteln, welche Verben verfügbar sind, suchen Sie in der Registrierung unter

**HKEY \_ Klassen \_** Stamm- \\ **CLSID** \\ *{Object \_ CLSID}* \\  \\ *shellverb*

Dabei ist die *Objekt- \_ CLSID* der Klassen Bezeichner (CLSID) des Objekts, und das *Verb* ist der Name des verfügbaren Verbs. Der Unterschlüssel des *Verbs*- \\ **Befehls** enthält die Daten, die angeben, was geschieht, wenn das Verb aufgerufen wird.

Wenn Sie herausfinden möchten, welche Verben für [vordefinierte Shellobjekte](handlers.md)verfügbar sind, suchen Sie in der Registrierung unter

**HKEY \_ Klassen \_** Stamm \\ *Objekt \_ Name* \\  \\ *shellverb*

Where *Object \_ Name* ist der Name des vordefinierten shellobjekts. Der Unterschlüssel des *Verbs*- \\ **Befehls** enthält die Daten, die angeben, was geschieht, wenn das Verb aufgerufen wird.

Häufig verfügbare Verben sind:



| Verb       | BESCHREIBUNG                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| Bearbeiten       | Öffnet einen Editor und öffnet das Dokument zum Bearbeiten.                                                   |
| Suchen       | Initiiert eine Suche beginnend mit dem angegebenen Verzeichnis.                                                |
| open       | Hiermit wird eine Anwendung gestartet. Wenn es sich bei dieser Datei nicht um eine ausführbare Datei handelt, wird die zugehörige Anwendung gestartet. |
| print      | Druckt die Dokument Datei.                                                                                |
| properties | Zeigt die Eigenschaften des Objekts an.                                                                        |
| RunAs      | Hiermit wird eine Anwendung als Administrator gestartet. Benutzerkontensteuerung (User Account Control, UAC) fordert den Benutzer zur Zustimmung zu |
|            | Ausführen der Anwendung mit erhöhten Rechten oder eingeben der Anmelde Informationen eines Administrator Kontos, das zum Ausführen des        |
|            | Anwendung.                                                                                             |

 

Jedes Verb entspricht dem Befehl, der zum Starten der Anwendung aus einem Konsolenfenster verwendet wird. Das **offene** Verb ist ein gutes Beispiel, da es häufig unterstützt wird. **Öffnen** Sie für exe-Dateien einfach die Anwendung. Es wird jedoch häufiger verwendet, um eine Anwendung zu starten, die für eine bestimmte Datei verwendet wird. Beispielsweise können txt-Dateien von Microsoft WordPad geöffnet werden. Das **geöffnete** Verb für eine txt-Datei entspricht daher etwa dem folgenden Befehl:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Wenn Sie [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Öffnen einer txt-Datei verwenden, wird Wordpad.exe mit der angegebenen Datei als Argument gestartet. Einige Befehle können über zusätzliche Argumente verfügen, z. b. Flags, die nach Bedarf hinzugefügt werden können, um die Anwendung ordnungsgemäß zu starten. Weitere Informationen zu Kontextmenüs und Verben finden Sie unter Erweitern von Kontext [Menüs](context.md).

Im Allgemeinen ist der Versuch, die Liste der verfügbaren Verben für eine bestimmte Datei zu ermitteln, etwas kompliziert. In vielen Fällen können Sie einfach den *lpverb* -Parameter auf **null** festlegen, wodurch der Standardbefehl für den Dateityp aufgerufen wird. Diese Prozedur entspricht in der Regel dem Festlegen von *lpverb* auf "Open", aber einige Dateitypen verfügen möglicherweise über einen anderen Standardbefehl. Weitere Informationen finden Sie unter [erweitern](context.md) von Kontextmenüs und der Referenz Dokumentation zu [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungs Diensten von einem Standort

Die Dienste einer Website Kette können viele Verhaltensweisen der Element Aktivierung steuern. Ab Windows 8 können Sie einen Zeiger auf die Site Kette auf [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) bereitstellen, um diese Verhaltensweisen zu aktivieren. So geben Sie **ShellExecuteEx** den Standort an:

-   Geben Sie \_ \_ \_ \_ \_ im **fmask** -Member von [**shellexecuteingefo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)das Flag hInst is-Flag für das Masken Kennzeichen anzeigen an.
-   Stellen Sie das [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Element im **hinstapp** -Mitglied von [**shellexecuteingefo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)bereit.

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Verwenden von ShellExecute zum Starten des Dialog Felds "suchen"

Wenn ein Benutzer mit der rechten Maustaste auf ein Ordnersymbol in Windows-Explorer klickt, ist eines der Menü Elemente "suchen". Wenn Sie dieses Element auswählen, wird das Such Dienstprogramm der Shell gestartet. Dieses Hilfsprogramm zeigt ein Dialogfeld an, das zum Durchsuchen von Dateien nach einer angegebenen Text Zeichenfolge verwendet werden kann. Eine Anwendung kann das Such Dienstprogramm für ein Verzeichnis Programm gesteuert starten, indem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)aufgerufen wird, wobei "Find" als *lpverb* -Parameter und der Verzeichnispfad als *lpder* -Parameter angegeben wird. Beispielsweise wird mit der folgenden Codezeile das Such Dienstprogramm für das Verzeichnis "c: \\ myprograms" gestartet.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Ein einfaches Beispiel für die Verwendung von ShellExecuteEx

Die folgende Beispiel Konsolenanwendung veranschaulicht die Verwendung von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). Der größte Fehler Überprüfungs Code wurde aus Gründen der Übersichtlichkeit ausgelassen.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



Die Anwendung ruft zunächst die PIDL des Windows-Verzeichnisses ab und listet ihren Inhalt auf, bis die erste BMP-Datei gefunden wird. Im Gegensatz zum vorherigen Beispiel wird [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um den Namen der Datei statt des anzeigen Amens abzurufen. Da es sich hierbei um einen Dateisystem Ordner handelt, ist der namens Name ein voll qualifizierter Pfad, der für [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)erforderlich ist.

Nachdem die erste BMP-Datei gefunden wurde, werden die entsprechenden Werte den Elementen einer [**shellexecuteinfo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) -Struktur zugewiesen. Das **lpfile** -Element wird auf den Namen der Datei und den **lpverb** -Member auf **null** festgelegt, um den Standard Vorgang zu starten. In diesem Fall ist der Standard Vorgang "Open". Die Struktur wird dann an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)übergeben, wodurch der Standard Handler für Bitmapdateien gestartet wird, in der Regel MSPaint.exe, um die Datei zu öffnen. Nachdem die Funktion zurückgegeben wurde, werden die pidls freigegeben, und die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Windows-Ordners wird freigegeben.

 

 
