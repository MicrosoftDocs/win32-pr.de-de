---
description: Es gibt viele Situationen, in denen Autorun möglicherweise temporär oder dauerhaft deaktiviert werden muss.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Aktivieren und Deaktivieren von Autorun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393454"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="3a6be-103">Aktivieren und Deaktivieren von Autorun</span><span class="sxs-lookup"><span data-stu-id="3a6be-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="3a6be-104">Es gibt viele Situationen, in denen Autorun möglicherweise temporär oder dauerhaft deaktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3a6be-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="3a6be-105">Autorun könnte z. b. den Betrieb einer laufenden Anwendung beeinträchtigen und muss für die Dauer deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="3a6be-106">Das System bietet mehrere Möglichkeiten, Autorun zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="3a6be-107">Programm gesteuertes unterdrücken von Autorun</span><span class="sxs-lookup"><span data-stu-id="3a6be-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="3a6be-108">Verwenden der Registrierung zum Deaktivieren von Autorun</span><span class="sxs-lookup"><span data-stu-id="3a6be-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="3a6be-109">Autorun für andere Typen von Speichermedien</span><span class="sxs-lookup"><span data-stu-id="3a6be-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="3a6be-110">Programm gesteuertes unterdrücken von Autorun</span><span class="sxs-lookup"><span data-stu-id="3a6be-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="3a6be-111">Es gibt eine Vielzahl von Situationen, in denen Autorun möglicherweise Programm gesteuert unterdrückt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3a6be-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="3a6be-112">Zwei Beispiele:</span><span class="sxs-lookup"><span data-stu-id="3a6be-112">Two examples are:</span></span>

-   <span data-ttu-id="3a6be-113">Die Anwendung verfügt über ein Setup Programm, mit dem der Benutzer einen anderen Datenträger einfügen muss, der möglicherweise eine Autorun. inf-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="3a6be-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="3a6be-114">Während der Ausführung der Anwendung muss der Benutzer möglicherweise eine andere CD einfügen, die eine Autorun. inf-Datei enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="3a6be-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="3a6be-115">In beiden Fällen möchten Sie normalerweise nicht eine andere Anwendung starten, während das Original ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a6be-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="3a6be-116">Benutzer können Autorun manuell unterdrücken, indem Sie die UMSCHALTTASTE gedrückt halten, wenn Sie die CD-ROM einfügen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="3a6be-117">Es ist jedoch in der Regel besser, diesen Vorgang Programm gesteuert und nicht in Abhängigkeit vom Benutzer zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3a6be-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="3a6be-118">Bei Systemen mit der Shell- [Version 4,70](versions.md) und höher wird von Windows eine "querycancelautoplay"-Meldung an das Vordergrund Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="3a6be-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="3a6be-119">Die Anwendung kann auf diese Meldung reagieren, um Autorun zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="3a6be-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="3a6be-120">Diese Vorgehensweise wird von System Dienstprogrammen wie dem Dialogfeld zum [Öffnen](../dlgbox/open-and-save-as-dialog-boxes.md) von Common verwendet, um Autorun zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="3a6be-121">Die folgenden Code Fragmente veranschaulichen, wie Sie diese Nachricht einrichten und behandeln.</span><span class="sxs-lookup"><span data-stu-id="3a6be-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="3a6be-122">Die Anwendung muss im Vordergrund Fenster ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="3a6be-123">Registrieren Sie zuerst "querycancelautoplay" als Windows-Meldung:</span><span class="sxs-lookup"><span data-stu-id="3a6be-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="3a6be-124">Das Fenster Ihrer Anwendung muss sich im Vordergrund befinden, um diese Meldung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="3a6be-125">Der Nachrichten Handler sollte **true** zurückgeben, um Autorun abzubrechen, und **false** , um ihn zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="3a6be-126">Im folgenden Code Fragment wird veranschaulicht, wie diese Meldung verwendet wird, um Autorun zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="3a6be-127">Wenn Ihre Anwendung ein Dialogfeld verwendet und auf eine "querycancelautoplay"-Meldung reagieren muss, kann Sie nicht einfach " **true** " oder " **false**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3a6be-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="3a6be-128">Aufrufen Sie stattdessen [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , wobei *nIndex* auf **DWL \_ msgresult** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a6be-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="3a6be-129">Legen Sie für den Parameter " *dwnewlong* " den Wert " **true** " fest, um den **Vorgang zu beenden** .</span><span class="sxs-lookup"><span data-stu-id="3a6be-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="3a6be-130">Beispielsweise wird beim Empfangen der Meldung "querycancelautoplay" die Autorun-Nachricht durch die folgende Beispiel Dialogfeld Prozedur abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="3a6be-131">Verwenden der Registrierung zum Deaktivieren von Autorun</span><span class="sxs-lookup"><span data-stu-id="3a6be-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="3a6be-132">Es gibt zwei Registrierungs Werte, die verwendet werden können, um Autorun dauerhaft zu deaktivieren: NoDriveAutoRun und nodrivetypeer Autorun.</span><span class="sxs-lookup"><span data-stu-id="3a6be-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="3a6be-133">Der erste Wert deaktiviert Autorun für angegebene Laufwerk Buchstaben, das zweite deaktiviert Autorun für eine Klasse von Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="3a6be-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="3a6be-134">Wenn einer dieser Werte so festgelegt ist, dass Autorun für ein bestimmtes Gerät deaktiviert wird, wird er deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a6be-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="3a6be-135">Weitere Informationen zum Deaktivieren der Autorun-Funktionalität finden Sie im Knowledge Base-Artikel [Deaktivieren der Autorun-Funktionalität in Windows](https://support.microsoft.com/kb/967715) .</span><span class="sxs-lookup"><span data-stu-id="3a6be-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="3a6be-136">In diesem Artikel werden die verschiedenen Updates aufgelistet, die installiert sein müssen, um die Autorun-Funktionalität ordnungsgemäß zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="3a6be-137">Die NoDriveAutoRun-und nodrivetypeer Autorun-Werte sollten nur von Systemadministratoren geändert werden, um den Wert für das gesamte System zu Test-oder Verwaltungszwecken zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3a6be-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="3a6be-138">Anwendungen sollten diese Werte nicht ändern, da es keine Möglichkeit gibt, Sie zuverlässig auf ihre ursprünglichen Werte wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="3a6be-139">Der NoDriveAutoRun-Wert deaktiviert Autorun für angegebene Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="3a6be-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="3a6be-140">Es handelt sich um einen reg \_ DWORD-Datenwert, der unter dem folgenden Schlüssel gefunden wird:</span><span class="sxs-lookup"><span data-stu-id="3a6be-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="3a6be-141">Das erste Bit des Werts entspricht Laufwerk A:, der zweiten zu B: usw.</span><span class="sxs-lookup"><span data-stu-id="3a6be-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="3a6be-142">Um Autorun für einen oder mehrere Laufwerk Buchstaben zu deaktivieren, legen Sie die entsprechenden Bits fest.</span><span class="sxs-lookup"><span data-stu-id="3a6be-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="3a6be-143">Wenn Sie z. b. die Laufwerke A: und C: deaktivieren möchten, legen Sie NoDriveAutoRun auf fest `0x00000005` .</span><span class="sxs-lookup"><span data-stu-id="3a6be-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="3a6be-144">Der nodrivetypeer Autorun-Wert deaktiviert Autorun für eine Klasse von Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="3a6be-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="3a6be-145">Dabei handelt es sich um einen reg \_ DWORD-oder 4-Byte-reg- \_ Binär Datenwert, der unter dem gleichen Schlüssel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3a6be-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="3a6be-146">Durch Festlegen der Bits des ersten Byte dieses Werts können unterschiedliche Laufwerke von der Arbeit mit Autorun ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="3a6be-147">Die folgende Tabelle enthält die Bits-und Bitmasken Konstanten, die im ersten Byte von nodrivetypeer Autorun festgelegt werden können, um Autorun für einen bestimmten Laufwerkstyp zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="3a6be-148">Sie müssen Windows-Explorer neu starten, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="3a6be-149">Bitzahl</span><span class="sxs-lookup"><span data-stu-id="3a6be-149">Bit Number</span></span> | <span data-ttu-id="3a6be-150">Bitmasken Konstante</span><span class="sxs-lookup"><span data-stu-id="3a6be-150">Bitmask Constant</span></span>      | <span data-ttu-id="3a6be-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a6be-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="3a6be-152">0x04</span><span class="sxs-lookup"><span data-stu-id="3a6be-152">0x04</span></span>       | <span data-ttu-id="3a6be-153">**Laufwerks \_ Removeable**</span><span class="sxs-lookup"><span data-stu-id="3a6be-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="3a6be-154">Der Datenträger kann von einem Laufwerk (z. b. einem Diskettenlaufwerk) entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="3a6be-155">0x08</span><span class="sxs-lookup"><span data-stu-id="3a6be-155">0x08</span></span>       | <span data-ttu-id="3a6be-156">**Laufwerk \_ korrigiert**</span><span class="sxs-lookup"><span data-stu-id="3a6be-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="3a6be-157">Der Datenträger kann nicht vom Laufwerk (einer Festplatte) entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="3a6be-158">0x10</span><span class="sxs-lookup"><span data-stu-id="3a6be-158">0x10</span></span>       | <span data-ttu-id="3a6be-159">**Laufwerk \_ Remote**</span><span class="sxs-lookup"><span data-stu-id="3a6be-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="3a6be-160">Netzwerklaufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a6be-160">Network drive.</span></span>                                          |
| <span data-ttu-id="3a6be-161">0x20</span><span class="sxs-lookup"><span data-stu-id="3a6be-161">0x20</span></span>       | <span data-ttu-id="3a6be-162">**Laufwerk- \_ CDROM**</span><span class="sxs-lookup"><span data-stu-id="3a6be-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="3a6be-163">CD-ROM-Laufwerk</span><span class="sxs-lookup"><span data-stu-id="3a6be-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="3a6be-164">0x40</span><span class="sxs-lookup"><span data-stu-id="3a6be-164">0x40</span></span>       | <span data-ttu-id="3a6be-165">**Laufwerk \_ Ramdisk**</span><span class="sxs-lookup"><span data-stu-id="3a6be-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="3a6be-166">RAM-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3a6be-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="3a6be-167">Autorun für andere Typen von Speichermedien</span><span class="sxs-lookup"><span data-stu-id="3a6be-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="3a6be-168">Autorun ist hauptsächlich für die öffentliche Verteilung von Anwendungen auf CD-ROM und DVD-ROM gedacht, und die Verwendung wird von anderen Speichermedien abgeraten.</span><span class="sxs-lookup"><span data-stu-id="3a6be-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="3a6be-169">Es ist jedoch oft hilfreich, Autorun auf anderen Typen von Wechselmedien zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a6be-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="3a6be-170">Diese Funktion wird normalerweise verwendet, um das Debuggen von Autorun-INF-Dateien zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="3a6be-171">Autorun funktioniert nur auf Wechsel Datenträgern, wenn die folgenden Kriterien erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="3a6be-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="3a6be-172">Das Gerät muss über Auto-kompatible Treiber verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="3a6be-173">Damit ein Treiber nicht kompatibel ist, muss er vom System benachrichtigt werden, dass ein Datenträger eingefügt wurde, indem eine [**WM \_ devicechange**](../devio/wm-devicechange.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a6be-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="3a6be-174">Das Stammverzeichnis des eingefügten Mediums muss eine Autorun. inf-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a6be-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="3a6be-175">Das Gerät darf nicht durch die [Registrierung](#using-the-registry-to-disable-autorun)deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="3a6be-176">Die Vordergrund Anwendung hat Autorun nicht unter [drückt](#suppressing-autorun-programmatically) .</span><span class="sxs-lookup"><span data-stu-id="3a6be-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="3a6be-177">Diese Funktion sollte nicht zum Verteilen von Anwendungen auf Wechselmedien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="3a6be-178">Da das Implementieren von Autorun auf Wechsel Datenträgern eine einfache Möglichkeit zum Verteilen von Computerviren darstellt, sollten die Benutzer für jede öffentlich verteilte Diskette, die eine Autorun. inf-Datei enthält, verdächtig sein.</span><span class="sxs-lookup"><span data-stu-id="3a6be-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="3a6be-179">Normalerweise startet Autorun automatisch, kann aber auch manuell gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="3a6be-180">Wenn das Gerät die oben aufgeführten Kriterien erfüllt, enthält das Kontextmenü des Laufwerk Buchstabens einen **AutoPlay** -Befehl.</span><span class="sxs-lookup"><span data-stu-id="3a6be-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="3a6be-181">Um Autorun manuell auszuführen, klicken Sie entweder mit der rechten Maustaste auf das Laufwerk Symbol, und wählen Sie im Kontextmenü die Option **AutoPlay** aus, oder Doppelklicken Sie auf das Laufwerk Symbol.</span><span class="sxs-lookup"><span data-stu-id="3a6be-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="3a6be-182">Wenn die Treiber nicht automatisch kompatibel sind, enthält das Kontextmenü kein **AutoPlay** -Element, und Autorun kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="3a6be-183">Auto-kompatible Treiber werden mit einigen Wechsel Datenträgern bereitgestellt, sowie einigen anderen Typen von Wechselmedien wie z. b. "CompactFlash Cards".</span><span class="sxs-lookup"><span data-stu-id="3a6be-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="3a6be-184">Autorun funktioniert auch mit Netzwerklaufwerken, die einem Laufwerk Buchstaben mit Windows-Explorer zugeordnet sind oder mit der [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)eingebunden sind.</span><span class="sxs-lookup"><span data-stu-id="3a6be-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="3a6be-185">Wie bei der bereitgestellten Hardware muss ein bereitgestelltes Netzwerklaufwerk über eine Autorun. inf-Datei im Stammverzeichnis verfügen, und es darf nicht über die [Registrierung](#using-the-registry-to-disable-autorun)deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3a6be-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
