---
description: Die im Objekt Pfad angegebene logische Auslagerungs Datei (oder das angegebene Verzeichnis) wird von unkomprimiert.
ms.assetid: 9bd98ba8-068e-49af-8dd4-e5ee987eb31d
ms.tgt_platform: multiple
title: Uncompress-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45a5b48ffa6b2249992b61eadf72f42f6d71969b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861607"
---
# <a name="uncompress-method-of-the-win32_pagefile-class"></a><span data-ttu-id="61a01-103">Uncompress-Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="61a01-103">Uncompress method of the Win32\_PageFile class</span></span>

<span data-ttu-id="61a01-104">Die **uncompress** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode entkomprimiert die logische Auslagerungs Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="61a01-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="61a01-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="61a01-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61a01-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="61a01-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61a01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="61a01-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="61a01-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61a01-108">Parameters</span></span>

<span data-ttu-id="61a01-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="61a01-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61a01-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61a01-110">Return value</span></span>

<span data-ttu-id="61a01-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich dekomprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="61a01-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="61a01-112">**0**</span><span class="sxs-lookup"><span data-stu-id="61a01-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="61a01-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-114">**2**</span><span class="sxs-lookup"><span data-stu-id="61a01-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="61a01-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-116">**8**</span><span class="sxs-lookup"><span data-stu-id="61a01-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="61a01-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-118">**9**</span><span class="sxs-lookup"><span data-stu-id="61a01-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="61a01-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-120">**10**</span><span class="sxs-lookup"><span data-stu-id="61a01-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="61a01-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-122">**11**</span><span class="sxs-lookup"><span data-stu-id="61a01-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="61a01-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-124">**12**</span><span class="sxs-lookup"><span data-stu-id="61a01-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="61a01-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-126">**13**</span><span class="sxs-lookup"><span data-stu-id="61a01-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="61a01-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-128">**14**</span><span class="sxs-lookup"><span data-stu-id="61a01-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="61a01-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-130">**15**</span><span class="sxs-lookup"><span data-stu-id="61a01-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="61a01-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-132">**16**</span><span class="sxs-lookup"><span data-stu-id="61a01-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="61a01-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-134">**17**</span><span class="sxs-lookup"><span data-stu-id="61a01-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="61a01-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="61a01-136">**21**</span><span class="sxs-lookup"><span data-stu-id="61a01-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="61a01-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="61a01-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61a01-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61a01-138">Requirements</span></span>



| <span data-ttu-id="61a01-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61a01-139">Requirement</span></span> | <span data-ttu-id="61a01-140">Wert</span><span class="sxs-lookup"><span data-stu-id="61a01-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61a01-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61a01-141">Minimum supported client</span></span><br/> | <span data-ttu-id="61a01-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61a01-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61a01-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61a01-143">Minimum supported server</span></span><br/> | <span data-ttu-id="61a01-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61a01-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61a01-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="61a01-145">Namespace</span></span><br/>                | <span data-ttu-id="61a01-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="61a01-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61a01-147">MOF</span><span class="sxs-lookup"><span data-stu-id="61a01-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61a01-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="61a01-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61a01-149">DLL</span><span class="sxs-lookup"><span data-stu-id="61a01-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a01-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61a01-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a01-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61a01-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="61a01-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61a01-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="61a01-153">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="61a01-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

