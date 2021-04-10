---
description: Die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis) wird von unkomprimiert.
ms.assetid: abe74267-1274-4b20-82ac-51ca94d7af33
ms.tgt_platform: multiple
title: Uncompress-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d1ffcf99877781c7070b42dac5ffe9ef83af2d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860831"
---
# <a name="uncompress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="d6791-103">Uncompress-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="d6791-103">Uncompress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="d6791-104">Durch die **uncompress** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode wird die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis) deinstalkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="d6791-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="d6791-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6791-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d6791-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d6791-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6791-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6791-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="d6791-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6791-108">Parameters</span></span>

<span data-ttu-id="d6791-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d6791-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6791-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6791-110">Return value</span></span>

<span data-ttu-id="d6791-111">Gibt einen ganzzahligen Wert von 0 (null) zurück, wenn die Datei erfolgreich dekomprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d6791-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d6791-112">**0**</span><span class="sxs-lookup"><span data-stu-id="d6791-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="d6791-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-114">**2**</span><span class="sxs-lookup"><span data-stu-id="d6791-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="d6791-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-116">**8**</span><span class="sxs-lookup"><span data-stu-id="d6791-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d6791-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-118">**9**</span><span class="sxs-lookup"><span data-stu-id="d6791-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="d6791-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-120">**10**</span><span class="sxs-lookup"><span data-stu-id="d6791-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d6791-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-122">**11**</span><span class="sxs-lookup"><span data-stu-id="d6791-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="d6791-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-124">**12**</span><span class="sxs-lookup"><span data-stu-id="d6791-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="d6791-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-126">**13**</span><span class="sxs-lookup"><span data-stu-id="d6791-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="d6791-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-128">**14**</span><span class="sxs-lookup"><span data-stu-id="d6791-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="d6791-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-130">**15**</span><span class="sxs-lookup"><span data-stu-id="d6791-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d6791-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-132">**16**</span><span class="sxs-lookup"><span data-stu-id="d6791-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="d6791-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-134">**17**</span><span class="sxs-lookup"><span data-stu-id="d6791-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="d6791-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d6791-136">**21**</span><span class="sxs-lookup"><span data-stu-id="d6791-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d6791-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d6791-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6791-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6791-138">Requirements</span></span>



| <span data-ttu-id="d6791-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6791-139">Requirement</span></span> | <span data-ttu-id="d6791-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d6791-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6791-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6791-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d6791-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6791-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6791-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6791-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d6791-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6791-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6791-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6791-145">Namespace</span></span><br/>                | <span data-ttu-id="d6791-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d6791-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6791-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d6791-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6791-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d6791-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6791-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d6791-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6791-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6791-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6791-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6791-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6791-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6791-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d6791-153">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="d6791-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

