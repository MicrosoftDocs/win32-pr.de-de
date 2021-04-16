---
description: Die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis) wird von unkomprimiert. Diese Methode ist eine erweiterte Version der uncompress-Methode.
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: UncompressEx-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524120"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="92bc7-104">UncompressEx-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="92bc7-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="92bc7-105">Die **UncompressEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode entkomprimiert die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="92bc7-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="92bc7-106">Diese Methode ist eine erweiterte Version der [**uncompress**](uncompress-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="92bc7-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="92bc7-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="92bc7-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="92bc7-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="92bc7-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="92bc7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="92bc7-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="92bc7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92bc7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bc7-111">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="92bc7-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-112">Der Name der Datei oder des Verzeichnisses, in der die **UncompressEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="92bc7-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="92bc7-113">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92bc7-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-114">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="92bc7-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-115">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **UncompressEx** verwendet werden soll. Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="92bc7-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="92bc7-116">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92bc7-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-117">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="92bc7-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-118">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="92bc7-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="92bc7-119">Hinweis: bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="92bc7-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bc7-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92bc7-120">Return value</span></span>

<span data-ttu-id="92bc7-121">Gibt einen ganzzahligen Wert von 0 (null) zurück, wenn die Datei erfolgreich dekomprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="92bc7-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="92bc7-122">**0**</span><span class="sxs-lookup"><span data-stu-id="92bc7-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-123">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="92bc7-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-124">**2**</span><span class="sxs-lookup"><span data-stu-id="92bc7-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-125">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="92bc7-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-126">**8**</span><span class="sxs-lookup"><span data-stu-id="92bc7-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-127">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="92bc7-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-128">**9**</span><span class="sxs-lookup"><span data-stu-id="92bc7-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-129">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="92bc7-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-130">**10**</span><span class="sxs-lookup"><span data-stu-id="92bc7-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-131">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92bc7-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-132">**11**</span><span class="sxs-lookup"><span data-stu-id="92bc7-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-133">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="92bc7-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-134">**12**</span><span class="sxs-lookup"><span data-stu-id="92bc7-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-135">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="92bc7-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-136">**13**</span><span class="sxs-lookup"><span data-stu-id="92bc7-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-137">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="92bc7-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-138">**14**</span><span class="sxs-lookup"><span data-stu-id="92bc7-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-139">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="92bc7-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-140">**15**</span><span class="sxs-lookup"><span data-stu-id="92bc7-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-141">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="92bc7-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-142">**16**</span><span class="sxs-lookup"><span data-stu-id="92bc7-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-143">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="92bc7-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-144">**17**</span><span class="sxs-lookup"><span data-stu-id="92bc7-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-145">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="92bc7-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="92bc7-146">**21**</span><span class="sxs-lookup"><span data-stu-id="92bc7-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="92bc7-147">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="92bc7-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92bc7-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92bc7-148">Requirements</span></span>



| <span data-ttu-id="92bc7-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92bc7-149">Requirement</span></span> | <span data-ttu-id="92bc7-150">Wert</span><span class="sxs-lookup"><span data-stu-id="92bc7-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92bc7-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92bc7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="92bc7-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92bc7-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92bc7-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92bc7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="92bc7-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92bc7-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92bc7-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="92bc7-155">Namespace</span></span><br/>                | <span data-ttu-id="92bc7-156">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="92bc7-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92bc7-157">MOF</span><span class="sxs-lookup"><span data-stu-id="92bc7-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92bc7-158"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="92bc7-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92bc7-159">DLL</span><span class="sxs-lookup"><span data-stu-id="92bc7-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92bc7-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92bc7-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92bc7-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92bc7-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="92bc7-162">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92bc7-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="92bc7-163">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="92bc7-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

