---
description: Die Properties- \_ Eigenschaft des "errbemubject"-Objekts gibt ein "errbempropertyset"-Objekt zurück, das eine Auflistung der Eigenschaften für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: SWbemObject.Properties_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348883"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="8ef93-104">Errbemubject. Properties- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ef93-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="8ef93-105">Die **Properties \_** -Eigenschaft des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbempropertyset**](swbempropertyset.md) "-Objekt zurück, das eine Auflistung der Eigenschaften für die aktuelle Klasse oder Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="8ef93-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="8ef93-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8ef93-106">This property is read-only.</span></span>

<span data-ttu-id="8ef93-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8ef93-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8ef93-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8ef93-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef93-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ef93-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="8ef93-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8ef93-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="8ef93-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ef93-111">Examples</span></span>

<span data-ttu-id="8ef93-112">Das PowerShell-Codebeispiel PowerShell- [WMI-Klassen Skripts generieren](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) in der TechNet Gallery verwendet die Properties \_ -Eigenschaft, um ein Skript für jede der WMI-Klassen zu generieren, die den WMI-Klassennamen und die Eigenschaften auflisten.</span><span class="sxs-lookup"><span data-stu-id="8ef93-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="8ef93-113">Der folgende Code, der aus der [Liste alle Eigenschaften für ein WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) -VBScript-Codebeispiel in der TechNet Gallery stammt, listet die Eigenschaften für eine angegebene WMI-Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="8ef93-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="8ef93-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ef93-114">Requirements</span></span>



| <span data-ttu-id="8ef93-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ef93-115">Requirement</span></span> | <span data-ttu-id="8ef93-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8ef93-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef93-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ef93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef93-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ef93-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ef93-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ef93-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef93-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ef93-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ef93-121">Header</span><span class="sxs-lookup"><span data-stu-id="8ef93-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ef93-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ef93-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ef93-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8ef93-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ef93-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8ef93-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8ef93-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8ef93-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ef93-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ef93-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ef93-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="8ef93-127">CLSID</span></span><br/>                    | <span data-ttu-id="8ef93-128">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="8ef93-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8ef93-129">IID</span><span class="sxs-lookup"><span data-stu-id="8ef93-129">IID</span></span><br/>                      | <span data-ttu-id="8ef93-130">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="8ef93-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




