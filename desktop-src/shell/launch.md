---
description: Sobald Ihre Anwendung ein Dateiobjekt gefunden hat, besteht der nächste Schritt häufig darin, auf irgendeine Weise darauf zu reagieren.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Starten von Anwendungen (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b871e3560ce1cb0c38e91d6ea3baa7a9364c16e500be949b734f9b4b195a24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720218"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Starten von Anwendungen (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Sobald Ihre Anwendung ein Dateiobjekt gefunden hat, besteht der nächste Schritt häufig darin, auf irgendeine Weise darauf zu reagieren. Beispielsweise kann Ihre Anwendung eine andere Anwendung starten, die es dem Benutzer ermöglicht, eine Datendatei zu ändern. Wenn die datei von Interesse eine ausführbare Datei ist, möchte Ihre Anwendung sie möglicherweise einfach starten. In diesem Dokument wird erläutert, wie Sie [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden, um diese Aufgaben auszuführen.

-   [Verwenden von ShellExecute und ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Objektverben](#object-verbs)
    -   [Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungsdiensten von einem Standort](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Verwenden von ShellExecute zum Starten des Suchdialogfelds](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Ein einfaches Beispiel für die Verwendung von ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Verwenden von ShellExecute und ShellExecuteEx

Um [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)zu verwenden, muss Ihre Anwendung das Datei- oder Ordnerobjekt angeben, auf das angewendet werden soll, und ein *Verb,* das den Vorgang angibt. Weisen Sie für **ShellExecute** diese Werte den entsprechenden Parametern zu. Geben Sie für **ShellExecuteEx** die entsprechenden Elemente einer [**SHELLEXECUTEINFO-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) ein. Es gibt auch mehrere andere Member oder Parameter, die verwendet werden können, um das Verhalten der beiden Funktionen zu optimieren.

Datei- und Ordnerobjekte können Teil des Dateisystems oder virtueller Objekte sein und entweder durch Pfade oder Zeiger auf Elementbezeichnerlisten (PIDLs) identifiziert werden.

### <a name="object-verbs"></a>Objektverben

Die für ein Objekt verfügbaren Verben sind im Wesentlichen die Elemente, die Sie im Kontextmenü eines Objekts finden. Um zu ermitteln, welche Verben verfügbar sind, suchen Sie in der Registrierung unter .

**HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\  \\ *Shellverb*

wobei *object \_ clsid* der Klassenbezeichner (CLSID) des Objekts und *verb* der Name des verfügbaren Verbs ist. Der Unterschlüssel des \\ **Verbbefehls** enthält die Daten, die angeben, was geschieht, wenn dieses Verb aufgerufen wird.

Um herauszufinden, welche Verben für [vordefinierte Shell-Objekte](handlers.md)verfügbar sind, suchen Sie in der Registrierung unter

**HKEY \_ CLASSES \_ ROOT object** \\ *\_ name* \\ **shell** \\ *verb*

dabei ist *der \_ Objektname* der Name des vordefinierten Shellobjekts. Auch hier enthält der Unterschlüssel des \\ **Verbbefehls** die Daten, die angeben, was geschieht, wenn dieses Verb aufgerufen wird.

Häufig verfügbare Verben:



| Verb       | BESCHREIBUNG                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| Bearbeiten       | Startet einen Editor und öffnet das Dokument zur Bearbeitung.                                                   |
| Suchen       | Initiiert eine Suche ab dem angegebenen Verzeichnis.                                                |
| öffnen       | Startet eine Anwendung. Wenn es sich bei dieser Datei nicht um eine ausführbare Datei handelt, wird die zugehörige Anwendung gestartet. |
| print      | Druckt die Dokumentdatei.                                                                                |
| properties | Zeigt die Eigenschaften des Objekts an.                                                                        |
| RunAs      | Startet eine Anwendung als Administrator. Die Benutzerkontensteuerung (User Account Control, UAC) fordert den Benutzer zur Zustimmung zur Ausführung der Anwendung mit erhöhten Rechten auf oder gibt die Anmeldeinformationen eines Administratorkontos ein, das zum Ausführen der Anwendung verwendet wird. |



Jedes Verb entspricht dem Befehl, mit dem die Anwendung über ein Konsolenfenster gestartet wird. Das **offene** Verb ist ein gutes Beispiel, da es häufig unterstützt wird. Für .exe Dateien startet **open** einfach die Anwendung. Es wird jedoch häufiger verwendet, um eine Anwendung zu starten, die mit einer bestimmten Datei arbeitet. Beispielsweise können .txt Dateien von Microsoft WordPad geöffnet werden. Das **geöffnete** Verb für eine .txt-Datei würde daher in etwa dem folgenden Befehl entsprechen:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Wenn Sie [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden, um eine .txt Datei zu öffnen, wird Wordpad.exe mit der angegebenen Datei als Argument gestartet. Einige Befehle können zusätzliche Argumente wie Flags aufweisen, die nach Bedarf hinzugefügt werden können, um die Anwendung ordnungsgemäß zu starten. Weitere Informationen zu Kontextmenüs und Verben finden Sie unter [Erweitern von Kontextmenüs.](context.md)

Im Allgemeinen ist der Versuch, die Liste der verfügbaren Verben für eine bestimmte Datei zu bestimmen, etwas kompliziert. In vielen Fällen können Sie einfach den *lpVerb-Parameter* auf **NULL** festlegen, wodurch der Standardbefehl für den Dateityp aufgerufen wird. Dieses Verfahren entspricht in der Regel dem Festlegen von *lpVerb* auf "open", aber einige Dateitypen verfügen möglicherweise über einen anderen Standardbefehl. Weitere Informationen finden Sie unter [Erweitern von Kontextmenüs](context.md) und in der [**ShellExecuteEx-Referenzdokumentation.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungsdiensten von einem Standort

Die Dienste einer Standortkette können viele Verhaltensweisen der Elementaktivierung steuern. Ab Windows 8 können Sie einen Zeiger auf die Websitekette auf [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) bereitstellen, um diese Verhaltensweisen zu aktivieren. So stellen Sie den Standort **für ShellExecuteEx** bereit:

-   Geben Sie das FLAG SEE \_ MASK \_ FLAG \_ HINST IS SITE im \_ \_ **fMask-Member** von [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)an.
-   Geben Sie [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) im **hInstApp-Member** von [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)an.

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Verwenden von ShellExecute zum Starten des Suchdialogfelds

Wenn ein Benutzer in Windows Explorer mit der rechten Maustaste auf ein Ordnersymbol klickt, ist eines der Menüelemente "Suchen". Wenn sie dieses Element auswählen, startet die Shell ihr Suchhilfsprogramm. Dieses Hilfsprogramm zeigt ein Dialogfeld an, das zum Durchsuchen von Dateien nach einer angegebenen Textzeichenfolge verwendet werden kann. Eine Anwendung kann das Suchhilfsprogramm für ein Verzeichnis programmgesteuert starten, indem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)aufgerufen wird, wobei "find" als *lpVerb-Parameter* und der Verzeichnispfad als *lpFile-Parameter* verwendet wird. Mit der folgenden Codezeile wird beispielsweise das Suchhilfsprogramm für das Verzeichnis c: \\ MyPrograms gestartet.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Ein einfaches Beispiel für die Verwendung von ShellExecuteEx

Die folgende Beispielkonsolenanwendung veranschaulicht die Verwendung von [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) Die meisten Fehlerüberprüfungscodes wurden aus Gründen der Übersichtlichkeit ausgelassen.


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



Die Anwendung ruft zuerst die PIDL des Windows Verzeichnisses ab und listet ihren Inhalt auf, bis sie die erste .bmp Datei findet. Im Gegensatz zum vorherigen Beispiel wird [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um den Analysenamen der Datei anstelle des Anzeigenamens abzurufen. Da es sich um einen Dateisystemordner handelt, ist der Analysename ein vollqualifizierter Pfad, der für [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)benötigt wird.

Sobald die erste .bmp Datei gefunden wurde, werden den Membern einer [**SHELLEXECUTEINFO-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) entsprechende Werte zugewiesen. Der **lpFile-Member** wird auf den Analysenamen der Datei und der **lpVerb-Member** auf **NULL** festgelegt, um den Standardvorgang zu starten. In diesem Fall ist der Standardvorgang "open". Die -Struktur wird dann an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)übergeben, wodurch der Standardhandler für Bitmapdateien gestartet wird, in der Regel MSPaint.exe, um die Datei zu öffnen. Nachdem die Funktion zurückgegeben wurde, werden die PIDLs freigegeben, und die [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Windows Ordners wird freigegeben.

 

 
