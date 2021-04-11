---
description: Ruft den Besitz der im Objekt Pfad angegebenen Datei des logischen Verzeichniseintrags ab. Bei dieser Methode handelt es sich um eine erweiterte Version der TakeOwnership-Methode, die von CIM \_ LogicalFile geerbt wird.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Takebesitzshipex-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126002"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="bc4ac-104">Takebesitzshipex-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="bc4ac-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="bc4ac-105">Die Methode " **takebesitzshipex** " erhält den Besitz der im Objekt Pfad angegebenen Datei für den logischen Verzeichniseintrag.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="bc4ac-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) -Methode, die von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="bc4ac-107">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc4ac-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bc4ac-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bc4ac-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bc4ac-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bc4ac-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bc4ac-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4ac-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc4ac-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="bc4ac-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc4ac-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc4ac-114">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc4ac-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4ac-115">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="bc4ac-116">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="bc4ac-117">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc4ac-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4ac-118">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="bc4ac-119">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen aufgetreten</span><span class="sxs-lookup"><span data-stu-id="bc4ac-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="bc4ac-120">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="bc4ac-121">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc4ac-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4ac-122">**True** gibt an, dass die Methode rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM- \_ Verzeichnis**](cim-directory.md) Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="bc4ac-123">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc4ac-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc4ac-124">Return value</span></span>

<span data-ttu-id="bc4ac-125">Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-126">0</span><span class="sxs-lookup"><span data-stu-id="bc4ac-126">0</span></span>

<span data-ttu-id="bc4ac-127">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-128">2</span><span class="sxs-lookup"><span data-stu-id="bc4ac-128">2</span></span>

<span data-ttu-id="bc4ac-129">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-130">8</span><span class="sxs-lookup"><span data-stu-id="bc4ac-130">8</span></span>

<span data-ttu-id="bc4ac-131">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-132">9</span><span class="sxs-lookup"><span data-stu-id="bc4ac-132">9</span></span>

<span data-ttu-id="bc4ac-133">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-134">10</span><span class="sxs-lookup"><span data-stu-id="bc4ac-134">10</span></span>

<span data-ttu-id="bc4ac-135">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-136">11</span><span class="sxs-lookup"><span data-stu-id="bc4ac-136">11</span></span>

<span data-ttu-id="bc4ac-137">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-138">12</span><span class="sxs-lookup"><span data-stu-id="bc4ac-138">12</span></span>

<span data-ttu-id="bc4ac-139">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-140">13</span><span class="sxs-lookup"><span data-stu-id="bc4ac-140">13</span></span>

<span data-ttu-id="bc4ac-141">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-142">14</span><span class="sxs-lookup"><span data-stu-id="bc4ac-142">14</span></span>

<span data-ttu-id="bc4ac-143">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="bc4ac-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-144">15</span><span class="sxs-lookup"><span data-stu-id="bc4ac-144">15</span></span>

<span data-ttu-id="bc4ac-145">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-146">16</span><span class="sxs-lookup"><span data-stu-id="bc4ac-146">16</span></span>

<span data-ttu-id="bc4ac-147">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-148">17</span><span class="sxs-lookup"><span data-stu-id="bc4ac-148">17</span></span>

<span data-ttu-id="bc4ac-149">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="bc4ac-150">21</span><span class="sxs-lookup"><span data-stu-id="bc4ac-150">21</span></span>

<span data-ttu-id="bc4ac-151">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc4ac-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc4ac-152">Remarks</span></span>

<span data-ttu-id="bc4ac-153">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="bc4ac-154">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="bc4ac-155">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bc4ac-156">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bc4ac-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="bc4ac-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc4ac-157">Examples</span></span>

<span data-ttu-id="bc4ac-158">Der folgende Visual Basic Skriptcode Ruft die **takebesitzshipex** -Methode auf, um den Besitz des Ordners "C: Temp" zu übernehmen \\ .</span><span class="sxs-lookup"><span data-stu-id="bc4ac-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="bc4ac-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc4ac-159">Requirements</span></span>



| <span data-ttu-id="bc4ac-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc4ac-160">Requirement</span></span> | <span data-ttu-id="bc4ac-161">Wert</span><span class="sxs-lookup"><span data-stu-id="bc4ac-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4ac-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc4ac-162">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4ac-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc4ac-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc4ac-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc4ac-164">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4ac-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc4ac-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc4ac-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc4ac-166">Namespace</span></span><br/>                | <span data-ttu-id="bc4ac-167">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc4ac-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bc4ac-168">MOF</span><span class="sxs-lookup"><span data-stu-id="bc4ac-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc4ac-169"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc4ac-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc4ac-170">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4ac-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc4ac-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc4ac-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc4ac-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc4ac-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4ac-173">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="bc4ac-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="bc4ac-174">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="bc4ac-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

