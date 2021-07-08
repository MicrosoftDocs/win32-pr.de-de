---
description: Sobald Ihre Anwendung ein Dateiobjekt gefunden hat, besteht der nächste Schritt häufig in einer bestimmten Weise darauf.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Starten von Anwendungen (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508611"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Starten von Anwendungen (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Sobald Ihre Anwendung ein Dateiobjekt gefunden hat, besteht der nächste Schritt häufig in einer bestimmten Weise darauf. Beispielsweise könnte Ihre Anwendung eine andere Anwendung starten, die es dem Benutzer ermöglicht, eine Datendatei zu ändern. Wenn es sich bei der datei von Interesse um eine ausführbare Datei handelt, möchte Ihre Anwendung sie möglicherweise einfach starten. In diesem Dokument wird erläutert, wie [**ShellExecute oder**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**ShellExecuteEx zum**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) Ausführen dieser Aufgaben verwendet wird.

-   [Verwenden von ShellExecute und ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Objektverben](#object-verbs)
    -   [Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungsdiensten von einem Standort](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Verwenden von ShellExecute zum Starten des Suchdialogfelds](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Ein einfaches Beispiel für die Verwendung von ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Verwenden von ShellExecute und ShellExecuteEx

Um [**ShellExecute oder**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)zu verwenden, muss Ihre Anwendung das Datei-  oder Ordnerobjekt angeben, für das bzw. das die Aktion ausgeführt werden soll, sowie ein Verb, das den Vorgang angibt. Weisen **Sie für ShellExecute** diese Werte den entsprechenden Parametern zu. Geben **Sie für ShellExecuteEx** die entsprechenden Member einer [**SHELLEXECUTEINFO-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) ein. Es gibt auch mehrere andere Member oder Parameter, die verwendet werden können, um das Verhalten der beiden Funktionen zu optimieren.

Datei- und Ordnerobjekte können Teil des Dateisystems oder virtueller Objekte sein und entweder durch Pfade oder Zeiger auf Elementbezeichnerlisten (PIDLs) identifiziert werden.

### <a name="object-verbs"></a>Objektverben

Die für ein Objekt verfügbaren Verben sind im Wesentlichen die Elemente, die Sie im Kontextmenü eines Objekts finden. Um herauszufinden, welche Verben verfügbar sind, suchen Sie in der Registrierung unter .

**HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\  \\ *Shellverb*

Wobei *object \_ clsid* der Klassenbezeichner (CLSID) des Objekts und *verb* der Name des verfügbaren Verbs ist. Der  \\ **Unterschlüssel des Verbbefehls** enthält die Daten, die angeben, was geschieht, wenn dieses Verb aufgerufen wird.

Um herauszufinden, welche Verben für vordefinierte [Shellobjekte verfügbar](handlers.md)sind, suchen Sie in der Registrierung unter .

**HKEY \_ CLASSES \_ ROOT-Objektnamen-Shellverb** \\ *\_* \\  \\ 

Wobei *\_ Objektname* der Name des vordefinierten Shell-Objekts ist. Auch hier enthält *der Unterschlüssel* des Verbbefehls die Daten, die angeben, was \\  geschieht, wenn dieses Verb aufgerufen wird.

Zu den häufig verfügbaren Verben gehören:



| Verb       | BESCHREIBUNG                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| Bearbeiten       | Startet einen Editor und öffnet das Dokument zur Bearbeitung.                                                   |
| Suchen       | Initiiert eine Suche ab dem angegebenen Verzeichnis.                                                |
| öffnen       | Startet eine Anwendung. Wenn es sich bei dieser Datei nicht um eine ausführbare Datei handelt, wird die zugehörige Anwendung gestartet. |
| print      | Druckt die Dokumentdatei.                                                                                |
| properties | Zeigt die Eigenschaften des Objekts an.                                                                        |
| RunAs      | Startet eine Anwendung als Administrator. Die Benutzerkontensteuerung (User Account Control, UAC) fordert den Benutzer zur Zustimmung auf, die Anwendung mit erhöhten Rechten ausführen zu können, oder gibt die Anmeldeinformationen eines Administratorkontos ein, das zum Ausführen der Anwendung verwendet wird. |



Jedes Verb entspricht dem Befehl, der zum Starten der Anwendung über ein Konsolenfenster verwendet wird. Das **offene** Verb ist ein gutes Beispiel, da es häufig unterstützt wird. Öffnen .exe, um dateien **zu öffnen,** startet einfach die Anwendung. Es wird jedoch häufiger verwendet, um eine Anwendung zu starten, die für eine bestimmte Datei verwendet wird. Beispielsweise können .txt von Microsoft WordPad geöffnet werden. Das **geöffnete** Verb für eine .txt entspricht daher etwa dem folgenden Befehl:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Wenn Sie [**ShellExecute oder**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden, um eine .txt zu öffnen, wird Wordpad.exe mit der angegebenen Datei als Argument gestartet. Einige Befehle können zusätzliche Argumente wie Flags enthalten, die nach Bedarf hinzugefügt werden können, um die Anwendung ordnungsgemäß zu starten. Weitere Informationen zu Kontextmenüs und Verben finden Sie unter [Erweitern von Kontextmenüs](context.md).

Im Allgemeinen ist der Versuch, die Liste der verfügbaren Verben für eine bestimmte Datei zu bestimmen, etwas kompliziert. In vielen Fällen können Sie einfach den *lpVerb-Parameter* auf **NULL** festlegen, wodurch der Standardbefehl für den Dateityp aufgerufen wird. Dieses Verfahren entspricht in der Regel dem Festlegen *von lpVerb* auf "open", aber einige Dateitypen verfügen möglicherweise über einen anderen Standardbefehl. Weitere Informationen finden Sie unter [Erweitern von Kontextmenüs](context.md) und in der [**Referenzdokumentation zu ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungsdiensten von einem Standort

Die Dienste einer Standortkette können viele Verhaltensweisen der Elementaktivierung steuern. Ab Windows 8 können Sie einen Zeiger auf die Standortkette auf [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) bereitstellen, um diese Verhaltensweisen zu aktivieren. So stellen Sie den Standort für **ShellExecuteEx zur Verfügung:**

-   Geben Sie das FLAG SEE \_ MASK \_ \_ HINST \_ IS SITE im \_ **fMask-Member** von [**SHELLEXECUTEINFO an.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)
-   Geben Sie [**IUnknown im**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **hInstApp-Member** von [**SHELLEXECUTEINFO an.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Verwenden von ShellExecute zum Starten des Suchdialogfelds

Wenn ein Benutzer im Explorer mit der rechten Maustaste auf ein Ordnersymbol Windows, ist eines der Menüelemente "Suchen". Wenn sie dieses Element auswählen, startet die Shell ihr Suchprogramm. Dieses Hilfsprogramm zeigt ein Dialogfeld an, in dem Dateien nach einer angegebenen Textzeichenfolge durchsucht werden können. Eine Anwendung kann programmgesteuert das Suchprogramm für ein Verzeichnis starten, indem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)mit "find" als *lpVerb-Parameter* und dem Verzeichnispfad als *lpFile-Parameter aufruft.* Mit der folgenden Codezeile wird beispielsweise das Hilfsprogramm Suche für das Verzeichnis c: \\ MyPrograms gestartet.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Ein einfaches Beispiel für die Verwendung von ShellExecuteEx

Die folgende Beispielkonsolenanwendung veranschaulicht die Verwendung von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). Die meisten Fehlerüberprüfungscodes wurden aus Gründen der Übersichtlichkeit ausgelassen.


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



Die Anwendung ruft zuerst die PIDL des Windows-Verzeichnisses ab und listet ihren Inhalt auf, bis sie die erste .bmp findet. Im Gegensatz zum früheren Beispiel wird [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um den Analysenamen der Datei anstelle des Anzeigenamens abzurufen. Da es sich um einen Dateisystemordner handelt, ist der Analysename ein vollqualifizierter Pfad, der für [**ShellExecuteEx erforderlich ist.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

Nachdem die erste .bmp gefunden wurde, werden den Membern einer [**SHELLEXECUTEINFO-Struktur entsprechende Werte**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) zugewiesen. Der **lpFile-Member** wird auf den Analysenamen der Datei und der **lpVerb-Member** auf **NULL** festgelegt, um den Standardvorgang zu starten. In diesem Fall ist der Standardvorgang "open". Die -Struktur wird dann an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)übergeben, die den Standardhandler für Bitmapdateien startet, in der Regel MSPaint.exe, um die Datei zu öffnen. Nachdem die Funktion zurückgegeben wurde, werden die PIDLs freigegeben, und Windows [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Ordners wird freigegeben.

 

 
