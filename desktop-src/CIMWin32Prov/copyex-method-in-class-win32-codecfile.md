---
description: Kopiert die im Objekt Pfad angegebene logische Codec-Datei oder das Verzeichnis in den Speicherort, der durch den filename-Parameter angegeben wird. Diese Methode ist eine erweiterte Version der Copy-Methode.
ms.assetid: 0e9097ed-a599-44f7-a654-8622c0618c27
ms.tgt_platform: multiple
title: CopyEx-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c649c60850c23313ad308a431714276ce30895b1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344628"
---
# <a name="copyex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="8d869-104">CopyEx-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="8d869-104">CopyEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="8d869-105">Die **CopyEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die im Objekt Pfad angegebene logische Codec-Datei bzw. das Verzeichnis in den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical codec file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="8d869-106">Diese Methode ist eine erweiterte Version der [**Copy**](copy-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8d869-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="8d869-107">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="8d869-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="8d869-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d869-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8d869-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8d869-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d869-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d869-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8d869-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d869-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d869-112">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d869-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d869-113">Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="8d869-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="8d869-114">Beispiel: c: \\ Temp \\ NewDirectory.</span><span class="sxs-lookup"><span data-stu-id="8d869-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-115">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8d869-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d869-116">Der Name der Datei oder des Verzeichnisses, in der die **CopyEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="8d869-117">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-118">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d869-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d869-119">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **CopyEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d869-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="8d869-120">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="8d869-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8d869-121">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d869-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-122">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d869-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d869-123">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-123">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="8d869-124">Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8d869-124">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d869-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d869-125">Return value</span></span>

<span data-ttu-id="8d869-126">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8d869-126">Returns an value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8d869-127">**0**</span><span class="sxs-lookup"><span data-stu-id="8d869-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-128">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="8d869-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-129">**2**</span><span class="sxs-lookup"><span data-stu-id="8d869-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-130">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="8d869-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-131">**8**</span><span class="sxs-lookup"><span data-stu-id="8d869-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-132">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8d869-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-133">**9**</span><span class="sxs-lookup"><span data-stu-id="8d869-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-134">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="8d869-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-135">**10**</span><span class="sxs-lookup"><span data-stu-id="8d869-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-136">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8d869-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-137">**11**</span><span class="sxs-lookup"><span data-stu-id="8d869-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-138">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="8d869-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-139">**12**</span><span class="sxs-lookup"><span data-stu-id="8d869-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-140">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="8d869-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-141">**13**</span><span class="sxs-lookup"><span data-stu-id="8d869-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-142">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="8d869-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-143">**14**</span><span class="sxs-lookup"><span data-stu-id="8d869-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-144">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="8d869-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-145">**15**</span><span class="sxs-lookup"><span data-stu-id="8d869-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-146">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8d869-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-147">**16**</span><span class="sxs-lookup"><span data-stu-id="8d869-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-148">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="8d869-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-149">**17**</span><span class="sxs-lookup"><span data-stu-id="8d869-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-150">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="8d869-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8d869-151">**21**</span><span class="sxs-lookup"><span data-stu-id="8d869-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8d869-152">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8d869-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d869-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d869-153">Requirements</span></span>



| <span data-ttu-id="8d869-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d869-154">Requirement</span></span> | <span data-ttu-id="8d869-155">Wert</span><span class="sxs-lookup"><span data-stu-id="8d869-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d869-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d869-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8d869-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d869-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d869-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d869-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8d869-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d869-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d869-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d869-160">Namespace</span></span><br/>                | <span data-ttu-id="8d869-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8d869-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d869-162">MOF</span><span class="sxs-lookup"><span data-stu-id="8d869-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d869-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8d869-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d869-164">DLL</span><span class="sxs-lookup"><span data-stu-id="8d869-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d869-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d869-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d869-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d869-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d869-167">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d869-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8d869-168">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="8d869-168">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

