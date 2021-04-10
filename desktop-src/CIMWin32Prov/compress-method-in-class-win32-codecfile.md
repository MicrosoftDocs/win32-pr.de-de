---
description: Komprimiert die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis).
ms.assetid: c53754cc-a220-428e-aaca-b7c27661f044
ms.tgt_platform: multiple
title: Compress-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f9eb201b1338dd4da9340519f88eab6c16c431
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214061"
---
# <a name="compress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="34b17-103">Methode komprimieren der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="34b17-103">Compress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="34b17-104">Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode komprimieren komprimiert die im Objekt Pfad angegebene logische Codec-Datei (oder das angegebene Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="34b17-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="34b17-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="34b17-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="34b17-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="34b17-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="34b17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="34b17-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="34b17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="34b17-108">Parameters</span></span>

<span data-ttu-id="34b17-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="34b17-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34b17-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34b17-110">Return value</span></span>

<span data-ttu-id="34b17-111">Gibt einen ganzzahligen Wert von 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="34b17-111">Returns an integer value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="34b17-112">**0**</span><span class="sxs-lookup"><span data-stu-id="34b17-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="34b17-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-114">**2**</span><span class="sxs-lookup"><span data-stu-id="34b17-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="34b17-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-116">**8**</span><span class="sxs-lookup"><span data-stu-id="34b17-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="34b17-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-118">**9**</span><span class="sxs-lookup"><span data-stu-id="34b17-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-120">**10**</span><span class="sxs-lookup"><span data-stu-id="34b17-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="34b17-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-122">**11**</span><span class="sxs-lookup"><span data-stu-id="34b17-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="34b17-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-124">**12**</span><span class="sxs-lookup"><span data-stu-id="34b17-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="34b17-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-126">**13**</span><span class="sxs-lookup"><span data-stu-id="34b17-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="34b17-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-128">**14**</span><span class="sxs-lookup"><span data-stu-id="34b17-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="34b17-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-130">**15**</span><span class="sxs-lookup"><span data-stu-id="34b17-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="34b17-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-132">**16**</span><span class="sxs-lookup"><span data-stu-id="34b17-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-134">**17**</span><span class="sxs-lookup"><span data-stu-id="34b17-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="34b17-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="34b17-136">**21**</span><span class="sxs-lookup"><span data-stu-id="34b17-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="34b17-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34b17-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34b17-138">Requirements</span></span>



| <span data-ttu-id="34b17-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34b17-139">Requirement</span></span> | <span data-ttu-id="34b17-140">Wert</span><span class="sxs-lookup"><span data-stu-id="34b17-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34b17-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34b17-141">Minimum supported client</span></span><br/> | <span data-ttu-id="34b17-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34b17-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34b17-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34b17-143">Minimum supported server</span></span><br/> | <span data-ttu-id="34b17-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34b17-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34b17-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="34b17-145">Namespace</span></span><br/>                | <span data-ttu-id="34b17-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="34b17-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34b17-147">MOF</span><span class="sxs-lookup"><span data-stu-id="34b17-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34b17-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="34b17-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34b17-149">DLL</span><span class="sxs-lookup"><span data-stu-id="34b17-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34b17-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34b17-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b17-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34b17-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="34b17-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34b17-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="34b17-153">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="34b17-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

