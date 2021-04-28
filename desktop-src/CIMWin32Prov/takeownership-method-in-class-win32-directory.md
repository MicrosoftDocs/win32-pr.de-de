---
description: 'TakeOwnerShip-Methode der Win32_Directory-Klasse: Die TakeOwnerShip-WMI-Klassenmethode erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist.'
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: TakeOwnerShip-Methode der Win32_Directory-Klasse
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
ms.openlocfilehash: 178f1bf523d939883a7fc18b5bdbd7142cc4f824
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086028"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="e9bdf-103">TakeOwnerShip-Methode der Win32 \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="e9bdf-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="e9bdf-104">Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="e9bdf-105">Wenn die logische Datei tatsächlich ein Verzeichnis ist, verhält **sich TakeOwnerShip** rekursiv und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="e9bdf-106">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9bdf-107">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="e9bdf-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bdf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9bdf-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="e9bdf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9bdf-109">Parameters</span></span>

<span data-ttu-id="e9bdf-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9bdf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9bdf-111">Return value</span></span>

<span data-ttu-id="e9bdf-112">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e9bdf-113">**0**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-114">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-115">**2**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-116">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-117">**8**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-118">Es ist ein nicht angegebener Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-119">**9**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-120">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-121">**10**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-122">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-123">**11**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-124">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-125">**12**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-126">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-127">**13**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-128">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-129">**14**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-130">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-131">**15**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-132">Es ist ein Freigabeverstoß vor worden.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-133">**16**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-134">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-135">**17**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-136">Für den Vorgang ist keine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e9bdf-137">**21**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e9bdf-138">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e9bdf-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9bdf-139">Examples</span></span>

<span data-ttu-id="e9bdf-140">Der folgende Visual Basic Script-Code ruft die [**TakeOwnerShip-Methode**](takeownership-method-in-class-cim-directory.md) auf, um den Besitz des Ordners C: \\ temp zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e9bdf-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9bdf-141">Requirements</span></span>



| <span data-ttu-id="e9bdf-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9bdf-142">Requirement</span></span> | <span data-ttu-id="e9bdf-143">Wert</span><span class="sxs-lookup"><span data-stu-id="e9bdf-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bdf-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9bdf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bdf-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9bdf-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9bdf-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9bdf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bdf-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9bdf-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9bdf-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9bdf-148">Namespace</span></span><br/>                | <span data-ttu-id="e9bdf-149">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="e9bdf-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9bdf-150">MOF</span><span class="sxs-lookup"><span data-stu-id="e9bdf-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9bdf-151"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9bdf-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9bdf-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e9bdf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9bdf-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9bdf-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9bdf-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9bdf-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9bdf-155">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9bdf-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9bdf-156">**\_Win32-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="e9bdf-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

