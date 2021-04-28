---
description: 'TakeOwnerShip-Methode der Win32_ShortcutFile-Klasse: TakeOwnerShip&\# 8194; Die WMI-Klassenmethode ruft den Besitz der logischen Datei ab, die im Objektpfad angegeben ist.'
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: TakeOwnerShip-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36364a55276842518480c3d3d37c57c3ae0a06ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085998"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="b5887-103">TakeOwnerShip-Methode der Win32 \_ ShortcutFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="b5887-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="b5887-104">Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** ruft den Besitz der logischen Datei ab, die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b5887-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="b5887-105">Wenn die logische Datei tatsächlich ein Verzeichnis ist, verhält **sich TakeOwnerShip** rekursiv und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="b5887-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="b5887-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5887-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b5887-107">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="b5887-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5887-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5887-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="b5887-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5887-109">Parameters</span></span>

<span data-ttu-id="b5887-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b5887-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5887-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5887-111">Return value</span></span>

<span data-ttu-id="b5887-112">Gibt einen der folgenden ganzzahligen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b5887-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="b5887-113">**0**</span><span class="sxs-lookup"><span data-stu-id="b5887-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-114">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="b5887-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-115">**2**</span><span class="sxs-lookup"><span data-stu-id="b5887-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-116">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="b5887-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-117">**8**</span><span class="sxs-lookup"><span data-stu-id="b5887-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-118">Es ist ein nicht angegebener Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b5887-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-119">**9**</span><span class="sxs-lookup"><span data-stu-id="b5887-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-120">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b5887-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-121">**10**</span><span class="sxs-lookup"><span data-stu-id="b5887-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-122">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b5887-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-123">**11**</span><span class="sxs-lookup"><span data-stu-id="b5887-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-124">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="b5887-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-125">**12**</span><span class="sxs-lookup"><span data-stu-id="b5887-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-126">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="b5887-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-127">**13**</span><span class="sxs-lookup"><span data-stu-id="b5887-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-128">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="b5887-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-129">**14**</span><span class="sxs-lookup"><span data-stu-id="b5887-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-130">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="b5887-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-131">**15**</span><span class="sxs-lookup"><span data-stu-id="b5887-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-132">Es ist ein Freigabeverstoß aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b5887-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-133">**16**</span><span class="sxs-lookup"><span data-stu-id="b5887-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-134">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b5887-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-135">**17**</span><span class="sxs-lookup"><span data-stu-id="b5887-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-136">Für den Vorgang ist keine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b5887-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b5887-137">**21**</span><span class="sxs-lookup"><span data-stu-id="b5887-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b5887-138">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b5887-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5887-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5887-139">Requirements</span></span>



| <span data-ttu-id="b5887-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5887-140">Requirement</span></span> | <span data-ttu-id="b5887-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b5887-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5887-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5887-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b5887-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5887-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5887-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5887-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b5887-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5887-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5887-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5887-146">Namespace</span></span><br/>                | <span data-ttu-id="b5887-147">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b5887-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5887-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b5887-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5887-149"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5887-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5887-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b5887-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5887-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5887-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5887-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5887-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5887-153">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5887-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b5887-154">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="b5887-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

