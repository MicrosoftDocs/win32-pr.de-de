---
description: Mit der Delete-Methode wird die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) gelöscht. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: 490d0578-a545-423b-9640-ec09f4ef8d96
ms.tgt_platform: multiple
title: Delete-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 32e29808b60c9933bec927ed7e351fc8c5aa9250
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041399"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a><span data-ttu-id="eb0de-104">Delete-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb0de-104">Delete method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="eb0de-105">Mit der **Delete** -Methode wird die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="eb0de-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="eb0de-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb0de-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb0de-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eb0de-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb0de-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb0de-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb0de-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb0de-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb0de-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb0de-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0de-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb0de-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="eb0de-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb0de-112">Parameters</span></span>

<span data-ttu-id="eb0de-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eb0de-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb0de-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb0de-114">Return value</span></span>

<span data-ttu-id="eb0de-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="eb0de-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="eb0de-116">**0**</span><span class="sxs-lookup"><span data-stu-id="eb0de-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eb0de-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-118">**2**</span><span class="sxs-lookup"><span data-stu-id="eb0de-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-119">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="eb0de-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-120">**8**</span><span class="sxs-lookup"><span data-stu-id="eb0de-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-121">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb0de-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-122">**9**</span><span class="sxs-lookup"><span data-stu-id="eb0de-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb0de-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-124">**10**</span><span class="sxs-lookup"><span data-stu-id="eb0de-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eb0de-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-126">**11**</span><span class="sxs-lookup"><span data-stu-id="eb0de-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-127">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="eb0de-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-128">**12**</span><span class="sxs-lookup"><span data-stu-id="eb0de-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-129">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="eb0de-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-130">**13**</span><span class="sxs-lookup"><span data-stu-id="eb0de-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-131">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="eb0de-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-132">**14**</span><span class="sxs-lookup"><span data-stu-id="eb0de-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="eb0de-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-134">**15**</span><span class="sxs-lookup"><span data-stu-id="eb0de-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="eb0de-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-136">**16**</span><span class="sxs-lookup"><span data-stu-id="eb0de-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="eb0de-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-138">**17**</span><span class="sxs-lookup"><span data-stu-id="eb0de-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-139">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="eb0de-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="eb0de-140">**21**</span><span class="sxs-lookup"><span data-stu-id="eb0de-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="eb0de-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="eb0de-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb0de-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb0de-142">Remarks</span></span>

<span data-ttu-id="eb0de-143">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb0de-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="eb0de-144">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="eb0de-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="eb0de-145">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eb0de-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb0de-146">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eb0de-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0de-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb0de-147">Requirements</span></span>



| <span data-ttu-id="eb0de-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb0de-148">Requirement</span></span> | <span data-ttu-id="eb0de-149">Wert</span><span class="sxs-lookup"><span data-stu-id="eb0de-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0de-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb0de-150">Minimum supported client</span></span><br/> | <span data-ttu-id="eb0de-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb0de-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb0de-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb0de-152">Minimum supported server</span></span><br/> | <span data-ttu-id="eb0de-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb0de-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb0de-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb0de-154">Namespace</span></span><br/>                | <span data-ttu-id="eb0de-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb0de-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb0de-156">MOF</span><span class="sxs-lookup"><span data-stu-id="eb0de-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb0de-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb0de-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb0de-158">DLL</span><span class="sxs-lookup"><span data-stu-id="eb0de-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb0de-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb0de-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb0de-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb0de-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0de-161">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="eb0de-161">CIM\_DeviceFile</span></span>](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="eb0de-162">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="eb0de-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

