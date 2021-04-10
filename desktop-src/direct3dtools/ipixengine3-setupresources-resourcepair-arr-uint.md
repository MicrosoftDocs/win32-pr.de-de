---
description: Übergibt Ressourcen an die-Engine, z. b. Zeichen folgen für Fehlermeldungen.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine3:: setupresources-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c2b103c5c27bf3929f72d909c9000a1e252e8dee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124729"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span data-ttu-id="de549-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3:: setupresources-Methode</span><span class="sxs-lookup"><span data-stu-id="de549-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3::SetupResources method</span></span>

<span data-ttu-id="de549-104">Übergibt Ressourcen an die-Engine, z. b. Zeichen folgen für Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="de549-104">Passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="de549-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de549-105">Syntax</span></span>


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a><span data-ttu-id="de549-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de549-106">Parameters</span></span>

<span data-ttu-id="de549-107">*count1- \_ Ressourcen* </span><span class="sxs-lookup"><span data-stu-id="de549-107">*count1\_resources* </span></span>  
<span data-ttu-id="de549-108">Die Ressourcen Ressourcen wurden übermittelt.</span><span class="sxs-lookup"><span data-stu-id="de549-108">The resources resources passed.</span></span>

<span data-ttu-id="de549-109">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="de549-109">*count* </span></span>  
<span data-ttu-id="de549-110">Die Anzahl der bestandenen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="de549-110">The number of resources passed.</span></span>

## <a name="return-value"></a><span data-ttu-id="de549-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de549-111">Return value</span></span>

<span data-ttu-id="de549-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="de549-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de549-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="de549-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de549-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de549-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="de549-115">Header</span><span class="sxs-lookup"><span data-stu-id="de549-115">Header</span></span></p></td><td><span data-ttu-id="de549-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="de549-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="de549-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de549-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="de549-118">**IPixEngine3**</span><span class="sxs-lookup"><span data-stu-id="de549-118">**IPixEngine3**</span></span>](/windows/desktop/direct3dtools/ipixengine3)

 

 
