---
description: 'Copy-Methode der CIM_DeviceFile-Klasse: Die Copy-Methode kopiert die im Objektpfad angegebene logische Datei (oder das Verzeichnis) an den speicherort, der durch den Eingabeparameter angegeben wird.'
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Copy-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 09c6d0f9400a04cc6e5a8ed4bd49ec7075b3c190
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089800"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="af57a-103">Copy-Methode der CIM \_ DeviceFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="af57a-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="af57a-104">Die **Copy-Methode** kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af57a-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="af57a-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="af57a-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="af57a-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af57a-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af57a-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="af57a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="af57a-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="af57a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="af57a-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="af57a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="af57a-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="af57a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="af57a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="af57a-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="af57a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="af57a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af57a-113">*FileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="af57a-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af57a-114">Der vollqualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="af57a-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="af57a-115">Beispiel: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="af57a-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af57a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af57a-116">Return value</span></span>

<span data-ttu-id="af57a-117">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="af57a-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="af57a-118">**0**</span><span class="sxs-lookup"><span data-stu-id="af57a-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="af57a-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-120">**2**</span><span class="sxs-lookup"><span data-stu-id="af57a-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-121">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="af57a-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-122">**8**</span><span class="sxs-lookup"><span data-stu-id="af57a-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-123">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="af57a-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-124">**9**</span><span class="sxs-lookup"><span data-stu-id="af57a-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="af57a-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-126">**10**</span><span class="sxs-lookup"><span data-stu-id="af57a-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-127">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="af57a-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-128">**11**</span><span class="sxs-lookup"><span data-stu-id="af57a-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-129">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="af57a-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-130">**12**</span><span class="sxs-lookup"><span data-stu-id="af57a-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-131">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="af57a-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-132">**13**</span><span class="sxs-lookup"><span data-stu-id="af57a-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-133">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="af57a-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-134">**14**</span><span class="sxs-lookup"><span data-stu-id="af57a-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-135">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="af57a-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-136">**15**</span><span class="sxs-lookup"><span data-stu-id="af57a-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-137">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="af57a-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-138">**16**</span><span class="sxs-lookup"><span data-stu-id="af57a-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-139">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="af57a-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-140">**17**</span><span class="sxs-lookup"><span data-stu-id="af57a-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-141">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="af57a-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="af57a-142">**21**</span><span class="sxs-lookup"><span data-stu-id="af57a-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="af57a-143">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="af57a-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af57a-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af57a-144">Remarks</span></span>

<span data-ttu-id="af57a-145">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="af57a-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="af57a-146">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="af57a-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="af57a-147">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="af57a-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="af57a-148">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="af57a-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="af57a-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af57a-149">Requirements</span></span>



| <span data-ttu-id="af57a-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af57a-150">Requirement</span></span> | <span data-ttu-id="af57a-151">Wert</span><span class="sxs-lookup"><span data-stu-id="af57a-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af57a-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af57a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="af57a-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af57a-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af57a-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af57a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="af57a-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af57a-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af57a-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="af57a-156">Namespace</span></span><br/>                | <span data-ttu-id="af57a-157">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="af57a-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af57a-158">MOF</span><span class="sxs-lookup"><span data-stu-id="af57a-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af57a-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="af57a-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af57a-160">DLL</span><span class="sxs-lookup"><span data-stu-id="af57a-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af57a-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af57a-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af57a-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="af57a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af57a-163">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="af57a-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="af57a-164">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="af57a-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

