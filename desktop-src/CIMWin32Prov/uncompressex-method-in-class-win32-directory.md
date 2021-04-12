---
description: Die im Objekt Pfad angegebene Datei (oder das Verzeichnis) für das logische Verzeichnis wird von deinstalkomprimiert. Diese Methode ist eine erweiterte Version der uncompress-Methode.
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: UncompressEx-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127501"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="5147a-104">UncompressEx-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="5147a-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="5147a-105">Die **UncompressEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode entkomprimiert die im Objekt Pfad angegebene Datei (oder das Verzeichnis) des logischen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="5147a-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="5147a-106">Diese Methode ist eine erweiterte Version der [**uncompress**](uncompress-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5147a-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="5147a-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5147a-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5147a-108">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5147a-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5147a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5147a-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="5147a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5147a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5147a-111">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5147a-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5147a-112">Der Name der Datei oder des Verzeichnisses, in der die **UncompressEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5147a-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="5147a-113">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5147a-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-114">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5147a-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5147a-115">Benennt die untergeordnete Datei bzw. das Verzeichnis, die als Ausgangspunkt für **UncompressEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5147a-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="5147a-116">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="5147a-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="5147a-117">Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5147a-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="5147a-118">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5147a-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-119">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5147a-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5147a-120">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5147a-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="5147a-121">Hinweis: bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5147a-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5147a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5147a-122">Return value</span></span>

<span data-ttu-id="5147a-123">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich dekomprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5147a-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5147a-124">**0**</span><span class="sxs-lookup"><span data-stu-id="5147a-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-125">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="5147a-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-126">**2**</span><span class="sxs-lookup"><span data-stu-id="5147a-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-127">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="5147a-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-128">**8**</span><span class="sxs-lookup"><span data-stu-id="5147a-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-129">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5147a-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-130">**9**</span><span class="sxs-lookup"><span data-stu-id="5147a-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-131">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5147a-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-132">**10**</span><span class="sxs-lookup"><span data-stu-id="5147a-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-133">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5147a-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-134">**11**</span><span class="sxs-lookup"><span data-stu-id="5147a-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-135">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="5147a-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-136">**12**</span><span class="sxs-lookup"><span data-stu-id="5147a-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-137">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="5147a-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-138">**13**</span><span class="sxs-lookup"><span data-stu-id="5147a-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-139">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="5147a-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-140">**14**</span><span class="sxs-lookup"><span data-stu-id="5147a-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-141">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="5147a-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-142">**15**</span><span class="sxs-lookup"><span data-stu-id="5147a-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-143">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5147a-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-144">**16**</span><span class="sxs-lookup"><span data-stu-id="5147a-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-145">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5147a-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-146">**17**</span><span class="sxs-lookup"><span data-stu-id="5147a-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-147">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="5147a-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5147a-148">**21**</span><span class="sxs-lookup"><span data-stu-id="5147a-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5147a-149">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5147a-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5147a-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5147a-150">Requirements</span></span>



| <span data-ttu-id="5147a-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5147a-151">Requirement</span></span> | <span data-ttu-id="5147a-152">Wert</span><span class="sxs-lookup"><span data-stu-id="5147a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5147a-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5147a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5147a-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5147a-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5147a-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5147a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5147a-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5147a-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5147a-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="5147a-157">Namespace</span></span><br/>                | <span data-ttu-id="5147a-158">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5147a-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5147a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="5147a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5147a-160"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5147a-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5147a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="5147a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5147a-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5147a-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5147a-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5147a-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="5147a-164">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5147a-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5147a-165">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="5147a-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

