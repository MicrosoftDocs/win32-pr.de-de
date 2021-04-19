---
description: Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den filename-Parameter angegeben wird.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: CopyEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346868"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="1d682-103">CopyEx-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="1d682-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="1d682-104">Die **CopyEx** -Methode kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d682-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="1d682-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="1d682-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="1d682-106">Diese Methode ist eine erweiterte Version der [**Copy**](copy-method-in-class-cim-logicalfile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1d682-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d682-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d682-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d682-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d682-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d682-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d682-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d682-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1d682-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d682-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d682-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1d682-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d682-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d682-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d682-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d682-114">Der voll qualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="1d682-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="1d682-115">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="1d682-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="1d682-116">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d682-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d682-117">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1d682-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="1d682-118">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1d682-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-119">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1d682-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d682-120">Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) benennt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d682-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="1d682-121">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="1d682-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1d682-122">Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d682-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-123">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1d682-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d682-124">TRUE gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d682-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="1d682-125">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1d682-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d682-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d682-126">Return value</span></span>

<span data-ttu-id="1d682-127">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="1d682-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1d682-128">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="1d682-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-129">0</span><span class="sxs-lookup"><span data-stu-id="1d682-129">0</span></span>

<span data-ttu-id="1d682-130">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1d682-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-131">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="1d682-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-132">2</span><span class="sxs-lookup"><span data-stu-id="1d682-132">2</span></span>

<span data-ttu-id="1d682-133">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="1d682-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-134">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="1d682-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-135">8</span><span class="sxs-lookup"><span data-stu-id="1d682-135">8</span></span>

<span data-ttu-id="1d682-136">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1d682-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-137">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d682-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-138">9</span><span class="sxs-lookup"><span data-stu-id="1d682-138">9</span></span>

<span data-ttu-id="1d682-139">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="1d682-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-140">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="1d682-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-141">10</span><span class="sxs-lookup"><span data-stu-id="1d682-141">10</span></span>

<span data-ttu-id="1d682-142">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1d682-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-143">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="1d682-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-144">11</span><span class="sxs-lookup"><span data-stu-id="1d682-144">11</span></span>

<span data-ttu-id="1d682-145">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="1d682-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-146">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="1d682-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-147">12</span><span class="sxs-lookup"><span data-stu-id="1d682-147">12</span></span>

<span data-ttu-id="1d682-148">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="1d682-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-149">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="1d682-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-150">13</span><span class="sxs-lookup"><span data-stu-id="1d682-150">13</span></span>

<span data-ttu-id="1d682-151">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="1d682-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-152">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="1d682-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-153">14</span><span class="sxs-lookup"><span data-stu-id="1d682-153">14</span></span>

<span data-ttu-id="1d682-154">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="1d682-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-155">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="1d682-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-156">15</span><span class="sxs-lookup"><span data-stu-id="1d682-156">15</span></span>

<span data-ttu-id="1d682-157">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="1d682-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-158">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="1d682-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-159">16</span><span class="sxs-lookup"><span data-stu-id="1d682-159">16</span></span>

<span data-ttu-id="1d682-160">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="1d682-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-161">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="1d682-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-162">17</span><span class="sxs-lookup"><span data-stu-id="1d682-162">17</span></span>

<span data-ttu-id="1d682-163">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="1d682-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="1d682-164">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="1d682-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1d682-165">21</span><span class="sxs-lookup"><span data-stu-id="1d682-165">21</span></span>

<span data-ttu-id="1d682-166">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="1d682-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d682-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d682-167">Remarks</span></span>

<span data-ttu-id="1d682-168">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="1d682-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1d682-169">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="1d682-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1d682-170">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1d682-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d682-171">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1d682-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d682-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d682-172">Requirements</span></span>



| <span data-ttu-id="1d682-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d682-173">Requirement</span></span> | <span data-ttu-id="1d682-174">Wert</span><span class="sxs-lookup"><span data-stu-id="1d682-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d682-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d682-175">Minimum supported client</span></span><br/> | <span data-ttu-id="1d682-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d682-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d682-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d682-177">Minimum supported server</span></span><br/> | <span data-ttu-id="1d682-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d682-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d682-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d682-179">Namespace</span></span><br/>                | <span data-ttu-id="1d682-180">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1d682-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d682-181">MOF</span><span class="sxs-lookup"><span data-stu-id="1d682-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d682-182"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1d682-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d682-183">DLL</span><span class="sxs-lookup"><span data-stu-id="1d682-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d682-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d682-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d682-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d682-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d682-186">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="1d682-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="1d682-187">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="1d682-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

