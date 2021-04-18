---
description: Kopiert die im Objekt Pfad angegebene logische Codec-Datei oder das Verzeichnis in den Speicherort, der durch den Eingabeparameter angegeben wird.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Copy-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3bd6621c065192eb45176444257f1c29c897201
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343979"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a><span data-ttu-id="3aa3e-103">Copy-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="3aa3e-103">Copy method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="3aa3e-104">Die **Copy** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die im Objekt Pfad angegebene logische Codec-Datei bzw. das Verzeichnis in den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical codec file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="3aa3e-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="3aa3e-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3aa3e-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3aa3e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa3e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa3e-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="3aa3e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aa3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa3e-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="3aa3e-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa3e-111">Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="3aa3e-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="3aa3e-112">Beispiel: c: \\ Temp \\ NewDirectory.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-112">Example: c:\\temp\\newdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa3e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3aa3e-113">Return value</span></span>

<span data-ttu-id="3aa3e-114">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-114">Returns an value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3aa3e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-116">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-117">**2**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-118">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-119">**8**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-120">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-121">**9**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-122">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-123">**10**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-124">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-125">**11**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-126">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-127">**12**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-128">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-129">**13**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-130">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-131">**14**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-132">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-133">**15**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-134">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-135">**16**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-136">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-137">**17**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-138">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3e-139">**21**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3aa3e-140">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3aa3e-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3aa3e-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3aa3e-141">Requirements</span></span>



| <span data-ttu-id="3aa3e-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3aa3e-142">Requirement</span></span> | <span data-ttu-id="3aa3e-143">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa3e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa3e-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3aa3e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa3e-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3aa3e-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3aa3e-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3aa3e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa3e-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aa3e-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3aa3e-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="3aa3e-148">Namespace</span></span><br/>                | <span data-ttu-id="3aa3e-149">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3aa3e-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3aa3e-150">MOF</span><span class="sxs-lookup"><span data-stu-id="3aa3e-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3aa3e-151"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3e-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3aa3e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="3aa3e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aa3e-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3e-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa3e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3aa3e-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="3aa3e-155">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3aa3e-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3aa3e-156">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="3aa3e-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

