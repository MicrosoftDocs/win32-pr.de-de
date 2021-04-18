---
description: Konstruktormethode.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Cpospassthru. cpospassthru-Konstruktor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343545"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="6004d-103">Cpospassthru. cpospassthru-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="6004d-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="6004d-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6004d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6004d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6004d-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="6004d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6004d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6004d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6004d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6004d-108">Zeiger auf den Namen des Objekts, zu Debuggingzwecken.</span><span class="sxs-lookup"><span data-stu-id="6004d-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="6004d-109">Weisen Sie diesen Parameter im statischen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="6004d-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="6004d-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="6004d-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6004d-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="6004d-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="6004d-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="6004d-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6004d-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="6004d-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6004d-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="6004d-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6004d-115">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="6004d-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6004d-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6004d-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6004d-117">*ppin*</span><span class="sxs-lookup"><span data-stu-id="6004d-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="6004d-118">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN des Filters.</span><span class="sxs-lookup"><span data-stu-id="6004d-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



