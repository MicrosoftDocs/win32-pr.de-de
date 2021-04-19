---
title: Methode ' iwmdrmdevice ' getsecureclockchallenge
description: Die getsecureclockchallenge-Methode ruft das Challenge-Ergebnis der sicheren Uhr ab.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Getsecureclockchallenge-Methode, Windows Media Device Manager
- Getsecureclockchallenge-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getsecureclockchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353790"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="1f897-106">Iwmdrmdevice:: getsecureclockchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="1f897-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="1f897-107">Die **getsecureclockchallenge** -Methode ruft das Challenge-Ergebnis der sicheren Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="1f897-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f897-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f897-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="1f897-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f897-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f897-110">*ppbchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f897-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f897-111">Das Abfrageergebnis wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1f897-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="1f897-112">*pcbchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f897-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f897-113">Größe des Challenge-Ergebnisses in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1f897-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f897-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f897-114">Return value</span></span>

<span data-ttu-id="1f897-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1f897-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1f897-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1f897-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1f897-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1f897-117">Return code</span></span>                                                                          | <span data-ttu-id="1f897-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f897-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1f897-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f897-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1f897-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f897-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1f897-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f897-121">Requirements</span></span>



| <span data-ttu-id="1f897-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f897-122">Requirement</span></span> | <span data-ttu-id="1f897-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1f897-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f897-124">Header</span><span class="sxs-lookup"><span data-stu-id="1f897-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1f897-125"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f897-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="1f897-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f897-126">Library</span></span><br/> | <dl> <span data-ttu-id="1f897-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f897-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f897-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f897-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f897-129">**Getsecureclock**</span><span class="sxs-lookup"><span data-stu-id="1f897-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="1f897-130">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1f897-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





