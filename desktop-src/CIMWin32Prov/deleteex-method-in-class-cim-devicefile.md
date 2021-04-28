---
description: 'DeleteEx-Methode der CIM_DeviceFile Klasse: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der Delete-Methode und wird von CIM \_ LogicalFile geerbt.'
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_DeviceFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e21fb57558d7704bf98740de8634bc91289e0038
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089597"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="d0c50-104">DeleteEx-Methode der CIM \_ DeviceFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="d0c50-104">DeleteEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="d0c50-105">Die **DeleteEx-Methode** löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d0c50-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d0c50-106">Diese Methode ist eine erweiterte Version der [**Delete-Methode**](delete-method-in-class-cim-devicefile.md) und wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="d0c50-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0c50-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d0c50-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d0c50-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="d0c50-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d0c50-109">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0c50-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d0c50-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="d0c50-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c50-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0c50-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="d0c50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0c50-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c50-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d0c50-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c50-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der bzw. dem die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="d0c50-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="d0c50-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d0c50-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d0c50-116">*StartFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d0c50-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c50-117">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0c50-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="d0c50-118">In der Regel ist der **StartFileName-Parameter** der **StopFileName-Parameter,** der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d0c50-118">Typically, the **StartFileName** parameter is the **StopFileName** parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="d0c50-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das [**im ExecMethod-Aufruf angegeben**](/windows/desktop/WmiSdk/swbemservices-execmethod) ist.</span><span class="sxs-lookup"><span data-stu-id="d0c50-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c50-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0c50-120">Return value</span></span>

<span data-ttu-id="d0c50-121">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d0c50-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-122">0</span><span class="sxs-lookup"><span data-stu-id="d0c50-122">0</span></span>

<span data-ttu-id="d0c50-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d0c50-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-124">2</span><span class="sxs-lookup"><span data-stu-id="d0c50-124">2</span></span>

<span data-ttu-id="d0c50-125">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="d0c50-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-126">8</span><span class="sxs-lookup"><span data-stu-id="d0c50-126">8</span></span>

<span data-ttu-id="d0c50-127">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="d0c50-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-128">9</span><span class="sxs-lookup"><span data-stu-id="d0c50-128">9</span></span>

<span data-ttu-id="d0c50-129">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="d0c50-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-130">10</span><span class="sxs-lookup"><span data-stu-id="d0c50-130">10</span></span>

<span data-ttu-id="d0c50-131">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d0c50-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-132">11</span><span class="sxs-lookup"><span data-stu-id="d0c50-132">11</span></span>

<span data-ttu-id="d0c50-133">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="d0c50-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-134">12</span><span class="sxs-lookup"><span data-stu-id="d0c50-134">12</span></span>

<span data-ttu-id="d0c50-135">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="d0c50-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-136">13</span><span class="sxs-lookup"><span data-stu-id="d0c50-136">13</span></span>

<span data-ttu-id="d0c50-137">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="d0c50-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-138">14</span><span class="sxs-lookup"><span data-stu-id="d0c50-138">14</span></span>

<span data-ttu-id="d0c50-139">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="d0c50-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-140">15</span><span class="sxs-lookup"><span data-stu-id="d0c50-140">15</span></span>

<span data-ttu-id="d0c50-141">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="d0c50-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-142">16</span><span class="sxs-lookup"><span data-stu-id="d0c50-142">16</span></span>

<span data-ttu-id="d0c50-143">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="d0c50-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-144">17</span><span class="sxs-lookup"><span data-stu-id="d0c50-144">17</span></span>

<span data-ttu-id="d0c50-145">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="d0c50-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d0c50-146">21</span><span class="sxs-lookup"><span data-stu-id="d0c50-146">21</span></span>

<span data-ttu-id="d0c50-147">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="d0c50-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0c50-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0c50-148">Remarks</span></span>

<span data-ttu-id="d0c50-149">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d0c50-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d0c50-150">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="d0c50-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d0c50-151">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="d0c50-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d0c50-152">Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d0c50-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c50-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0c50-153">Requirements</span></span>



| <span data-ttu-id="d0c50-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0c50-154">Requirement</span></span> | <span data-ttu-id="d0c50-155">Wert</span><span class="sxs-lookup"><span data-stu-id="d0c50-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c50-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0c50-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c50-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0c50-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0c50-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0c50-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c50-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0c50-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0c50-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c50-160">Namespace</span></span><br/>                | <span data-ttu-id="d0c50-161">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d0c50-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0c50-162">MOF</span><span class="sxs-lookup"><span data-stu-id="d0c50-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0c50-163"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0c50-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0c50-164">DLL</span><span class="sxs-lookup"><span data-stu-id="d0c50-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0c50-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0c50-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c50-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0c50-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c50-167">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="d0c50-167">CIM\_DeviceFile</span></span>](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="d0c50-168">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="d0c50-168">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

