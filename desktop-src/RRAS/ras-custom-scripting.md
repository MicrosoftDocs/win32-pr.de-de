---
title: Benutzerdefinierte RAS-Skript
description: Entwickler können eine benutzerdefinierte Skript-DLL erstellen, die sich auf einem RAS-Client Computer befindet. Diese DLL kann während der Verbindungs Herstellung mit dem Server kommunizieren.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c625f020d9dafcb352c5f1b382014f9dba189330
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948849"
---
# <a name="ras-custom-scripting"></a>Benutzerdefinierte RAS-Skript

Entwickler können eine benutzerdefinierte Skript-DLL erstellen, die sich auf einem RAS-Client Computer befindet. Diese DLL kann während der Verbindungs Herstellung mit dem Server kommunizieren.

**Windows NT:** Die benutzerdefinierte Skripterstellung ist nicht verfügbar.

## <a name="setting-up-the-dll"></a>Einrichten der dll

Um die dll einzurichten, erstellen Sie einen Wert mit dem Namen " **customscriptdllpath** " unter dem folgenden Registrierungsschlüssel:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Dieser Wert muss vom Typ " **reg \_ Expand \_ SZ**" sein. Der Wert sollte den Pfad zur benutzerdefinierten Skript-dll enthalten. Nur eine benutzerdefinierte Skript-dll wird für jeden RAS-Client Computer unterstützt.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interaktion zwischen dem Server, RAS und der Custom-Scripting-dll

Die benutzerdefinierte Skript-DLL sollte einen einzelnen Einstiegspunkt exportieren: [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS ruft diese Funktion während des interaktiven rascs- \_ Zustands des Verbindungsprozesses auf. Der interaktive rascs \_ -Status ist ein angehaltene Zustand, mit dem der Benutzer mit einer Benutzeroberfläche interagieren kann, die von der benutzerdefinierten Skript-dll angezeigt wird. Weitere Informationen zu Verbindungs Zuständen finden Sie unter " [**rasrestate**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) ".

RAS übergibt als Parameter an die [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) -Funktion:

-   Ein Handle für den Port auf dem Client Computer, der für die Verbindung verwendet wird.
-   Zeichen folgen, die das Telefonbuch und den Eintrag für die Verbindung identifizieren.
-   RAS übergibt auch ein Handle an ein Fenster, damit die DLL eine Benutzeroberfläche bereitstellen kann.
-   Eine Reihe von Funktions Zeigern, die von der DLL für die Kommunikation mit dem Server verwendet werden können.

Weitere Informationen zu diesen Parametern finden Sie unter [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) .

RAS übergibt einen Zeiger auf eine [**rascustomscriptextensions**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) -Struktur als letzten Parameter an [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Diese Struktur enthält einen Zeiger auf eine Funktion vom Typ [**pfnrassetcommsettings**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). Die benutzerdefinierte Skript-dll ruft diese Funktion auf, um die Kommunikationseinstellungen auf dem Port zu ändern, der von der Verbindung verwendet wird.

RAS vermittelt die Interaktion zwischen dem Server und der benutzerdefinierten Skript-dll. In der Regel initiiert der Server das Dialogfeld. Der Server kann z. b. den Benutzernamen und das Kennwort des Benutzers anfordern.

Wenn Sie die benutzerdefinierte Skripterstellung verwenden, um eine Verbindung herzustellen, muss auf dem Server Windows NT 4,0 oder Windows 2000 nicht ausgeführt werden.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>Benutzerdefinierte Skripterstellung für Benutzeroberfläche muss IDCANCEL unterstützen

Wenn die benutzerdefinierte Einwählprogramm eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche die WM-befehlsnachrichten unterstützen, \_ wobei LoWord (*wParam*) gleich IDCANCEL ist.

## <a name="configuring-the-connection"></a>Konfigurieren der Verbindung

Der [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) -Einstiegspunkt kann von der [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) -oder unter Windows XP von der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)aufgerufen werden.

Zum Aufrufen von [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) von [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)legen Sie die Option raseo \_ CustomScript im Telefonbucheintrag für die Verbindung fest. Unter dem **dwfoptions** -Member von [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) finden Sie eine Beschreibung der Optionen für den Telefonbucheintrag. Verwenden Sie die Funktionen " [**rasgetentryproperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) " und " [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) ", um diese Option Programm gesteuert festzulegen.

**Windows XP:** Zum Aufrufen von [**rascustomscriptexecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) von [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)muss beim Aufruf von " **rasdial** " eine " [**rasdialextensions**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) "-Struktur angegeben werden, und diese Struktur muss das rtoopt \_ usecustomscripting-Flag angeben. Außerdem muss für den Telefonbucheintrag für die Verbindung die Option "raseo CustomScript" angegeben werden, \_ wie im vorherigen Abschnitt beschrieben.

## <a name="invoking-the-custom-scripting-dll"></a>Aufrufen der benutzerdefinierten Skript-dll

Wenn der Benutzer eine Verbindung für einen Telefonbucheintrag aktiviert, bei dem raseo \_ CustomScript festgelegt ist, ruft RAS die benutzerdefinierte Skript-dll auf. In diesem Szenario ruft RAS die benutzerdefinierte Skript-DLL von [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)auf.

Wenn Sie die benutzerdefinierte Skript-dll Programm gesteuert aufrufen möchten, stellen Sie die Verbindung mithilfe der Funktion " [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) " her. Unter Windows XP Ruft die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " auch die benutzerdefinierte Skript-dll auf.

 

 