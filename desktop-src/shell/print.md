---
description: Die Shell-API stellt Funktionen bereit, mit denen Sie Netzwerkdrucker verwalten können. Wenn einer Datei das Druckverb zugeordnet ist, können Sie sie mit dem Befehl ShellExecuteEx drucken.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Verwalten von Druckern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7086b360355d0ad85be440bc8bc9e330bfa6dd25793cc943d3aacdbaa0d4a8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719598"
---
# <a name="managing-printers"></a>Verwalten von Druckern

Die Shell-API stellt Funktionen bereit, mit denen Sie Netzwerkdrucker verwalten können. Wenn einer Datei das **Druckverb** zugeordnet ist, können Sie sie mit dem [**Befehl ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) drucken.

-   [Druckerverwaltung](#printer-management)
-   [Drucken von Dateien mit ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Druckerverwaltung

Sie können Drucker auf einem System mit der [**SHInvokePrinterCommand-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) verwalten. Mit dieser Funktion können Sie:

-   Installieren Sie Drucker.
-   Öffnen Sie Drucker.
-   Hier erhalten Sie Druckereigenschaften.
-   Erstellen sie Druckerlinks.
-   Drucken Sie eine Testseite.

## <a name="printing-files-with-shellexecuteex"></a>Drucken von Dateien mit ShellExecuteEx

Wenn einem Dateityp ein Druckbefehl zugeordnet ist, können Sie die Datei drucken, indem Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) mit **print** als Verb aufrufen. Dieser Befehl ist häufig mit dem  für das geöffnete Verb identisch, mit dem Zusatz eines Flags, das die Anwendung anfing, die Datei zu drucken. Beispielsweise können .txt von Microsoft WordPad gedruckt werden. Das **offene** Verb für eine .txt würde daher etwa dem folgenden Befehl entsprechen:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Wenn Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Drucken einer .txt-Datei verwenden, öffnet WordPad die Datei, druckt sie und schließt sie dann und gibt die Steuerung an die Anwendung zurück. Die folgende Beispielfunktion verwendet einen vollqualifizierten Pfad und verwendet **ShellExecuteEx,** um sie mithilfe des Druckbefehls zu drucken, der der Dateierweiterung zugeordnet ist.


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



