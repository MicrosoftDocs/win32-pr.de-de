---
description: Komprimiert die im Objekt Pfad angegebene logische Verknüpfungs Datei (oder das angegebene Verzeichnis).
ms.assetid: ade588a5-4e0c-486b-b187-805fcabbf326
ms.tgt_platform: multiple
title: Compress-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490f4d1a76844dc9ebad0449432f06833580d949
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343157"
---
# <a name="compress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="40187-103">Methode komprimieren der Win32- \_ Klasse shortcutfile</span><span class="sxs-lookup"><span data-stu-id="40187-103">Compress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="40187-104">Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode komprimieren komprimiert die logische Verknüpfungs Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="40187-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="40187-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="40187-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40187-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40187-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40187-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40187-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="40187-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40187-108">Parameters</span></span>

<span data-ttu-id="40187-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="40187-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40187-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40187-110">Return value</span></span>

<span data-ttu-id="40187-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="40187-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="40187-112">**0**</span><span class="sxs-lookup"><span data-stu-id="40187-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="40187-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="40187-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="40187-114">**2**</span><span class="sxs-lookup"><span data-stu-id="40187-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="40187-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="40187-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="40187-116">**8**</span><span class="sxs-lookup"><span data-stu-id="40187-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="40187-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="40187-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="40187-118">**9**</span><span class="sxs-lookup"><span data-stu-id="40187-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="40187-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="40187-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="40187-120">**10**</span><span class="sxs-lookup"><span data-stu-id="40187-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="40187-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="40187-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="40187-122">**11**</span><span class="sxs-lookup"><span data-stu-id="40187-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="40187-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="40187-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="40187-124">**12**</span><span class="sxs-lookup"><span data-stu-id="40187-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="40187-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="40187-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="40187-126">**13**</span><span class="sxs-lookup"><span data-stu-id="40187-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="40187-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="40187-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="40187-128">**14**</span><span class="sxs-lookup"><span data-stu-id="40187-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="40187-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="40187-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="40187-130">**15**</span><span class="sxs-lookup"><span data-stu-id="40187-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="40187-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="40187-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="40187-132">**16**</span><span class="sxs-lookup"><span data-stu-id="40187-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="40187-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="40187-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="40187-134">**17**</span><span class="sxs-lookup"><span data-stu-id="40187-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="40187-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="40187-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="40187-136">**21**</span><span class="sxs-lookup"><span data-stu-id="40187-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="40187-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="40187-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40187-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40187-138">Requirements</span></span>



| <span data-ttu-id="40187-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40187-139">Requirement</span></span> | <span data-ttu-id="40187-140">Wert</span><span class="sxs-lookup"><span data-stu-id="40187-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40187-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40187-141">Minimum supported client</span></span><br/> | <span data-ttu-id="40187-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40187-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40187-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40187-143">Minimum supported server</span></span><br/> | <span data-ttu-id="40187-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40187-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40187-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="40187-145">Namespace</span></span><br/>                | <span data-ttu-id="40187-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40187-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40187-147">MOF</span><span class="sxs-lookup"><span data-stu-id="40187-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40187-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="40187-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40187-149">DLL</span><span class="sxs-lookup"><span data-stu-id="40187-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40187-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40187-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40187-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40187-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="40187-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40187-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="40187-153">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="40187-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

