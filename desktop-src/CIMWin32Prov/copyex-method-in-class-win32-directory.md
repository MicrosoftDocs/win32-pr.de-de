---
description: Kopiert die im Objekt Pfad angegebene Datei bzw. das Verzeichnis für den logischen Verzeichniseintrag an den Speicherort, der durch den filename-Parameter angegeben wird. Diese Methode ist eine erweiterte Version der Copy-Methode.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: CopyEx-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861756"
---
# <a name="copyex-method-of-the-win32_directory-class"></a><span data-ttu-id="b1cab-104">CopyEx-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="b1cab-104">CopyEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="b1cab-105">Die **CopyEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die im Objekt Pfad angegebene Datei bzw. das Verzeichnis für den logischen Verzeichniseintrag an den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1cab-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="b1cab-106">Diese Methode ist eine erweiterte Version der [**Copy**](copy-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b1cab-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="b1cab-107">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="b1cab-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="b1cab-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1cab-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b1cab-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b1cab-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cab-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1cab-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b1cab-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1cab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1cab-112">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1cab-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-113">Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="b1cab-113">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="b1cab-114">Beispiel: c: \\ Temp \\ NewDirectory.</span><span class="sxs-lookup"><span data-stu-id="b1cab-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-115">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b1cab-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-116">Der Name der Datei oder des Verzeichnisses, in der die **CopyEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b1cab-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="b1cab-117">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1cab-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-118">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b1cab-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-119">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **CopyEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1cab-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="b1cab-120">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="b1cab-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b1cab-121">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1cab-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="b1cab-122">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b1cab-122">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-123">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b1cab-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-124">**True** gibt an, dass Dateien und Verzeichnisse rekursiv innerhalb des Verzeichnisses kopiert werden, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1cab-124">If **true**, files and directories will be copied recursively within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="b1cab-125">Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b1cab-125">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1cab-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1cab-126">Return value</span></span>

<span data-ttu-id="b1cab-127">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="b1cab-127">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b1cab-128">**0**</span><span class="sxs-lookup"><span data-stu-id="b1cab-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-129">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="b1cab-129">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-130">**2**</span><span class="sxs-lookup"><span data-stu-id="b1cab-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-131">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="b1cab-131">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-132">**8**</span><span class="sxs-lookup"><span data-stu-id="b1cab-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-133">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b1cab-133">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-134">**9**</span><span class="sxs-lookup"><span data-stu-id="b1cab-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-135">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b1cab-135">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-136">**10**</span><span class="sxs-lookup"><span data-stu-id="b1cab-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-137">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b1cab-137">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-138">**11**</span><span class="sxs-lookup"><span data-stu-id="b1cab-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-139">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="b1cab-139">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-140">**12**</span><span class="sxs-lookup"><span data-stu-id="b1cab-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-141">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="b1cab-141">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-142">**13**</span><span class="sxs-lookup"><span data-stu-id="b1cab-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-143">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="b1cab-143">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-144">**14**</span><span class="sxs-lookup"><span data-stu-id="b1cab-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-145">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="b1cab-145">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-146">**15**</span><span class="sxs-lookup"><span data-stu-id="b1cab-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-147">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b1cab-147">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-148">**16**</span><span class="sxs-lookup"><span data-stu-id="b1cab-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-149">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b1cab-149">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-150">**17**</span><span class="sxs-lookup"><span data-stu-id="b1cab-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-151">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="b1cab-151">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b1cab-152">**21**</span><span class="sxs-lookup"><span data-stu-id="b1cab-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b1cab-153">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b1cab-153">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1cab-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1cab-154">Requirements</span></span>



| <span data-ttu-id="b1cab-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1cab-155">Requirement</span></span> | <span data-ttu-id="b1cab-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b1cab-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cab-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1cab-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b1cab-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1cab-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1cab-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1cab-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b1cab-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1cab-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1cab-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1cab-161">Namespace</span></span><br/>                | <span data-ttu-id="b1cab-162">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b1cab-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1cab-163">MOF</span><span class="sxs-lookup"><span data-stu-id="b1cab-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1cab-164"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1cab-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b1cab-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1cab-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1cab-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1cab-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1cab-168">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1cab-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b1cab-169">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="b1cab-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

