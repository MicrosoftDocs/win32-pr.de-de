---
description: Benutzer können das automatische Debuggen konfigurieren, um zu bestimmen, warum ihr System oder eine Anwendung nicht mehr reagiert.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Konfigurieren des automatischen Debuggens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990f2f52e6227e4b1a2cf92656794c90fb5d465915a5d888025d0f3b2c438630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076504"
---
# <a name="configuring-automatic-debugging"></a>Konfigurieren des automatischen Debuggens

Benutzer können das automatische Debuggen konfigurieren, um zu bestimmen, warum ihr System oder eine Anwendung nicht mehr reagiert.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Konfigurieren des automatischen Debuggens für Systemabstürze

Um den Zielcomputer so zu konfigurieren, dass eine Absturzabbilddatei generiert wird, wenn das System nicht mehr reagiert, verwenden Sie die **Systemanwendung** in Systemsteuerung. Klicken **Sie auf Erweiterte Systemeinstellungen,** um das Dialogfeld **Systemeigenschaften** anzuzeigen. Klicken Sie **in diesem** Feld  auf der Registerkarte Erweitert auf Einstellungen unter **Start** und Wiederherstellung, und verwenden Sie dann die entsprechenden Wiederherstellungsoptionen. Alternativ können Sie Absturzabbildoptionen mit dem folgenden Registrierungsschlüssel konfigurieren:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet-Steuerelement** \\  \\ **CrashControl**

Die Datei, die Sie angeben können, ist die Absturzabbilddatei. Der Standardname ist Memory.dmp. Sie können ein Absturzabbild mit einem Kernelmodusdebugger wie WinDbg oder KD debuggen. Weitere Informationen finden Sie in der Dokumentation, die im Debugger enthalten ist.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Konfigurieren des automatischen Debuggens für Anwendungsabstürze

Wenn eine Anwendung nicht mehr reagiert (z. B. nach einer Zugriffsverletzung), ruft das System automatisch einen Debugger auf, der in der Registrierung für das postungstem-Debuggen angegeben ist. Die Prozess-ID und das Ereignishand handle werden an den Debugger übergeben, wenn die Befehlszeile ordnungsgemäß konfiguriert ist. Im folgenden Verfahren wird beschrieben, wie Sie einen Debugger in der Registrierung angeben.

**So legen Sie einen Debugger als postungtem-Debugger fest**

1.  Wechseln Sie zum folgenden Registrierungsschlüssel:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Fügen Sie den Debuggerwert **hinzu, oder** bearbeiten Sie diesen mithilfe einer REG SZ-Zeichenfolge, die \_ die Befehlszeile für den Debugger angibt.

    Die Zeichenfolge sollte den vollqualifizierten Pfad zur ausführbaren Debuggerdatei enthalten. Geben Sie die Prozess-ID und das Ereignishand handle mit "%ld"-Parametern in der Debuggerbefehlszeile an. Verschiedene Debugger verfügen möglicherweise über eigene Parametersyntaxen zum Angeben dieser Werte. Wenn der Debugger aufgerufen wird, wird das erste "%ld" durch die Prozess-ID und das zweite "%ld" durch das Ereignishand handle ersetzt.

    Der folgende Text ist ein Beispiel für das Einrichten von WinDbg als Debugger.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Wenn der Debugger ohne Benutzerinteraktion aufgerufen werden soll, fügen Sie den Auto-Wert hinzu oder bearbeiten ihn mithilfe einer REG SZ-Zeichenfolge, die angibt, ob dem Benutzer ein Dialogfeld angezeigt werden soll, bevor der Debugger aufgerufen  \_ wird. Die Zeichenfolge "1" deaktiviert das Dialogfeld. Die Zeichenfolge "0" aktiviert das Dialogfeld.

## <a name="excluding-an-application-from-automatic-debugging"></a>Ausschließen einer Anwendung vom automatischen Debuggen

Im folgenden Verfahren wird beschrieben, wie Eine Anwendung vom automatischen Debuggen ausgeschlossen wird, nachdem der **Auto-Wert** unter dem **AeDebug-Schlüssel** auf 1 festgelegt wurde.

**So schließen Sie eine Anwendung vom automatischen Debuggen aus**

1.  Wechseln Sie zum folgenden Registrierungsschlüssel:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Fügen Sie dem Unterschlüssel \_ **AutoExclusionList** einen REG DWORD-Wert hinzu, wobei der Name der Name der ausführbaren Datei und der Wert 1 ist. Standardmäßig wird Desktopfenster-Manager (Dwm.exe) vom automatischen Debuggen ausgeschlossen, da andernfalls ein System deadlock auftreten kann, wenn Dwm.exe nicht mehr reagiert (der Benutzer kann die vom Debugger angezeigte Schnittstelle nicht sehen, da Dwm.exe nicht reagiert, und Dwm.exe kann nicht beendet werden, da sie vom Debugger gehalten wird).

    **Windows Server 2003 und Windows XP:** Der **Unterschlüssel AutoExclusionList** ist nicht verfügbar. Daher können Sie keine Anwendung, einschließlich Dwm.exe, vom automatischen Debuggen ausschließen.

Die **standardmäßigen AeDebug-Registrierungseinträge** können wie folgt dargestellt werden:

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

[Aktivieren des postungstem-Debuggens mit WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
