---
description: Die Path- \_ Eigenschaft des "errbemlasterror"-Objekts gibt ein "errbeapbjectpath"-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042474"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="a783d-104">' Swap. Path '- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a783d-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="a783d-105">Die **path \_** -Eigenschaft des " [**errbemlasterror**](swbemlasterror.md) "-Objekts gibt ein " [**errbeapbjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="a783d-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="a783d-106">Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.</span><span class="sxs-lookup"><span data-stu-id="a783d-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="a783d-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a783d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a783d-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a783d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a783d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a783d-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="a783d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a783d-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a783d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a783d-111">Remarks</span></span>

<span data-ttu-id="a783d-112">Nur die [**Class**](swbemobjectpath-class.md) -Eigenschaft der zurückgegebenen [**errbemubjectpath**](swbemobjectpath.md) -Instanz kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a783d-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="a783d-113">Wenn Sie versuchen, eine andere Eigenschaft zu ändern, oder wenn Sie versuchen [**, die Methoden**](swbemobjectpath-setasclass.md) " [**-Methode"**](swbemobjectpath-setassingleton.md) oder "-Methode" aufzurufen, wird die Fehlermeldung " **wbemErrReadOnly**" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a783d-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="a783d-114">Aus diesem Grund können Sie das Objekt " [**errbemnamedvalueset**](swbemnamedvalueset.md) ", das den Wert der [**Keys**](swbemobjectpath-keys.md) -Eigenschaft der zurückgegebenen " [**errbemubjectpath**](swbemobjectpath.md) "-Instanz ist, nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a783d-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="a783d-115">Wenn Sie versuchen, die [**Add**](swbemnamedvalueset-add.md)-, [**Remove**](swbemnamedvalueset-remove.md)-oder [**DeleteAll**](swbemnamedvalueset-deleteall.md) -Methoden für diesen Wert aufzurufen, erhalten Sie einen **wbemErrReadOnly** -Fehler.</span><span class="sxs-lookup"><span data-stu-id="a783d-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="a783d-116">Außerdem ist es nicht möglich, einen aus dieser Sammlung erhaltenen " [**Swap Name**](swbemnamedvalue.md) "-Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a783d-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="a783d-117">Wenn Sie versuchen, die [**value**](swbemnamedvalue-value.md) -Eigenschaft zu ändern, wird derselbe Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a783d-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="a783d-118">Wenn Sie jedoch " [**errbemubject. \_ Clone**](swbemobject-clone-.md) " zum Erstellen einer Kopie aufruft, ist die [**path \_**](swbemobject-path-.md) -Eigenschaft der Kopie vollständig änderbar.</span><span class="sxs-lookup"><span data-stu-id="a783d-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a783d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a783d-119">Requirements</span></span>



| <span data-ttu-id="a783d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a783d-120">Requirement</span></span> | <span data-ttu-id="a783d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a783d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a783d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a783d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a783d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a783d-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a783d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a783d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a783d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a783d-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a783d-126">Header</span><span class="sxs-lookup"><span data-stu-id="a783d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a783d-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a783d-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a783d-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a783d-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a783d-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a783d-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a783d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a783d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a783d-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a783d-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a783d-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="a783d-132">CLSID</span></span><br/>                    | <span data-ttu-id="a783d-133">CLSID- \_ Austausch Fehler</span><span class="sxs-lookup"><span data-stu-id="a783d-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="a783d-134">IID</span><span class="sxs-lookup"><span data-stu-id="a783d-134">IID</span></span><br/>                      | <span data-ttu-id="a783d-135">IID \_ iswbemlasterror</span><span class="sxs-lookup"><span data-stu-id="a783d-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




