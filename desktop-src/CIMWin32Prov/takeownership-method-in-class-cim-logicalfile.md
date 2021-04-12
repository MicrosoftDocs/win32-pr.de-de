---
description: Die TakeOwnership-Methode ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist. Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: TakeOwnership-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523016"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="855ff-104">TakeOwnership-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="855ff-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="855ff-105">Die **TakeOwnership** -Methode ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="855ff-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="855ff-106">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="855ff-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="855ff-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="855ff-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="855ff-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="855ff-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="855ff-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="855ff-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="855ff-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="855ff-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="855ff-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="855ff-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="855ff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="855ff-112">Parameters</span></span>

<span data-ttu-id="855ff-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="855ff-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="855ff-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="855ff-114">Return value</span></span>

<span data-ttu-id="855ff-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="855ff-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="855ff-116">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="855ff-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-117">0</span><span class="sxs-lookup"><span data-stu-id="855ff-117">0</span></span>

<span data-ttu-id="855ff-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="855ff-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-119">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="855ff-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-120">2</span><span class="sxs-lookup"><span data-stu-id="855ff-120">2</span></span>

<span data-ttu-id="855ff-121">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="855ff-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-122">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="855ff-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-123">8</span><span class="sxs-lookup"><span data-stu-id="855ff-123">8</span></span>

<span data-ttu-id="855ff-124">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="855ff-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-125">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="855ff-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-126">9</span><span class="sxs-lookup"><span data-stu-id="855ff-126">9</span></span>

<span data-ttu-id="855ff-127">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="855ff-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-128">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="855ff-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-129">10</span><span class="sxs-lookup"><span data-stu-id="855ff-129">10</span></span>

<span data-ttu-id="855ff-130">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="855ff-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-131">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="855ff-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-132">11</span><span class="sxs-lookup"><span data-stu-id="855ff-132">11</span></span>

<span data-ttu-id="855ff-133">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="855ff-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-134">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="855ff-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-135">12</span><span class="sxs-lookup"><span data-stu-id="855ff-135">12</span></span>

<span data-ttu-id="855ff-136">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="855ff-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-137">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="855ff-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-138">13</span><span class="sxs-lookup"><span data-stu-id="855ff-138">13</span></span>

<span data-ttu-id="855ff-139">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="855ff-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-140">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="855ff-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-141">14</span><span class="sxs-lookup"><span data-stu-id="855ff-141">14</span></span>

<span data-ttu-id="855ff-142">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="855ff-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-143">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="855ff-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-144">15</span><span class="sxs-lookup"><span data-stu-id="855ff-144">15</span></span>

<span data-ttu-id="855ff-145">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="855ff-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-146">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="855ff-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-147">16</span><span class="sxs-lookup"><span data-stu-id="855ff-147">16</span></span>

<span data-ttu-id="855ff-148">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="855ff-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-149">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="855ff-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-150">17</span><span class="sxs-lookup"><span data-stu-id="855ff-150">17</span></span>

<span data-ttu-id="855ff-151">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="855ff-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="855ff-152">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="855ff-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="855ff-153">21</span><span class="sxs-lookup"><span data-stu-id="855ff-153">21</span></span>

<span data-ttu-id="855ff-154">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="855ff-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="855ff-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="855ff-155">Remarks</span></span>

<span data-ttu-id="855ff-156">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="855ff-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="855ff-157">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="855ff-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="855ff-158">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="855ff-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="855ff-159">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="855ff-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="855ff-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="855ff-160">Requirements</span></span>



| <span data-ttu-id="855ff-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="855ff-161">Requirement</span></span> | <span data-ttu-id="855ff-162">Wert</span><span class="sxs-lookup"><span data-stu-id="855ff-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="855ff-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="855ff-163">Minimum supported client</span></span><br/> | <span data-ttu-id="855ff-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="855ff-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="855ff-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="855ff-165">Minimum supported server</span></span><br/> | <span data-ttu-id="855ff-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="855ff-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="855ff-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="855ff-167">Namespace</span></span><br/>                | <span data-ttu-id="855ff-168">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="855ff-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="855ff-169">MOF</span><span class="sxs-lookup"><span data-stu-id="855ff-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="855ff-170"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="855ff-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="855ff-171">DLL</span><span class="sxs-lookup"><span data-stu-id="855ff-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="855ff-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="855ff-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="855ff-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="855ff-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="855ff-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="855ff-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="855ff-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="855ff-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

