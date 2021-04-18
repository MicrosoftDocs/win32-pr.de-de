---
description: Kopiert die im Objekt Pfad angegebene logische Verknüpfungs Datei oder das Verzeichnis in den Speicherort, der durch den filename-Parameter angegeben wird. Diese Methode ist eine erweiterte Version der Copy-Methode.
ms.assetid: 06b629bb-d35e-4bc2-b0e5-c6a981b6d968
ms.tgt_platform: multiple
title: CopyEx-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cbf1cbb622610a01a533195752b3532b25f8959
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340121"
---
# <a name="copyex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="08874-104">CopyEx-Methode der Win32- \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="08874-104">CopyEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="08874-105">Die **CopyEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die logische Verknüpfungs Datei oder das im Objekt Pfad angegebene Verzeichnis in den Speicherort, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08874-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical shortcut file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="08874-106">Diese Methode ist eine erweiterte Version der [**Copy**](copy-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="08874-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="08874-107">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="08874-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="08874-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="08874-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="08874-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="08874-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="08874-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="08874-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="08874-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="08874-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08874-112">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08874-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08874-113">Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="08874-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="08874-114">Beispiel: c: \\ Temp \\ NewDirectory.</span><span class="sxs-lookup"><span data-stu-id="08874-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="08874-115">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08874-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08874-116">Der Name der Datei oder des Verzeichnisses, in der die **CopyEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="08874-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="08874-117">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="08874-117">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="08874-118">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="08874-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08874-119">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **CopyEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08874-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="08874-120">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="08874-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="08874-121">Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08874-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="08874-122">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="08874-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08874-123">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08874-123">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="08874-124">Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="08874-124">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08874-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08874-125">Return value</span></span>

<span data-ttu-id="08874-126">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="08874-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="08874-127">**0**</span><span class="sxs-lookup"><span data-stu-id="08874-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="08874-128">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="08874-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="08874-129">**2**</span><span class="sxs-lookup"><span data-stu-id="08874-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="08874-130">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="08874-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="08874-131">**8**</span><span class="sxs-lookup"><span data-stu-id="08874-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="08874-132">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="08874-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="08874-133">**9**</span><span class="sxs-lookup"><span data-stu-id="08874-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="08874-134">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="08874-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="08874-135">**10**</span><span class="sxs-lookup"><span data-stu-id="08874-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="08874-136">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="08874-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="08874-137">**11**</span><span class="sxs-lookup"><span data-stu-id="08874-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="08874-138">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="08874-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="08874-139">**12**</span><span class="sxs-lookup"><span data-stu-id="08874-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="08874-140">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="08874-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="08874-141">**13**</span><span class="sxs-lookup"><span data-stu-id="08874-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="08874-142">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="08874-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="08874-143">**14**</span><span class="sxs-lookup"><span data-stu-id="08874-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="08874-144">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="08874-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="08874-145">**15**</span><span class="sxs-lookup"><span data-stu-id="08874-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="08874-146">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="08874-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="08874-147">**16**</span><span class="sxs-lookup"><span data-stu-id="08874-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="08874-148">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="08874-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="08874-149">**17**</span><span class="sxs-lookup"><span data-stu-id="08874-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="08874-150">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="08874-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="08874-151">**21**</span><span class="sxs-lookup"><span data-stu-id="08874-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="08874-152">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="08874-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08874-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08874-153">Requirements</span></span>



| <span data-ttu-id="08874-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08874-154">Requirement</span></span> | <span data-ttu-id="08874-155">Wert</span><span class="sxs-lookup"><span data-stu-id="08874-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08874-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08874-156">Minimum supported client</span></span><br/> | <span data-ttu-id="08874-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08874-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08874-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08874-158">Minimum supported server</span></span><br/> | <span data-ttu-id="08874-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08874-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08874-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="08874-160">Namespace</span></span><br/>                | <span data-ttu-id="08874-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="08874-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08874-162">MOF</span><span class="sxs-lookup"><span data-stu-id="08874-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08874-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="08874-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08874-164">DLL</span><span class="sxs-lookup"><span data-stu-id="08874-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08874-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08874-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08874-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08874-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="08874-167">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08874-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="08874-168">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="08874-168">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

