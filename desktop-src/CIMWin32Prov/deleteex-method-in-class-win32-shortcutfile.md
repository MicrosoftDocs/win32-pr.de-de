---
description: Löscht die im Objekt Pfad angegebene logische Verknüpfungs Datei (oder das angegebene Verzeichnis).
ms.assetid: 278cd856-bb8d-4494-b43c-f0858366e136
ms.tgt_platform: multiple
title: DeleteEx-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbe382ca57c4bdef36b19742313965c8bac68fd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346435"
---
# <a name="deleteex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="bdabb-103">DeleteEx-Methode der Win32 \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="bdabb-103">DeleteEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="bdabb-104">Die **DeleteEx** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode löscht die im Objekt Pfad angegebene logische Verknüpfungs Datei (oder das Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="bdabb-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="bdabb-105">**DeleteEx** ist eine erweiterte Version der [**Delete**](delete-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bdabb-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="bdabb-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdabb-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bdabb-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bdabb-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bdabb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdabb-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="bdabb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdabb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdabb-110">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bdabb-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-111">Der Name der Datei oder des Verzeichnisses, in der die **DeleteEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="bdabb-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="bdabb-112">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bdabb-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-113">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bdabb-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-114">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **DeleteEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdabb-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="bdabb-115">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden Aufrufs</span><span class="sxs-lookup"><span data-stu-id="bdabb-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="bdabb-116">Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdabb-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdabb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdabb-117">Return value</span></span>

<span data-ttu-id="bdabb-118">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="bdabb-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="bdabb-119">**0**</span><span class="sxs-lookup"><span data-stu-id="bdabb-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-120">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="bdabb-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-121">**2**</span><span class="sxs-lookup"><span data-stu-id="bdabb-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-122">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="bdabb-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-123">**8**</span><span class="sxs-lookup"><span data-stu-id="bdabb-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-124">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bdabb-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-125">**9**</span><span class="sxs-lookup"><span data-stu-id="bdabb-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-126">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="bdabb-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-127">**10**</span><span class="sxs-lookup"><span data-stu-id="bdabb-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-128">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bdabb-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-129">**11**</span><span class="sxs-lookup"><span data-stu-id="bdabb-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-130">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="bdabb-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-131">**12**</span><span class="sxs-lookup"><span data-stu-id="bdabb-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-132">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="bdabb-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-133">**13**</span><span class="sxs-lookup"><span data-stu-id="bdabb-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-134">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="bdabb-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-135">**14**</span><span class="sxs-lookup"><span data-stu-id="bdabb-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-136">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="bdabb-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-137">**15**</span><span class="sxs-lookup"><span data-stu-id="bdabb-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-138">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bdabb-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-139">**16**</span><span class="sxs-lookup"><span data-stu-id="bdabb-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-140">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="bdabb-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-141">**17**</span><span class="sxs-lookup"><span data-stu-id="bdabb-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-142">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="bdabb-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="bdabb-143">**21**</span><span class="sxs-lookup"><span data-stu-id="bdabb-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="bdabb-144">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bdabb-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdabb-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdabb-145">Requirements</span></span>



| <span data-ttu-id="bdabb-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdabb-146">Requirement</span></span> | <span data-ttu-id="bdabb-147">Wert</span><span class="sxs-lookup"><span data-stu-id="bdabb-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdabb-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdabb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bdabb-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdabb-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bdabb-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdabb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bdabb-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdabb-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bdabb-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdabb-152">Namespace</span></span><br/>                | <span data-ttu-id="bdabb-153">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bdabb-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bdabb-154">MOF</span><span class="sxs-lookup"><span data-stu-id="bdabb-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdabb-155"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bdabb-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bdabb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="bdabb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdabb-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdabb-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdabb-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdabb-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdabb-159">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bdabb-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bdabb-160">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="bdabb-160">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

