---
description: 'TakeOwnerShip-Methode der CIM_DeviceFile-Klasse: Die TakeOwnerShip-Methode erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist.'
ms.assetid: ef7d5ce7-99fb-464f-9739-ec9189148f94
ms.tgt_platform: multiple
title: TakeOwnerShip-Methode der CIM_DeviceFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7c745df18e1725199c4027d22882a00f6143a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086048"
---
# <a name="takeownership-method-of-the-cim_devicefile-class"></a><span data-ttu-id="cad47-103">TakeOwnerShip-Methode der CIM \_ DeviceFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="cad47-103">TakeOwnerShip method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="cad47-104">Die **TakeOwnerShip-Methode** erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cad47-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="cad47-105">Wenn die logische Datei ein Verzeichnis ist, handelt diese Methode rekursiv und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="cad47-105">If the logical file is a directory, then this method will act recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="cad47-106">Diese Methode wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="cad47-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cad47-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cad47-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cad47-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="cad47-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cad47-109">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cad47-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cad47-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="cad47-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cad47-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad47-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="cad47-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cad47-112">Parameters</span></span>

<span data-ttu-id="cad47-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cad47-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cad47-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cad47-114">Return value</span></span>

<span data-ttu-id="cad47-115">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cad47-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="cad47-116">**0**</span><span class="sxs-lookup"><span data-stu-id="cad47-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cad47-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-118">**2**</span><span class="sxs-lookup"><span data-stu-id="cad47-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-119">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="cad47-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-120">**8**</span><span class="sxs-lookup"><span data-stu-id="cad47-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-121">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="cad47-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-122">**9**</span><span class="sxs-lookup"><span data-stu-id="cad47-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="cad47-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-124">**10**</span><span class="sxs-lookup"><span data-stu-id="cad47-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cad47-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-126">**11**</span><span class="sxs-lookup"><span data-stu-id="cad47-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-127">Dateisystem, nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="cad47-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-128">**12**</span><span class="sxs-lookup"><span data-stu-id="cad47-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-129">Plattform, nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="cad47-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-130">**13**</span><span class="sxs-lookup"><span data-stu-id="cad47-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-131">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="cad47-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-132">**14**</span><span class="sxs-lookup"><span data-stu-id="cad47-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="cad47-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-134">**15**</span><span class="sxs-lookup"><span data-stu-id="cad47-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="cad47-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-136">**16**</span><span class="sxs-lookup"><span data-stu-id="cad47-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="cad47-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-138">**17**</span><span class="sxs-lookup"><span data-stu-id="cad47-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-139">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="cad47-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="cad47-140">**21**</span><span class="sxs-lookup"><span data-stu-id="cad47-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cad47-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="cad47-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cad47-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cad47-142">Remarks</span></span>

<span data-ttu-id="cad47-143">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="cad47-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cad47-144">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="cad47-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cad47-145">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="cad47-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cad47-146">Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cad47-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad47-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad47-147">Requirements</span></span>



| <span data-ttu-id="cad47-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad47-148">Requirement</span></span> | <span data-ttu-id="cad47-149">Wert</span><span class="sxs-lookup"><span data-stu-id="cad47-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad47-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cad47-150">Minimum supported client</span></span><br/> | <span data-ttu-id="cad47-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cad47-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cad47-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cad47-152">Minimum supported server</span></span><br/> | <span data-ttu-id="cad47-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cad47-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cad47-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="cad47-154">Namespace</span></span><br/>                | <span data-ttu-id="cad47-155">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cad47-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cad47-156">MOF</span><span class="sxs-lookup"><span data-stu-id="cad47-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cad47-157"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="cad47-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cad47-158">DLL</span><span class="sxs-lookup"><span data-stu-id="cad47-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cad47-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad47-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad47-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cad47-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad47-161">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="cad47-161">CIM\_DeviceFile</span></span>](takeownership-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="cad47-162">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="cad47-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

