---
description: 'CompressEx-Methode der CIM_DataFile-Klasse: Verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objektpfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.'
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: CompressEx-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089788"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="128fc-104">CompressEx-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="128fc-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="128fc-105">Die **CompressEx-Methode** verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="128fc-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="128fc-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="128fc-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="128fc-107">Diese Methode ist eine erweiterte Version der [**Compress-Methode**](compress-method-in-class-cim-datafile.md) und wird von [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method)geerbt.</span><span class="sxs-lookup"><span data-stu-id="128fc-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="128fc-108">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="128fc-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="128fc-109">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="128fc-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="128fc-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="128fc-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="128fc-111">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="128fc-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="128fc-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="128fc-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="128fc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="128fc-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128fc-114">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="128fc-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="128fc-115">Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="128fc-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="128fc-116">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="128fc-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-117">*StartFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="128fc-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128fc-118">Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="128fc-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="128fc-119">In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="128fc-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="128fc-120">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im **ExecMethod-Aufruf** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="128fc-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="128fc-121">Wenn *StartFileName* verwendet wird, muss *Recursive* auch auf TRUE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="128fc-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-122">*Rekursiv* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="128fc-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128fc-123">True **gibt** an, dass die -Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile-Instanz angegeben**](cim-datafile.md) wird.</span><span class="sxs-lookup"><span data-stu-id="128fc-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="128fc-124">Bei Dateiinstanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="128fc-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128fc-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="128fc-125">Return value</span></span>

<span data-ttu-id="128fc-126">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="128fc-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="128fc-127">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="128fc-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="128fc-128">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="128fc-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="128fc-129">**0**</span><span class="sxs-lookup"><span data-stu-id="128fc-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-130">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="128fc-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-131">**2**</span><span class="sxs-lookup"><span data-stu-id="128fc-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-132">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="128fc-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-133">**8**</span><span class="sxs-lookup"><span data-stu-id="128fc-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-134">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="128fc-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-135">**9**</span><span class="sxs-lookup"><span data-stu-id="128fc-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-136">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="128fc-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-137">**10**</span><span class="sxs-lookup"><span data-stu-id="128fc-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-138">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="128fc-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-139">**11**</span><span class="sxs-lookup"><span data-stu-id="128fc-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-140">Dateisystem, nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="128fc-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-141">**12**</span><span class="sxs-lookup"><span data-stu-id="128fc-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-142">Plattform, nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="128fc-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-143">**13**</span><span class="sxs-lookup"><span data-stu-id="128fc-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-144">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="128fc-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-145">**14**</span><span class="sxs-lookup"><span data-stu-id="128fc-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-146">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="128fc-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-147">**15**</span><span class="sxs-lookup"><span data-stu-id="128fc-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-148">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="128fc-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-149">**16**</span><span class="sxs-lookup"><span data-stu-id="128fc-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-150">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="128fc-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-151">**17**</span><span class="sxs-lookup"><span data-stu-id="128fc-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-152">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="128fc-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-153">**21**</span><span class="sxs-lookup"><span data-stu-id="128fc-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="128fc-154">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="128fc-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="128fc-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="128fc-155">Remarks</span></span>

<span data-ttu-id="128fc-156">Die **CompressEx-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="128fc-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="128fc-157">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="128fc-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="128fc-158">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="128fc-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="128fc-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="128fc-159">Requirements</span></span>



| <span data-ttu-id="128fc-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="128fc-160">Requirement</span></span> | <span data-ttu-id="128fc-161">Wert</span><span class="sxs-lookup"><span data-stu-id="128fc-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="128fc-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="128fc-162">Minimum supported client</span></span><br/> | <span data-ttu-id="128fc-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="128fc-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="128fc-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="128fc-164">Minimum supported server</span></span><br/> | <span data-ttu-id="128fc-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="128fc-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="128fc-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="128fc-166">Namespace</span></span><br/>                | <span data-ttu-id="128fc-167">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="128fc-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="128fc-168">MOF</span><span class="sxs-lookup"><span data-stu-id="128fc-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="128fc-169"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="128fc-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="128fc-170">DLL</span><span class="sxs-lookup"><span data-stu-id="128fc-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="128fc-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="128fc-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="128fc-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="128fc-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="128fc-173">CIM \_ DataFile</span><span class="sxs-lookup"><span data-stu-id="128fc-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="128fc-174">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="128fc-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="128fc-175">WMI-Aufgaben: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="128fc-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="128fc-176">**Datei- und Verzeichniszugriffsrechtekonstanten**</span><span class="sxs-lookup"><span data-stu-id="128fc-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

