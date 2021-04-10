---
description: Deinstalkomprimieren Sie die im Objekt Pfad angegebene Datei (oder das Verzeichnis) des logischen Geräts. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: a9b5e9bc-1c31-4518-ade4-8e9a0106608e
ms.tgt_platform: multiple
title: Uncompress-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bc7bd0a9759a3eb02d1faee6b6fb669cde4dba8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214079"
---
# <a name="uncompress-method-of-the-cim_devicefile-class"></a><span data-ttu-id="0b621-104">Uncompress-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b621-104">Uncompress method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="0b621-105">Mit der **uncompress** -Methode wird die im Objekt Pfad angegebene logische Gerätedatei (oder das angegebene Verzeichnis) entpackt.</span><span class="sxs-lookup"><span data-stu-id="0b621-105">The **Uncompress** method uncompressed the logical device file (or directory) specified in the object path.</span></span> <span data-ttu-id="0b621-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0b621-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b621-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0b621-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b621-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b621-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b621-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b621-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0b621-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0b621-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b621-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b621-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="0b621-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b621-112">Parameters</span></span>

<span data-ttu-id="0b621-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0b621-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b621-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b621-114">Return value</span></span>

<span data-ttu-id="0b621-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0b621-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0b621-116">**0**</span><span class="sxs-lookup"><span data-stu-id="0b621-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0b621-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-118">**2**</span><span class="sxs-lookup"><span data-stu-id="0b621-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-119">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="0b621-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-120">**8**</span><span class="sxs-lookup"><span data-stu-id="0b621-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-121">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0b621-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-122">**9**</span><span class="sxs-lookup"><span data-stu-id="0b621-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="0b621-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-124">**10**</span><span class="sxs-lookup"><span data-stu-id="0b621-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0b621-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-126">**11**</span><span class="sxs-lookup"><span data-stu-id="0b621-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-127">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="0b621-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-128">**12**</span><span class="sxs-lookup"><span data-stu-id="0b621-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-129">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0b621-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-130">**13**</span><span class="sxs-lookup"><span data-stu-id="0b621-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-131">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0b621-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-132">**14**</span><span class="sxs-lookup"><span data-stu-id="0b621-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="0b621-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-134">**15**</span><span class="sxs-lookup"><span data-stu-id="0b621-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="0b621-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-136">**16**</span><span class="sxs-lookup"><span data-stu-id="0b621-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="0b621-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-138">**17**</span><span class="sxs-lookup"><span data-stu-id="0b621-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-139">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0b621-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0b621-140">**21**</span><span class="sxs-lookup"><span data-stu-id="0b621-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0b621-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="0b621-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b621-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b621-142">Remarks</span></span>

<span data-ttu-id="0b621-143">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="0b621-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0b621-144">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="0b621-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0b621-145">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0b621-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b621-146">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0b621-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b621-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b621-147">Requirements</span></span>



| <span data-ttu-id="0b621-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b621-148">Requirement</span></span> | <span data-ttu-id="0b621-149">Wert</span><span class="sxs-lookup"><span data-stu-id="0b621-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b621-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b621-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0b621-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b621-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b621-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b621-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0b621-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b621-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b621-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b621-154">Namespace</span></span><br/>                | <span data-ttu-id="0b621-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0b621-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b621-156">MOF</span><span class="sxs-lookup"><span data-stu-id="0b621-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b621-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0b621-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b621-158">DLL</span><span class="sxs-lookup"><span data-stu-id="0b621-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b621-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b621-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b621-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b621-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b621-161">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="0b621-161">CIM\_DeviceFile</span></span>](uncompress-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="0b621-162">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="0b621-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

