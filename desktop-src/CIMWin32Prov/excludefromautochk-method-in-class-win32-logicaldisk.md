---
description: Schließt Datenträger aus dem Autochk-Vorgang aus, der beim nächsten Neustart ausgeführt werden soll.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Excludefromautochk-Methode der Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343594"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="9f43f-103">Excludefromautochk-Methode der Win32 \_ LogicalDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="9f43f-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="9f43f-104">Die **excludefromautochk** -Methode schließt Datenträger aus dem **Autochk** -Vorgang aus, der beim nächsten Neustart ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f43f-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="9f43f-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f43f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9f43f-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9f43f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f43f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f43f-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="9f43f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f43f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f43f-109">*LogicalDisk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f43f-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f43f-110">Liste der Laufwerke, die beim nächsten Neustart vom **Autochk** ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f43f-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="9f43f-111">Die Zeichen folgen Syntax besteht aus dem Laufwerk Buchstaben, gefolgt von einem Doppelpunkt für den logischen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9f43f-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="9f43f-112">Beispiel: "C:"</span><span class="sxs-lookup"><span data-stu-id="9f43f-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f43f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f43f-113">Return value</span></span>

<span data-ttu-id="9f43f-114">Gibt einen Wert von 0 (null) zurück, wenn kein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="9f43f-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="9f43f-115">Die Werte sind in der folgenden Liste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f43f-115">Values are listed in the following list.</span></span> <span data-ttu-id="9f43f-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9f43f-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9f43f-117">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9f43f-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9f43f-118">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="9f43f-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f43f-119">**Fehler: Remote Laufwerk** (1)</span><span class="sxs-lookup"><span data-stu-id="9f43f-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9f43f-120">**Fehler-** Wechsel Datenträger (2)</span><span class="sxs-lookup"><span data-stu-id="9f43f-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9f43f-121">**Fehler-Laufwerk nicht Stammverzeichnis** (3)</span><span class="sxs-lookup"><span data-stu-id="9f43f-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9f43f-122">**Fehler-Unbekanntes Laufwerk** (4)</span><span class="sxs-lookup"><span data-stu-id="9f43f-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9f43f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f43f-123">Remarks</span></span>

<span data-ttu-id="9f43f-124">Wenn nicht ausgeschlossen, wird **Autochk** auf dem Datenträger ausgeführt, wenn das änderungsbit für den Datenträger festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f43f-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="9f43f-125">Beachten Sie, dass die Aufrufe zum Ausschließen von Datenträgern nicht kumulativ sind.</span><span class="sxs-lookup"><span data-stu-id="9f43f-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="9f43f-126">Wenn ein-Rückruf zum Ausschließen einiger Datenträger durchgeführt wird, wird die neue Liste nicht zur Liste der Datenträger hinzugefügt, die bereits für den Ausschluss markiert sind.</span><span class="sxs-lookup"><span data-stu-id="9f43f-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="9f43f-127">Die neue Liste der Datenträger überschreibt die vorherige Liste.</span><span class="sxs-lookup"><span data-stu-id="9f43f-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="9f43f-128">Diese Methode gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="9f43f-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="9f43f-129">Sie ist nicht auf zugeordnete logische Laufwerke anwendbar.</span><span class="sxs-lookup"><span data-stu-id="9f43f-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="9f43f-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f43f-130">Examples</span></span>

<span data-ttu-id="9f43f-131">Mit dem folgenden VBScript-Codebeispiel wird sichergestellt, dass Autochk.exe nicht für Laufwerk c ausgeführt wird, wenn der Computer das nächste Mal neu gestartet wird, selbst wenn das "Dirty Bit" auf Laufwerk c festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9f43f-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="9f43f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f43f-132">Requirements</span></span>



| <span data-ttu-id="9f43f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f43f-133">Requirement</span></span> | <span data-ttu-id="9f43f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9f43f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f43f-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f43f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9f43f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f43f-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f43f-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f43f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9f43f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f43f-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f43f-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f43f-139">Namespace</span></span><br/>                | <span data-ttu-id="9f43f-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9f43f-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f43f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9f43f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f43f-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f43f-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f43f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9f43f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f43f-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f43f-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f43f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f43f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f43f-146">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="9f43f-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="9f43f-147">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9f43f-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

