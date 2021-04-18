---
description: Die Delete WMI class-Methode löscht die im Objekt Pfad angegebene logische Verknüpfungs Datei (oder das Verzeichnis).
ms.assetid: 4059eca3-44d9-48a7-b69f-e9598f939266
ms.tgt_platform: multiple
title: Delete-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 46ad2ffcd768603d90c86a8d4751e76268a9e919
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343977"
---
# <a name="delete-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="67701-103">Delete-Methode der Win32- \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="67701-103">Delete method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="67701-104">Die **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode löscht die im Objekt Pfad angegebene logische Verknüpfungs Datei (oder das Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="67701-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="67701-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="67701-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="67701-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="67701-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="67701-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67701-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="67701-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67701-108">Parameters</span></span>

<span data-ttu-id="67701-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="67701-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67701-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67701-110">Return value</span></span>

<span data-ttu-id="67701-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="67701-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="67701-112">**0**</span><span class="sxs-lookup"><span data-stu-id="67701-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="67701-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="67701-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="67701-114">**2**</span><span class="sxs-lookup"><span data-stu-id="67701-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="67701-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="67701-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="67701-116">**8**</span><span class="sxs-lookup"><span data-stu-id="67701-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="67701-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="67701-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="67701-118">**9**</span><span class="sxs-lookup"><span data-stu-id="67701-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="67701-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="67701-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="67701-120">**10**</span><span class="sxs-lookup"><span data-stu-id="67701-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="67701-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67701-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="67701-122">**11**</span><span class="sxs-lookup"><span data-stu-id="67701-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="67701-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="67701-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="67701-124">**12**</span><span class="sxs-lookup"><span data-stu-id="67701-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="67701-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="67701-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="67701-126">**13**</span><span class="sxs-lookup"><span data-stu-id="67701-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="67701-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="67701-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="67701-128">**14**</span><span class="sxs-lookup"><span data-stu-id="67701-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="67701-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="67701-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="67701-130">**15**</span><span class="sxs-lookup"><span data-stu-id="67701-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="67701-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="67701-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="67701-132">**16**</span><span class="sxs-lookup"><span data-stu-id="67701-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="67701-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="67701-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="67701-134">**17**</span><span class="sxs-lookup"><span data-stu-id="67701-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="67701-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="67701-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="67701-136">**21**</span><span class="sxs-lookup"><span data-stu-id="67701-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="67701-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="67701-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67701-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67701-138">Requirements</span></span>



| <span data-ttu-id="67701-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67701-139">Requirement</span></span> | <span data-ttu-id="67701-140">Wert</span><span class="sxs-lookup"><span data-stu-id="67701-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67701-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67701-141">Minimum supported client</span></span><br/> | <span data-ttu-id="67701-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67701-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67701-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67701-143">Minimum supported server</span></span><br/> | <span data-ttu-id="67701-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67701-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67701-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="67701-145">Namespace</span></span><br/>                | <span data-ttu-id="67701-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67701-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67701-147">MOF</span><span class="sxs-lookup"><span data-stu-id="67701-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67701-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="67701-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67701-149">DLL</span><span class="sxs-lookup"><span data-stu-id="67701-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67701-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67701-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67701-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67701-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="67701-152">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="67701-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="67701-153">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="67701-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

