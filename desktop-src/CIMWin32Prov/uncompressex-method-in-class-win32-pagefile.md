---
description: Die im Objekt Pfad angegebene logische Auslagerungs Datei (oder das angegebene Verzeichnis) wird von unkomprimiert. Diese Methode ist eine erweiterte Version der uncompress-Methode.
ms.assetid: d4cfa42e-7f05-4d12-b629-14195fc04e77
ms.tgt_platform: multiple
title: UncompressEx-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 158efe4d2390762433d66d170b774838c9e534d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127497"
---
# <a name="uncompressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="ca125-104">UncompressEx-Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="ca125-104">UncompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="ca125-105">Die **UncompressEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode entkomprimiert die logische Auslagerungs Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ca125-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca125-106">Diese Methode ist eine erweiterte Version der [**uncompress**](uncompress-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ca125-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="ca125-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca125-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca125-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca125-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca125-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca125-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ca125-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca125-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca125-111">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca125-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca125-112">Der Name der Datei oder des Verzeichnisses, in der die **UncompressEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="ca125-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="ca125-113">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca125-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-114">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ca125-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca125-115">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **UncompressEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca125-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="ca125-116">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="ca125-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ca125-117">Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca125-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-118">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ca125-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca125-119">**True** gibt an, dass die Eigentums Änderung rekursiv auf die Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca125-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="ca125-120">Bei Datei Instanzen wird der *rekursive* Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ca125-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca125-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca125-121">Return value</span></span>

<span data-ttu-id="ca125-122">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich dekomprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ca125-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca125-123">**0**</span><span class="sxs-lookup"><span data-stu-id="ca125-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-124">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="ca125-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-125">**2**</span><span class="sxs-lookup"><span data-stu-id="ca125-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-126">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ca125-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-127">**8**</span><span class="sxs-lookup"><span data-stu-id="ca125-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-128">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ca125-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-129">**9**</span><span class="sxs-lookup"><span data-stu-id="ca125-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-130">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ca125-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-131">**10**</span><span class="sxs-lookup"><span data-stu-id="ca125-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-132">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ca125-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-133">**11**</span><span class="sxs-lookup"><span data-stu-id="ca125-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-134">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="ca125-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-135">**12**</span><span class="sxs-lookup"><span data-stu-id="ca125-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-136">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="ca125-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-137">**13**</span><span class="sxs-lookup"><span data-stu-id="ca125-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-138">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="ca125-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-139">**14**</span><span class="sxs-lookup"><span data-stu-id="ca125-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-140">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="ca125-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-141">**15**</span><span class="sxs-lookup"><span data-stu-id="ca125-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-142">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ca125-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-143">**16**</span><span class="sxs-lookup"><span data-stu-id="ca125-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-144">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ca125-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-145">**17**</span><span class="sxs-lookup"><span data-stu-id="ca125-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-146">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="ca125-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ca125-147">**21**</span><span class="sxs-lookup"><span data-stu-id="ca125-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ca125-148">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ca125-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca125-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca125-149">Requirements</span></span>



| <span data-ttu-id="ca125-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca125-150">Requirement</span></span> | <span data-ttu-id="ca125-151">Wert</span><span class="sxs-lookup"><span data-stu-id="ca125-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca125-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca125-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ca125-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca125-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca125-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca125-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ca125-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca125-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca125-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca125-156">Namespace</span></span><br/>                | <span data-ttu-id="ca125-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ca125-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca125-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ca125-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca125-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ca125-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca125-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ca125-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca125-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca125-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca125-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca125-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca125-163">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca125-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca125-164">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="ca125-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

