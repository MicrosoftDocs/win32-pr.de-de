---
description: 'TakeOwnerShip-Methode der CIM_Directory-Klasse: Die TakeOwnerShip-Methode erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist.'
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: TakeOwnerShip-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12c328f30e56db348b018b73b02aa4320bf99505
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086058"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="332ca-103">TakeOwnerShip-Methode der CIM \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="332ca-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="332ca-104">Die **TakeOwnerShip-Methode** ruft den Besitz der logischen Datei ab, die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="332ca-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="332ca-105">Wenn die logische Datei ein Verzeichnis ist, verhält sich diese Methode rekursiv und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="332ca-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="332ca-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="332ca-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="332ca-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="332ca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="332ca-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="332ca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="332ca-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="332ca-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="332ca-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="332ca-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="332ca-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="332ca-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="332ca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="332ca-112">Parameters</span></span>

<span data-ttu-id="332ca-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="332ca-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="332ca-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="332ca-114">Return value</span></span>

<span data-ttu-id="332ca-115">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="332ca-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="332ca-116">**0**</span><span class="sxs-lookup"><span data-stu-id="332ca-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="332ca-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-118">**2**</span><span class="sxs-lookup"><span data-stu-id="332ca-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-119">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="332ca-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-120">**8**</span><span class="sxs-lookup"><span data-stu-id="332ca-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-121">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="332ca-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-122">**9**</span><span class="sxs-lookup"><span data-stu-id="332ca-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-123">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="332ca-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-124">**10**</span><span class="sxs-lookup"><span data-stu-id="332ca-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-125">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="332ca-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-126">**11**</span><span class="sxs-lookup"><span data-stu-id="332ca-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-127">Dateisystem nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="332ca-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-128">**12**</span><span class="sxs-lookup"><span data-stu-id="332ca-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-129">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="332ca-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-130">**13**</span><span class="sxs-lookup"><span data-stu-id="332ca-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-131">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="332ca-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-132">**14**</span><span class="sxs-lookup"><span data-stu-id="332ca-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-133">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="332ca-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-134">**15**</span><span class="sxs-lookup"><span data-stu-id="332ca-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-135">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="332ca-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-136">**16**</span><span class="sxs-lookup"><span data-stu-id="332ca-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-137">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="332ca-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-138">**17**</span><span class="sxs-lookup"><span data-stu-id="332ca-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-139">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="332ca-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="332ca-140">**21**</span><span class="sxs-lookup"><span data-stu-id="332ca-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="332ca-141">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="332ca-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="332ca-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="332ca-142">Remarks</span></span>

<span data-ttu-id="332ca-143">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="332ca-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="332ca-144">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="332ca-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="332ca-145">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="332ca-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="332ca-146">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="332ca-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="332ca-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="332ca-147">Examples</span></span>

<span data-ttu-id="332ca-148">Der folgende Visual Basic Script-Code ruft die **TakeOwnerShip-Methode** auf, um den Besitz des Ordners C: \\ temp zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="332ca-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="332ca-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332ca-149">Requirements</span></span>



| <span data-ttu-id="332ca-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332ca-150">Requirement</span></span> | <span data-ttu-id="332ca-151">Wert</span><span class="sxs-lookup"><span data-stu-id="332ca-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="332ca-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="332ca-152">Minimum supported client</span></span><br/> | <span data-ttu-id="332ca-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="332ca-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="332ca-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="332ca-154">Minimum supported server</span></span><br/> | <span data-ttu-id="332ca-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="332ca-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="332ca-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="332ca-156">Namespace</span></span><br/>                | <span data-ttu-id="332ca-157">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="332ca-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="332ca-158">MOF</span><span class="sxs-lookup"><span data-stu-id="332ca-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="332ca-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="332ca-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="332ca-160">DLL</span><span class="sxs-lookup"><span data-stu-id="332ca-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="332ca-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="332ca-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332ca-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="332ca-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332ca-163">\_CIM-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="332ca-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="332ca-164">**\_CIM-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="332ca-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

