---
description: 'Delete-Methode der Win32_PageFile Klasse: Löscht die logische Auslagerungsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist.'
ms.assetid: cc36d621-597e-4343-8bf6-bfca7fa29276
ms.tgt_platform: multiple
title: Delete-Methode der Win32_PageFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b35751633387f3db1d7dccbf13694f56717a1d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089588"
---
# <a name="delete-method-of-the-win32_pagefile-class"></a><span data-ttu-id="25135-103">Delete-Methode der Win32 \_ PageFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="25135-103">Delete method of the Win32\_PageFile class</span></span>

<span data-ttu-id="25135-104">Die **Delete** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht die logische Auslagerungsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="25135-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="25135-105">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="25135-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="25135-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="25135-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="25135-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="25135-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="25135-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="25135-108">Parameters</span></span>

<span data-ttu-id="25135-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="25135-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25135-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25135-110">Return value</span></span>

<span data-ttu-id="25135-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="25135-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="25135-112">**0**</span><span class="sxs-lookup"><span data-stu-id="25135-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="25135-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="25135-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="25135-114">**2**</span><span class="sxs-lookup"><span data-stu-id="25135-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="25135-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="25135-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="25135-116">**8**</span><span class="sxs-lookup"><span data-stu-id="25135-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="25135-117">Es ist ein nicht angegebener Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="25135-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="25135-118">**9**</span><span class="sxs-lookup"><span data-stu-id="25135-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="25135-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="25135-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="25135-120">**10**</span><span class="sxs-lookup"><span data-stu-id="25135-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="25135-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="25135-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="25135-122">**11**</span><span class="sxs-lookup"><span data-stu-id="25135-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="25135-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="25135-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="25135-124">**12**</span><span class="sxs-lookup"><span data-stu-id="25135-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="25135-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="25135-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="25135-126">**13**</span><span class="sxs-lookup"><span data-stu-id="25135-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="25135-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="25135-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="25135-128">**14**</span><span class="sxs-lookup"><span data-stu-id="25135-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="25135-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="25135-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="25135-130">**15**</span><span class="sxs-lookup"><span data-stu-id="25135-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="25135-131">Es ist ein Freigabeverstoß vor worden.</span><span class="sxs-lookup"><span data-stu-id="25135-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="25135-132">**16**</span><span class="sxs-lookup"><span data-stu-id="25135-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="25135-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="25135-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="25135-134">**17**</span><span class="sxs-lookup"><span data-stu-id="25135-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="25135-135">Für den Vorgang ist keine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25135-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="25135-136">**21**</span><span class="sxs-lookup"><span data-stu-id="25135-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="25135-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="25135-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25135-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25135-138">Requirements</span></span>



| <span data-ttu-id="25135-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25135-139">Requirement</span></span> | <span data-ttu-id="25135-140">Wert</span><span class="sxs-lookup"><span data-stu-id="25135-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25135-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25135-141">Minimum supported client</span></span><br/> | <span data-ttu-id="25135-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25135-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25135-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25135-143">Minimum supported server</span></span><br/> | <span data-ttu-id="25135-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25135-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25135-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="25135-145">Namespace</span></span><br/>                | <span data-ttu-id="25135-146">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="25135-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25135-147">MOF</span><span class="sxs-lookup"><span data-stu-id="25135-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25135-148"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="25135-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25135-149">DLL</span><span class="sxs-lookup"><span data-stu-id="25135-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25135-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25135-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25135-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25135-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="25135-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="25135-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="25135-153">**Win32 \_ PageFile**</span><span class="sxs-lookup"><span data-stu-id="25135-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

