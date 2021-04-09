---
description: Die CompressEx-Methode komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der Methode compress.
ms.assetid: 7d119865-c246-4cb5-9de4-48a4c42efd90
ms.tgt_platform: multiple
title: CompressEx-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7570cbe3ebc00708023a18da42ef35ff3306d3b0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860716"
---
# <a name="compressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="6513a-104">CompressEx-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="6513a-104">CompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="6513a-105">Die **CompressEx** -Methode komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6513a-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6513a-106">Diese Methode ist eine erweiterte Version der Methode [**Compress**](compress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="6513a-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6513a-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6513a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6513a-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6513a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6513a-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6513a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6513a-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6513a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6513a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6513a-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6513a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6513a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6513a-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6513a-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6513a-114">Der Name der Datei (oder des Verzeichnisses), in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6513a-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="6513a-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6513a-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-116">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6513a-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6513a-117">Die untergeordnete Datei (oder das Verzeichnis), die als Ausgangspunkt für die Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6513a-117">Child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="6513a-118">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="6513a-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6513a-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6513a-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-120">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6513a-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6513a-121">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6513a-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="6513a-122">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6513a-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6513a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6513a-123">Return value</span></span>

<span data-ttu-id="6513a-124">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="6513a-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6513a-125">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="6513a-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-126">0</span><span class="sxs-lookup"><span data-stu-id="6513a-126">0</span></span>

<span data-ttu-id="6513a-127">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6513a-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-128">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="6513a-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-129">2</span><span class="sxs-lookup"><span data-stu-id="6513a-129">2</span></span>

<span data-ttu-id="6513a-130">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6513a-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-131">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="6513a-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-132">8</span><span class="sxs-lookup"><span data-stu-id="6513a-132">8</span></span>

<span data-ttu-id="6513a-133">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6513a-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-134">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="6513a-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-135">9</span><span class="sxs-lookup"><span data-stu-id="6513a-135">9</span></span>

<span data-ttu-id="6513a-136">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="6513a-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-137">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6513a-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-138">10</span><span class="sxs-lookup"><span data-stu-id="6513a-138">10</span></span>

<span data-ttu-id="6513a-139">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6513a-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-140">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="6513a-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-141">11</span><span class="sxs-lookup"><span data-stu-id="6513a-141">11</span></span>

<span data-ttu-id="6513a-142">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="6513a-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-143">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6513a-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-144">12</span><span class="sxs-lookup"><span data-stu-id="6513a-144">12</span></span>

<span data-ttu-id="6513a-145">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="6513a-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-146">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="6513a-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-147">13</span><span class="sxs-lookup"><span data-stu-id="6513a-147">13</span></span>

<span data-ttu-id="6513a-148">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="6513a-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-149">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="6513a-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-150">14</span><span class="sxs-lookup"><span data-stu-id="6513a-150">14</span></span>

<span data-ttu-id="6513a-151">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="6513a-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-152">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="6513a-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-153">15</span><span class="sxs-lookup"><span data-stu-id="6513a-153">15</span></span>

<span data-ttu-id="6513a-154">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="6513a-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-155">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="6513a-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-156">16</span><span class="sxs-lookup"><span data-stu-id="6513a-156">16</span></span>

<span data-ttu-id="6513a-157">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="6513a-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-158">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="6513a-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-159">17</span><span class="sxs-lookup"><span data-stu-id="6513a-159">17</span></span>

<span data-ttu-id="6513a-160">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="6513a-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="6513a-161">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="6513a-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6513a-162">21</span><span class="sxs-lookup"><span data-stu-id="6513a-162">21</span></span>

<span data-ttu-id="6513a-163">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="6513a-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6513a-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6513a-164">Remarks</span></span>

<span data-ttu-id="6513a-165">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6513a-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6513a-166">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="6513a-166">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="6513a-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6513a-167">Requirements</span></span>



| <span data-ttu-id="6513a-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6513a-168">Requirement</span></span> | <span data-ttu-id="6513a-169">Wert</span><span class="sxs-lookup"><span data-stu-id="6513a-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6513a-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6513a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="6513a-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6513a-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6513a-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6513a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="6513a-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6513a-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6513a-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="6513a-174">Namespace</span></span><br/>                | <span data-ttu-id="6513a-175">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6513a-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6513a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="6513a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6513a-177"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6513a-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6513a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="6513a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6513a-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6513a-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6513a-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6513a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6513a-181">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="6513a-181">CIM\_LogicalFile</span></span>](compressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="6513a-182">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="6513a-182">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

