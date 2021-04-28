---
description: 'DeleteEx-Methode der Win32_PageFile-Klasse: Löscht die logische Auslagerungsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist.'
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: DeleteEx-Methode der Win32_PageFile Klasse
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
ms.openlocfilehash: 34e27e80c3cfaea352ee97ad29aed0b7ca358546
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097048"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="2df64-103">DeleteEx-Methode der Win32 \_ PageFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="2df64-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="2df64-104">Die **DeleteEx** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht die logische Auslagerungsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2df64-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="2df64-105">**DeleteEx** ist eine erweiterte Version der [**Delete-Methode.**](delete-method-in-class-win32-directory.md)</span><span class="sxs-lookup"><span data-stu-id="2df64-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="2df64-106">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2df64-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2df64-107">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="2df64-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2df64-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df64-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="2df64-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2df64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df64-110">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2df64-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2df64-111">Name der Datei oder des Verzeichnisses, bei der bzw. dem die **DeleteEx-Methode** fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2df64-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="2df64-112">Dieser Parameter ist **NULL,** wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="2df64-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-113">*StartFileName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2df64-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2df64-114">Benennt die untergeordnete Datei oder das untergeordnete Verzeichnis, die bzw. das als Ausgangspunkt für **DeleteEx verwendet werden soll.**</span><span class="sxs-lookup"><span data-stu-id="2df64-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="2df64-115">Der *StartFileName-Parameter* ist in der Regel der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2df64-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2df64-116">Wenn dieser Parameter **NULL ist,** wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im ExecMethod-Aufruf angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2df64-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df64-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2df64-117">Return value</span></span>

<span data-ttu-id="2df64-118">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2df64-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2df64-119">**0**</span><span class="sxs-lookup"><span data-stu-id="2df64-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-120">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="2df64-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-121">**2**</span><span class="sxs-lookup"><span data-stu-id="2df64-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-122">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="2df64-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-123">**8**</span><span class="sxs-lookup"><span data-stu-id="2df64-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-124">Es ist ein nicht angegebener Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2df64-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-125">**9**</span><span class="sxs-lookup"><span data-stu-id="2df64-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-126">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2df64-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-127">**10**</span><span class="sxs-lookup"><span data-stu-id="2df64-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-128">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2df64-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-129">**11**</span><span class="sxs-lookup"><span data-stu-id="2df64-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-130">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="2df64-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-131">**12**</span><span class="sxs-lookup"><span data-stu-id="2df64-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-132">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="2df64-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-133">**13**</span><span class="sxs-lookup"><span data-stu-id="2df64-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-134">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="2df64-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-135">**14**</span><span class="sxs-lookup"><span data-stu-id="2df64-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-136">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="2df64-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-137">**15**</span><span class="sxs-lookup"><span data-stu-id="2df64-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-138">Es ist ein Freigabeverstoß aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2df64-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-139">**16**</span><span class="sxs-lookup"><span data-stu-id="2df64-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-140">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2df64-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-141">**17**</span><span class="sxs-lookup"><span data-stu-id="2df64-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-142">Für den Vorgang ist keine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2df64-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2df64-143">**21**</span><span class="sxs-lookup"><span data-stu-id="2df64-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2df64-144">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2df64-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2df64-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df64-145">Requirements</span></span>



| <span data-ttu-id="2df64-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df64-146">Requirement</span></span> | <span data-ttu-id="2df64-147">Wert</span><span class="sxs-lookup"><span data-stu-id="2df64-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2df64-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2df64-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2df64-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2df64-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2df64-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2df64-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2df64-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2df64-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2df64-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="2df64-152">Namespace</span></span><br/>                | <span data-ttu-id="2df64-153">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2df64-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2df64-154">MOF</span><span class="sxs-lookup"><span data-stu-id="2df64-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2df64-155"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2df64-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2df64-156">DLL</span><span class="sxs-lookup"><span data-stu-id="2df64-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2df64-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2df64-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2df64-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2df64-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="2df64-159">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2df64-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2df64-160">**Win32 \_ PageFile**</span><span class="sxs-lookup"><span data-stu-id="2df64-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

