---
description: 'Delete-Methode der CIM_Directory-Klasse: Die Delete-Methode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.'
ms.assetid: 74f59073-a17a-4be5-8247-fba8d023f448
ms.tgt_platform: multiple
title: Delete-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6d02c9eb6b603673228671b12df98c7b6884abdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089637"
---
# <a name="delete-method-of-the-cim_directory-class"></a><span data-ttu-id="8be28-104">Delete-Methode der CIM \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="8be28-104">Delete method of the CIM\_Directory class</span></span>

<span data-ttu-id="8be28-105">Die **Delete-Methode** löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8be28-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8be28-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8be28-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8be28-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8be28-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8be28-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="8be28-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8be28-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8be28-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8be28-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="8be28-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8be28-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8be28-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="8be28-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be28-112">Parameters</span></span>

<span data-ttu-id="8be28-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8be28-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8be28-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8be28-114">Return value</span></span>

<span data-ttu-id="8be28-115">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8be28-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8be28-116">**0**</span><span class="sxs-lookup"><span data-stu-id="8be28-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8be28-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-118">**2**</span><span class="sxs-lookup"><span data-stu-id="8be28-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-119">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="8be28-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-120">**8**</span><span class="sxs-lookup"><span data-stu-id="8be28-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-121">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="8be28-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-122">**9**</span><span class="sxs-lookup"><span data-stu-id="8be28-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="8be28-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-124">**10**</span><span class="sxs-lookup"><span data-stu-id="8be28-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8be28-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-126">**11**</span><span class="sxs-lookup"><span data-stu-id="8be28-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-127">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="8be28-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-128">**12**</span><span class="sxs-lookup"><span data-stu-id="8be28-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-129">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="8be28-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-130">**13**</span><span class="sxs-lookup"><span data-stu-id="8be28-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-131">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="8be28-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-132">**14**</span><span class="sxs-lookup"><span data-stu-id="8be28-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="8be28-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-134">**15**</span><span class="sxs-lookup"><span data-stu-id="8be28-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="8be28-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-136">**16**</span><span class="sxs-lookup"><span data-stu-id="8be28-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="8be28-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-138">**17**</span><span class="sxs-lookup"><span data-stu-id="8be28-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-139">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="8be28-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8be28-140">**21**</span><span class="sxs-lookup"><span data-stu-id="8be28-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8be28-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="8be28-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8be28-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8be28-142">Remarks</span></span>

<span data-ttu-id="8be28-143">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8be28-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8be28-144">Um diese Methode verwenden zu können, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8be28-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8be28-145">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="8be28-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8be28-146">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="8be28-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be28-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8be28-147">Requirements</span></span>



| <span data-ttu-id="8be28-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8be28-148">Requirement</span></span> | <span data-ttu-id="8be28-149">Wert</span><span class="sxs-lookup"><span data-stu-id="8be28-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8be28-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8be28-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8be28-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8be28-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8be28-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8be28-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8be28-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8be28-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8be28-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="8be28-154">Namespace</span></span><br/>                | <span data-ttu-id="8be28-155">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="8be28-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8be28-156">MOF</span><span class="sxs-lookup"><span data-stu-id="8be28-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8be28-157"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8be28-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8be28-158">DLL</span><span class="sxs-lookup"><span data-stu-id="8be28-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8be28-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be28-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be28-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8be28-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be28-161">\_CIM-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8be28-161">CIM\_Directory</span></span>](delete-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="8be28-162">**\_CIM-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="8be28-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

