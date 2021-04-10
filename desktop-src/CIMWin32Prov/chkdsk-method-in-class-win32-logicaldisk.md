---
description: Ruft den CHKDSK-Vorgang auf dem Datenträger auf.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: CHKDSK-Methode der Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127224"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="6f23e-103">CHKDSK-Methode der Win32 \_ LogicalDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="6f23e-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="6f23e-104">Die **chkdsk** -Instanzmethode ruft den **chkdsk** -Vorgang auf dem Datenträger auf.</span><span class="sxs-lookup"><span data-stu-id="6f23e-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="6f23e-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f23e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6f23e-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6f23e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f23e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f23e-107">Syntax</span></span>


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a><span data-ttu-id="6f23e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f23e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f23e-109">*Fixerrors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f23e-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-110">Gibt an, was mit den auf dem Datenträger gefundenen Fehlern geschehen soll.</span><span class="sxs-lookup"><span data-stu-id="6f23e-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="6f23e-111">**True** gibt an, dass Fehler korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f23e-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="6f23e-112">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f23e-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-113">*VigorousIndexCheck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f23e-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-114">**True** gibt an, dass eine weniger kräftige Überprüfung der Indexeinträge ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f23e-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="6f23e-115">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f23e-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-116">*Skipfoldercycle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f23e-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-117">**True** gibt an, dass die Überprüfung des Ordner Überlaufs ausgelassen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f23e-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="6f23e-118">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="6f23e-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-119">*ForceDismount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f23e-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-120">**True** gibt an, dass das Laufwerk vor der Überprüfung gezwungen werden muss, die Einbindung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="6f23e-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="6f23e-121">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f23e-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-122">*Recoverbadsektoren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f23e-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-123">**True** gibt an, dass die fehlerhaften Sektoren gefunden und die lesbaren Informationen aus diesen Sektoren wieder hergestellt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="6f23e-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="6f23e-124">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f23e-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-125">*Oktorunatbootup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f23e-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-126">**True** gibt an, dass der **chkdsk** -Vorgang beim nächsten Startzeitpunkt ausgeführt werden soll, falls der Vorgang nicht ausgeführt werden konnte, weil der Datenträger zum Zeitpunkt des Aufrufs dieser Methode gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="6f23e-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="6f23e-127">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f23e-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f23e-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f23e-128">Return value</span></span>

<span data-ttu-id="6f23e-129">Gibt bei erfolgreicher Ausführung den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="6f23e-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="6f23e-130">Andere Werte sind in der folgenden Liste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f23e-130">Other values are listed in the following list.</span></span> <span data-ttu-id="6f23e-131">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6f23e-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6f23e-132">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6f23e-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6f23e-133">**Erfolg-Chkdsk abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="6f23e-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-134">0</span><span class="sxs-lookup"><span data-stu-id="6f23e-134">0</span></span>

<span data-ttu-id="6f23e-135">Erfolg- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6f23e-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-136">**Erfolg: gesperrt und chkdsk geplant beim Neustart**</span><span class="sxs-lookup"><span data-stu-id="6f23e-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-137">1</span><span class="sxs-lookup"><span data-stu-id="6f23e-137">1</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-138">**Fehler-unbekanntes Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="6f23e-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-139">2</span><span class="sxs-lookup"><span data-stu-id="6f23e-139">2</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-140">**Fehler-unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="6f23e-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-141">3</span><span class="sxs-lookup"><span data-stu-id="6f23e-141">3</span></span>

</dd> <dt>

<span data-ttu-id="6f23e-142">**Fehler: nicht unterstütztes Datei System**</span><span class="sxs-lookup"><span data-stu-id="6f23e-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="6f23e-143">4</span><span class="sxs-lookup"><span data-stu-id="6f23e-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f23e-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f23e-144">Remarks</span></span>

<span data-ttu-id="6f23e-145">Diese Methode gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="6f23e-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="6f23e-146">Sie ist nicht auf zugeordnete logische Laufwerke anwendbar.</span><span class="sxs-lookup"><span data-stu-id="6f23e-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="6f23e-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f23e-147">Examples</span></span>

<span data-ttu-id="6f23e-148">Das in einem Server-PowerShell-Codebeispiel festgelegte geändertes[chkdsk-Bit](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) untersucht das Remote System und gibt true oder false zurück, wenn das chkdsk/f-Flag festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f23e-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="6f23e-149">Das PowerShell-Codebeispiel für die [Remote](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) Überprüfung von Datenträgern startet oder plant den Scan Datenträger</span><span class="sxs-lookup"><span data-stu-id="6f23e-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="6f23e-150">Im folgenden VBScript-Codebeispiel wird ChkDsk.exe für Laufwerk D auf einem Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f23e-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="6f23e-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f23e-151">Requirements</span></span>



| <span data-ttu-id="6f23e-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f23e-152">Requirement</span></span> | <span data-ttu-id="6f23e-153">Wert</span><span class="sxs-lookup"><span data-stu-id="6f23e-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f23e-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f23e-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6f23e-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f23e-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f23e-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f23e-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6f23e-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f23e-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f23e-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f23e-158">Namespace</span></span><br/>                | <span data-ttu-id="6f23e-159">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6f23e-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f23e-160">MOF</span><span class="sxs-lookup"><span data-stu-id="6f23e-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f23e-161"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6f23e-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f23e-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6f23e-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f23e-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f23e-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f23e-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f23e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f23e-165">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="6f23e-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="6f23e-166">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="6f23e-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

