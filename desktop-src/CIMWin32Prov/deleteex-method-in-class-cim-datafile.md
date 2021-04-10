---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der Delete-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126530"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="a2212-104">DeleteEx-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2212-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="a2212-105">Die **DeleteEx** -Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a2212-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="a2212-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**Delete**](delete-method-in-class-cim-datafile.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="a2212-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2212-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2212-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a2212-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a2212-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a2212-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2212-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a2212-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a2212-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2212-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2212-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="a2212-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2212-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2212-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a2212-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2212-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a2212-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="a2212-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a2212-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="a2212-116">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2212-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2212-117">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2212-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="a2212-118">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten</span><span class="sxs-lookup"><span data-stu-id="a2212-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="a2212-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a2212-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2212-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2212-120">Return value</span></span>

<span data-ttu-id="a2212-121">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="a2212-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="a2212-122">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a2212-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a2212-123">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a2212-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a2212-124">0</span><span class="sxs-lookup"><span data-stu-id="a2212-124">0</span></span>

<span data-ttu-id="a2212-125">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a2212-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-126">2</span><span class="sxs-lookup"><span data-stu-id="a2212-126">2</span></span>

<span data-ttu-id="a2212-127">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a2212-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-128">8</span><span class="sxs-lookup"><span data-stu-id="a2212-128">8</span></span>

<span data-ttu-id="a2212-129">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a2212-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-130">9</span><span class="sxs-lookup"><span data-stu-id="a2212-130">9</span></span>

<span data-ttu-id="a2212-131">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="a2212-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-132">10</span><span class="sxs-lookup"><span data-stu-id="a2212-132">10</span></span>

<span data-ttu-id="a2212-133">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2212-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-134">11</span><span class="sxs-lookup"><span data-stu-id="a2212-134">11</span></span>

<span data-ttu-id="a2212-135">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="a2212-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-136">12</span><span class="sxs-lookup"><span data-stu-id="a2212-136">12</span></span>

<span data-ttu-id="a2212-137">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="a2212-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-138">13</span><span class="sxs-lookup"><span data-stu-id="a2212-138">13</span></span>

<span data-ttu-id="a2212-139">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="a2212-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-140">14</span><span class="sxs-lookup"><span data-stu-id="a2212-140">14</span></span>

<span data-ttu-id="a2212-141">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="a2212-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-142">15</span><span class="sxs-lookup"><span data-stu-id="a2212-142">15</span></span>

<span data-ttu-id="a2212-143">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="a2212-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-144">16</span><span class="sxs-lookup"><span data-stu-id="a2212-144">16</span></span>

<span data-ttu-id="a2212-145">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="a2212-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-146">17</span><span class="sxs-lookup"><span data-stu-id="a2212-146">17</span></span>

<span data-ttu-id="a2212-147">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="a2212-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a2212-148">21</span><span class="sxs-lookup"><span data-stu-id="a2212-148">21</span></span>

<span data-ttu-id="a2212-149">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="a2212-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2212-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2212-150">Remarks</span></span>

<span data-ttu-id="a2212-151">Die **DeleteEx** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a2212-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="a2212-152">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a2212-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a2212-153">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a2212-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2212-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2212-154">Requirements</span></span>



| <span data-ttu-id="a2212-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2212-155">Requirement</span></span> | <span data-ttu-id="a2212-156">Wert</span><span class="sxs-lookup"><span data-stu-id="a2212-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2212-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2212-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a2212-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2212-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2212-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2212-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a2212-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2212-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2212-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2212-161">Namespace</span></span><br/>                | <span data-ttu-id="a2212-162">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2212-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2212-163">MOF</span><span class="sxs-lookup"><span data-stu-id="a2212-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2212-164"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a2212-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2212-165">DLL</span><span class="sxs-lookup"><span data-stu-id="a2212-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2212-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2212-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2212-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2212-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2212-168">CIM- \_ Datendatei</span><span class="sxs-lookup"><span data-stu-id="a2212-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="a2212-169">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="a2212-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="a2212-170">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="a2212-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="a2212-171">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="a2212-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

