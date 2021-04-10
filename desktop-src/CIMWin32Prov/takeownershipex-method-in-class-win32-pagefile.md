---
description: Ruft den Besitz der logischen Auslagerungs Datei ab, die im Objekt Pfad angegeben ist. Diese Methode ist eine erweiterte Version der TakeOwnership-Methode.
ms.assetid: 6c359910-713a-441e-b2e1-949929c07e93
ms.tgt_platform: multiple
title: Takebesitzshipex-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b0f4662b4884da227a64768cc29bce4c615f8f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214031"
---
# <a name="takeownershipex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="1440b-104">Takebesitzshipex-Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="1440b-104">TakeOwnerShipEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="1440b-105">Die " **takebesitzshipex** "- [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode erhält den Besitz der logischen Auslagerungs Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1440b-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical paging file specified in the object path.</span></span> <span data-ttu-id="1440b-106">Diese Methode ist eine erweiterte Version der [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1440b-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="1440b-107">Wenn die logische Datei tatsächlich ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="1440b-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="1440b-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1440b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1440b-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1440b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1440b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1440b-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1440b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1440b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1440b-112">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1440b-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1440b-113">Der Name der Datei oder des Verzeichnisses, in der die Methode " **takebesitzshipex** " fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1440b-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="1440b-114">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1440b-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-115">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1440b-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1440b-116">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für " **takebesitzshipex**" verwendet werden soll. Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="1440b-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1440b-117">Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1440b-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-118">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1440b-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1440b-119">**True** gibt an, dass die Eigentums Änderung rekursiv auf die Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1440b-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="1440b-120">Bei Datei Instanzen wird der *rekursive* Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1440b-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1440b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1440b-121">Return value</span></span>

<span data-ttu-id="1440b-122">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="1440b-122">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1440b-123">**0**</span><span class="sxs-lookup"><span data-stu-id="1440b-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-124">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="1440b-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-125">**2**</span><span class="sxs-lookup"><span data-stu-id="1440b-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-126">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="1440b-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-127">**8**</span><span class="sxs-lookup"><span data-stu-id="1440b-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-128">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1440b-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-129">**9**</span><span class="sxs-lookup"><span data-stu-id="1440b-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-130">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="1440b-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-131">**10**</span><span class="sxs-lookup"><span data-stu-id="1440b-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-132">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1440b-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-133">**11**</span><span class="sxs-lookup"><span data-stu-id="1440b-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-134">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="1440b-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-135">**12**</span><span class="sxs-lookup"><span data-stu-id="1440b-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-136">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="1440b-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-137">**13**</span><span class="sxs-lookup"><span data-stu-id="1440b-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-138">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="1440b-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-139">**14**</span><span class="sxs-lookup"><span data-stu-id="1440b-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-140">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="1440b-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-141">**15**</span><span class="sxs-lookup"><span data-stu-id="1440b-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-142">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1440b-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-143">**16**</span><span class="sxs-lookup"><span data-stu-id="1440b-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-144">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="1440b-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-145">**17**</span><span class="sxs-lookup"><span data-stu-id="1440b-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-146">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="1440b-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1440b-147">**21**</span><span class="sxs-lookup"><span data-stu-id="1440b-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1440b-148">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1440b-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1440b-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1440b-149">Requirements</span></span>



| <span data-ttu-id="1440b-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1440b-150">Requirement</span></span> | <span data-ttu-id="1440b-151">Wert</span><span class="sxs-lookup"><span data-stu-id="1440b-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1440b-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1440b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1440b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1440b-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1440b-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1440b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1440b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1440b-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1440b-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="1440b-156">Namespace</span></span><br/>                | <span data-ttu-id="1440b-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1440b-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1440b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1440b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1440b-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1440b-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1440b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1440b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1440b-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1440b-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1440b-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1440b-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="1440b-163">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1440b-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1440b-164">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="1440b-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

