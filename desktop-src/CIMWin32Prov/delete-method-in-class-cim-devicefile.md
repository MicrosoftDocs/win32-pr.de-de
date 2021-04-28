---
description: 'Delete-Methode der CIM_DeviceFile-Klasse: Die Delete-Methode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.'
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
ms.openlocfilehash: 5e96ba9837252158510c306a622df86c09bbfd96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089628"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a><span data-ttu-id="95a3b-104">Delete-Methode der CIM \_ DeviceFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="95a3b-104">Delete method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="95a3b-105">Die **Delete-Methode** löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="95a3b-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="95a3b-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="95a3b-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95a3b-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95a3b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="95a3b-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="95a3b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="95a3b-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="95a3b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="95a3b-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="95a3b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="95a3b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="95a3b-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="95a3b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="95a3b-112">Parameters</span></span>

<span data-ttu-id="95a3b-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="95a3b-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95a3b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95a3b-114">Return value</span></span>

<span data-ttu-id="95a3b-115">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="95a3b-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="95a3b-116">**0**</span><span class="sxs-lookup"><span data-stu-id="95a3b-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="95a3b-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-118">**2**</span><span class="sxs-lookup"><span data-stu-id="95a3b-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-119">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="95a3b-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-120">**8**</span><span class="sxs-lookup"><span data-stu-id="95a3b-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-121">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="95a3b-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-122">**9**</span><span class="sxs-lookup"><span data-stu-id="95a3b-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="95a3b-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-124">**10**</span><span class="sxs-lookup"><span data-stu-id="95a3b-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95a3b-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-126">**11**</span><span class="sxs-lookup"><span data-stu-id="95a3b-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-127">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="95a3b-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-128">**12**</span><span class="sxs-lookup"><span data-stu-id="95a3b-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-129">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="95a3b-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-130">**13**</span><span class="sxs-lookup"><span data-stu-id="95a3b-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-131">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="95a3b-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-132">**14**</span><span class="sxs-lookup"><span data-stu-id="95a3b-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="95a3b-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-134">**15**</span><span class="sxs-lookup"><span data-stu-id="95a3b-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="95a3b-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-136">**16**</span><span class="sxs-lookup"><span data-stu-id="95a3b-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="95a3b-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-138">**17**</span><span class="sxs-lookup"><span data-stu-id="95a3b-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-139">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="95a3b-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="95a3b-140">**21**</span><span class="sxs-lookup"><span data-stu-id="95a3b-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="95a3b-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="95a3b-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95a3b-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95a3b-142">Remarks</span></span>

<span data-ttu-id="95a3b-143">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="95a3b-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="95a3b-144">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="95a3b-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="95a3b-145">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="95a3b-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="95a3b-146">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="95a3b-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a3b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95a3b-147">Requirements</span></span>



| <span data-ttu-id="95a3b-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95a3b-148">Requirement</span></span> | <span data-ttu-id="95a3b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="95a3b-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95a3b-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95a3b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="95a3b-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95a3b-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95a3b-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95a3b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="95a3b-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95a3b-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95a3b-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="95a3b-154">Namespace</span></span><br/>                | <span data-ttu-id="95a3b-155">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="95a3b-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95a3b-156">MOF</span><span class="sxs-lookup"><span data-stu-id="95a3b-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95a3b-157"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="95a3b-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95a3b-158">DLL</span><span class="sxs-lookup"><span data-stu-id="95a3b-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95a3b-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95a3b-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a3b-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95a3b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a3b-161">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="95a3b-161">CIM\_DeviceFile</span></span>](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="95a3b-162">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="95a3b-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

