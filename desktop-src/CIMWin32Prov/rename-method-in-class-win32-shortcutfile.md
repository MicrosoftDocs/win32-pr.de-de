---
description: Benennt die im Objekt Pfad angegebene Verknüpfungs Datei (oder das Verzeichnis) um.
ms.assetid: 6325fe96-19ee-4ccc-934c-ef0c0668f353
ms.tgt_platform: multiple
title: Rename-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c095a702269084a938887ef9717253df4653aea0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338887"
---
# <a name="rename-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="d2d38-103">Rename-Methode der Win32- \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="d2d38-103">Rename method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="d2d38-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **Umbenennen** benennt die im Objekt Pfad angegebene Verknüpfungs Datei (oder das Verzeichnis) um.</span><span class="sxs-lookup"><span data-stu-id="d2d38-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="d2d38-105">Ein umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d2d38-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="d2d38-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2d38-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d2d38-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d2d38-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d38-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2d38-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d2d38-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2d38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d38-110">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2d38-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-111">Voll qualifizierter neuer Name der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="d2d38-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="d2d38-112">Beispiel: c: \\ Temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="d2d38-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d38-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2d38-113">Return value</span></span>

<span data-ttu-id="d2d38-114">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich umbenannt wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d2d38-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d2d38-115">**0**</span><span class="sxs-lookup"><span data-stu-id="d2d38-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-116">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="d2d38-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-117">**2**</span><span class="sxs-lookup"><span data-stu-id="d2d38-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-118">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="d2d38-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-119">**8**</span><span class="sxs-lookup"><span data-stu-id="d2d38-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-120">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d2d38-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-121">**9**</span><span class="sxs-lookup"><span data-stu-id="d2d38-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-122">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="d2d38-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-123">**10**</span><span class="sxs-lookup"><span data-stu-id="d2d38-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-124">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d2d38-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-125">**11**</span><span class="sxs-lookup"><span data-stu-id="d2d38-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-126">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="d2d38-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-127">**12**</span><span class="sxs-lookup"><span data-stu-id="d2d38-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-128">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="d2d38-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-129">**13**</span><span class="sxs-lookup"><span data-stu-id="d2d38-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-130">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="d2d38-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-131">**14**</span><span class="sxs-lookup"><span data-stu-id="d2d38-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-132">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="d2d38-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-133">**15**</span><span class="sxs-lookup"><span data-stu-id="d2d38-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-134">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d2d38-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-135">**16**</span><span class="sxs-lookup"><span data-stu-id="d2d38-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-136">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="d2d38-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-137">**17**</span><span class="sxs-lookup"><span data-stu-id="d2d38-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-138">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="d2d38-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d2d38-139">**21**</span><span class="sxs-lookup"><span data-stu-id="d2d38-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d2d38-140">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d2d38-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2d38-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2d38-141">Requirements</span></span>



| <span data-ttu-id="d2d38-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2d38-142">Requirement</span></span> | <span data-ttu-id="d2d38-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d2d38-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d38-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2d38-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d38-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2d38-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2d38-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2d38-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d38-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2d38-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2d38-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2d38-148">Namespace</span></span><br/>                | <span data-ttu-id="d2d38-149">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d2d38-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2d38-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d2d38-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2d38-151"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d2d38-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2d38-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d38-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2d38-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2d38-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d38-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2d38-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2d38-155">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2d38-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d2d38-156">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="d2d38-156">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

