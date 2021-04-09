---
description: Die im Objekt Pfad angegebene Datei (oder das Verzeichnis) für das logische Verzeichnis wird von deinstalkomprimiert. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: da3616d0-ce45-4e9a-a570-ca9e6bd0a4fa
ms.tgt_platform: multiple
title: Uncompress-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d852305d9153fa61f33168303ccb791caad00f28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958262"
---
# <a name="uncompress-method-of-the-cim_directory-class"></a><span data-ttu-id="0d093-104">Uncompress-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="0d093-104">Uncompress method of the CIM\_Directory class</span></span>

<span data-ttu-id="0d093-105">Durch die **uncompress** -Methode wird die im Objekt Pfad angegebene Datei für das logische Verzeichnis (oder das Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="0d093-105">The **Uncompress** method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="0d093-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0d093-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d093-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d093-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d093-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0d093-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d093-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d093-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d093-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0d093-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d093-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d093-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="0d093-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d093-112">Parameters</span></span>

<span data-ttu-id="0d093-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0d093-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d093-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d093-114">Return value</span></span>

<span data-ttu-id="0d093-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0d093-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d093-116">**0**</span><span class="sxs-lookup"><span data-stu-id="0d093-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0d093-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-118">**2**</span><span class="sxs-lookup"><span data-stu-id="0d093-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-119">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="0d093-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-120">**8**</span><span class="sxs-lookup"><span data-stu-id="0d093-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-121">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0d093-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-122">**9**</span><span class="sxs-lookup"><span data-stu-id="0d093-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="0d093-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-124">**10**</span><span class="sxs-lookup"><span data-stu-id="0d093-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0d093-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-126">**11**</span><span class="sxs-lookup"><span data-stu-id="0d093-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-127">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="0d093-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-128">**12**</span><span class="sxs-lookup"><span data-stu-id="0d093-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-129">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0d093-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-130">**13**</span><span class="sxs-lookup"><span data-stu-id="0d093-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-131">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0d093-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-132">**14**</span><span class="sxs-lookup"><span data-stu-id="0d093-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="0d093-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-134">**15**</span><span class="sxs-lookup"><span data-stu-id="0d093-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="0d093-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-136">**16**</span><span class="sxs-lookup"><span data-stu-id="0d093-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="0d093-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-138">**17**</span><span class="sxs-lookup"><span data-stu-id="0d093-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-139">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0d093-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0d093-140">**21**</span><span class="sxs-lookup"><span data-stu-id="0d093-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0d093-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="0d093-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d093-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d093-142">Remarks</span></span>

<span data-ttu-id="0d093-143">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="0d093-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0d093-144">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="0d093-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0d093-145">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0d093-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d093-146">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0d093-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d093-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d093-147">Requirements</span></span>



| <span data-ttu-id="0d093-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d093-148">Requirement</span></span> | <span data-ttu-id="0d093-149">Wert</span><span class="sxs-lookup"><span data-stu-id="0d093-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d093-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d093-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0d093-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d093-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d093-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d093-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0d093-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d093-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d093-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d093-154">Namespace</span></span><br/>                | <span data-ttu-id="0d093-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d093-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d093-156">MOF</span><span class="sxs-lookup"><span data-stu-id="0d093-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d093-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d093-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d093-158">DLL</span><span class="sxs-lookup"><span data-stu-id="0d093-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d093-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d093-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d093-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d093-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d093-161">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="0d093-161">**CIM\_Directory**</span></span>](uncompress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="0d093-162">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="0d093-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

