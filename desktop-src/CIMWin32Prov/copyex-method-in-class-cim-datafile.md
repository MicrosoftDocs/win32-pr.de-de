---
description: Die CopyEx-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, an den Speicherort, der durch den filename-Parameter angegeben wird.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: CopyEx-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340122"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="feca0-103">CopyEx-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="feca0-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="feca0-104">Die **CopyEx** -Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, an den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="feca0-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="feca0-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="feca0-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="feca0-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**Copy**](copy-method-in-class-cim-datafile.md) -Methode, die von der [CIM \_ LogicalFile](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="feca0-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="feca0-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="feca0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="feca0-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="feca0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="feca0-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="feca0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="feca0-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="feca0-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="feca0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="feca0-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="feca0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="feca0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feca0-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="feca0-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feca0-114">Der voll qualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="feca0-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="feca0-115">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="feca0-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="feca0-116">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="feca0-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feca0-117">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="feca0-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="feca0-118">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="feca0-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="feca0-119">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="feca0-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feca0-120">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="feca0-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="feca0-121">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="feca0-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="feca0-122">Wenn dieser Parameter **null** ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="feca0-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="feca0-123">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="feca0-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="feca0-124">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="feca0-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feca0-125">TRUE gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DataFile**](cim-datafile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="feca0-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="feca0-126">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="feca0-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feca0-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="feca0-127">Return value</span></span>

<span data-ttu-id="feca0-128">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="feca0-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="feca0-129">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="feca0-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="feca0-130">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="feca0-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="feca0-131">0</span><span class="sxs-lookup"><span data-stu-id="feca0-131">0</span></span>

<span data-ttu-id="feca0-132">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="feca0-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-133">2</span><span class="sxs-lookup"><span data-stu-id="feca0-133">2</span></span>

<span data-ttu-id="feca0-134">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="feca0-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-135">8</span><span class="sxs-lookup"><span data-stu-id="feca0-135">8</span></span>

<span data-ttu-id="feca0-136">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="feca0-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-137">9</span><span class="sxs-lookup"><span data-stu-id="feca0-137">9</span></span>

<span data-ttu-id="feca0-138">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="feca0-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-139">10</span><span class="sxs-lookup"><span data-stu-id="feca0-139">10</span></span>

<span data-ttu-id="feca0-140">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="feca0-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-141">11</span><span class="sxs-lookup"><span data-stu-id="feca0-141">11</span></span>

<span data-ttu-id="feca0-142">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="feca0-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-143">12</span><span class="sxs-lookup"><span data-stu-id="feca0-143">12</span></span>

<span data-ttu-id="feca0-144">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="feca0-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-145">13</span><span class="sxs-lookup"><span data-stu-id="feca0-145">13</span></span>

<span data-ttu-id="feca0-146">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="feca0-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-147">14</span><span class="sxs-lookup"><span data-stu-id="feca0-147">14</span></span>

<span data-ttu-id="feca0-148">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="feca0-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-149">15</span><span class="sxs-lookup"><span data-stu-id="feca0-149">15</span></span>

<span data-ttu-id="feca0-150">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="feca0-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-151">16</span><span class="sxs-lookup"><span data-stu-id="feca0-151">16</span></span>

<span data-ttu-id="feca0-152">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="feca0-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-153">17</span><span class="sxs-lookup"><span data-stu-id="feca0-153">17</span></span>

<span data-ttu-id="feca0-154">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="feca0-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="feca0-155">21</span><span class="sxs-lookup"><span data-stu-id="feca0-155">21</span></span>

<span data-ttu-id="feca0-156">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="feca0-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="feca0-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feca0-157">Remarks</span></span>

<span data-ttu-id="feca0-158">Die **CopyEx** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="feca0-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="feca0-159">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="feca0-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="feca0-160">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="feca0-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="feca0-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="feca0-161">Requirements</span></span>



| <span data-ttu-id="feca0-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="feca0-162">Requirement</span></span> | <span data-ttu-id="feca0-163">Wert</span><span class="sxs-lookup"><span data-stu-id="feca0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feca0-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="feca0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="feca0-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feca0-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="feca0-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="feca0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="feca0-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="feca0-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="feca0-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="feca0-168">Namespace</span></span><br/>                | <span data-ttu-id="feca0-169">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="feca0-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="feca0-170">MOF</span><span class="sxs-lookup"><span data-stu-id="feca0-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="feca0-171"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="feca0-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="feca0-172">DLL</span><span class="sxs-lookup"><span data-stu-id="feca0-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feca0-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feca0-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feca0-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feca0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feca0-175">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="feca0-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="feca0-176">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="feca0-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="feca0-177">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="feca0-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

