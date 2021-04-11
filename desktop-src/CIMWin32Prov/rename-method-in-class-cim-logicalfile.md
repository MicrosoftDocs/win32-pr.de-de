---
description: Die Rename-Methode benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist. Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Rename-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127365"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="a8010-104">Rename-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="a8010-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="a8010-105">Die **Rename** -Methode benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a8010-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a8010-106">Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="a8010-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8010-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8010-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8010-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a8010-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8010-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8010-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a8010-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a8010-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8010-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8010-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="a8010-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8010-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8010-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8010-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8010-114">Voll qualifizierter Name der neuen Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="a8010-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="a8010-115">Beispiel: "c: \\ Temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="a8010-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8010-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8010-116">Return value</span></span>

<span data-ttu-id="a8010-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="a8010-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a8010-118">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="a8010-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-119">0</span><span class="sxs-lookup"><span data-stu-id="a8010-119">0</span></span>

<span data-ttu-id="a8010-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a8010-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-121">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="a8010-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-122">2</span><span class="sxs-lookup"><span data-stu-id="a8010-122">2</span></span>

<span data-ttu-id="a8010-123">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a8010-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-124">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="a8010-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-125">8</span><span class="sxs-lookup"><span data-stu-id="a8010-125">8</span></span>

<span data-ttu-id="a8010-126">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a8010-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-127">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="a8010-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-128">9</span><span class="sxs-lookup"><span data-stu-id="a8010-128">9</span></span>

<span data-ttu-id="a8010-129">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="a8010-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-130">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="a8010-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-131">10</span><span class="sxs-lookup"><span data-stu-id="a8010-131">10</span></span>

<span data-ttu-id="a8010-132">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a8010-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-133">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="a8010-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-134">11</span><span class="sxs-lookup"><span data-stu-id="a8010-134">11</span></span>

<span data-ttu-id="a8010-135">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="a8010-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-136">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="a8010-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-137">12</span><span class="sxs-lookup"><span data-stu-id="a8010-137">12</span></span>

<span data-ttu-id="a8010-138">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="a8010-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-139">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="a8010-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-140">13</span><span class="sxs-lookup"><span data-stu-id="a8010-140">13</span></span>

<span data-ttu-id="a8010-141">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="a8010-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-142">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="a8010-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-143">14</span><span class="sxs-lookup"><span data-stu-id="a8010-143">14</span></span>

<span data-ttu-id="a8010-144">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="a8010-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-145">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="a8010-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-146">15</span><span class="sxs-lookup"><span data-stu-id="a8010-146">15</span></span>

<span data-ttu-id="a8010-147">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="a8010-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-148">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="a8010-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-149">16</span><span class="sxs-lookup"><span data-stu-id="a8010-149">16</span></span>

<span data-ttu-id="a8010-150">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="a8010-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-151">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="a8010-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-152">17</span><span class="sxs-lookup"><span data-stu-id="a8010-152">17</span></span>

<span data-ttu-id="a8010-153">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="a8010-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="a8010-154">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="a8010-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a8010-155">21</span><span class="sxs-lookup"><span data-stu-id="a8010-155">21</span></span>

<span data-ttu-id="a8010-156">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="a8010-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8010-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8010-157">Remarks</span></span>

<span data-ttu-id="a8010-158">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a8010-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a8010-159">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="a8010-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a8010-160">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a8010-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8010-161">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a8010-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8010-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8010-162">Requirements</span></span>



| <span data-ttu-id="a8010-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8010-163">Requirement</span></span> | <span data-ttu-id="a8010-164">Wert</span><span class="sxs-lookup"><span data-stu-id="a8010-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8010-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8010-165">Minimum supported client</span></span><br/> | <span data-ttu-id="a8010-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8010-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8010-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8010-167">Minimum supported server</span></span><br/> | <span data-ttu-id="a8010-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8010-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8010-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8010-169">Namespace</span></span><br/>                | <span data-ttu-id="a8010-170">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8010-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8010-171">MOF</span><span class="sxs-lookup"><span data-stu-id="a8010-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8010-172"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a8010-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8010-173">DLL</span><span class="sxs-lookup"><span data-stu-id="a8010-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8010-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8010-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8010-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8010-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8010-176">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="a8010-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="a8010-177">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="a8010-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

