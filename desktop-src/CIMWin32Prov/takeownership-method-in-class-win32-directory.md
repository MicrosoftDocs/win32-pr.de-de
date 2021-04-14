---
description: Die Methode "Take Ownership" der WMI-Klasse ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: TakeOwnership-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c06441b7728ed8b9178e889cbd60c047f0f3a497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523011"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="cadbf-103">TakeOwnership-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="cadbf-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="cadbf-104">Die Methode " **Take Ownership** " der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cadbf-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="cadbf-105">Wenn die logische Datei tatsächlich ein Verzeichnis ist, wird der **Take Ownership** rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="cadbf-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="cadbf-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cadbf-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cadbf-107">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cadbf-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cadbf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cadbf-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="cadbf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cadbf-109">Parameters</span></span>

<span data-ttu-id="cadbf-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cadbf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cadbf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cadbf-111">Return value</span></span>

<span data-ttu-id="cadbf-112">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cadbf-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cadbf-113">**0**</span><span class="sxs-lookup"><span data-stu-id="cadbf-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-114">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="cadbf-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-115">**2**</span><span class="sxs-lookup"><span data-stu-id="cadbf-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-116">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="cadbf-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-117">**8**</span><span class="sxs-lookup"><span data-stu-id="cadbf-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-118">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cadbf-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-119">**9**</span><span class="sxs-lookup"><span data-stu-id="cadbf-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-120">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="cadbf-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-121">**10**</span><span class="sxs-lookup"><span data-stu-id="cadbf-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-122">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cadbf-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-123">**11**</span><span class="sxs-lookup"><span data-stu-id="cadbf-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-124">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="cadbf-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-125">**12**</span><span class="sxs-lookup"><span data-stu-id="cadbf-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-126">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="cadbf-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-127">**13**</span><span class="sxs-lookup"><span data-stu-id="cadbf-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-128">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="cadbf-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-129">**14**</span><span class="sxs-lookup"><span data-stu-id="cadbf-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-130">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="cadbf-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-131">**15**</span><span class="sxs-lookup"><span data-stu-id="cadbf-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-132">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cadbf-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-133">**16**</span><span class="sxs-lookup"><span data-stu-id="cadbf-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-134">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="cadbf-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-135">**17**</span><span class="sxs-lookup"><span data-stu-id="cadbf-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-136">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="cadbf-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="cadbf-137">**21**</span><span class="sxs-lookup"><span data-stu-id="cadbf-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cadbf-138">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cadbf-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cadbf-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cadbf-139">Examples</span></span>

<span data-ttu-id="cadbf-140">Der folgende Visual Basic Skriptcode Ruft die [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) -Methode auf, um den Besitz des Ordners "C: Temp" zu übernehmen \\ .</span><span class="sxs-lookup"><span data-stu-id="cadbf-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="cadbf-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cadbf-141">Requirements</span></span>



| <span data-ttu-id="cadbf-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cadbf-142">Requirement</span></span> | <span data-ttu-id="cadbf-143">Wert</span><span class="sxs-lookup"><span data-stu-id="cadbf-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cadbf-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cadbf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="cadbf-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cadbf-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cadbf-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cadbf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="cadbf-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cadbf-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cadbf-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="cadbf-148">Namespace</span></span><br/>                | <span data-ttu-id="cadbf-149">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cadbf-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cadbf-150">MOF</span><span class="sxs-lookup"><span data-stu-id="cadbf-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cadbf-151"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cadbf-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cadbf-152">DLL</span><span class="sxs-lookup"><span data-stu-id="cadbf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cadbf-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cadbf-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cadbf-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cadbf-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="cadbf-155">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cadbf-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cadbf-156">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="cadbf-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

