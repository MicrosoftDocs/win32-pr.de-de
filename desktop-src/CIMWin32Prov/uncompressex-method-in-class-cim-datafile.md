---
description: Deinstalkomprimiert die logische Datendatei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der uncompress-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: UncompressEx-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127509"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="8b1f1-104">UncompressEx-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b1f1-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="8b1f1-105">Die **UncompressEx** -Methode entkomprimiert die logische Datendatei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="8b1f1-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**uncompress**](uncompress-method-in-class-cim-datafile.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b1f1-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8b1f1-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8b1f1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8b1f1-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8b1f1-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8b1f1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b1f1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b1f1-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8b1f1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b1f1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b1f1-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b1f1-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-114">Der Name der Datei (oder des Verzeichnisses), in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8b1f1-115">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-116">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b1f1-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-117">Die untergeordnete Datei (oder das Verzeichnis), die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="8b1f1-118">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="8b1f1-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8b1f1-119">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="8b1f1-120">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-121">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b1f1-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-122">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile**](cim-datafile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="8b1f1-123">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b1f1-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b1f1-124">Return value</span></span>

<span data-ttu-id="8b1f1-125">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="8b1f1-126">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8b1f1-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8b1f1-127">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8b1f1-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8b1f1-128">**0**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-129">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-130">**2**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-131">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-132">**8**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-133">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-134">**9**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-135">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-136">**10**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-137">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-138">**11**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-139">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-140">**12**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-141">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-142">**13**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-143">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-144">**14**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-145">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="8b1f1-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-146">**15**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-147">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-148">**16**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-149">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-150">**17**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-151">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8b1f1-152">**21**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8b1f1-153">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b1f1-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b1f1-154">Remarks</span></span>

<span data-ttu-id="8b1f1-155">Die **UncompressEx** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="8b1f1-156">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8b1f1-157">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1f1-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b1f1-158">Requirements</span></span>



| <span data-ttu-id="8b1f1-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b1f1-159">Requirement</span></span> | <span data-ttu-id="8b1f1-160">Wert</span><span class="sxs-lookup"><span data-stu-id="8b1f1-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1f1-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b1f1-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1f1-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b1f1-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b1f1-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b1f1-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1f1-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b1f1-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b1f1-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b1f1-165">Namespace</span></span><br/>                | <span data-ttu-id="8b1f1-166">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b1f1-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b1f1-167">MOF</span><span class="sxs-lookup"><span data-stu-id="8b1f1-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b1f1-168"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b1f1-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b1f1-169">DLL</span><span class="sxs-lookup"><span data-stu-id="8b1f1-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b1f1-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b1f1-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1f1-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b1f1-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1f1-172">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8b1f1-173">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8b1f1-174">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="8b1f1-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="8b1f1-175">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

