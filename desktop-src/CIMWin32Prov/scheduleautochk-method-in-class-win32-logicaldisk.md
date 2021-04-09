---
description: Plant das Ausführen von AUTOCHK auf dem Laufwerk, das durch den Win32 \_ LogicalDisk beim nächsten Neustart dargestellt wird, wenn das geänderte Bit festgelegt ist.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Scheduleautochk-Methode der Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958267"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="aeeef-103">Scheduleautochk-Methode der Win32 \_ LogicalDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="aeeef-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="aeeef-104">Die **scheduleautochk** -Klassenmethode plant das Ausführen von AUTOCHK auf dem Laufwerk, das beim nächsten Neustart durch den [**Win32 \_ LogicalDisk**](win32-logicaldisk.md) dargestellt wird, wenn das geänderte Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aeeef-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="aeeef-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="aeeef-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aeeef-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aeeef-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aeeef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeeef-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="aeeef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeeef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeeef-109">*LogicalDisk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeeef-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeeef-110">Gibt die Liste der Laufwerke an, die beim nächsten Neustart für Autochk geplant werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aeeef-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="aeeef-111">Die Zeichen folgen Syntax besteht aus dem Laufwerk Buchstaben, gefolgt von einem Doppelpunkt für den logischen Datenträger, z. b. "C:".</span><span class="sxs-lookup"><span data-stu-id="aeeef-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="aeeef-112">Überprüfen Sie immer die Gültigkeit der Laufwerk Buchstaben im *LogicalDisk* -Array, wenn die Daten aus einer unbekannten Quelle stammen, oder aus einer nicht vertrauenswürdigen Quelle.</span><span class="sxs-lookup"><span data-stu-id="aeeef-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeeef-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aeeef-113">Return value</span></span>

<span data-ttu-id="aeeef-114">Gibt bei Erfolg den Wert 0 (null) und einen anderen Wert zurück, wenn ein anderer Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="aeeef-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="aeeef-115">Die Werte sind in der folgenden Liste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="aeeef-115">Values are listed in the following list.</span></span> <span data-ttu-id="aeeef-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="aeeef-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="aeeef-117">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="aeeef-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="aeeef-118">**Kein Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="aeeef-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aeeef-119">**Fehler: Remote Laufwerk** (1)</span><span class="sxs-lookup"><span data-stu-id="aeeef-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="aeeef-120">**Fehler-** Wechsel Datenträger (2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="aeeef-121">**Fehler-Laufwerk nicht Stammverzeichnis** (3)</span><span class="sxs-lookup"><span data-stu-id="aeeef-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="aeeef-122">**Fehler-Unbekanntes Laufwerk** (4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="aeeef-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aeeef-123">Remarks</span></span>

<span data-ttu-id="aeeef-124">Diese Methode gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="aeeef-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="aeeef-125">Diese Methode ist nicht auf zugeordnete logische Laufwerke anwendbar.</span><span class="sxs-lookup"><span data-stu-id="aeeef-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="aeeef-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeeef-126">Examples</span></span>

<span data-ttu-id="aeeef-127">Die folgenden VBScript-und PowerShell-Beispiele planen Autochk.exe bei der nächsten Neustarts des Computers auf Laufwerk C ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aeeef-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="aeeef-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aeeef-128">Requirements</span></span>



| <span data-ttu-id="aeeef-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aeeef-129">Requirement</span></span> | <span data-ttu-id="aeeef-130">Wert</span><span class="sxs-lookup"><span data-stu-id="aeeef-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeeef-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aeeef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="aeeef-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aeeef-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aeeef-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aeeef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="aeeef-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aeeef-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aeeef-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="aeeef-135">Namespace</span></span><br/>                | <span data-ttu-id="aeeef-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aeeef-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aeeef-137">MOF</span><span class="sxs-lookup"><span data-stu-id="aeeef-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeeef-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aeeef-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeeef-139">DLL</span><span class="sxs-lookup"><span data-stu-id="aeeef-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeeef-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeeef-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeeef-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeeef-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeeef-142">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="aeeef-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

