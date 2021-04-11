---
description: Benennt die im Objekt Pfad angegebene Gerätedatei (oder das Verzeichnis) um.
ms.assetid: 48c2eab3-c76d-4e4b-927e-dbb17584cccd
ms.tgt_platform: multiple
title: Rename-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 484d66a1b98ea58b7cb5de25c8f7d15065ce905b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127369"
---
# <a name="rename-method-of-the-cim_devicefile-class"></a><span data-ttu-id="07bf0-103">Rename-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="07bf0-103">Rename method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="07bf0-104">Die **Rename** -Methode benennt die im Objekt Pfad angegebene Gerätedatei (oder das Verzeichnis) um.</span><span class="sxs-lookup"><span data-stu-id="07bf0-104">The **Rename** method renames the device file (or directory) specified in the object path.</span></span> <span data-ttu-id="07bf0-105">Das Umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="07bf0-105">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span> <span data-ttu-id="07bf0-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bf0-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07bf0-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07bf0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="07bf0-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="07bf0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="07bf0-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="07bf0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07bf0-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07bf0-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07bf0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="07bf0-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="07bf0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="07bf0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07bf0-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07bf0-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-114">Voll qualifizierter neuer Name der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="07bf0-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="07bf0-115">Beispiel: "c: \\ Temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="07bf0-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07bf0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07bf0-116">Return value</span></span>

<span data-ttu-id="07bf0-117">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="07bf0-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="07bf0-118">**0**</span><span class="sxs-lookup"><span data-stu-id="07bf0-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="07bf0-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-120">**2**</span><span class="sxs-lookup"><span data-stu-id="07bf0-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-121">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="07bf0-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-122">**8**</span><span class="sxs-lookup"><span data-stu-id="07bf0-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-123">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="07bf0-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-124">**9**</span><span class="sxs-lookup"><span data-stu-id="07bf0-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="07bf0-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-126">**10**</span><span class="sxs-lookup"><span data-stu-id="07bf0-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-127">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="07bf0-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-128">**11**</span><span class="sxs-lookup"><span data-stu-id="07bf0-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-129">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="07bf0-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-130">**12**</span><span class="sxs-lookup"><span data-stu-id="07bf0-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-131">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="07bf0-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-132">**13**</span><span class="sxs-lookup"><span data-stu-id="07bf0-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-133">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="07bf0-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-134">**14**</span><span class="sxs-lookup"><span data-stu-id="07bf0-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-135">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="07bf0-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-136">**15**</span><span class="sxs-lookup"><span data-stu-id="07bf0-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-137">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="07bf0-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-138">**16**</span><span class="sxs-lookup"><span data-stu-id="07bf0-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-139">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="07bf0-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-140">**17**</span><span class="sxs-lookup"><span data-stu-id="07bf0-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-141">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="07bf0-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="07bf0-142">**21**</span><span class="sxs-lookup"><span data-stu-id="07bf0-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="07bf0-143">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="07bf0-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07bf0-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07bf0-144">Remarks</span></span>

<span data-ttu-id="07bf0-145">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="07bf0-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="07bf0-146">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="07bf0-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="07bf0-147">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="07bf0-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="07bf0-148">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="07bf0-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="07bf0-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07bf0-149">Requirements</span></span>



| <span data-ttu-id="07bf0-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07bf0-150">Requirement</span></span> | <span data-ttu-id="07bf0-151">Wert</span><span class="sxs-lookup"><span data-stu-id="07bf0-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07bf0-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07bf0-152">Minimum supported client</span></span><br/> | <span data-ttu-id="07bf0-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07bf0-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07bf0-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07bf0-154">Minimum supported server</span></span><br/> | <span data-ttu-id="07bf0-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07bf0-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07bf0-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="07bf0-156">Namespace</span></span><br/>                | <span data-ttu-id="07bf0-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07bf0-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07bf0-158">MOF</span><span class="sxs-lookup"><span data-stu-id="07bf0-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07bf0-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="07bf0-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07bf0-160">DLL</span><span class="sxs-lookup"><span data-stu-id="07bf0-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07bf0-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07bf0-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07bf0-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07bf0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bf0-163">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="07bf0-163">CIM\_DeviceFile</span></span>](rename-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="07bf0-164">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="07bf0-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

