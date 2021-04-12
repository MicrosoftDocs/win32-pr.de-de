---
description: Die Path- \_ Eigenschaft des "errbemubject"-Objekts gibt ein "errbemubjectpath"-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: SWbemObject.Path_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216702"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="50826-104">"Errbemubject. Path"- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50826-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="50826-105">Die **path \_** -Eigenschaft des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="50826-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="50826-106">Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.</span><span class="sxs-lookup"><span data-stu-id="50826-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="50826-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="50826-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="50826-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="50826-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50826-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="50826-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="50826-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="50826-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="50826-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50826-111">Remarks</span></span>

<span data-ttu-id="50826-112">Nur die [**Class**](swbemobjectpath-class.md) -Eigenschaft der zurückgegebenen [**errbemubjectpath**](swbemobjectpath.md) -Instanz kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="50826-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="50826-113">Wenn Sie versuchen, eine andere Eigenschaft zu ändern, oder wenn Sie versuchen, die Methoden " [**stasclass**](swbemobjectpath-setasclass.md) " oder " [**sstassingleton**](swbemobjectpath-setassingleton.md)" aufzurufen, wird ein **wbemErrReadOnly** -Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="50826-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="50826-114">Aus diesem Grund können Sie das Objekt " [**errbemnamedvalueset**](swbemnamedvalueset.md) ", das den Wert der [**Keys**](swbemobjectpath-keys.md) -Eigenschaft der zurückgegebenen " [**errbemubjectpath**](swbemobjectpath.md) "-Instanz ist, nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="50826-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="50826-115">Wenn Sie versuchen, die [**Add**](swbemnamedvalueset-add.md)-, [**Remove**](swbemnamedvalueset-remove.md)-oder [**DeleteAll**](swbemnamedvalueset-deleteall.md) -Methoden für diesen Wert aufzurufen, erhalten Sie einen wbemErrReadOnly-Fehler.</span><span class="sxs-lookup"><span data-stu-id="50826-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="50826-116">Außerdem ist es nicht möglich, einen aus dieser Sammlung erhaltenen " [**Swap Name**](swbemnamedvalue.md) "-Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="50826-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="50826-117">Wenn Sie versuchen, die **value** -Eigenschaft zu ändern, wird derselbe Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50826-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="50826-118">Wenn Sie jedoch " [**errbemubject. Clone \_**](swbemobject-clone-.md) " aufrufen, um eine Kopie zu erstellen, ist die Eigenschaft " [**errbemubjectpath. Path**](swbemobjectpath-path.md) " der Kopie vollständig änderbar.</span><span class="sxs-lookup"><span data-stu-id="50826-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="50826-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50826-119">Examples</span></span>

<span data-ttu-id="50826-120">Im folgenden Codebeispiel, das aus [Auflisten aller WMI-cimV2-Klassen](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in der TechNet-Galerie stammt, wird die Path-Eigenschaft verwendet, \_ um alle WMI cimV2-Klassen aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="50826-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="50826-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50826-121">Requirements</span></span>



| <span data-ttu-id="50826-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50826-122">Requirement</span></span> | <span data-ttu-id="50826-123">Wert</span><span class="sxs-lookup"><span data-stu-id="50826-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50826-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50826-124">Minimum supported client</span></span><br/> | <span data-ttu-id="50826-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50826-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50826-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50826-126">Minimum supported server</span></span><br/> | <span data-ttu-id="50826-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50826-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50826-128">Header</span><span class="sxs-lookup"><span data-stu-id="50826-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="50826-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50826-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50826-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="50826-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="50826-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50826-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50826-132">DLL</span><span class="sxs-lookup"><span data-stu-id="50826-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50826-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50826-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="50826-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="50826-134">CLSID</span></span><br/>                    | <span data-ttu-id="50826-135">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="50826-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="50826-136">IID</span><span class="sxs-lookup"><span data-stu-id="50826-136">IID</span></span><br/>                      | <span data-ttu-id="50826-137">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="50826-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




