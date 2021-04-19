---
description: Mit der setasclass-Methode des Objekts "errbemubjectpath" erzwingt der Pfad die Adressierung einer WMI-Klasse.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: "' Errbemubjectpath. '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356874"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="33e4e-103">' Errbemubjectpath. '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33e4e-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="33e4e-104">Mit der **setasclass** -Methode des Objekts " [**errbemubjectpath**](swbemobjectpath.md) " erzwingt der Pfad die Adressierung einer WMI-Klasse.</span><span class="sxs-lookup"><span data-stu-id="33e4e-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="33e4e-105">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="33e4e-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e4e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e4e-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="33e4e-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="33e4e-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="33e4e-108">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="33e4e-108">Error codes</span></span>

<span data-ttu-id="33e4e-109">Nachdem Sie die **setasclass** -Eigenschaft erhalten oder festgelegt haben, enthält das **Err** -Objekt möglicherweise den folgenden Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="33e4e-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="33e4e-110">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="33e4e-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="33e4e-111">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="33e4e-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33e4e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33e4e-112">Requirements</span></span>



| <span data-ttu-id="33e4e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33e4e-113">Requirement</span></span> | <span data-ttu-id="33e4e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="33e4e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e4e-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33e4e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33e4e-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33e4e-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33e4e-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33e4e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33e4e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33e4e-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33e4e-119">Header</span><span class="sxs-lookup"><span data-stu-id="33e4e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e4e-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e4e-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="33e4e-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="33e4e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="33e4e-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="33e4e-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="33e4e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33e4e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33e4e-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33e4e-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="33e4e-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="33e4e-125">CLSID</span></span><br/>                    | <span data-ttu-id="33e4e-126">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="33e4e-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="33e4e-127">IID</span><span class="sxs-lookup"><span data-stu-id="33e4e-127">IID</span></span><br/>                      | <span data-ttu-id="33e4e-128">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="33e4e-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




