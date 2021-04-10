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
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="ec081-103">Konfigurieren von automatischem Debugging</span><span class="sxs-lookup"><span data-stu-id="ec081-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="ec081-104">Benutzer können das automatische Debuggen konfigurieren, damit Sie bestimmen können, warum Ihr System oder eine Anwendung nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="ec081-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="ec081-105">Konfigurieren des automatischen Debuggens für System Abstürze</span><span class="sxs-lookup"><span data-stu-id="ec081-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="ec081-106">Um den Zielcomputer so zu konfigurieren, dass eine Absturz Abbild Datei generiert wird, wenn das System nicht mehr reagiert, verwenden Sie die Systemanwendung in der **System** Steuerung.</span><span class="sxs-lookup"><span data-stu-id="ec081-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="ec081-107">Klicken Sie auf **Erweiterte Systemeinstellungen**, wodurch das Dialogfeld **Systemeigenschaften** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec081-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="ec081-108">Klicken Sie in diesem Feld auf der Registerkarte **erweitert** auf **Einstellungen** unter **Start und Wiederherstellung**, und verwenden Sie dann die entsprechenden Wiederherstellungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="ec081-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="ec081-109">Alternativ können Sie Optionen für Absturz Abbilder mit dem folgenden Registrierungsschlüssel konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="ec081-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="ec081-110">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="ec081-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="ec081-111">Die Datei, die Sie angeben können, ist die Absturz Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="ec081-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="ec081-112">Der Standardname ist "Memory. dmp".</span><span class="sxs-lookup"><span data-stu-id="ec081-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="ec081-113">Sie können ein Absturz Abbild mit einem Kernel Modus-Debugger Debuggen, z. b. WinDbg oder KD.</span><span class="sxs-lookup"><span data-stu-id="ec081-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="ec081-114">Weitere Informationen finden Sie in der Dokumentation, die im Debugger enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ec081-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="ec081-115">Konfigurieren des automatischen Debuggens für Anwendungs Abstürze</span><span class="sxs-lookup"><span data-stu-id="ec081-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="ec081-116">Wenn eine Anwendung nicht mehr reagiert (z. b. nach einer Zugriffsverletzung), ruft das System automatisch einen Debugger auf, der in der Registrierung für das mortem-Debugging angegeben ist. die Prozess-ID und das Ereignis handle werden an den Debugger übergeben, wenn die Befehlszeile ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ec081-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="ec081-117">Im folgenden Verfahren wird beschrieben, wie ein Debugger in der Registrierung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec081-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="ec081-118">**So legen Sie einen Debugger als mortem-Debugger fest**</span><span class="sxs-lookup"><span data-stu-id="ec081-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="ec081-119">Wechseln Sie zum folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="ec081-119">Go to the following registry key:</span></span>

    <span data-ttu-id="ec081-120">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**</span><span class="sxs-lookup"><span data-stu-id="ec081-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="ec081-121">Fügen Sie den **Debugger** -Wert hinzu, oder bearbeiten Sie ihn mithilfe einer reg \_ SZ-Zeichenfolge, die die Befehlszeile für den Debugger angibt.</span><span class="sxs-lookup"><span data-stu-id="ec081-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="ec081-122">Die Zeichenfolge sollte den voll qualifizierten Pfad zur ausführbaren Debugger-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec081-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="ec081-123">Geben Sie die Prozess-ID und das Ereignis Handle mit den Parametern "% LD" an der Debugger-Befehlszeile an.</span><span class="sxs-lookup"><span data-stu-id="ec081-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="ec081-124">Verschiedene-konstruktormodule verfügen möglicherweise über eine eigene Parameter Syntax zum Angeben dieser Werte.</span><span class="sxs-lookup"><span data-stu-id="ec081-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="ec081-125">Wenn der Debugger aufgerufen wird, wird das erste "% LD" durch die Prozess-ID und das zweite "% LD" durch das Ereignis handle ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ec081-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="ec081-126">Der folgende Text ist ein Beispiel für das Einrichten von WinDBG als Debugger.</span><span class="sxs-lookup"><span data-stu-id="ec081-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="ec081-127">Wenn Sie möchten, dass der Debugger ohne Benutzerinteraktion aufgerufen wird, können Sie den **automatischen** Wert hinzufügen oder bearbeiten. verwenden Sie dazu eine reg \_ SZ-Zeichenfolge, die angibt, ob das System ein Dialogfeld für den Benutzer anzeigen soll, bevor der Debugger aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ec081-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="ec081-128">Mit der Zeichenfolge "1" wird das Dialogfeld deaktiviert. mit der Zeichenfolge "0" wird das Dialogfeld aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ec081-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="ec081-129">Ausschließen einer Anwendung vom automatischen Debuggen</span><span class="sxs-lookup"><span data-stu-id="ec081-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="ec081-130">Im folgenden Verfahren wird beschrieben, wie eine Anwendung **aus dem automatischen** Debuggen ausgeschlossen wird, nachdem der automatische Wert unter dem Schlüssel " **AEDebug** " auf 1 festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec081-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="ec081-131">**So schließen Sie eine Anwendung vom automatischen Debuggen aus**</span><span class="sxs-lookup"><span data-stu-id="ec081-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="ec081-132">Wechseln Sie zum folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="ec081-132">Go to the following registry key:</span></span>

    <span data-ttu-id="ec081-133">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**</span><span class="sxs-lookup"><span data-stu-id="ec081-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="ec081-134">Fügen Sie einen reg \_ DWORD-Wert zum Unterschlüssel **autoexclusionlist** hinzu, wobei Name der Name der ausführbaren Datei und der Wert 1 ist.</span><span class="sxs-lookup"><span data-stu-id="ec081-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="ec081-135">Standardmäßig wird der Desktopfenster-Manager (Dwm.exe) vom automatischen Debuggen ausgeschlossen, da andernfalls ein System Deadlock auftreten kann, wenn Dwm.exe nicht mehr reagiert (der Benutzer kann die vom Debugger angezeigte Schnittstelle nicht sehen, weil Dwm.exe nicht antwortet und Dwm.exe nicht beenden kann, weil er vom Debugger aufbewahrt wird).</span><span class="sxs-lookup"><span data-stu-id="ec081-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="ec081-136">**Windows Server 2003 und Windows XP:** Der Unterschlüssel **autoexclusionlist** ist nicht verfügbar. Folglich ist es nicht möglich, eine Anwendung, einschließlich Dwm.exe, vom automatischen Debugging auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="ec081-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="ec081-137">Die standardmäßigen **AEDebug** -Registrierungseinträge können wie folgt dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="ec081-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ec081-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec081-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec081-139">Aktivieren des Postmortem-Debuggens mit WinDbg</span><span class="sxs-lookup"><span data-stu-id="ec081-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
