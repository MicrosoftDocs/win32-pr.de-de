---
description: Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der TakeOwnership-Methode.
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: Takebesitzshipex-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343958"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="285c0-104">Takebesitzshipex-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="285c0-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="285c0-105">Die Methode " **takebesitzshipex** " Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="285c0-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="285c0-106">Diese Methode ist eine erweiterte Version der [**TakeOwnership**](takeownership-method-in-class-cim-logicalfile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="285c0-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="285c0-107">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="285c0-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="285c0-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="285c0-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="285c0-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="285c0-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="285c0-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="285c0-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="285c0-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="285c0-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="285c0-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="285c0-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="285c0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="285c0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285c0-114">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="285c0-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="285c0-115">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="285c0-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="285c0-116">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="285c0-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-117">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="285c0-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="285c0-118">Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) benennt, die als Ausgangspunkt für die Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="285c0-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="285c0-119">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="285c0-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="285c0-120">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="285c0-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-121">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="285c0-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="285c0-122">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="285c0-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="285c0-123">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="285c0-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285c0-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="285c0-124">Return value</span></span>

<span data-ttu-id="285c0-125">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="285c0-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="285c0-126">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="285c0-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-127">0</span><span class="sxs-lookup"><span data-stu-id="285c0-127">0</span></span>

<span data-ttu-id="285c0-128">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="285c0-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-129">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="285c0-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-130">2</span><span class="sxs-lookup"><span data-stu-id="285c0-130">2</span></span>

<span data-ttu-id="285c0-131">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="285c0-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-132">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="285c0-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-133">8</span><span class="sxs-lookup"><span data-stu-id="285c0-133">8</span></span>

<span data-ttu-id="285c0-134">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="285c0-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-135">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="285c0-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-136">9</span><span class="sxs-lookup"><span data-stu-id="285c0-136">9</span></span>

<span data-ttu-id="285c0-137">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="285c0-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-138">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="285c0-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-139">10</span><span class="sxs-lookup"><span data-stu-id="285c0-139">10</span></span>

<span data-ttu-id="285c0-140">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="285c0-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-141">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="285c0-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-142">11</span><span class="sxs-lookup"><span data-stu-id="285c0-142">11</span></span>

<span data-ttu-id="285c0-143">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="285c0-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-144">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="285c0-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-145">12</span><span class="sxs-lookup"><span data-stu-id="285c0-145">12</span></span>

<span data-ttu-id="285c0-146">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="285c0-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-147">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="285c0-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-148">13</span><span class="sxs-lookup"><span data-stu-id="285c0-148">13</span></span>

<span data-ttu-id="285c0-149">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="285c0-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-150">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="285c0-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-151">14</span><span class="sxs-lookup"><span data-stu-id="285c0-151">14</span></span>

<span data-ttu-id="285c0-152">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="285c0-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-153">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="285c0-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-154">15</span><span class="sxs-lookup"><span data-stu-id="285c0-154">15</span></span>

<span data-ttu-id="285c0-155">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="285c0-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-156">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="285c0-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-157">16</span><span class="sxs-lookup"><span data-stu-id="285c0-157">16</span></span>

<span data-ttu-id="285c0-158">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="285c0-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-159">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="285c0-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-160">17</span><span class="sxs-lookup"><span data-stu-id="285c0-160">17</span></span>

<span data-ttu-id="285c0-161">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="285c0-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="285c0-162">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="285c0-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="285c0-163">21</span><span class="sxs-lookup"><span data-stu-id="285c0-163">21</span></span>

<span data-ttu-id="285c0-164">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="285c0-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="285c0-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="285c0-165">Remarks</span></span>

<span data-ttu-id="285c0-166">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="285c0-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="285c0-167">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="285c0-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="285c0-168">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="285c0-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="285c0-169">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="285c0-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="285c0-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="285c0-170">Requirements</span></span>



| <span data-ttu-id="285c0-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="285c0-171">Requirement</span></span> | <span data-ttu-id="285c0-172">Wert</span><span class="sxs-lookup"><span data-stu-id="285c0-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="285c0-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="285c0-173">Minimum supported client</span></span><br/> | <span data-ttu-id="285c0-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="285c0-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="285c0-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="285c0-175">Minimum supported server</span></span><br/> | <span data-ttu-id="285c0-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="285c0-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="285c0-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="285c0-177">Namespace</span></span><br/>                | <span data-ttu-id="285c0-178">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="285c0-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="285c0-179">MOF</span><span class="sxs-lookup"><span data-stu-id="285c0-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="285c0-180"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="285c0-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="285c0-181">DLL</span><span class="sxs-lookup"><span data-stu-id="285c0-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="285c0-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="285c0-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285c0-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="285c0-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285c0-184">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="285c0-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="285c0-185">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="285c0-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

