---
description: Kopiert die im Objekt Pfad angegebene logische Gerätedatei (oder das Verzeichnis) an den Speicherort, der durch den filename-Parameter angegeben wird.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: CopyEx-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393097"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="9953f-103">CopyEx-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="9953f-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="9953f-104">Die **CopyEx** -Methode kopiert die im Objekt Pfad angegebene logische Gerätedatei (oder das Verzeichnis) an den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9953f-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="9953f-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="9953f-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="9953f-106">Diese Methode ist eine erweiterte Version der [**Copy**](copy-method-in-class-cim-devicefile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9953f-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="9953f-107">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9953f-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9953f-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9953f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9953f-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9953f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9953f-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9953f-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9953f-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9953f-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9953f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="9953f-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="9953f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9953f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9953f-114">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9953f-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9953f-115">Der voll qualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="9953f-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="9953f-116">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="9953f-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="9953f-117">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9953f-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9953f-118">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="9953f-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="9953f-119">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9953f-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="9953f-120">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9953f-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9953f-121">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9953f-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="9953f-122">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten</span><span class="sxs-lookup"><span data-stu-id="9953f-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="9953f-123">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9953f-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="9953f-124">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9953f-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9953f-125">TRUE gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ Devicefile**](cim-devicefile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9953f-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="9953f-126">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9953f-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9953f-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9953f-127">Return value</span></span>

<span data-ttu-id="9953f-128">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="9953f-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="9953f-129">0</span><span class="sxs-lookup"><span data-stu-id="9953f-129">0</span></span>

<span data-ttu-id="9953f-130">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9953f-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-131">2</span><span class="sxs-lookup"><span data-stu-id="9953f-131">2</span></span>

<span data-ttu-id="9953f-132">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9953f-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-133">8</span><span class="sxs-lookup"><span data-stu-id="9953f-133">8</span></span>

<span data-ttu-id="9953f-134">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9953f-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-135">9</span><span class="sxs-lookup"><span data-stu-id="9953f-135">9</span></span>

<span data-ttu-id="9953f-136">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="9953f-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-137">10</span><span class="sxs-lookup"><span data-stu-id="9953f-137">10</span></span>

<span data-ttu-id="9953f-138">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9953f-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-139">11</span><span class="sxs-lookup"><span data-stu-id="9953f-139">11</span></span>

<span data-ttu-id="9953f-140">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="9953f-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-141">12</span><span class="sxs-lookup"><span data-stu-id="9953f-141">12</span></span>

<span data-ttu-id="9953f-142">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="9953f-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-143">13</span><span class="sxs-lookup"><span data-stu-id="9953f-143">13</span></span>

<span data-ttu-id="9953f-144">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="9953f-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-145">14</span><span class="sxs-lookup"><span data-stu-id="9953f-145">14</span></span>

<span data-ttu-id="9953f-146">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="9953f-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-147">15</span><span class="sxs-lookup"><span data-stu-id="9953f-147">15</span></span>

<span data-ttu-id="9953f-148">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="9953f-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-149">16</span><span class="sxs-lookup"><span data-stu-id="9953f-149">16</span></span>

<span data-ttu-id="9953f-150">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="9953f-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-151">17</span><span class="sxs-lookup"><span data-stu-id="9953f-151">17</span></span>

<span data-ttu-id="9953f-152">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="9953f-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9953f-153">21</span><span class="sxs-lookup"><span data-stu-id="9953f-153">21</span></span>

<span data-ttu-id="9953f-154">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="9953f-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9953f-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9953f-155">Remarks</span></span>

<span data-ttu-id="9953f-156">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="9953f-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9953f-157">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="9953f-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9953f-158">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9953f-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9953f-159">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9953f-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9953f-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9953f-160">Requirements</span></span>



| <span data-ttu-id="9953f-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9953f-161">Requirement</span></span> | <span data-ttu-id="9953f-162">Wert</span><span class="sxs-lookup"><span data-stu-id="9953f-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9953f-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9953f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9953f-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9953f-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9953f-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9953f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9953f-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9953f-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9953f-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="9953f-167">Namespace</span></span><br/>                | <span data-ttu-id="9953f-168">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9953f-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9953f-169">MOF</span><span class="sxs-lookup"><span data-stu-id="9953f-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9953f-170"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9953f-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9953f-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9953f-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9953f-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9953f-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9953f-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9953f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9953f-174">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="9953f-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="9953f-175">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="9953f-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

