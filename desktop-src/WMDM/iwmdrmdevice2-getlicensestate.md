---
title: IWMDRMDevice2 getlicenerstate-Methode
description: Die getlicencstate-Methode ruft den Lizenzstatus ab.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Getlicencstate-Methode, Windows Media Device Manager
- Getlicencstate-Methode, Windows Media Device Manager, IWMDRMDevice2-Schnittstelle
- IWMDRMDevice2-Schnittstelle Windows Media Device Manager, getlicenanstate-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355052"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="4b536-106">IWMDRMDevice2:: getlicenerstate-Methode</span><span class="sxs-lookup"><span data-stu-id="4b536-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="4b536-107">Die **getlicencstate** -Methode ruft den Lizenzstatus ab.</span><span class="sxs-lookup"><span data-stu-id="4b536-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b536-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b536-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="4b536-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b536-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b536-110">*pbstatus-erydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b536-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b536-111">Zeiger auf die abgefragten Daten des Lizenz Zustands.</span><span class="sxs-lookup"><span data-stu-id="4b536-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="4b536-112">*cbstatuequerydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b536-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b536-113">Anzahl der abgefragten Daten.</span><span class="sxs-lookup"><span data-stu-id="4b536-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="4b536-114">*pdwcategory* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4b536-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b536-115">Ein Zeiger auf die Kategorie.</span><span class="sxs-lookup"><span data-stu-id="4b536-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="4b536-116">*pkremainingcounts* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4b536-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b536-117">Zeiger auf die verbleibenden Zähler.</span><span class="sxs-lookup"><span data-stu-id="4b536-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="4b536-118">*pkremaininghours* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4b536-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b536-119">Zeiger auf die verbleibenden Stunden.</span><span class="sxs-lookup"><span data-stu-id="4b536-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="4b536-120">*pdwreserved* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4b536-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b536-121">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4b536-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b536-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b536-122">Return value</span></span>

<span data-ttu-id="4b536-123">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="4b536-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4b536-124">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4b536-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4b536-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4b536-125">Return code</span></span>                                                                          | <span data-ttu-id="4b536-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b536-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="4b536-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b536-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4b536-128">Die Methode ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4b536-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b536-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b536-129">Requirements</span></span>



| <span data-ttu-id="4b536-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b536-130">Requirement</span></span> | <span data-ttu-id="4b536-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4b536-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b536-132">Header</span><span class="sxs-lookup"><span data-stu-id="4b536-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4b536-133"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b536-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="4b536-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b536-134">Library</span></span><br/> | <dl> <span data-ttu-id="4b536-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b536-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b536-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b536-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b536-137">**IWMDRMDevice2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4b536-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





