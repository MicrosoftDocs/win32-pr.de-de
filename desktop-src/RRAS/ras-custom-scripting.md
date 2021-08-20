---
title: Benutzerdefinierte RAS-Skripterstellung
description: Entwickler können eine benutzerdefinierte Skripterstellungs-DLL erstellen, die sich auf einem RAS-Clientcomputer befindet. Diese DLL kann während des Verbindungsvorgangs mit dem Server kommunizieren.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ac0bd83b8d7c48ee8b0468d89a70d19a5e5e6555b9a8bc8ac86d66c8cd666e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673280"
---
# <a name="ras-custom-scripting"></a>Benutzerdefinierte RAS-Skripterstellung

Entwickler können eine benutzerdefinierte Skripterstellungs-DLL erstellen, die sich auf einem RAS-Clientcomputer befindet. Diese DLL kann während des Verbindungsvorgangs mit dem Server kommunizieren.

**Windows NT:** Benutzerdefinierte Skripts sind nicht verfügbar.

## <a name="setting-up-the-dll"></a>Einrichten der DLL

Erstellen Sie zum Einrichten der DLL einen Wert mit dem Namen **CustomScriptDllPath unter** dem folgenden Registrierungsschlüssel:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Dieser Wert sollte vom Typ **REG \_ EXPAND SZ \_ sein.** Der Wert sollte den Pfad zur DLL für benutzerdefinierte Skripts enthalten. Für jeden RAS-Clientcomputer wird nur eine DLL mit benutzerdefinierter Skripterstellung unterstützt.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interaktion zwischen Server, RAS und der Custom-Scripting DLL

Die benutzerdefinierte Skript-DLL sollte einen einzelnen Einstiegspunkt exportieren: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS ruft diese Funktion während des interaktiven \_ RASCS-Zustands des Verbindungsprozesses auf. Der status "RASCS Interactive" ist ein angehaltener Zustand, der es dem Benutzer ermöglicht, mit einer Benutzeroberfläche zu interagieren, die von der DLL mit benutzerdefinierten \_ Skripts dargestellt wird. Weitere Informationen zu Verbindungszuständen finden Sie unter [**RASCONNSTATE.**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))

RAS über gibt als Parameter an die [**RasCustomScriptExecute-Funktion**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) weiter:

-   Ein Handle für den Port auf dem Clientcomputer, der für die Verbindung verwendet wird.
-   Zeichenfolgen, die das Telefonbuch und den Eintrag für die Verbindung identifizieren.
-   RAS übergibt auch ein Handle an ein Fenster, damit die DLL eine Benutzeroberfläche präsentieren kann.
-   Ein Satz von Funktionsze0ern, die die DLL für die Kommunikation mit dem Server verwenden kann.

Weitere Informationen zu diesen Parametern finden Sie unter [**RasCustomScriptExecute.**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)

RAS übergibt einen Zeiger auf eine [**RASCUSTOMSCRIPTEXTENSIONS-Struktur**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) als letzten Parameter an [**RasCustomScriptExecute.**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) Diese Struktur enthält einen Zeiger auf eine Funktion vom Typ [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). Die DLL für benutzerdefinierte Skripts ruft diese Funktion auf, um die Kommunikationseinstellungen auf dem Port zu ändern, der von der Verbindung verwendet wird.

RAS vermittelt die Interaktion zwischen dem Server und der DLL mit benutzerdefinierten Skripts. In der Regel initiiert der Server den Dialog. Beispielsweise kann der Server den Benutzernamen und das Kennwort des Benutzers anfordern.

Wenn Sie benutzerdefinierte Skripts zum Herstellen einer Verbindung verwenden, muss auf dem Server Windows NT 4.0 oder Windows 2000 ausgeführt werden.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>Benutzerdefinierte Skripterstellungs Benutzeroberfläche muss IDCANCEL unterstützen

Wenn das benutzerdefinierte Telefon eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche WM COMMAND-Nachrichten unterstützen, bei denen \_ LOWORD(*wParam*) IDCANCEL entspricht.

## <a name="configuring-the-connection"></a>Konfigurieren der Verbindung

Der [**Einstiegspunkt RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) kann von [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) oder auf Windows XP von [**RasDial aufgerufen werden.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Legen Sie [**zum Aufrufen von RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) aus [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)die Option RASEO CustomScript im Telefonbucheintrag für \_ die Verbindung fest. Eine Beschreibung der Optionen für die Telefonbucheingabe finden Sie unter **dwfOptions-Mitglied** von [**RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) Verwenden Sie [**die Funktionen RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) und [**RasSetEntryProperties,**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) um diese Option programmgesteuert festlegen.

**Windows XP:** Zum Aufrufen [**von RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) aus [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)muss der Aufruf von **RasDial** eine [**RASDIALEXTENSIONS-Struktur**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) angeben, und diese Struktur muss das RDEOPT \_ UseCustomScripting-Flag angeben. Darüber hinaus muss im Telefonbucheintrag für die Verbindung die Option RASEO CustomScript angegeben werden, wie \_ im vorherigen Absatz beschrieben.

## <a name="invoking-the-custom-scripting-dll"></a>Aufrufen der DLL für benutzerdefinierte Skripts

Wenn der Benutzer eine Verbindung für einen Telefonbucheintrag aktiviert, für den RASEO CustomScript festgelegt ist, ruft RAS die CUSTOM \_ SCRIPTING-DLL auf. In diesem Szenario ruft RAS die DLL mit benutzerdefinierten Skripts von [**RasDialDlg auf.**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)

Stellen Sie die Verbindung mithilfe der [**RasDialDlg-Funktion**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) auf, um die DLL für die benutzerdefinierte Skripterstellung programmgesteuert aufrufen zu können. Auf Windows XP ruft die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) auch die DLL für die benutzerdefinierte Skripterstellung auf.

 

 