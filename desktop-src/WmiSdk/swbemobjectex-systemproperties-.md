---
description: Gibt ein Objekt vom Typ "Swap PropertySet" zurück, das die Auflistung von WMI-System Eigenschaften enthält, die auf das Objekt angewendet werden.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: SWbemObjectEx.SystemProperties_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218168"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="d0fa6-103">SWbemObjectEx.Systemproperties ( \_ Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d0fa6-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="d0fa6-104">Die **SystemProperties \_** -Eigenschaft des " [**errbemubjectex**](swbemobjectex.md) "-Objekts gibt ein " [**errbempropertyset**](swbempropertyset.md) "-Objekt zurück, das die Sammlung von [WMI-System Eigenschaften](wmi-system-properties.md) enthält, die auf das Objekt angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0fa6-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="d0fa6-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d0fa6-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d0fa6-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d0fa6-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fa6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0fa6-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="d0fa6-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d0fa6-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="d0fa6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0fa6-109">Examples</span></span>

<span data-ttu-id="d0fa6-110">Im folgenden Codebeispiel werden die Eigenschaftswerte für die Win32- \_ Prozess Klasse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d0fa6-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="d0fa6-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0fa6-111">Requirements</span></span>



| <span data-ttu-id="d0fa6-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0fa6-112">Requirement</span></span> | <span data-ttu-id="d0fa6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d0fa6-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fa6-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0fa6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d0fa6-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0fa6-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0fa6-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0fa6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d0fa6-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0fa6-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0fa6-118">Header</span><span class="sxs-lookup"><span data-stu-id="d0fa6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0fa6-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0fa6-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0fa6-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d0fa6-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0fa6-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0fa6-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0fa6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d0fa6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0fa6-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0fa6-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0fa6-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="d0fa6-124">CLSID</span></span><br/>                    | <span data-ttu-id="d0fa6-125">CLSID- \_ Swap-Austausch</span><span class="sxs-lookup"><span data-stu-id="d0fa6-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="d0fa6-126">IID</span><span class="sxs-lookup"><span data-stu-id="d0fa6-126">IID</span></span><br/>                      | <span data-ttu-id="d0fa6-127">IID \_ iswbejebjectex</span><span class="sxs-lookup"><span data-stu-id="d0fa6-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d0fa6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0fa6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fa6-129">**Austauschen von "errbemubjectex"**</span><span class="sxs-lookup"><span data-stu-id="d0fa6-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




