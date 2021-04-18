---
title: Iwmdrmnonsilentlicenseaquisition getchallenge-Methode (wmdrmsdk. h)
description: Die getchallenge-Methode ruft die Lizenz Herausforderung ab, die auf dem Lizenzserver gepostet werden soll.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Getchallenge-Methode Windows Media-Format
- Getchallenge-Methode Windows Media-Format, iwmdrmnonsilentlicenseaquisition-Schnittstelle
- Iwmdrmnonsilentlicenseaquisition-Schnittstelle Windows Media-Format, getchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357654"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="4e97d-106">Iwmdrmnonsilentlicenseaquisition:: getchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="4e97d-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="4e97d-107">Die **getchallenge** -Methode ruft die Lizenz Herausforderung ab, die auf dem Lizenzserver gepostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e97d-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e97d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e97d-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="4e97d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e97d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e97d-110">*pbstranchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4e97d-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e97d-111">Adresse einer Variablen, die die Lizenz Herausforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="4e97d-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e97d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e97d-112">Return value</span></span>

<span data-ttu-id="4e97d-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e97d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4e97d-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4e97d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4e97d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4e97d-115">Return code</span></span>                                                                          | <span data-ttu-id="4e97d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e97d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4e97d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e97d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4e97d-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e97d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e97d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e97d-119">Remarks</span></span>

<span data-ttu-id="4e97d-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="4e97d-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e97d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e97d-121">Requirements</span></span>



| <span data-ttu-id="4e97d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e97d-122">Requirement</span></span> | <span data-ttu-id="4e97d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4e97d-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e97d-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e97d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4e97d-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e97d-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e97d-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e97d-126">Library</span></span><br/> | <dl> <span data-ttu-id="4e97d-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e97d-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e97d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e97d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e97d-129">**Iwmdrmnonsilentlicenseaquisition-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4e97d-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





