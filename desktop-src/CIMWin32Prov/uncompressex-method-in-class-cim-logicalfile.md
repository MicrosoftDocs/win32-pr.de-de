---
description: Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der uncompress-Methode.
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: UncompressEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748936"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="55a4b-104">UncompressEx-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="55a4b-104">UncompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="55a4b-105">Die **UncompressEx** -Methode entkomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="55a4b-105">The **UncompressEx** method uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55a4b-106">Diese Methode ist eine erweiterte Version der [**uncompress**](uncompress-method-in-class-cim-logicalfile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="55a4b-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55a4b-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="55a4b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55a4b-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="55a4b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55a4b-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="55a4b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55a4b-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="55a4b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="55a4b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="55a4b-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="55a4b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="55a4b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a4b-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="55a4b-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-114">Der Name der Datei (oder des Verzeichnisses), in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="55a4b-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="55a4b-115">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="55a4b-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-116">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="55a4b-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-117">Der Name der untergeordneten Datei (oder des Verzeichnisses), die als Ausgangspunkt für die Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55a4b-117">Name of the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="55a4b-118">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="55a4b-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="55a4b-119">Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55a4b-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-120">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="55a4b-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-121">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55a4b-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="55a4b-122">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="55a4b-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a4b-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55a4b-123">Return value</span></span>

<span data-ttu-id="55a4b-124">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="55a4b-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="55a4b-125">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="55a4b-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-126">0</span><span class="sxs-lookup"><span data-stu-id="55a4b-126">0</span></span>

<span data-ttu-id="55a4b-127">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="55a4b-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-128">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="55a4b-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-129">2</span><span class="sxs-lookup"><span data-stu-id="55a4b-129">2</span></span>

<span data-ttu-id="55a4b-130">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="55a4b-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-131">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="55a4b-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-132">8</span><span class="sxs-lookup"><span data-stu-id="55a4b-132">8</span></span>

<span data-ttu-id="55a4b-133">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="55a4b-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-134">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="55a4b-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-135">9</span><span class="sxs-lookup"><span data-stu-id="55a4b-135">9</span></span>

<span data-ttu-id="55a4b-136">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="55a4b-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-137">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="55a4b-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-138">10</span><span class="sxs-lookup"><span data-stu-id="55a4b-138">10</span></span>

<span data-ttu-id="55a4b-139">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="55a4b-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-140">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="55a4b-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-141">11</span><span class="sxs-lookup"><span data-stu-id="55a4b-141">11</span></span>

<span data-ttu-id="55a4b-142">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="55a4b-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-143">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="55a4b-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-144">12</span><span class="sxs-lookup"><span data-stu-id="55a4b-144">12</span></span>

<span data-ttu-id="55a4b-145">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="55a4b-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-146">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="55a4b-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-147">13</span><span class="sxs-lookup"><span data-stu-id="55a4b-147">13</span></span>

<span data-ttu-id="55a4b-148">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="55a4b-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-149">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="55a4b-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-150">14</span><span class="sxs-lookup"><span data-stu-id="55a4b-150">14</span></span>

<span data-ttu-id="55a4b-151">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="55a4b-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-152">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="55a4b-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-153">15</span><span class="sxs-lookup"><span data-stu-id="55a4b-153">15</span></span>

<span data-ttu-id="55a4b-154">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="55a4b-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-155">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="55a4b-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-156">16</span><span class="sxs-lookup"><span data-stu-id="55a4b-156">16</span></span>

<span data-ttu-id="55a4b-157">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="55a4b-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-158">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="55a4b-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-159">17</span><span class="sxs-lookup"><span data-stu-id="55a4b-159">17</span></span>

<span data-ttu-id="55a4b-160">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="55a4b-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="55a4b-161">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="55a4b-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55a4b-162">21</span><span class="sxs-lookup"><span data-stu-id="55a4b-162">21</span></span>

<span data-ttu-id="55a4b-163">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="55a4b-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55a4b-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55a4b-164">Remarks</span></span>

<span data-ttu-id="55a4b-165">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="55a4b-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="55a4b-166">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="55a4b-166">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="55a4b-167">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="55a4b-167">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55a4b-168">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="55a4b-168">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a4b-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a4b-169">Requirements</span></span>



| <span data-ttu-id="55a4b-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a4b-170">Requirement</span></span> | <span data-ttu-id="55a4b-171">Wert</span><span class="sxs-lookup"><span data-stu-id="55a4b-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a4b-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55a4b-172">Minimum supported client</span></span><br/> | <span data-ttu-id="55a4b-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55a4b-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55a4b-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55a4b-174">Minimum supported server</span></span><br/> | <span data-ttu-id="55a4b-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55a4b-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55a4b-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="55a4b-176">Namespace</span></span><br/>                | <span data-ttu-id="55a4b-177">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55a4b-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55a4b-178">MOF</span><span class="sxs-lookup"><span data-stu-id="55a4b-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55a4b-179"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="55a4b-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55a4b-180">DLL</span><span class="sxs-lookup"><span data-stu-id="55a4b-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a4b-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a4b-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a4b-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a4b-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a4b-183">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="55a4b-183">CIM\_LogicalFile</span></span>](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="55a4b-184">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="55a4b-184">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

