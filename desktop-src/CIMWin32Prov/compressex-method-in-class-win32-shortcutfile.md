---
description: Komprimiert die im Objekt Pfad angegebene logische Verknüpfungs Datei (oder das angegebene Verzeichnis) (diese Methode ist eine erweiterte Version der Methode compress).
ms.assetid: 1f7b6182-6ab7-4801-83a8-b57b1c78001f
ms.tgt_platform: multiple
title: CompressEx-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 512511b690ed6769895e9c4f9922d479d66f847e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958238"
---
# <a name="compressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="ef72d-103">CompressEx-Methode der Win32- \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="ef72d-103">CompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="ef72d-104">Die **CompressEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode komprimiert die logische Verknüpfungs Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der Methode [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="ef72d-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="ef72d-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef72d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ef72d-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ef72d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef72d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef72d-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ef72d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef72d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef72d-109">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ef72d-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-110">Der Name der Datei oder des Verzeichnisses, in der die [**CompressEx**](compressex-method-in-class-win32-directory.md) -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="ef72d-110">Name of the file or directory where the [**CompressEx**](compressex-method-in-class-win32-directory.md) method failed.</span></span> <span data-ttu-id="ef72d-111">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef72d-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-112">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ef72d-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-113">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für [**CompressEx**](compressex-method-in-class-win32-directory.md)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef72d-113">Names the child file or directory to use as a starting point for [**CompressEx**](compressex-method-in-class-win32-directory.md).</span></span> <span data-ttu-id="ef72d-114">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="ef72d-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ef72d-115">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef72d-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-116">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ef72d-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-117">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef72d-117">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="ef72d-118">Bei Datei Instanzen wird der *rekursive* Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ef72d-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef72d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef72d-119">Return value</span></span>

<span data-ttu-id="ef72d-120">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ef72d-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ef72d-121">**0**</span><span class="sxs-lookup"><span data-stu-id="ef72d-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-122">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="ef72d-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-123">**2**</span><span class="sxs-lookup"><span data-stu-id="ef72d-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-124">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ef72d-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-125">**8**</span><span class="sxs-lookup"><span data-stu-id="ef72d-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-126">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ef72d-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-127">**9**</span><span class="sxs-lookup"><span data-stu-id="ef72d-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-128">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ef72d-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-129">**10**</span><span class="sxs-lookup"><span data-stu-id="ef72d-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-130">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ef72d-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-131">**11**</span><span class="sxs-lookup"><span data-stu-id="ef72d-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-132">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="ef72d-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-133">**12**</span><span class="sxs-lookup"><span data-stu-id="ef72d-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-134">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72d-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-135">**13**</span><span class="sxs-lookup"><span data-stu-id="ef72d-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-136">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="ef72d-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-137">**14**</span><span class="sxs-lookup"><span data-stu-id="ef72d-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-138">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="ef72d-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-139">**15**</span><span class="sxs-lookup"><span data-stu-id="ef72d-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-140">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ef72d-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-141">**16**</span><span class="sxs-lookup"><span data-stu-id="ef72d-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-142">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ef72d-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-143">**17**</span><span class="sxs-lookup"><span data-stu-id="ef72d-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-144">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="ef72d-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-145">**21**</span><span class="sxs-lookup"><span data-stu-id="ef72d-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ef72d-146">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ef72d-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef72d-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef72d-147">Requirements</span></span>



| <span data-ttu-id="ef72d-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef72d-148">Requirement</span></span> | <span data-ttu-id="ef72d-149">Wert</span><span class="sxs-lookup"><span data-stu-id="ef72d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef72d-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef72d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ef72d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef72d-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef72d-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef72d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ef72d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef72d-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef72d-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef72d-154">Namespace</span></span><br/>                | <span data-ttu-id="ef72d-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ef72d-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef72d-156">MOF</span><span class="sxs-lookup"><span data-stu-id="ef72d-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef72d-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ef72d-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef72d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="ef72d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef72d-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef72d-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef72d-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef72d-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef72d-161">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef72d-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef72d-162">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="ef72d-162">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

