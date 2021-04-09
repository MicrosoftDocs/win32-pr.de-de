---
description: Die CopyEx-Methode kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den filename-Parameter angegeben wird. Bei dieser Methode handelt es sich um eine erweiterte Version der Copy-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: e207cc80-055e-41bc-ab80-dc50131b544d
ms.tgt_platform: multiple
title: CopyEx-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d7502c46c616d9b8e1fffeebf5aefcd022dd4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958236"
---
# <a name="copyex-method-of-the-cim_directory-class"></a><span data-ttu-id="e270c-104">CopyEx-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="e270c-104">CopyEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="e270c-105">Die **CopyEx** -Methode kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e270c-105">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="e270c-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**Copy**](copy-method-in-class-cim-directory.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="e270c-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e270c-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e270c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e270c-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e270c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e270c-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e270c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e270c-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e270c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e270c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e270c-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string REF FileName,
  [out] string     StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e270c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e270c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e270c-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e270c-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e270c-114">Der voll qualifizierte Name der Kopie der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="e270c-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="e270c-115">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="e270c-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="e270c-116">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e270c-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e270c-117">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e270c-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="e270c-118">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e270c-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e270c-119">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e270c-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e270c-120">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e270c-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="e270c-121">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="e270c-121">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e270c-122">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e270c-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="e270c-123">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e270c-123">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e270c-124">TRUE gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM- \_ Verzeichnis**](cim-directory.md) Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e270c-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="e270c-125">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e270c-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e270c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e270c-126">Return value</span></span>

<span data-ttu-id="e270c-127">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e270c-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="e270c-128">0</span><span class="sxs-lookup"><span data-stu-id="e270c-128">0</span></span>

<span data-ttu-id="e270c-129">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e270c-129">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-130">2</span><span class="sxs-lookup"><span data-stu-id="e270c-130">2</span></span>

<span data-ttu-id="e270c-131">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="e270c-131">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-132">8</span><span class="sxs-lookup"><span data-stu-id="e270c-132">8</span></span>

<span data-ttu-id="e270c-133">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="e270c-133">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-134">9</span><span class="sxs-lookup"><span data-stu-id="e270c-134">9</span></span>

<span data-ttu-id="e270c-135">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="e270c-135">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-136">10</span><span class="sxs-lookup"><span data-stu-id="e270c-136">10</span></span>

<span data-ttu-id="e270c-137">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e270c-137">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-138">11</span><span class="sxs-lookup"><span data-stu-id="e270c-138">11</span></span>

<span data-ttu-id="e270c-139">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="e270c-139">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-140">12</span><span class="sxs-lookup"><span data-stu-id="e270c-140">12</span></span>

<span data-ttu-id="e270c-141">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="e270c-141">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-142">13</span><span class="sxs-lookup"><span data-stu-id="e270c-142">13</span></span>

<span data-ttu-id="e270c-143">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="e270c-143">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-144">14</span><span class="sxs-lookup"><span data-stu-id="e270c-144">14</span></span>

<span data-ttu-id="e270c-145">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="e270c-145">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-146">15</span><span class="sxs-lookup"><span data-stu-id="e270c-146">15</span></span>

<span data-ttu-id="e270c-147">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="e270c-147">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-148">16</span><span class="sxs-lookup"><span data-stu-id="e270c-148">16</span></span>

<span data-ttu-id="e270c-149">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="e270c-149">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-150">17</span><span class="sxs-lookup"><span data-stu-id="e270c-150">17</span></span>

<span data-ttu-id="e270c-151">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="e270c-151">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e270c-152">21</span><span class="sxs-lookup"><span data-stu-id="e270c-152">21</span></span>

<span data-ttu-id="e270c-153">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="e270c-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e270c-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e270c-154">Remarks</span></span>

<span data-ttu-id="e270c-155">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e270c-155">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e270c-156">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="e270c-156">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e270c-157">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e270c-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e270c-158">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e270c-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e270c-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e270c-159">Requirements</span></span>



| <span data-ttu-id="e270c-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e270c-160">Requirement</span></span> | <span data-ttu-id="e270c-161">Wert</span><span class="sxs-lookup"><span data-stu-id="e270c-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e270c-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e270c-162">Minimum supported client</span></span><br/> | <span data-ttu-id="e270c-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e270c-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e270c-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e270c-164">Minimum supported server</span></span><br/> | <span data-ttu-id="e270c-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e270c-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e270c-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="e270c-166">Namespace</span></span><br/>                | <span data-ttu-id="e270c-167">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e270c-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e270c-168">MOF</span><span class="sxs-lookup"><span data-stu-id="e270c-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e270c-169"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e270c-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e270c-170">DLL</span><span class="sxs-lookup"><span data-stu-id="e270c-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e270c-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e270c-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e270c-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e270c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e270c-173">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="e270c-173">CIM\_Directory</span></span>](copyex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="e270c-174">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="e270c-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

