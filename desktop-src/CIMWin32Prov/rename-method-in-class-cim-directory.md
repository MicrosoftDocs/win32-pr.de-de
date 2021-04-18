---
description: Benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist. Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Rename-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483731"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="8443d-104">Rename-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="8443d-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="8443d-105">Die **Rename** -Methode benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8443d-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8443d-106">Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="8443d-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="8443d-107">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8443d-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8443d-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8443d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8443d-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8443d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8443d-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8443d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8443d-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8443d-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8443d-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="8443d-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="8443d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8443d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8443d-114">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8443d-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8443d-115">Voll qualifizierter neuer Name der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="8443d-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="8443d-116">Beispiel: "c: \\ Temp \\newname.txt"</span><span class="sxs-lookup"><span data-stu-id="8443d-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8443d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8443d-117">Return value</span></span>

<span data-ttu-id="8443d-118">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8443d-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8443d-119">**0**</span><span class="sxs-lookup"><span data-stu-id="8443d-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8443d-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-121">**2**</span><span class="sxs-lookup"><span data-stu-id="8443d-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-122">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="8443d-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-123">**8**</span><span class="sxs-lookup"><span data-stu-id="8443d-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-124">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8443d-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-125">**9**</span><span class="sxs-lookup"><span data-stu-id="8443d-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-126">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="8443d-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-127">**10**</span><span class="sxs-lookup"><span data-stu-id="8443d-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-128">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8443d-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-129">**11**</span><span class="sxs-lookup"><span data-stu-id="8443d-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-130">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="8443d-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-131">**12**</span><span class="sxs-lookup"><span data-stu-id="8443d-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-132">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="8443d-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-133">**13**</span><span class="sxs-lookup"><span data-stu-id="8443d-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-134">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="8443d-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-135">**14**</span><span class="sxs-lookup"><span data-stu-id="8443d-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-136">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="8443d-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-137">**15**</span><span class="sxs-lookup"><span data-stu-id="8443d-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-138">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="8443d-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-139">**16**</span><span class="sxs-lookup"><span data-stu-id="8443d-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-140">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="8443d-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-141">**17**</span><span class="sxs-lookup"><span data-stu-id="8443d-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-142">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="8443d-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8443d-143">**21**</span><span class="sxs-lookup"><span data-stu-id="8443d-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8443d-144">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="8443d-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8443d-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8443d-145">Remarks</span></span>

<span data-ttu-id="8443d-146">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8443d-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8443d-147">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8443d-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8443d-148">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8443d-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8443d-149">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8443d-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8443d-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8443d-150">Requirements</span></span>



| <span data-ttu-id="8443d-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8443d-151">Requirement</span></span> | <span data-ttu-id="8443d-152">Wert</span><span class="sxs-lookup"><span data-stu-id="8443d-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8443d-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8443d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8443d-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8443d-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8443d-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8443d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8443d-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8443d-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8443d-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="8443d-157">Namespace</span></span><br/>                | <span data-ttu-id="8443d-158">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8443d-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8443d-159">MOF</span><span class="sxs-lookup"><span data-stu-id="8443d-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8443d-160"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8443d-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8443d-161">DLL</span><span class="sxs-lookup"><span data-stu-id="8443d-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8443d-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8443d-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8443d-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8443d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8443d-164">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8443d-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="8443d-165">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="8443d-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

