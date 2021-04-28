---
description: 'CPosPassThru.CPosPassThru-Konstruktor : Konstruktormethode.'
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: CPosPassThru.CPosPassThru-Konstruktor
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
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085598"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="eb762-103">CPosPassThru.CPosPassThru-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="eb762-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="eb762-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eb762-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb762-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb762-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="eb762-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb762-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb762-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="eb762-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="eb762-108">Zeiger auf den Namen des Objekts zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="eb762-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="eb762-109">Ordnen Sie diesen Parameter im statischen Speicher zu.</span><span class="sxs-lookup"><span data-stu-id="eb762-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="eb762-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="eb762-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="eb762-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="eb762-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="eb762-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="eb762-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="eb762-113">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="eb762-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eb762-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="eb762-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="eb762-115">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="eb762-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="eb762-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="eb762-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="eb762-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="eb762-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="eb762-118">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins des Filters.</span><span class="sxs-lookup"><span data-stu-id="eb762-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



