---
description: Ruft den Besitz der im Objekt Pfad angegebenen Datei des logischen Verzeichniseintrags ab. Diese Methode ist eine erweiterte Version der TakeOwnership-Methode.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Takebesitzshipex-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342579"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="0d084-104">Takebesitzshipex-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="0d084-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="0d084-105">Die " **takebesitzshipex** "- [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode erhält den Besitz der im Objekt Pfad angegebenen Datei mit dem logischen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="0d084-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="0d084-106">Diese Methode ist eine erweiterte Version der [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d084-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="0d084-107">Wenn die logische Datei tatsächlich ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="0d084-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="0d084-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d084-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d084-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0d084-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d084-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d084-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0d084-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d084-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d084-112">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0d084-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d084-113">Der Name der Datei oder des Verzeichnisses, in der die Methode " **takebesitzshipex** " fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0d084-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="0d084-114">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0d084-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-115">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0d084-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d084-116">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für " **takebesitzshipex**" verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d084-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="0d084-117">Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden Aufrufs</span><span class="sxs-lookup"><span data-stu-id="0d084-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0d084-118">Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d084-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="0d084-119">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0d084-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-120">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0d084-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d084-121">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d084-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="0d084-122">Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0d084-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d084-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d084-123">Return value</span></span>

<span data-ttu-id="0d084-124">Gibt bei Erfolg einen ganzzahligen Wert von 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0d084-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d084-125">**0**</span><span class="sxs-lookup"><span data-stu-id="0d084-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-126">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="0d084-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-127">**2**</span><span class="sxs-lookup"><span data-stu-id="0d084-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-128">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="0d084-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-129">**8**</span><span class="sxs-lookup"><span data-stu-id="0d084-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-130">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0d084-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-131">**9**</span><span class="sxs-lookup"><span data-stu-id="0d084-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-132">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="0d084-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-133">**10**</span><span class="sxs-lookup"><span data-stu-id="0d084-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-134">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0d084-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-135">**11**</span><span class="sxs-lookup"><span data-stu-id="0d084-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-136">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="0d084-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-137">**12**</span><span class="sxs-lookup"><span data-stu-id="0d084-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-138">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0d084-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-139">**13**</span><span class="sxs-lookup"><span data-stu-id="0d084-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-140">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0d084-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-141">**14**</span><span class="sxs-lookup"><span data-stu-id="0d084-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-142">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="0d084-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-143">**15**</span><span class="sxs-lookup"><span data-stu-id="0d084-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-144">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0d084-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-145">**16**</span><span class="sxs-lookup"><span data-stu-id="0d084-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-146">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="0d084-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-147">**17**</span><span class="sxs-lookup"><span data-stu-id="0d084-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-148">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0d084-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0d084-149">**21**</span><span class="sxs-lookup"><span data-stu-id="0d084-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0d084-150">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0d084-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0d084-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d084-151">Examples</span></span>

<span data-ttu-id="0d084-152">Der folgende Visual Basic Skriptcode Ruft die [**takebesitzshipex**](takeownershipex-method-in-class-cim-directory.md) -Methode auf, um den Besitz des Ordners "C: Temp" zu übernehmen \\ .</span><span class="sxs-lookup"><span data-stu-id="0d084-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="0d084-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d084-153">Requirements</span></span>



| <span data-ttu-id="0d084-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d084-154">Requirement</span></span> | <span data-ttu-id="0d084-155">Wert</span><span class="sxs-lookup"><span data-stu-id="0d084-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d084-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d084-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0d084-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d084-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d084-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d084-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0d084-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d084-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d084-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d084-160">Namespace</span></span><br/>                | <span data-ttu-id="0d084-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d084-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d084-162">MOF</span><span class="sxs-lookup"><span data-stu-id="0d084-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d084-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d084-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d084-164">DLL</span><span class="sxs-lookup"><span data-stu-id="0d084-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d084-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d084-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d084-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d084-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d084-167">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d084-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0d084-168">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="0d084-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

