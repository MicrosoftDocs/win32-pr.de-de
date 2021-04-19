---
description: Verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objekt Pfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: Compress-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99d9a0a346d8a9394edd9f30ff23490549f6de76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343158"
---
# <a name="compress-method-of-the-cim_datafile-class"></a><span data-ttu-id="ff32c-104">Compress-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff32c-104">Compress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="ff32c-105">Die Methode **Compress** verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff32c-105">The **Compress** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="ff32c-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff32c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff32c-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff32c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff32c-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff32c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff32c-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff32c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ff32c-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ff32c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff32c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff32c-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="ff32c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff32c-112">Parameters</span></span>

<span data-ttu-id="ff32c-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ff32c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff32c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff32c-114">Return value</span></span>

<span data-ttu-id="ff32c-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ff32c-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="ff32c-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ff32c-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ff32c-117">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ff32c-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ff32c-118">**0**</span><span class="sxs-lookup"><span data-stu-id="ff32c-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ff32c-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-120">**2**</span><span class="sxs-lookup"><span data-stu-id="ff32c-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-121">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="ff32c-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-122">**8**</span><span class="sxs-lookup"><span data-stu-id="ff32c-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-123">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ff32c-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-124">**9**</span><span class="sxs-lookup"><span data-stu-id="ff32c-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff32c-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-126">**10**</span><span class="sxs-lookup"><span data-stu-id="ff32c-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-127">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ff32c-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-128">**11**</span><span class="sxs-lookup"><span data-stu-id="ff32c-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-129">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="ff32c-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-130">**12**</span><span class="sxs-lookup"><span data-stu-id="ff32c-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-131">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="ff32c-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-132">**13**</span><span class="sxs-lookup"><span data-stu-id="ff32c-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-133">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="ff32c-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-134">**14**</span><span class="sxs-lookup"><span data-stu-id="ff32c-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-135">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="ff32c-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-136">**15**</span><span class="sxs-lookup"><span data-stu-id="ff32c-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-137">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="ff32c-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-138">**16**</span><span class="sxs-lookup"><span data-stu-id="ff32c-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-139">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="ff32c-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-140">**17**</span><span class="sxs-lookup"><span data-stu-id="ff32c-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-141">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="ff32c-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="ff32c-142">**21**</span><span class="sxs-lookup"><span data-stu-id="ff32c-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ff32c-143">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="ff32c-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff32c-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff32c-144">Remarks</span></span>

<span data-ttu-id="ff32c-145">Die Methode **komprimieren** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff32c-145">The **Compress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="ff32c-146">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ff32c-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff32c-147">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ff32c-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff32c-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff32c-148">Requirements</span></span>



| <span data-ttu-id="ff32c-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff32c-149">Requirement</span></span> | <span data-ttu-id="ff32c-150">Wert</span><span class="sxs-lookup"><span data-stu-id="ff32c-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff32c-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff32c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ff32c-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff32c-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff32c-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff32c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ff32c-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff32c-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff32c-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff32c-155">Namespace</span></span><br/>                | <span data-ttu-id="ff32c-156">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ff32c-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff32c-157">MOF</span><span class="sxs-lookup"><span data-stu-id="ff32c-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff32c-158"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ff32c-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff32c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="ff32c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff32c-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff32c-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff32c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff32c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff32c-162">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="ff32c-162">**CIM\_DataFile**</span></span>](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ff32c-163">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="ff32c-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ff32c-164">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="ff32c-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="ff32c-165">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="ff32c-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

