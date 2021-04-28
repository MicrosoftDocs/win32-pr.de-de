---
description: 'DeleteEx-Methode der CIM_Directory-Klasse: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Diese Methode ist eine erweiterte Version der Delete-Methode und wird von CIM \_ LogicalFile geerbt.'
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_Directory Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a3704507405ebb2d310ed7341cd1db174e00588
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097098"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a><span data-ttu-id="be22b-104">DeleteEx-Methode der CIM \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="be22b-104">DeleteEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="be22b-105">Die **DeleteEx-Methode** löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="be22b-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="be22b-106">Diese Methode ist eine erweiterte Version der [**Delete-Methode**](delete-method-in-class-cim-directory.md) und wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="be22b-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be22b-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="be22b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be22b-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="be22b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be22b-109">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="be22b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="be22b-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="be22b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="be22b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="be22b-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="be22b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="be22b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be22b-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be22b-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be22b-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der bzw. dem die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="be22b-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="be22b-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="be22b-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="be22b-116">*StartFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="be22b-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be22b-117">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="be22b-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="be22b-118">In der Regel ist dieser Parameter der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="be22b-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="be22b-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die Im [**ExecMethod-Aufruf**](/windows/desktop/WmiSdk/swbemservices-execmethod) angegebene Datei (oder das Verzeichnis) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be22b-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be22b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be22b-120">Return value</span></span>

<span data-ttu-id="be22b-121">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="be22b-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="be22b-122">0</span><span class="sxs-lookup"><span data-stu-id="be22b-122">0</span></span>

<span data-ttu-id="be22b-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="be22b-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-124">2</span><span class="sxs-lookup"><span data-stu-id="be22b-124">2</span></span>

<span data-ttu-id="be22b-125">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="be22b-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-126">8</span><span class="sxs-lookup"><span data-stu-id="be22b-126">8</span></span>

<span data-ttu-id="be22b-127">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="be22b-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-128">9</span><span class="sxs-lookup"><span data-stu-id="be22b-128">9</span></span>

<span data-ttu-id="be22b-129">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="be22b-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-130">10</span><span class="sxs-lookup"><span data-stu-id="be22b-130">10</span></span>

<span data-ttu-id="be22b-131">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="be22b-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-132">11</span><span class="sxs-lookup"><span data-stu-id="be22b-132">11</span></span>

<span data-ttu-id="be22b-133">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="be22b-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-134">12</span><span class="sxs-lookup"><span data-stu-id="be22b-134">12</span></span>

<span data-ttu-id="be22b-135">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="be22b-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-136">13</span><span class="sxs-lookup"><span data-stu-id="be22b-136">13</span></span>

<span data-ttu-id="be22b-137">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="be22b-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-138">14</span><span class="sxs-lookup"><span data-stu-id="be22b-138">14</span></span>

<span data-ttu-id="be22b-139">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="be22b-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-140">15</span><span class="sxs-lookup"><span data-stu-id="be22b-140">15</span></span>

<span data-ttu-id="be22b-141">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="be22b-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-142">16</span><span class="sxs-lookup"><span data-stu-id="be22b-142">16</span></span>

<span data-ttu-id="be22b-143">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="be22b-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-144">17</span><span class="sxs-lookup"><span data-stu-id="be22b-144">17</span></span>

<span data-ttu-id="be22b-145">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="be22b-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="be22b-146">21</span><span class="sxs-lookup"><span data-stu-id="be22b-146">21</span></span>

<span data-ttu-id="be22b-147">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="be22b-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be22b-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be22b-148">Remarks</span></span>

<span data-ttu-id="be22b-149">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="be22b-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="be22b-150">Um diese Methode verwenden zu können, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="be22b-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="be22b-151">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="be22b-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be22b-152">Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="be22b-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be22b-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be22b-153">Requirements</span></span>



| <span data-ttu-id="be22b-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be22b-154">Requirement</span></span> | <span data-ttu-id="be22b-155">Wert</span><span class="sxs-lookup"><span data-stu-id="be22b-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be22b-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be22b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="be22b-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be22b-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be22b-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be22b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="be22b-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be22b-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be22b-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="be22b-160">Namespace</span></span><br/>                | <span data-ttu-id="be22b-161">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="be22b-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be22b-162">MOF</span><span class="sxs-lookup"><span data-stu-id="be22b-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be22b-163"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="be22b-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be22b-164">DLL</span><span class="sxs-lookup"><span data-stu-id="be22b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be22b-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be22b-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be22b-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be22b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be22b-167">\_CIM-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="be22b-167">CIM\_Directory</span></span>](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="be22b-168">**\_CIM-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="be22b-168">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

