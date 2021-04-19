---
description: Gibt das dem angegebenen Index zugeordnete Austausch Objekt in der Auflistung zurück.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Errbemubjectset. ItemIndex-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350067"
---
# <a name="swbemobjectsetitemindex-method"></a><span data-ttu-id="ca016-103">Errbemubjectset. ItemIndex-Methode</span><span class="sxs-lookup"><span data-stu-id="ca016-103">SWbemObjectSet.ItemIndex method</span></span>

<span data-ttu-id="ca016-104">Die **itemIndex** -Methode gibt das mit dem angegebenen Index verknüpfte [**Austausch Objekt**](swbemobject.md) in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="ca016-104">The **ItemIndex** method returns the [**SWbemObject**](swbemobject.md) associated with the specified index into the collection.</span></span> <span data-ttu-id="ca016-105">Der Index gibt die Position des Elements in der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="ca016-105">The index indicates the position of the element within the collection.</span></span> <span data-ttu-id="ca016-106">Die Sammlungs Nummerierung beginnt bei Null.</span><span class="sxs-lookup"><span data-stu-id="ca016-106">Collection numbering starts at zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca016-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca016-107">Syntax</span></span>


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="ca016-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca016-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca016-109">*Lindex*</span><span class="sxs-lookup"><span data-stu-id="ca016-109">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ca016-110">Der Index des Elements in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ca016-110">Index of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca016-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca016-111">Return value</span></span>

<span data-ttu-id="ca016-112">Wenn der Vorgang erfolgreich ist, gibt das angeforderte [**Swap**](swbemobject.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ca016-112">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca016-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ca016-113">Error codes</span></span>

<span data-ttu-id="ca016-114">Nach Abschluss der [**Element**](swbemobjectset-item.md) Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca016-114">Upon completion of the [**Item**](swbemobjectset-item.md) method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="ca016-115">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ca016-115">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ca016-116">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ca016-116">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ca016-117">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ca016-117">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ca016-118">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="ca016-118">Invalid parameter was specified.</span></span> <span data-ttu-id="ca016-119">Dieser Fehler wird zurückgegeben, wenn eine negative Indexnummer angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca016-119">This error is returned if a negative index number is supplied.</span></span>

</dd> <dt>

<span data-ttu-id="ca016-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ca016-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ca016-121">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ca016-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca016-122">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="ca016-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ca016-123">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ca016-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca016-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca016-124">Remarks</span></span>

<span data-ttu-id="ca016-125">Mit der **itemIndex** -Methode können Skripts und Anwendungen von WMI-Clients, die in einer beliebigen Sprache geschrieben wurden, eine einheitliche Methode zum Bearbeiten einer Auflistung wie einem Array</span><span class="sxs-lookup"><span data-stu-id="ca016-125">The **ItemIndex** method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array.</span></span> <span data-ttu-id="ca016-126">Diese Methode kann mit den [**Swap-Auflistungen von Swap-Objekte**](swbemobjectset.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca016-126">This method can be used with [**SWbemObjectSet**](swbemobjectset.md) collections.</span></span> <span data-ttu-id="ca016-127">Abfragen, wie z. b. " [**errbemservices. associatorsof**](swbemservices-associatorsof.md)", " [**errbemservices. referencesto**](swbemservices-referencesto.md)", " [**errbemservices. InstancesOf**](swbemservices-instancesof.md)" oder " [**SWbemServices.Execquery**](swbemservices-execquery.md) ", geben " **errbewbjectset** Collections</span><span class="sxs-lookup"><span data-stu-id="ca016-127">Queries, such as [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), or [**SWbemServices.ExecQuery**](swbemservices-execquery.md) return **SWbemObjectSet** collections.</span></span> <span data-ttu-id="ca016-128">Die **itemIndex** -Methode kann nicht mit Auflistungen verwendet werden, die keine Austausch Vorgänge enthalten, wie z. [**b**](swbemobject.md). " [**errbemmethodset**](swbemmethodset.md)", " [**errbemnamedvalueset**](swbemnamedvalueset.md)", " [**errbemprivilegeset**](swbemprivilegeset.md)", " [**taubempropertyset**](swbempropertyset.md)" und " [**errbemqualifierset**](swbemqualifierset.md)".</span><span class="sxs-lookup"><span data-stu-id="ca016-128">The **ItemIndex** method does not work with collections which do not contain [**SWbemObjects**](swbemobject.md), such as [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md), and [**SWbemQualifierSet**](swbemqualifierset.md).</span></span>

<span data-ttu-id="ca016-129">**ItemIndex** kann auch zum Abrufen der einzelnen Instanz einer Singleton-Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca016-129">**ItemIndex** can also be used to obtain the single instance of a singleton class.</span></span>

## <a name="examples"></a><span data-ttu-id="ca016-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca016-130">Examples</span></span>

<span data-ttu-id="ca016-131">Im folgenden VBScript-Codebeispiel wird eine Auflistung aller Win32- [**\_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Instanzen abgefragt. Anschließend werden die Namen der ersten drei Prozesse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca016-131">The following VBScript code example queries for a collection of all the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instances then displays the names of the first three processes.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



<span data-ttu-id="ca016-132">Für jede Betriebssystem Installation ist nur eine Instanz des [**Win32- \_ OperatingSystems**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ca016-132">Only one instance of [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) exists for each operating system installation.</span></span> <span data-ttu-id="ca016-133">Das Erstellen des [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) -Pfads zum Abrufen der einzelnen Instanz ist umständlich, sodass Skripts das **Win32- \_ OperatingSystem** normalerweise auflisten, auch wenn nur eine Instanz verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ca016-133">Creating the [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) path to obtain the single instance is awkward so scripts normally enumerate **Win32\_OperatingSystem** even though only one instance is available.</span></span> <span data-ttu-id="ca016-134">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie die **itemIndex** -Methode verwendet wird, um ein **Win32- \_ OperatingSystem** ohne Verwendung einer **for each** -Schleife zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca016-134">The following VBScript code example shows how to use the **ItemIndex** method to get to the one **Win32\_OperatingSystem** without using a **For Each** loop.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



<span data-ttu-id="ca016-135">Im folgenden VBScript-Codebeispiel werden die dem [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)zugeordneten Instanzen abgerufen, z. b. [**Win32 \_ systemoperatingsystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span><span class="sxs-lookup"><span data-stu-id="ca016-135">The following VBScript code example gets instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), such as [**Win32\_SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



<span data-ttu-id="ca016-136">Die folgende Codebeispiel Ausgabe zeigt die Instanzen, die mit dem [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ca016-136">The following code example output shows instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a><span data-ttu-id="ca016-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca016-137">Requirements</span></span>



| <span data-ttu-id="ca016-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca016-138">Requirement</span></span> | <span data-ttu-id="ca016-139">Wert</span><span class="sxs-lookup"><span data-stu-id="ca016-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca016-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca016-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ca016-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca016-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca016-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca016-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ca016-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca016-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca016-144">Header</span><span class="sxs-lookup"><span data-stu-id="ca016-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca016-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca016-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca016-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ca016-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca016-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca016-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca016-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ca016-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca016-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca016-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca016-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="ca016-150">CLSID</span></span><br/>                    | <span data-ttu-id="ca016-151">CLSID- \_ Swap-Objekt Satz</span><span class="sxs-lookup"><span data-stu-id="ca016-151">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="ca016-152">IID</span><span class="sxs-lookup"><span data-stu-id="ca016-152">IID</span></span><br/>                      | <span data-ttu-id="ca016-153">IID \_ iswbemubjectset</span><span class="sxs-lookup"><span data-stu-id="ca016-153">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="ca016-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca016-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca016-155">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="ca016-155">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

