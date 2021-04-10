---
description: Löschen Sie die im Objekt Pfad angegebene logische Audiodatei oder Videocodec-Datei (oder das Verzeichnis).
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: DeleteEx-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860964"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="27fb5-103">DeleteEx-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="27fb5-103">DeleteEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="27fb5-104">Die **DeleteEx** [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode löscht die im Objekt Pfad angegebene logische Audiodatei oder Videocodec-Datei (oder das Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="27fb5-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical audio or video codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="27fb5-105">**DeleteEx** ist eine erweiterte Version der [**Delete**](delete-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="27fb5-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="27fb5-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="27fb5-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="27fb5-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="27fb5-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="27fb5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="27fb5-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="27fb5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="27fb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27fb5-110">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="27fb5-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-111">Der Name der Datei oder des Verzeichnisses, in der die **DeleteEx** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="27fb5-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="27fb5-112">Dieser Parameter ist **null** , wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27fb5-112">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-113">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fb5-113">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-114">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **DeleteEx** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27fb5-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="27fb5-115">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="27fb5-115">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="27fb5-116">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27fb5-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span> <span data-ttu-id="27fb5-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="27fb5-117">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27fb5-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27fb5-118">Return value</span></span>

<span data-ttu-id="27fb5-119">Gibt einen ganzzahligen Wert von 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="27fb5-119">Returns an integer value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="27fb5-120">**0**</span><span class="sxs-lookup"><span data-stu-id="27fb5-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-121">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="27fb5-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-122">**2**</span><span class="sxs-lookup"><span data-stu-id="27fb5-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-123">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="27fb5-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-124">**8**</span><span class="sxs-lookup"><span data-stu-id="27fb5-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-125">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="27fb5-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-126">**9**</span><span class="sxs-lookup"><span data-stu-id="27fb5-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-127">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="27fb5-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-128">**10**</span><span class="sxs-lookup"><span data-stu-id="27fb5-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-129">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="27fb5-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-130">**11**</span><span class="sxs-lookup"><span data-stu-id="27fb5-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-131">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="27fb5-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-132">**12**</span><span class="sxs-lookup"><span data-stu-id="27fb5-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-133">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="27fb5-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-134">**13**</span><span class="sxs-lookup"><span data-stu-id="27fb5-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-135">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="27fb5-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-136">**14**</span><span class="sxs-lookup"><span data-stu-id="27fb5-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-137">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="27fb5-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-138">**15**</span><span class="sxs-lookup"><span data-stu-id="27fb5-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-139">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="27fb5-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-140">**16**</span><span class="sxs-lookup"><span data-stu-id="27fb5-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-141">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="27fb5-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-142">**17**</span><span class="sxs-lookup"><span data-stu-id="27fb5-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-143">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="27fb5-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="27fb5-144">**21**</span><span class="sxs-lookup"><span data-stu-id="27fb5-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="27fb5-145">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="27fb5-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27fb5-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27fb5-146">Requirements</span></span>



| <span data-ttu-id="27fb5-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27fb5-147">Requirement</span></span> | <span data-ttu-id="27fb5-148">Wert</span><span class="sxs-lookup"><span data-stu-id="27fb5-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27fb5-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27fb5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="27fb5-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27fb5-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27fb5-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27fb5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="27fb5-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27fb5-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27fb5-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="27fb5-153">Namespace</span></span><br/>                | <span data-ttu-id="27fb5-154">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="27fb5-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27fb5-155">MOF</span><span class="sxs-lookup"><span data-stu-id="27fb5-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27fb5-156"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="27fb5-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27fb5-157">DLL</span><span class="sxs-lookup"><span data-stu-id="27fb5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27fb5-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27fb5-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27fb5-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27fb5-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="27fb5-160">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27fb5-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="27fb5-161">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="27fb5-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

