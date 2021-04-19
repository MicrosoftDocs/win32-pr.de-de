---
description: Komprimiert die im Objekt Pfad angegebene logische Verzeichniseintrags Datei (oder das angegebene Verzeichnis). Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: 40aac2f8-4ff6-4e21-9395-5d3d40b39b00
ms.tgt_platform: multiple
title: Compress-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1717e77fdedb0c6b2e218e66f61d67bcef7c1a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346429"
---
# <a name="compress-method-of-the-cim_directory-class"></a><span data-ttu-id="62e20-104">Methode komprimieren der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="62e20-104">Compress method of the CIM\_Directory class</span></span>

<span data-ttu-id="62e20-105">Die Methode **komprimieren** komprimiert die im Objekt Pfad angegebene Datei (oder das Verzeichnis) des logischen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="62e20-105">The **Compress** method compresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="62e20-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62e20-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62e20-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="62e20-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62e20-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="62e20-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62e20-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="62e20-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="62e20-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="62e20-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="62e20-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="62e20-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="62e20-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="62e20-112">Parameters</span></span>

<span data-ttu-id="62e20-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="62e20-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62e20-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62e20-114">Return value</span></span>

<span data-ttu-id="62e20-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="62e20-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="62e20-116">**0**</span><span class="sxs-lookup"><span data-stu-id="62e20-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="62e20-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-118">**2**</span><span class="sxs-lookup"><span data-stu-id="62e20-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-119">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="62e20-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-120">**8**</span><span class="sxs-lookup"><span data-stu-id="62e20-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-121">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="62e20-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-122">**9**</span><span class="sxs-lookup"><span data-stu-id="62e20-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="62e20-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-124">**10**</span><span class="sxs-lookup"><span data-stu-id="62e20-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="62e20-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-126">**11**</span><span class="sxs-lookup"><span data-stu-id="62e20-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-127">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="62e20-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-128">**12**</span><span class="sxs-lookup"><span data-stu-id="62e20-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-129">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="62e20-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-130">**13**</span><span class="sxs-lookup"><span data-stu-id="62e20-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-131">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="62e20-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-132">**14**</span><span class="sxs-lookup"><span data-stu-id="62e20-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="62e20-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-134">**15**</span><span class="sxs-lookup"><span data-stu-id="62e20-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="62e20-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-136">**16**</span><span class="sxs-lookup"><span data-stu-id="62e20-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="62e20-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-138">**17**</span><span class="sxs-lookup"><span data-stu-id="62e20-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-139">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="62e20-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="62e20-140">**21**</span><span class="sxs-lookup"><span data-stu-id="62e20-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="62e20-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="62e20-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62e20-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62e20-142">Remarks</span></span>

<span data-ttu-id="62e20-143">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="62e20-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="62e20-144">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="62e20-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="62e20-145">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="62e20-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62e20-146">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="62e20-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e20-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62e20-147">Requirements</span></span>



| <span data-ttu-id="62e20-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62e20-148">Requirement</span></span> | <span data-ttu-id="62e20-149">Wert</span><span class="sxs-lookup"><span data-stu-id="62e20-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62e20-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62e20-150">Minimum supported client</span></span><br/> | <span data-ttu-id="62e20-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62e20-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62e20-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62e20-152">Minimum supported server</span></span><br/> | <span data-ttu-id="62e20-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62e20-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62e20-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="62e20-154">Namespace</span></span><br/>                | <span data-ttu-id="62e20-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62e20-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62e20-156">MOF</span><span class="sxs-lookup"><span data-stu-id="62e20-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62e20-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62e20-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62e20-158">DLL</span><span class="sxs-lookup"><span data-stu-id="62e20-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62e20-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62e20-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e20-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62e20-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e20-161">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="62e20-161">CIM\_Directory</span></span>](compress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="62e20-162">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="62e20-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

