---
description: Komprimiert die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis) (diese Methode ist eine erweiterte Version der Methode compress).
ms.assetid: e1ecf0de-3b81-443e-9936-326d7d2d9210
ms.tgt_platform: multiple
title: CompressEx-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ab2915a4f550c799fed8a58e5573e8264b92f1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482926"
---
# <a name="compressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="20f84-103">CompressEx-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="20f84-103">CompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="20f84-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **CompressEx** komprimiert die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis) (diese Methode ist eine erweiterte Version der Methode [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="20f84-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="20f84-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="20f84-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="20f84-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="20f84-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="20f84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="20f84-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="20f84-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20f84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f84-109">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="20f84-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20f84-110">Der Name der Datei oder des Verzeichnisses, in der die **CompressEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="20f84-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="20f84-111">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20f84-111">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-112">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="20f84-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20f84-113">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **CompressEx** verwendet werden soll. Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="20f84-113">Names the child file or directory to use as a starting point for **CompressEx** .The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="20f84-114">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20f84-114">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-115">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="20f84-115">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20f84-116">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="20f84-116">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="20f84-117">Hinweis: bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="20f84-117">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f84-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20f84-118">Return value</span></span>

<span data-ttu-id="20f84-119">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="20f84-119">Returns an value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="20f84-120">**0**</span><span class="sxs-lookup"><span data-stu-id="20f84-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-121">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="20f84-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-122">**2**</span><span class="sxs-lookup"><span data-stu-id="20f84-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-123">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="20f84-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-124">**8**</span><span class="sxs-lookup"><span data-stu-id="20f84-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-125">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="20f84-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-126">**9**</span><span class="sxs-lookup"><span data-stu-id="20f84-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-127">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="20f84-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-128">**10**</span><span class="sxs-lookup"><span data-stu-id="20f84-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-129">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20f84-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-130">**11**</span><span class="sxs-lookup"><span data-stu-id="20f84-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-131">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="20f84-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-132">**12**</span><span class="sxs-lookup"><span data-stu-id="20f84-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-133">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="20f84-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-134">**13**</span><span class="sxs-lookup"><span data-stu-id="20f84-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-135">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="20f84-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-136">**14**</span><span class="sxs-lookup"><span data-stu-id="20f84-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-137">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="20f84-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-138">**15**</span><span class="sxs-lookup"><span data-stu-id="20f84-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-139">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="20f84-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-140">**16**</span><span class="sxs-lookup"><span data-stu-id="20f84-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-141">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="20f84-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-142">**17**</span><span class="sxs-lookup"><span data-stu-id="20f84-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-143">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="20f84-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="20f84-144">**21**</span><span class="sxs-lookup"><span data-stu-id="20f84-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="20f84-145">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="20f84-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20f84-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20f84-146">Requirements</span></span>



| <span data-ttu-id="20f84-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20f84-147">Requirement</span></span> | <span data-ttu-id="20f84-148">Wert</span><span class="sxs-lookup"><span data-stu-id="20f84-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20f84-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20f84-149">Minimum supported client</span></span><br/> | <span data-ttu-id="20f84-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20f84-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20f84-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20f84-151">Minimum supported server</span></span><br/> | <span data-ttu-id="20f84-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20f84-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20f84-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="20f84-153">Namespace</span></span><br/>                | <span data-ttu-id="20f84-154">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="20f84-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20f84-155">MOF</span><span class="sxs-lookup"><span data-stu-id="20f84-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20f84-156"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="20f84-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20f84-157">DLL</span><span class="sxs-lookup"><span data-stu-id="20f84-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20f84-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20f84-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f84-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20f84-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="20f84-160">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20f84-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="20f84-161">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="20f84-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

