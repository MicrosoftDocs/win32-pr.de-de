---
description: Die Shell-API stellt Funktionen bereit, die Sie zum Verwalten von Netzwerkdruckern verwenden können. Wenn einer Datei das Druck Verb zugeordnet ist, können Sie den Befehl ShellExecuteEx verwenden, um Sie zu drucken.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Verwalten von Druckern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979953"
---
# <a name="managing-printers"></a>Verwalten von Druckern

Die Shell-API stellt Funktionen bereit, die Sie zum Verwalten von Netzwerkdruckern verwenden können. Wenn einer Datei das **Druck** Verb zugeordnet ist, können Sie den Befehl [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden, um Sie zu drucken.

-   [Druckerverwaltung](#printer-management)
-   [Drucken von Dateien mit ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Druckerverwaltung

Sie können Drucker auf einem System mit der [**shinvokeprintercommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) -Funktion verwalten. Diese Funktion ermöglicht Ihnen Folgendes:

-   Installieren Sie Drucker.
-   Öffnen Sie Drucker.
-   Druckereigenschaften erhalten.
-   Erstellen Sie Drucker Verknüpfungen.
-   Drucken Sie eine Testseite.

## <a name="printing-files-with-shellexecuteex"></a>Drucken von Dateien mit ShellExecuteEx

Wenn einem Dateityp ein Druckbefehl zugeordnet ist, können Sie die Datei drucken, indem Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) mit dem Wert " **Print** " als Verb aufrufen. Dieser Befehl ist häufig identisch mit dem, der für das **geöffnete** Verb verwendet wurde, mit dem Hinzufügen eines Flags, um der Anwendung mitzuteilen, dass die Datei gedruckt werden soll. Beispielsweise können txt-Dateien von Microsoft WordPad gedruckt werden. Das **geöffnete** Verb für eine txt-Datei entspricht daher etwa dem folgenden Befehl:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Wenn Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Drucken einer txt-Datei verwenden, wird die Datei von WordPad geöffnet, gedruckt und dann geschlossen, und die Steuerung wird an die Anwendung zurückgegeben. Die folgende Beispiel Funktion verwendet einen voll qualifizierten Pfad und verwendet **ShellExecuteEx** , um Sie zu drucken, wobei der der Dateinamenerweiterung zugeordnete Print-Befehl verwendet wird.


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



 

 



