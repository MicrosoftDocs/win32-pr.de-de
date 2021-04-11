---
description: Die Methode "Take Ownership" der WMI-Klasse ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: TakeOwnership-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1de05f444e99be9a1ebcb5d32fa0ba754cf34254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126007"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a><span data-ttu-id="0fbe7-103">TakeOwnership-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0fbe7-103">TakeOwnerShip method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="0fbe7-104">Die Methode " **Take Ownership** " der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="0fbe7-105">Wenn die logische Datei tatsächlich ein Verzeichnis ist, wird der **Take Ownership** rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="0fbe7-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0fbe7-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0fbe7-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbe7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbe7-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="0fbe7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbe7-109">Parameters</span></span>

<span data-ttu-id="0fbe7-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fbe7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fbe7-111">Return value</span></span>

<span data-ttu-id="0fbe7-112">Gibt einen der folgenden ganzzahligen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="0fbe7-113">**0**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-114">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-115">**2**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-116">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-117">**8**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-118">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-119">**9**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-120">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-121">**10**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-122">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-123">**11**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-124">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-125">**12**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-126">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-127">**13**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-128">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-129">**14**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-130">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-131">**15**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-132">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-133">**16**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-134">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-135">**17**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-136">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0fbe7-137">**21**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0fbe7-138">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0fbe7-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fbe7-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fbe7-139">Requirements</span></span>



| <span data-ttu-id="0fbe7-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fbe7-140">Requirement</span></span> | <span data-ttu-id="0fbe7-141">Wert</span><span class="sxs-lookup"><span data-stu-id="0fbe7-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbe7-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fbe7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0fbe7-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fbe7-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fbe7-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fbe7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0fbe7-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fbe7-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fbe7-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fbe7-146">Namespace</span></span><br/>                | <span data-ttu-id="0fbe7-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0fbe7-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fbe7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0fbe7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fbe7-149"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0fbe7-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fbe7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0fbe7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fbe7-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fbe7-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fbe7-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fbe7-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fbe7-153">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fbe7-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0fbe7-154">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="0fbe7-154">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

