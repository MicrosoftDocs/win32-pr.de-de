---
description: Die Copy-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, in den Speicherort, der durch den Eingabeparameter angegeben wird.
ms.assetid: 71481cc8-9052-4c62-9c26-6887ea646ee1
ms.tgt_platform: multiple
title: Copy-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 02bca61e559cea9ee56b9d36b28d13c33e423f9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126928"
---
# <a name="copy-method-of-the-cim_directory-class"></a><span data-ttu-id="5613d-103">Copy-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="5613d-103">Copy method of the CIM\_Directory class</span></span>

<span data-ttu-id="5613d-104">Die **Copy** -Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, in den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5613d-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="5613d-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="5613d-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="5613d-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5613d-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5613d-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5613d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5613d-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5613d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5613d-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5613d-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5613d-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5613d-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5613d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5613d-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5613d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5613d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5613d-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5613d-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5613d-114">Der voll qualifizierte Name der Kopie der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="5613d-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="5613d-115">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="5613d-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5613d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5613d-116">Return value</span></span>

<span data-ttu-id="5613d-117">Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5613d-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5613d-118">**0**</span><span class="sxs-lookup"><span data-stu-id="5613d-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5613d-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-120">**2**</span><span class="sxs-lookup"><span data-stu-id="5613d-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-121">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5613d-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-122">**8**</span><span class="sxs-lookup"><span data-stu-id="5613d-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-123">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="5613d-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-124">**9**</span><span class="sxs-lookup"><span data-stu-id="5613d-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="5613d-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-126">**10**</span><span class="sxs-lookup"><span data-stu-id="5613d-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-127">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5613d-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-128">**11**</span><span class="sxs-lookup"><span data-stu-id="5613d-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-129">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="5613d-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-130">**12**</span><span class="sxs-lookup"><span data-stu-id="5613d-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-131">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="5613d-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-132">**13**</span><span class="sxs-lookup"><span data-stu-id="5613d-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-133">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="5613d-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-134">**14**</span><span class="sxs-lookup"><span data-stu-id="5613d-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-135">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="5613d-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-136">**15**</span><span class="sxs-lookup"><span data-stu-id="5613d-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-137">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="5613d-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-138">**16**</span><span class="sxs-lookup"><span data-stu-id="5613d-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-139">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="5613d-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-140">**17**</span><span class="sxs-lookup"><span data-stu-id="5613d-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-141">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="5613d-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="5613d-142">**21**</span><span class="sxs-lookup"><span data-stu-id="5613d-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5613d-143">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="5613d-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5613d-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5613d-144">Remarks</span></span>

<span data-ttu-id="5613d-145">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5613d-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5613d-146">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="5613d-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5613d-147">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5613d-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5613d-148">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5613d-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5613d-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5613d-149">Requirements</span></span>



| <span data-ttu-id="5613d-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5613d-150">Requirement</span></span> | <span data-ttu-id="5613d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="5613d-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5613d-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5613d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="5613d-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5613d-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5613d-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5613d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="5613d-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5613d-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5613d-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="5613d-156">Namespace</span></span><br/>                | <span data-ttu-id="5613d-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5613d-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5613d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="5613d-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5613d-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5613d-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5613d-160">DLL</span><span class="sxs-lookup"><span data-stu-id="5613d-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5613d-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5613d-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5613d-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5613d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5613d-163">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="5613d-163">CIM\_Directory</span></span>](copy-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="5613d-164">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="5613d-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

