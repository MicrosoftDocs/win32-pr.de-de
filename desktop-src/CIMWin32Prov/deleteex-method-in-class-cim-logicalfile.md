---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der Delete-Methode.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523400"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="96b77-104">DeleteEx-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="96b77-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="96b77-105">Die **DeleteEx** -Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="96b77-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="96b77-106">Diese Methode ist eine erweiterte Version der [**Delete**](delete-method-in-class-cim-logicalfile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="96b77-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96b77-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="96b77-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="96b77-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="96b77-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="96b77-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="96b77-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="96b77-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="96b77-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="96b77-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="96b77-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="96b77-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="96b77-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b77-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="96b77-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96b77-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="96b77-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="96b77-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="96b77-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-116">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="96b77-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="96b77-117">Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) benennt, die als Ausgangspunkt für die Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96b77-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="96b77-118">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="96b77-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="96b77-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96b77-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b77-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96b77-120">Return value</span></span>

<span data-ttu-id="96b77-121">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="96b77-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="96b77-122">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="96b77-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-123">0</span><span class="sxs-lookup"><span data-stu-id="96b77-123">0</span></span>

<span data-ttu-id="96b77-124">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="96b77-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-125">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="96b77-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-126">2</span><span class="sxs-lookup"><span data-stu-id="96b77-126">2</span></span>

<span data-ttu-id="96b77-127">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="96b77-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-128">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="96b77-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-129">8</span><span class="sxs-lookup"><span data-stu-id="96b77-129">8</span></span>

<span data-ttu-id="96b77-130">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="96b77-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-131">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="96b77-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-132">9</span><span class="sxs-lookup"><span data-stu-id="96b77-132">9</span></span>

<span data-ttu-id="96b77-133">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="96b77-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-134">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="96b77-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-135">10</span><span class="sxs-lookup"><span data-stu-id="96b77-135">10</span></span>

<span data-ttu-id="96b77-136">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="96b77-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-137">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="96b77-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-138">11</span><span class="sxs-lookup"><span data-stu-id="96b77-138">11</span></span>

<span data-ttu-id="96b77-139">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="96b77-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-140">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="96b77-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-141">12</span><span class="sxs-lookup"><span data-stu-id="96b77-141">12</span></span>

<span data-ttu-id="96b77-142">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="96b77-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-143">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="96b77-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-144">13</span><span class="sxs-lookup"><span data-stu-id="96b77-144">13</span></span>

<span data-ttu-id="96b77-145">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="96b77-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-146">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="96b77-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-147">14</span><span class="sxs-lookup"><span data-stu-id="96b77-147">14</span></span>

<span data-ttu-id="96b77-148">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="96b77-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-149">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="96b77-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-150">15</span><span class="sxs-lookup"><span data-stu-id="96b77-150">15</span></span>

<span data-ttu-id="96b77-151">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="96b77-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-152">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="96b77-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-153">16</span><span class="sxs-lookup"><span data-stu-id="96b77-153">16</span></span>

<span data-ttu-id="96b77-154">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="96b77-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-155">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="96b77-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-156">17</span><span class="sxs-lookup"><span data-stu-id="96b77-156">17</span></span>

<span data-ttu-id="96b77-157">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="96b77-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="96b77-158">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="96b77-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="96b77-159">21</span><span class="sxs-lookup"><span data-stu-id="96b77-159">21</span></span>

<span data-ttu-id="96b77-160">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="96b77-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96b77-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96b77-161">Remarks</span></span>

<span data-ttu-id="96b77-162">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="96b77-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="96b77-163">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="96b77-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="96b77-164">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="96b77-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="96b77-165">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="96b77-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b77-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96b77-166">Requirements</span></span>



| <span data-ttu-id="96b77-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96b77-167">Requirement</span></span> | <span data-ttu-id="96b77-168">Wert</span><span class="sxs-lookup"><span data-stu-id="96b77-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96b77-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96b77-169">Minimum supported client</span></span><br/> | <span data-ttu-id="96b77-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96b77-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96b77-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96b77-171">Minimum supported server</span></span><br/> | <span data-ttu-id="96b77-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96b77-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96b77-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="96b77-173">Namespace</span></span><br/>                | <span data-ttu-id="96b77-174">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="96b77-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96b77-175">MOF</span><span class="sxs-lookup"><span data-stu-id="96b77-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96b77-176"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="96b77-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96b77-177">DLL</span><span class="sxs-lookup"><span data-stu-id="96b77-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96b77-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96b77-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b77-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96b77-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b77-180">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="96b77-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="96b77-181">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="96b77-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

