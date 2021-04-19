---
description: Die OutParameters-Eigenschaft des "errbemmethod"-Objekts ist ein Objekt vom Typ "OutParameters", dessen Eigenschaften die Out-Parameter und den Rückgabetyp dieser Methode definieren. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: "' Taubemmethod. OutParameters '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353547"
---
# <a name="swbemmethodoutparameters-property"></a><span data-ttu-id="cdc3b-104">' Taubemmethod. OutParameters '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cdc3b-104">SWbemMethod.OutParameters property</span></span>

<span data-ttu-id="cdc3b-105">Die **OutParameters** -Eigenschaft des " [**errbemmethod**](swbemmethod.md) "- [**Objekts ist ein Objekt**](swbemobject.md) vom Typ "OutParameters", dessen Eigenschaften die Out-Parameter und den Rückgabetyp dieser Methode definieren.</span><span class="sxs-lookup"><span data-stu-id="cdc3b-105">The **OutParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span> <span data-ttu-id="cdc3b-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cdc3b-106">This property is read-only.</span></span>

<span data-ttu-id="cdc3b-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cdc3b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="cdc3b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cdc3b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc3b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdc3b-109">Syntax</span></span>


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="cdc3b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cdc3b-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc3b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdc3b-111">Remarks</span></span>

<span data-ttu-id="cdc3b-112">Weitere Informationen zur Verwendung dieser Eigenschaft zum Abrufen von Ausgabeparametern von Anbieter Methoden finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cdc3b-112">For more information about how to use this property to obtain output parameters from provider methods, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="cdc3b-113">Beachten Sie, dass alle an diesem Objekt vorgenommenen Änderungen nicht in der zugrunde liegenden Methoden Definition widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="cdc3b-113">Note that any changes made to this object are not reflected in the underlying method definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc3b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdc3b-114">Requirements</span></span>



| <span data-ttu-id="cdc3b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdc3b-115">Requirement</span></span> | <span data-ttu-id="cdc3b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cdc3b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc3b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdc3b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc3b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdc3b-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdc3b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdc3b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc3b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdc3b-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdc3b-121">Header</span><span class="sxs-lookup"><span data-stu-id="cdc3b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc3b-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3b-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdc3b-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cdc3b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="cdc3b-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3b-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cdc3b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cdc3b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdc3b-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3b-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cdc3b-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="cdc3b-127">CLSID</span></span><br/>                    | <span data-ttu-id="cdc3b-128">CLSID- \_ Swap-Methode</span><span class="sxs-lookup"><span data-stu-id="cdc3b-128">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="cdc3b-129">IID</span><span class="sxs-lookup"><span data-stu-id="cdc3b-129">IID</span></span><br/>                      | <span data-ttu-id="cdc3b-130">IID \_ iswbemmethod</span><span class="sxs-lookup"><span data-stu-id="cdc3b-130">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="cdc3b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc3b-132">**Swap-Methode**</span><span class="sxs-lookup"><span data-stu-id="cdc3b-132">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="cdc3b-133">**SWbemObject.Execmethod\_**</span><span class="sxs-lookup"><span data-stu-id="cdc3b-133">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="cdc3b-134">**SWbemObject.Execmethodasync\_**</span><span class="sxs-lookup"><span data-stu-id="cdc3b-134">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="cdc3b-135">**SWbemServices.Execmethod**</span><span class="sxs-lookup"><span data-stu-id="cdc3b-135">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="cdc3b-136">**SWbemServices.Execmethodasync**</span><span class="sxs-lookup"><span data-stu-id="cdc3b-136">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




