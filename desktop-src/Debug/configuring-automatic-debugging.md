---
description: Benutzer können das automatische Debuggen konfigurieren, damit Sie bestimmen können, warum Ihr System oder eine Anwendung nicht mehr reagiert.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Konfigurieren von automatischem Debugging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125749"
---
# <a name="configuring-automatic-debugging"></a>Konfigurieren von automatischem Debugging

Benutzer können das automatische Debuggen konfigurieren, damit Sie bestimmen können, warum Ihr System oder eine Anwendung nicht mehr reagiert.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Konfigurieren des automatischen Debuggens für System Abstürze

Um den Zielcomputer so zu konfigurieren, dass eine Absturz Abbild Datei generiert wird, wenn das System nicht mehr reagiert, verwenden Sie die Systemanwendung in der **System** Steuerung. Klicken Sie auf **Erweiterte Systemeinstellungen**, wodurch das Dialogfeld **Systemeigenschaften** angezeigt wird. Klicken Sie in diesem Feld auf der Registerkarte **erweitert** auf **Einstellungen** unter **Start und Wiederherstellung**, und verwenden Sie dann die entsprechenden Wiederherstellungsoptionen. Alternativ können Sie Optionen für Absturz Abbilder mit dem folgenden Registrierungsschlüssel konfigurieren:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**

Die Datei, die Sie angeben können, ist die Absturz Abbild Datei. Der Standardname ist "Memory. dmp". Sie können ein Absturz Abbild mit einem Kernel Modus-Debugger Debuggen, z. b. WinDbg oder KD. Weitere Informationen finden Sie in der Dokumentation, die im Debugger enthalten ist.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Konfigurieren des automatischen Debuggens für Anwendungs Abstürze

Wenn eine Anwendung nicht mehr reagiert (z. b. nach einer Zugriffsverletzung), ruft das System automatisch einen Debugger auf, der in der Registrierung für das mortem-Debugging angegeben ist. die Prozess-ID und das Ereignis handle werden an den Debugger übergeben, wenn die Befehlszeile ordnungsgemäß konfiguriert ist. Im folgenden Verfahren wird beschrieben, wie ein Debugger in der Registrierung angegeben wird.

**So legen Sie einen Debugger als mortem-Debugger fest**

1.  Wechseln Sie zum folgenden Registrierungsschlüssel:

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**

2.  Fügen Sie den **Debugger** -Wert hinzu, oder bearbeiten Sie ihn mithilfe einer reg \_ SZ-Zeichenfolge, die die Befehlszeile für den Debugger angibt.

    Die Zeichenfolge sollte den voll qualifizierten Pfad zur ausführbaren Debugger-Datei enthalten. Geben Sie die Prozess-ID und das Ereignis Handle mit den Parametern "% LD" an der Debugger-Befehlszeile an. Verschiedene-konstruktormodule verfügen möglicherweise über eine eigene Parameter Syntax zum Angeben dieser Werte. Wenn der Debugger aufgerufen wird, wird das erste "% LD" durch die Prozess-ID und das zweite "% LD" durch das Ereignis handle ersetzt.

    Der folgende Text ist ein Beispiel für das Einrichten von WinDBG als Debugger.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Wenn Sie möchten, dass der Debugger ohne Benutzerinteraktion aufgerufen wird, können Sie den **automatischen** Wert hinzufügen oder bearbeiten. verwenden Sie dazu eine reg \_ SZ-Zeichenfolge, die angibt, ob das System ein Dialogfeld für den Benutzer anzeigen soll, bevor der Debugger aufgerufen wird. Mit der Zeichenfolge "1" wird das Dialogfeld deaktiviert. mit der Zeichenfolge "0" wird das Dialogfeld aktiviert.

## <a name="excluding-an-application-from-automatic-debugging"></a>Ausschließen einer Anwendung vom automatischen Debuggen

Im folgenden Verfahren wird beschrieben, wie eine Anwendung **aus dem automatischen** Debuggen ausgeschlossen wird, nachdem der automatische Wert unter dem Schlüssel " **AEDebug** " auf 1 festgelegt wurde.

**So schließen Sie eine Anwendung vom automatischen Debuggen aus**

1.  Wechseln Sie zum folgenden Registrierungsschlüssel:

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**

2.  Fügen Sie einen reg \_ DWORD-Wert zum Unterschlüssel **autoexclusionlist** hinzu, wobei Name der Name der ausführbaren Datei und der Wert 1 ist. Standardmäßig wird der Desktopfenster-Manager (Dwm.exe) vom automatischen Debuggen ausgeschlossen, da andernfalls ein System Deadlock auftreten kann, wenn Dwm.exe nicht mehr reagiert (der Benutzer kann die vom Debugger angezeigte Schnittstelle nicht sehen, weil Dwm.exe nicht antwortet und Dwm.exe nicht beenden kann, weil er vom Debugger aufbewahrt wird).

    **Windows Server 2003 und Windows XP:** Der Unterschlüssel **autoexclusionlist** ist nicht verfügbar. Folglich ist es nicht möglich, eine Anwendung, einschließlich Dwm.exe, vom automatischen Debugging auszuschließen.

Die standardmäßigen **AEDebug** -Registrierungseinträge können wie folgt dargestellt werden:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren des Postmortem-Debuggens mit WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
