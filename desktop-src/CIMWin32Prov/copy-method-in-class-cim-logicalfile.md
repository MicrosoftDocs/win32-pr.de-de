---
description: 'Copy-Methode der CIM_LogicalFile-Klasse: Die Copy-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den speicherort, der durch den Eingabeparameter angegeben wird.'
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
ms.openlocfilehash: 10ba9c28bde9d909d947e5a73241ce1aa8f1e956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089728"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="3af95-103">Copy-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="3af95-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="3af95-104">Die **Copy-Methode** kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3af95-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3af95-105">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3af95-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3af95-106">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="3af95-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3af95-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3af95-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3af95-108">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="3af95-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3af95-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3af95-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="3af95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3af95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3af95-111">*FileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3af95-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af95-112">Vollqualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="3af95-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="3af95-113">Beispiel: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="3af95-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3af95-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3af95-114">Return value</span></span>

<span data-ttu-id="3af95-115">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3af95-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3af95-116">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="3af95-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-117">0</span><span class="sxs-lookup"><span data-stu-id="3af95-117">0</span></span>

<span data-ttu-id="3af95-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3af95-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-119">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="3af95-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-120">2</span><span class="sxs-lookup"><span data-stu-id="3af95-120">2</span></span>

<span data-ttu-id="3af95-121">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="3af95-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-122">**Nicht angegebener Fehler**</span><span class="sxs-lookup"><span data-stu-id="3af95-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-123">8</span><span class="sxs-lookup"><span data-stu-id="3af95-123">8</span></span>

<span data-ttu-id="3af95-124">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="3af95-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-125">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="3af95-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-126">9</span><span class="sxs-lookup"><span data-stu-id="3af95-126">9</span></span>

<span data-ttu-id="3af95-127">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="3af95-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-128">**Objekt ist bereits vorhanden**</span><span class="sxs-lookup"><span data-stu-id="3af95-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-129">10</span><span class="sxs-lookup"><span data-stu-id="3af95-129">10</span></span>

<span data-ttu-id="3af95-130">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3af95-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-131">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="3af95-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-132">11</span><span class="sxs-lookup"><span data-stu-id="3af95-132">11</span></span>

<span data-ttu-id="3af95-133">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="3af95-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-134">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3af95-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-135">12</span><span class="sxs-lookup"><span data-stu-id="3af95-135">12</span></span>

<span data-ttu-id="3af95-136">Plattform, nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="3af95-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-137">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="3af95-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-138">13</span><span class="sxs-lookup"><span data-stu-id="3af95-138">13</span></span>

<span data-ttu-id="3af95-139">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="3af95-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-140">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="3af95-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-141">14</span><span class="sxs-lookup"><span data-stu-id="3af95-141">14</span></span>

<span data-ttu-id="3af95-142">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="3af95-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-143">**Freigabeverletzung**</span><span class="sxs-lookup"><span data-stu-id="3af95-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-144">15</span><span class="sxs-lookup"><span data-stu-id="3af95-144">15</span></span>

<span data-ttu-id="3af95-145">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="3af95-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-146">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="3af95-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-147">16</span><span class="sxs-lookup"><span data-stu-id="3af95-147">16</span></span>

<span data-ttu-id="3af95-148">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="3af95-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-149">**Nicht privileg**</span><span class="sxs-lookup"><span data-stu-id="3af95-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-150">17</span><span class="sxs-lookup"><span data-stu-id="3af95-150">17</span></span>

<span data-ttu-id="3af95-151">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="3af95-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3af95-152">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="3af95-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3af95-153">21</span><span class="sxs-lookup"><span data-stu-id="3af95-153">21</span></span>

<span data-ttu-id="3af95-154">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="3af95-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3af95-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3af95-155">Remarks</span></span>

<span data-ttu-id="3af95-156">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="3af95-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3af95-157">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="3af95-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3af95-158">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="3af95-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3af95-159">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="3af95-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3af95-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3af95-160">Requirements</span></span>



| <span data-ttu-id="3af95-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3af95-161">Requirement</span></span> | <span data-ttu-id="3af95-162">Wert</span><span class="sxs-lookup"><span data-stu-id="3af95-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3af95-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3af95-163">Minimum supported client</span></span><br/> | <span data-ttu-id="3af95-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3af95-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3af95-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3af95-165">Minimum supported server</span></span><br/> | <span data-ttu-id="3af95-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3af95-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3af95-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="3af95-167">Namespace</span></span><br/>                | <span data-ttu-id="3af95-168">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="3af95-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3af95-169">MOF</span><span class="sxs-lookup"><span data-stu-id="3af95-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3af95-170"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3af95-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3af95-171">DLL</span><span class="sxs-lookup"><span data-stu-id="3af95-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3af95-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3af95-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af95-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3af95-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af95-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="3af95-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="3af95-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="3af95-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

