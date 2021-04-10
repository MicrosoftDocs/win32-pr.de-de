---
description: Die Copy-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, in den Speicherort, der durch den Eingabeparameter angegeben wird.
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Copy-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a69107bd173be0aa853c1541a1e1365148c2e59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041448"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="6d9fb-103">Copy-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="6d9fb-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="6d9fb-104">Die **Copy** -Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, in den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d9fb-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6d9fb-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6d9fb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6d9fb-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6d9fb-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6d9fb-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9fb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d9fb-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="6d9fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d9fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d9fb-111">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d9fb-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-112">Der voll qualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="6d9fb-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="6d9fb-113">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="6d9fb-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d9fb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d9fb-114">Return value</span></span>

<span data-ttu-id="6d9fb-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6d9fb-116">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-117">0</span><span class="sxs-lookup"><span data-stu-id="6d9fb-117">0</span></span>

<span data-ttu-id="6d9fb-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-119">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-120">2</span><span class="sxs-lookup"><span data-stu-id="6d9fb-120">2</span></span>

<span data-ttu-id="6d9fb-121">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-122">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-123">8</span><span class="sxs-lookup"><span data-stu-id="6d9fb-123">8</span></span>

<span data-ttu-id="6d9fb-124">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-125">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-126">9</span><span class="sxs-lookup"><span data-stu-id="6d9fb-126">9</span></span>

<span data-ttu-id="6d9fb-127">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-128">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-129">10</span><span class="sxs-lookup"><span data-stu-id="6d9fb-129">10</span></span>

<span data-ttu-id="6d9fb-130">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-131">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-132">11</span><span class="sxs-lookup"><span data-stu-id="6d9fb-132">11</span></span>

<span data-ttu-id="6d9fb-133">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-134">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-135">12</span><span class="sxs-lookup"><span data-stu-id="6d9fb-135">12</span></span>

<span data-ttu-id="6d9fb-136">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-137">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-138">13</span><span class="sxs-lookup"><span data-stu-id="6d9fb-138">13</span></span>

<span data-ttu-id="6d9fb-139">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-140">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-141">14</span><span class="sxs-lookup"><span data-stu-id="6d9fb-141">14</span></span>

<span data-ttu-id="6d9fb-142">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="6d9fb-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-143">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-144">15</span><span class="sxs-lookup"><span data-stu-id="6d9fb-144">15</span></span>

<span data-ttu-id="6d9fb-145">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-146">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-147">16</span><span class="sxs-lookup"><span data-stu-id="6d9fb-147">16</span></span>

<span data-ttu-id="6d9fb-148">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-149">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-150">17</span><span class="sxs-lookup"><span data-stu-id="6d9fb-150">17</span></span>

<span data-ttu-id="6d9fb-151">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="6d9fb-152">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6d9fb-153">21</span><span class="sxs-lookup"><span data-stu-id="6d9fb-153">21</span></span>

<span data-ttu-id="6d9fb-154">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d9fb-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d9fb-155">Remarks</span></span>

<span data-ttu-id="6d9fb-156">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6d9fb-157">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6d9fb-158">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6d9fb-159">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9fb-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d9fb-160">Requirements</span></span>



| <span data-ttu-id="6d9fb-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d9fb-161">Requirement</span></span> | <span data-ttu-id="6d9fb-162">Wert</span><span class="sxs-lookup"><span data-stu-id="6d9fb-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9fb-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d9fb-163">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9fb-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d9fb-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d9fb-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d9fb-165">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9fb-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d9fb-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d9fb-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d9fb-167">Namespace</span></span><br/>                | <span data-ttu-id="6d9fb-168">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6d9fb-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d9fb-169">MOF</span><span class="sxs-lookup"><span data-stu-id="6d9fb-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d9fb-170"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6d9fb-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d9fb-171">DLL</span><span class="sxs-lookup"><span data-stu-id="6d9fb-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9fb-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9fb-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9fb-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d9fb-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9fb-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="6d9fb-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="6d9fb-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

