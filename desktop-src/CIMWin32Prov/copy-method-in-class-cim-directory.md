---
description: 'Copy-Methode der CIM_Directory-Klasse: Die Copy-Methode kopiert die im Objektpfad angegebene logische Datei (oder das Verzeichnis) an den speicherort, der durch den Eingabeparameter angegeben wird.'
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
ms.openlocfilehash: 6aff8ce62cf0358f494d5b3d83872b831e07ec4b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089738"
---
# <a name="copy-method-of-the-cim_directory-class"></a><span data-ttu-id="364b5-103">Copy-Methode der CIM \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="364b5-103">Copy method of the CIM\_Directory class</span></span>

<span data-ttu-id="364b5-104">Die **Copy-Methode** kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="364b5-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="364b5-105">Eine Kopie wird nicht unterstützt, wenn das Überschreiben einer vorhandenen logischen Datei erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="364b5-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="364b5-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="364b5-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="364b5-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="364b5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="364b5-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="364b5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="364b5-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="364b5-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="364b5-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="364b5-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="364b5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="364b5-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="364b5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="364b5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="364b5-113">*FileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="364b5-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="364b5-114">Vollqualifizierte Name der Kopie der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="364b5-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="364b5-115">Beispiel: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="364b5-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="364b5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="364b5-116">Return value</span></span>

<span data-ttu-id="364b5-117">Gibt bei Erfolg den Wert 0 und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="364b5-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="364b5-118">**0**</span><span class="sxs-lookup"><span data-stu-id="364b5-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="364b5-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-120">**2**</span><span class="sxs-lookup"><span data-stu-id="364b5-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-121">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="364b5-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-122">**8**</span><span class="sxs-lookup"><span data-stu-id="364b5-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-123">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="364b5-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-124">**9**</span><span class="sxs-lookup"><span data-stu-id="364b5-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="364b5-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-126">**10**</span><span class="sxs-lookup"><span data-stu-id="364b5-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-127">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="364b5-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-128">**11**</span><span class="sxs-lookup"><span data-stu-id="364b5-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-129">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="364b5-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-130">**12**</span><span class="sxs-lookup"><span data-stu-id="364b5-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-131">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="364b5-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-132">**13**</span><span class="sxs-lookup"><span data-stu-id="364b5-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-133">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="364b5-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-134">**14**</span><span class="sxs-lookup"><span data-stu-id="364b5-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-135">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="364b5-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-136">**15**</span><span class="sxs-lookup"><span data-stu-id="364b5-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-137">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="364b5-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-138">**16**</span><span class="sxs-lookup"><span data-stu-id="364b5-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-139">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="364b5-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-140">**17**</span><span class="sxs-lookup"><span data-stu-id="364b5-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-141">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="364b5-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="364b5-142">**21**</span><span class="sxs-lookup"><span data-stu-id="364b5-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="364b5-143">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="364b5-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="364b5-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="364b5-144">Remarks</span></span>

<span data-ttu-id="364b5-145">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="364b5-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="364b5-146">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="364b5-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="364b5-147">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="364b5-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="364b5-148">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="364b5-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="364b5-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="364b5-149">Requirements</span></span>



| <span data-ttu-id="364b5-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="364b5-150">Requirement</span></span> | <span data-ttu-id="364b5-151">Wert</span><span class="sxs-lookup"><span data-stu-id="364b5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="364b5-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="364b5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="364b5-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="364b5-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="364b5-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="364b5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="364b5-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="364b5-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="364b5-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="364b5-156">Namespace</span></span><br/>                | <span data-ttu-id="364b5-157">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="364b5-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="364b5-158">MOF</span><span class="sxs-lookup"><span data-stu-id="364b5-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="364b5-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="364b5-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="364b5-160">DLL</span><span class="sxs-lookup"><span data-stu-id="364b5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="364b5-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="364b5-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="364b5-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="364b5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="364b5-163">\_CIM-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="364b5-163">CIM\_Directory</span></span>](copy-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="364b5-164">**\_CIM-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="364b5-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

