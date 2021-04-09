---
description: Die CompressEx-Methode komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der Methode compress. Diese Methode wird von CIM \_ LogicalFile geerbt.
ms.assetid: a5f7b35b-5d52-4129-bf7e-6db5e0ff6852
ms.tgt_platform: multiple
title: CompressEx-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e607497a8bb49d0a5926e5b50eb3310c671d9f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860715"
---
# <a name="compressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="241db-105">CompressEx-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="241db-105">CompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="241db-106">Die **CompressEx** -Methode komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="241db-106">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="241db-107">Diese Methode ist eine erweiterte Version der Methode [**Compress**](compress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="241db-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="241db-108">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="241db-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="241db-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="241db-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="241db-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="241db-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="241db-111">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="241db-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="241db-112">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="241db-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="241db-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="241db-113">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="241db-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="241db-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="241db-115">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="241db-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="241db-116">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="241db-116">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="241db-117">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="241db-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="241db-118">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="241db-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241db-119">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="241db-119">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="241db-120">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="241db-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="241db-121">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="241db-121">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="241db-122">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="241db-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241db-123">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ Devicefile**](cim-devicefile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="241db-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="241db-124">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="241db-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="241db-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="241db-125">Return value</span></span>

<span data-ttu-id="241db-126">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="241db-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="241db-127">0</span><span class="sxs-lookup"><span data-stu-id="241db-127">0</span></span>

<span data-ttu-id="241db-128">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="241db-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-129">2</span><span class="sxs-lookup"><span data-stu-id="241db-129">2</span></span>

<span data-ttu-id="241db-130">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="241db-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-131">8</span><span class="sxs-lookup"><span data-stu-id="241db-131">8</span></span>

<span data-ttu-id="241db-132">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="241db-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-133">9</span><span class="sxs-lookup"><span data-stu-id="241db-133">9</span></span>

<span data-ttu-id="241db-134">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="241db-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-135">10</span><span class="sxs-lookup"><span data-stu-id="241db-135">10</span></span>

<span data-ttu-id="241db-136">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="241db-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-137">11</span><span class="sxs-lookup"><span data-stu-id="241db-137">11</span></span>

<span data-ttu-id="241db-138">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="241db-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-139">12</span><span class="sxs-lookup"><span data-stu-id="241db-139">12</span></span>

<span data-ttu-id="241db-140">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="241db-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-141">13</span><span class="sxs-lookup"><span data-stu-id="241db-141">13</span></span>

<span data-ttu-id="241db-142">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="241db-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-143">14</span><span class="sxs-lookup"><span data-stu-id="241db-143">14</span></span>

<span data-ttu-id="241db-144">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="241db-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-145">15</span><span class="sxs-lookup"><span data-stu-id="241db-145">15</span></span>

<span data-ttu-id="241db-146">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="241db-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-147">16</span><span class="sxs-lookup"><span data-stu-id="241db-147">16</span></span>

<span data-ttu-id="241db-148">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="241db-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-149">17</span><span class="sxs-lookup"><span data-stu-id="241db-149">17</span></span>

<span data-ttu-id="241db-150">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="241db-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="241db-151">21</span><span class="sxs-lookup"><span data-stu-id="241db-151">21</span></span>

<span data-ttu-id="241db-152">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="241db-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="241db-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="241db-153">Remarks</span></span>

<span data-ttu-id="241db-154">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="241db-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="241db-155">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="241db-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="241db-156">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="241db-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="241db-157">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="241db-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="241db-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="241db-158">Requirements</span></span>



| <span data-ttu-id="241db-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="241db-159">Requirement</span></span> | <span data-ttu-id="241db-160">Wert</span><span class="sxs-lookup"><span data-stu-id="241db-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="241db-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="241db-161">Minimum supported client</span></span><br/> | <span data-ttu-id="241db-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="241db-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="241db-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="241db-163">Minimum supported server</span></span><br/> | <span data-ttu-id="241db-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="241db-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="241db-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="241db-165">Namespace</span></span><br/>                | <span data-ttu-id="241db-166">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="241db-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="241db-167">MOF</span><span class="sxs-lookup"><span data-stu-id="241db-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="241db-168"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="241db-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="241db-169">DLL</span><span class="sxs-lookup"><span data-stu-id="241db-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="241db-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="241db-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="241db-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="241db-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241db-172">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="241db-172">CIM\_DeviceFile</span></span>](compressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="241db-173">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="241db-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

