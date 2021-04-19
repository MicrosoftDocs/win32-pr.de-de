---
title: Iwmpcdromburn IsAvailable-Methode
description: Die IsAvailable-Methode stellt Informationen über das CD-Laufwerk und die Medien bereit.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- IsAvailable-Methode, Windows-Media Player
- IsAvailable-Methode, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, IsAvailable-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373831"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="778ff-106">Iwmpcdromburn:: IsAvailable-Methode</span><span class="sxs-lookup"><span data-stu-id="778ff-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="778ff-107">Die **IsAvailable** -Methode stellt Informationen über das CD-Laufwerk und die Medien bereit.</span><span class="sxs-lookup"><span data-stu-id="778ff-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="778ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="778ff-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="778ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="778ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="778ff-110">*bstritem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778ff-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778ff-111">Ein **System. String** -Wert, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="778ff-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="778ff-112">Wert</span><span class="sxs-lookup"><span data-stu-id="778ff-112">Value</span></span> | <span data-ttu-id="778ff-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="778ff-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="778ff-114">Brenn</span><span class="sxs-lookup"><span data-stu-id="778ff-114">Burn</span></span>  | <span data-ttu-id="778ff-115">Das Laufwerk ist ein CD-Brenner.</span><span class="sxs-lookup"><span data-stu-id="778ff-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="778ff-116">Discs</span><span class="sxs-lookup"><span data-stu-id="778ff-116">Disc</span></span>  | <span data-ttu-id="778ff-117">Das Laufwerk enthält eine CD.</span><span class="sxs-lookup"><span data-stu-id="778ff-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="778ff-118">Löschen</span><span class="sxs-lookup"><span data-stu-id="778ff-118">Erase</span></span> | <span data-ttu-id="778ff-119">Die CD kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="778ff-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="778ff-120">Schreiben</span><span class="sxs-lookup"><span data-stu-id="778ff-120">Write</span></span> | <span data-ttu-id="778ff-121">Die CD kann in geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="778ff-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="778ff-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="778ff-122">Return value</span></span>

<span data-ttu-id="778ff-123">Ein **System. Boolean** -Wert, der das Ergebnis angibt.</span><span class="sxs-lookup"><span data-stu-id="778ff-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="778ff-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="778ff-124">Requirements</span></span>



| <span data-ttu-id="778ff-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="778ff-125">Requirement</span></span> | <span data-ttu-id="778ff-126">Wert</span><span class="sxs-lookup"><span data-stu-id="778ff-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="778ff-127">Version</span><span class="sxs-lookup"><span data-stu-id="778ff-127">Version</span></span><br/>   | <span data-ttu-id="778ff-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="778ff-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="778ff-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="778ff-129">Namespace</span></span><br/> | <span data-ttu-id="778ff-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="778ff-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="778ff-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="778ff-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="778ff-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="778ff-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778ff-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="778ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="778ff-134">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="778ff-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





