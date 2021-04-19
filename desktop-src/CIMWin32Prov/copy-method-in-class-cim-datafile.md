---
description: Die Copy-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, an den Speicherort, der durch den Eingabeparameter angegeben wird.
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: Copy-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c126f1cd54470e50a700fdea1c121776d687a9dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346440"
---
# <a name="copy-method-of-the-cim_datafile-class"></a><span data-ttu-id="fbf4c-103">Copy-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="fbf4c-103">Copy method of the CIM\_DataFile class</span></span>

<span data-ttu-id="fbf4c-104">Die **Copy** -Methode kopiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist, an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-104">The **Copy** method copies the logical file (or directory) that is specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="fbf4c-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="fbf4c-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbf4c-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fbf4c-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fbf4c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fbf4c-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fbf4c-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fbf4c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf4c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf4c-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="fbf4c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbf4c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf4c-113">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbf4c-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-114">Der voll qualifizierte Name der Zieldatei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="fbf4c-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="fbf4c-115">Beispiel: "c: \\ Temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="fbf4c-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf4c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbf4c-116">Return value</span></span>

<span data-ttu-id="fbf4c-117">Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="fbf4c-118">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fbf4c-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fbf4c-119">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fbf4c-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fbf4c-120">**0**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-122">**2**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-123">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-124">**8**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-125">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-126">**9**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-127">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-128">**10**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-129">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-130">**11**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-131">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-132">**12**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-133">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-134">**13**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-135">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-136">**14**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-137">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="fbf4c-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-138">**15**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-139">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-140">**16**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-141">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-142">**17**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-143">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="fbf4c-144">**21**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fbf4c-145">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbf4c-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbf4c-146">Remarks</span></span>

<span data-ttu-id="fbf4c-147">Die **Copy** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-147">The **Copy** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="fbf4c-148">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fbf4c-149">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf4c-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf4c-150">Requirements</span></span>



| <span data-ttu-id="fbf4c-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf4c-151">Requirement</span></span> | <span data-ttu-id="fbf4c-152">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf4c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf4c-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbf4c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf4c-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbf4c-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbf4c-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbf4c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf4c-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbf4c-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbf4c-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbf4c-157">Namespace</span></span><br/>                | <span data-ttu-id="fbf4c-158">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fbf4c-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fbf4c-159">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf4c-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf4c-160"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fbf4c-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf4c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf4c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf4c-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf4c-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf4c-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf4c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf4c-164">CIM- \_ Datendatei</span><span class="sxs-lookup"><span data-stu-id="fbf4c-164">CIM\_DataFile</span></span>](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="fbf4c-165">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="fbf4c-166">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="fbf4c-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="fbf4c-167">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="fbf4c-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

