---
description: Mit der Delete-Methode wird die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) gelöscht.
ms.assetid: 04d43ac5-b7e6-409f-999a-577232539c15
ms.tgt_platform: multiple
title: Delete-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8462d097834015883d47ec3da0d70e517a4ead0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346249"
---
# <a name="delete-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="c7037-103">Delete-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="c7037-103">Delete method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="c7037-104">Mit der **Delete** -Methode wird die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c7037-104">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7037-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c7037-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c7037-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c7037-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c7037-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7037-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c7037-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c7037-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7037-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7037-109">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="c7037-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7037-110">Parameters</span></span>

<span data-ttu-id="c7037-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7037-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7037-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7037-112">Return value</span></span>

<span data-ttu-id="c7037-113">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="c7037-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c7037-114">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="c7037-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-115">0</span><span class="sxs-lookup"><span data-stu-id="c7037-115">0</span></span>

<span data-ttu-id="c7037-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c7037-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-117">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="c7037-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-118">2</span><span class="sxs-lookup"><span data-stu-id="c7037-118">2</span></span>

<span data-ttu-id="c7037-119">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c7037-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-120">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7037-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-121">8</span><span class="sxs-lookup"><span data-stu-id="c7037-121">8</span></span>

<span data-ttu-id="c7037-122">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c7037-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-123">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="c7037-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-124">9</span><span class="sxs-lookup"><span data-stu-id="c7037-124">9</span></span>

<span data-ttu-id="c7037-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="c7037-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-126">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="c7037-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-127">10</span><span class="sxs-lookup"><span data-stu-id="c7037-127">10</span></span>

<span data-ttu-id="c7037-128">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7037-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-129">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="c7037-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-130">11</span><span class="sxs-lookup"><span data-stu-id="c7037-130">11</span></span>

<span data-ttu-id="c7037-131">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="c7037-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-132">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="c7037-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-133">12</span><span class="sxs-lookup"><span data-stu-id="c7037-133">12</span></span>

<span data-ttu-id="c7037-134">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="c7037-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-135">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="c7037-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-136">13</span><span class="sxs-lookup"><span data-stu-id="c7037-136">13</span></span>

<span data-ttu-id="c7037-137">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="c7037-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-138">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="c7037-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-139">14</span><span class="sxs-lookup"><span data-stu-id="c7037-139">14</span></span>

<span data-ttu-id="c7037-140">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="c7037-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-141">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="c7037-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-142">15</span><span class="sxs-lookup"><span data-stu-id="c7037-142">15</span></span>

<span data-ttu-id="c7037-143">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="c7037-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-144">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="c7037-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-145">16</span><span class="sxs-lookup"><span data-stu-id="c7037-145">16</span></span>

<span data-ttu-id="c7037-146">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="c7037-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-147">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="c7037-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-148">17</span><span class="sxs-lookup"><span data-stu-id="c7037-148">17</span></span>

<span data-ttu-id="c7037-149">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="c7037-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c7037-150">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="c7037-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c7037-151">21</span><span class="sxs-lookup"><span data-stu-id="c7037-151">21</span></span>

<span data-ttu-id="c7037-152">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7037-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7037-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7037-153">Remarks</span></span>

<span data-ttu-id="c7037-154">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c7037-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c7037-155">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="c7037-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c7037-156">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c7037-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c7037-157">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c7037-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7037-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7037-158">Requirements</span></span>



| <span data-ttu-id="c7037-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7037-159">Requirement</span></span> | <span data-ttu-id="c7037-160">Wert</span><span class="sxs-lookup"><span data-stu-id="c7037-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7037-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7037-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c7037-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7037-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7037-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7037-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c7037-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7037-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7037-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7037-165">Namespace</span></span><br/>                | <span data-ttu-id="c7037-166">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c7037-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7037-167">MOF</span><span class="sxs-lookup"><span data-stu-id="c7037-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7037-168"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c7037-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7037-169">DLL</span><span class="sxs-lookup"><span data-stu-id="c7037-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7037-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7037-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7037-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7037-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7037-172">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="c7037-172">CIM\_LogicalFile</span></span>](delete-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="c7037-173">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="c7037-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

