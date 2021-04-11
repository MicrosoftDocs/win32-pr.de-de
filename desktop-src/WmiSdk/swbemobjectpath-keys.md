---
description: Die Keys-Eigenschaft des "errbemubjectpath"-Objekts ist ein "errbemnamedvalueset"-Objekt, das die Schlüsselwert Bindungen enthält. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Errbemubjectpath. Keys-Eigenschaft (adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042001"
---
# <a name="swbemobjectpathkeys-property"></a><span data-ttu-id="84b41-104">Errbemubjectpath. Keys-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="84b41-104">SWbemObjectPath.Keys property</span></span>

<span data-ttu-id="84b41-105">Die **Keys** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts ist ein " [**errbemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das die Schlüsselwert Bindungen enthält.</span><span class="sxs-lookup"><span data-stu-id="84b41-105">The **Keys** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span> <span data-ttu-id="84b41-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="84b41-106">This property is read-only.</span></span>

<span data-ttu-id="84b41-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="84b41-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="84b41-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="84b41-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b41-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="84b41-109">Syntax</span></span>


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a><span data-ttu-id="84b41-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="84b41-110">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="84b41-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="84b41-111">Error codes</span></span>

<span data-ttu-id="84b41-112">Nachdem Sie die **Keys** -Eigenschaft abgerufen haben, enthält das **Err** -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="84b41-112">After you retrieve the **Keys** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="84b41-113">**wbemErrNotSupported** -2147749900 (0x8004100c)</span><span class="sxs-lookup"><span data-stu-id="84b41-113">**wbemErrNotSupported** - 2147749900 (0x8004100C)</span></span>
</dt> <dd>

<span data-ttu-id="84b41-114">Das Feature bzw. die Operation wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84b41-114">The feature or operation is not supported.</span></span> <span data-ttu-id="84b41-115">Dieser Fehler wird zurückgegeben, wenn ein Skript versucht, in diese Eigenschaft zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="84b41-115">This error is returned if a script attempts to write to this property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84b41-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84b41-116">Requirements</span></span>



| <span data-ttu-id="84b41-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84b41-117">Requirement</span></span> | <span data-ttu-id="84b41-118">Wert</span><span class="sxs-lookup"><span data-stu-id="84b41-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b41-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84b41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84b41-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84b41-120">Windows Vista</span></span><br/>                                                                                   |
| <span data-ttu-id="84b41-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84b41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84b41-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84b41-122">Windows Server 2008</span></span><br/>                                                                             |
| <span data-ttu-id="84b41-123">Header</span><span class="sxs-lookup"><span data-stu-id="84b41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84b41-124"><dt>Adoctint. h (Include wbemdisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84b41-124"><dt>Adoctint.h (include Wbemdisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="84b41-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="84b41-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="84b41-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84b41-126"><dt>Wbemdisp.tlb</dt></span></span> </dl>                    |
| <span data-ttu-id="84b41-127">DLL</span><span class="sxs-lookup"><span data-stu-id="84b41-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84b41-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84b41-128"><dt>Wbemdisp.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="84b41-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="84b41-129">CLSID</span></span><br/>                    | <span data-ttu-id="84b41-130">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="84b41-130">CLSID\_SWbemObjectPath</span></span><br/>                                                                          |
| <span data-ttu-id="84b41-131">IID</span><span class="sxs-lookup"><span data-stu-id="84b41-131">IID</span></span><br/>                      | <span data-ttu-id="84b41-132">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="84b41-132">IID\_ISWbemObjectPath</span></span><br/>                                                                           |



 

 




