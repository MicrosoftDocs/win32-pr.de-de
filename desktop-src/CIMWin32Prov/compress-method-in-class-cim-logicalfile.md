---
description: Die Methode komprimieren komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.
ms.assetid: 4a26beaf-388b-4f37-b4ee-ef3a7d15d2b6
ms.tgt_platform: multiple
title: Compress-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12938001d62920916e75d70ad632170c3e92bd51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860728"
---
# <a name="compress-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="efe0e-103">Compress-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="efe0e-103">Compress method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="efe0e-104">Die Methode **komprimieren** komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="efe0e-104">The **Compress** method compresses the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efe0e-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="efe0e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="efe0e-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="efe0e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="efe0e-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="efe0e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="efe0e-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="efe0e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="efe0e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="efe0e-109">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="efe0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="efe0e-110">Parameters</span></span>

<span data-ttu-id="efe0e-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="efe0e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="efe0e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efe0e-112">Return value</span></span>

<span data-ttu-id="efe0e-113">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="efe0e-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="efe0e-114">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="efe0e-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-115">0</span><span class="sxs-lookup"><span data-stu-id="efe0e-115">0</span></span>

<span data-ttu-id="efe0e-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="efe0e-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-117">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="efe0e-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-118">2</span><span class="sxs-lookup"><span data-stu-id="efe0e-118">2</span></span>

<span data-ttu-id="efe0e-119">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="efe0e-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-120">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="efe0e-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-121">8</span><span class="sxs-lookup"><span data-stu-id="efe0e-121">8</span></span>

<span data-ttu-id="efe0e-122">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="efe0e-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-123">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="efe0e-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-124">9</span><span class="sxs-lookup"><span data-stu-id="efe0e-124">9</span></span>

<span data-ttu-id="efe0e-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="efe0e-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-126">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="efe0e-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-127">10</span><span class="sxs-lookup"><span data-stu-id="efe0e-127">10</span></span>

<span data-ttu-id="efe0e-128">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="efe0e-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-129">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="efe0e-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-130">11</span><span class="sxs-lookup"><span data-stu-id="efe0e-130">11</span></span>

<span data-ttu-id="efe0e-131">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="efe0e-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-132">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="efe0e-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-133">12</span><span class="sxs-lookup"><span data-stu-id="efe0e-133">12</span></span>

<span data-ttu-id="efe0e-134">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="efe0e-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-135">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="efe0e-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-136">13</span><span class="sxs-lookup"><span data-stu-id="efe0e-136">13</span></span>

<span data-ttu-id="efe0e-137">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="efe0e-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-138">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="efe0e-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-139">14</span><span class="sxs-lookup"><span data-stu-id="efe0e-139">14</span></span>

<span data-ttu-id="efe0e-140">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="efe0e-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-141">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="efe0e-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-142">15</span><span class="sxs-lookup"><span data-stu-id="efe0e-142">15</span></span>

<span data-ttu-id="efe0e-143">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="efe0e-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-144">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="efe0e-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-145">16</span><span class="sxs-lookup"><span data-stu-id="efe0e-145">16</span></span>

<span data-ttu-id="efe0e-146">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="efe0e-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-147">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="efe0e-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-148">17</span><span class="sxs-lookup"><span data-stu-id="efe0e-148">17</span></span>

<span data-ttu-id="efe0e-149">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="efe0e-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="efe0e-150">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="efe0e-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="efe0e-151">21</span><span class="sxs-lookup"><span data-stu-id="efe0e-151">21</span></span>

<span data-ttu-id="efe0e-152">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="efe0e-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efe0e-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efe0e-153">Remarks</span></span>

<span data-ttu-id="efe0e-154">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="efe0e-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="efe0e-155">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="efe0e-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="efe0e-156">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="efe0e-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="efe0e-157">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="efe0e-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe0e-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efe0e-158">Requirements</span></span>



| <span data-ttu-id="efe0e-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efe0e-159">Requirement</span></span> | <span data-ttu-id="efe0e-160">Wert</span><span class="sxs-lookup"><span data-stu-id="efe0e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efe0e-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efe0e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="efe0e-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efe0e-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efe0e-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efe0e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="efe0e-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efe0e-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efe0e-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="efe0e-165">Namespace</span></span><br/>                | <span data-ttu-id="efe0e-166">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="efe0e-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="efe0e-167">MOF</span><span class="sxs-lookup"><span data-stu-id="efe0e-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efe0e-168"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="efe0e-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="efe0e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="efe0e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe0e-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe0e-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe0e-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efe0e-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe0e-172">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="efe0e-172">CIM\_LogicalFile</span></span>](compress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="efe0e-173">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="efe0e-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

