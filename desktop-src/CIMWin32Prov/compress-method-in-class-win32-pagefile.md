---
description: Komprimiert die logische Auslagerungs Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.
ms.assetid: ebc69c9d-5a86-462b-9362-1ae02869ffa2
ms.tgt_platform: multiple
title: Compress-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eabbe266356a5a5f4b0645b897bf36288b6174de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860720"
---
# <a name="compress-method-of-the-win32_pagefile-class"></a><span data-ttu-id="5060f-103">Methode komprimieren der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="5060f-103">Compress method of the Win32\_PageFile class</span></span>

<span data-ttu-id="5060f-104">Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode komprimieren komprimiert die logische Auslagerungs Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5060f-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="5060f-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5060f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5060f-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5060f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5060f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5060f-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="5060f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5060f-108">Parameters</span></span>

<span data-ttu-id="5060f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5060f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5060f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5060f-110">Return value</span></span>

<span data-ttu-id="5060f-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5060f-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5060f-112">**0**</span><span class="sxs-lookup"><span data-stu-id="5060f-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="5060f-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-114">**2**</span><span class="sxs-lookup"><span data-stu-id="5060f-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="5060f-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-116">**8**</span><span class="sxs-lookup"><span data-stu-id="5060f-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5060f-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-118">**9**</span><span class="sxs-lookup"><span data-stu-id="5060f-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5060f-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-120">**10**</span><span class="sxs-lookup"><span data-stu-id="5060f-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5060f-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-122">**11**</span><span class="sxs-lookup"><span data-stu-id="5060f-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="5060f-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-124">**12**</span><span class="sxs-lookup"><span data-stu-id="5060f-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="5060f-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-126">**13**</span><span class="sxs-lookup"><span data-stu-id="5060f-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="5060f-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-128">**14**</span><span class="sxs-lookup"><span data-stu-id="5060f-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="5060f-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-130">**15**</span><span class="sxs-lookup"><span data-stu-id="5060f-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5060f-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-132">**16**</span><span class="sxs-lookup"><span data-stu-id="5060f-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5060f-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-134">**17**</span><span class="sxs-lookup"><span data-stu-id="5060f-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="5060f-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5060f-136">**21**</span><span class="sxs-lookup"><span data-stu-id="5060f-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5060f-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5060f-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5060f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5060f-138">Requirements</span></span>



| <span data-ttu-id="5060f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5060f-139">Requirement</span></span> | <span data-ttu-id="5060f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5060f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5060f-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5060f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5060f-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5060f-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5060f-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5060f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5060f-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5060f-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5060f-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="5060f-145">Namespace</span></span><br/>                | <span data-ttu-id="5060f-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5060f-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5060f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="5060f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5060f-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5060f-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5060f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5060f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5060f-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5060f-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5060f-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5060f-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="5060f-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5060f-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5060f-153">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="5060f-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

