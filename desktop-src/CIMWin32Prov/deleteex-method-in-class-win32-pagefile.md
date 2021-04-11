---
description: Löscht die im Objekt Pfad angegebene logische Auslagerungs Datei (oder das angegebene Verzeichnis).
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: DeleteEx-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f62875313f6be432ab191fc91bbac381627de3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126524"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="0a048-103">DeleteEx-Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a048-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="0a048-104">Die **DeleteEx** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode löscht die im Objekt Pfad angegebene logische Auslagerungs Datei (oder das angegebene Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="0a048-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="0a048-105">**DeleteEx** ist eine erweiterte Version der [**Delete**](delete-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0a048-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="0a048-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a048-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0a048-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0a048-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a048-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a048-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="0a048-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a048-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a048-110">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a048-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a048-111">Der Name der Datei oder des Verzeichnisses, in der die **DeleteEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0a048-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="0a048-112">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0a048-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-113">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0a048-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0a048-114">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **DeleteEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a048-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="0a048-115">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden Aufrufs</span><span class="sxs-lookup"><span data-stu-id="0a048-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0a048-116">Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a048-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a048-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a048-117">Return value</span></span>

<span data-ttu-id="0a048-118">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0a048-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0a048-119">**0**</span><span class="sxs-lookup"><span data-stu-id="0a048-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-120">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="0a048-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-121">**2**</span><span class="sxs-lookup"><span data-stu-id="0a048-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-122">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="0a048-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-123">**8**</span><span class="sxs-lookup"><span data-stu-id="0a048-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-124">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0a048-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-125">**9**</span><span class="sxs-lookup"><span data-stu-id="0a048-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-126">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="0a048-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-127">**10**</span><span class="sxs-lookup"><span data-stu-id="0a048-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-128">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0a048-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-129">**11**</span><span class="sxs-lookup"><span data-stu-id="0a048-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-130">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="0a048-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-131">**12**</span><span class="sxs-lookup"><span data-stu-id="0a048-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-132">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0a048-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-133">**13**</span><span class="sxs-lookup"><span data-stu-id="0a048-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-134">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0a048-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-135">**14**</span><span class="sxs-lookup"><span data-stu-id="0a048-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-136">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="0a048-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-137">**15**</span><span class="sxs-lookup"><span data-stu-id="0a048-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-138">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0a048-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-139">**16**</span><span class="sxs-lookup"><span data-stu-id="0a048-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-140">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="0a048-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-141">**17**</span><span class="sxs-lookup"><span data-stu-id="0a048-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-142">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0a048-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0a048-143">**21**</span><span class="sxs-lookup"><span data-stu-id="0a048-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0a048-144">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0a048-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a048-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a048-145">Requirements</span></span>



| <span data-ttu-id="0a048-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a048-146">Requirement</span></span> | <span data-ttu-id="0a048-147">Wert</span><span class="sxs-lookup"><span data-stu-id="0a048-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a048-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a048-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0a048-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a048-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a048-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a048-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0a048-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a048-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a048-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a048-152">Namespace</span></span><br/>                | <span data-ttu-id="0a048-153">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0a048-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a048-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0a048-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a048-155"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0a048-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a048-156">DLL</span><span class="sxs-lookup"><span data-stu-id="0a048-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a048-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a048-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a048-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a048-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a048-159">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a048-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0a048-160">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="0a048-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

