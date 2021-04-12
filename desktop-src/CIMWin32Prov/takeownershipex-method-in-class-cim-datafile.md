---
description: Ruft den Besitz der logischen Datendatei ab, die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der TakeOwnership-Methode, die von CIM \_ LogicalFile geerbt wird.
ms.assetid: 3bc5a060-d805-46f6-802d-9ed16b52da59
ms.tgt_platform: multiple
title: Takebesitzshipex-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41124567e8743227f46c9cb3b84dcb0d1f788bc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483718"
---
# <a name="takeownershipex-method-of-the-cim_datafile-class"></a><span data-ttu-id="c161a-104">Takebesitzshipex-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="c161a-104">TakeOwnerShipEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="c161a-105">Die Methode " **takebesitzshipex** " erhält den Besitz der logischen Datendatei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c161a-105">The **TakeOwnerShipEx** method obtains ownership of the logical data file that is specified in the object path.</span></span> <span data-ttu-id="c161a-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**TakeOwnership**](takeownership-method-in-class-cim-datafile.md) -Methode, die von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="c161a-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="c161a-107">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c161a-107">If the logical file is a directory, then this method will act recursively, taking ownership of all files and subdirectories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c161a-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c161a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c161a-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c161a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c161a-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c161a-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c161a-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c161a-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c161a-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c161a-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="c161a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c161a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c161a-114">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c161a-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c161a-115">Der Name der Datei (oder des Verzeichnisses), in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="c161a-115">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="c161a-116">Dieser Parameter ist NULL, wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c161a-116">This parameter will be null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-117">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c161a-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c161a-118">Die untergeordnete Datei (oder das Verzeichnis), die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c161a-118">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="c161a-119">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="c161a-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c161a-120">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c161a-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="c161a-121">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c161a-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-122">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c161a-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c161a-123">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile**](cim-datafile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c161a-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="c161a-124">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c161a-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c161a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c161a-125">Return value</span></span>

<span data-ttu-id="c161a-126">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="c161a-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="c161a-127">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c161a-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c161a-128">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c161a-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c161a-129">**0**</span><span class="sxs-lookup"><span data-stu-id="c161a-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-130">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c161a-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-131">**2**</span><span class="sxs-lookup"><span data-stu-id="c161a-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-132">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c161a-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-133">**8**</span><span class="sxs-lookup"><span data-stu-id="c161a-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-134">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c161a-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-135">**9**</span><span class="sxs-lookup"><span data-stu-id="c161a-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-136">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="c161a-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-137">**10**</span><span class="sxs-lookup"><span data-stu-id="c161a-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-138">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c161a-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-139">**11**</span><span class="sxs-lookup"><span data-stu-id="c161a-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-140">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="c161a-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-141">**12**</span><span class="sxs-lookup"><span data-stu-id="c161a-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-142">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="c161a-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-143">**13**</span><span class="sxs-lookup"><span data-stu-id="c161a-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-144">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="c161a-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-145">**14**</span><span class="sxs-lookup"><span data-stu-id="c161a-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-146">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="c161a-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-147">**15**</span><span class="sxs-lookup"><span data-stu-id="c161a-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-148">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="c161a-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-149">**16**</span><span class="sxs-lookup"><span data-stu-id="c161a-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-150">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="c161a-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-151">**17**</span><span class="sxs-lookup"><span data-stu-id="c161a-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-152">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="c161a-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c161a-153">**21**</span><span class="sxs-lookup"><span data-stu-id="c161a-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c161a-154">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="c161a-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c161a-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c161a-155">Remarks</span></span>

<span data-ttu-id="c161a-156">Die Methode " **takebesitzshipex** " in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c161a-156">The **TakeOwnerShipEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="c161a-157">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c161a-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c161a-158">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c161a-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c161a-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c161a-159">Requirements</span></span>



| <span data-ttu-id="c161a-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c161a-160">Requirement</span></span> | <span data-ttu-id="c161a-161">Wert</span><span class="sxs-lookup"><span data-stu-id="c161a-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c161a-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c161a-162">Minimum supported client</span></span><br/> | <span data-ttu-id="c161a-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c161a-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c161a-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c161a-164">Minimum supported server</span></span><br/> | <span data-ttu-id="c161a-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c161a-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c161a-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="c161a-166">Namespace</span></span><br/>                | <span data-ttu-id="c161a-167">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c161a-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c161a-168">MOF</span><span class="sxs-lookup"><span data-stu-id="c161a-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c161a-169"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c161a-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c161a-170">DLL</span><span class="sxs-lookup"><span data-stu-id="c161a-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c161a-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c161a-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c161a-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c161a-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c161a-173">CIM- \_ Datendatei</span><span class="sxs-lookup"><span data-stu-id="c161a-173">CIM\_DataFile</span></span>](takeownershipex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="c161a-174">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="c161a-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="c161a-175">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="c161a-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="c161a-176">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="c161a-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

