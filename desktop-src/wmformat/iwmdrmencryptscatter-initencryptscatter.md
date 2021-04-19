---
title: Iwmdrmencryptscatter initencryptscatter-Methode (wmdrmsdk. h)
description: Die initencryptscatter-Methode initialisiert die iwmdrmencryptscatter-Schnittstelle zur Verwendung.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Initencryptscatter-Methode Windows Media-Format
- Initencryptscatter-Methode Windows Media-Format, iwmdrmencryptscatter-Schnittstelle
- Iwmdrmencryptscatter-Schnittstelle Windows Media-Format, initencryptscatter-Methode
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355896"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="0efc2-106">Iwmdrmencryptscatter:: initencryptscatter-Methode</span><span class="sxs-lookup"><span data-stu-id="0efc2-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="0efc2-107">Die **initencryptscatter** -Methode initialisiert die **iwmdrmencryptscatter** -Schnittstelle zur Verwendung.</span><span class="sxs-lookup"><span data-stu-id="0efc2-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efc2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0efc2-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="0efc2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0efc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0efc2-110">*cstreams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0efc2-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0efc2-111">Anzahl der Elemente im *rginfos* -Array.</span><span class="sxs-lookup"><span data-stu-id="0efc2-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="0efc2-112">Dies ist auch die Anzahl der Streams, die in den zu verschlüsselnden Daten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0efc2-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="0efc2-113">*rginfos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0efc2-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0efc2-114">Array von mindestens einer [**WMDRM- \_ Verschlüsselungs \_ Punkt \_ Info**](wmdrm-encrypt-scatter-info.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0efc2-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="0efc2-115">Jedes-Element enthält Verschlüsselungs Informationen für einen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="0efc2-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="0efc2-116">Die Anzahl der Elemente in diesem Array muss gleich dem Wert von *cstreams* sein.</span><span class="sxs-lookup"><span data-stu-id="0efc2-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0efc2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0efc2-117">Return value</span></span>

<span data-ttu-id="0efc2-118">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0efc2-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0efc2-119">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0efc2-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0efc2-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0efc2-120">Return code</span></span>                                                                          | <span data-ttu-id="0efc2-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0efc2-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0efc2-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0efc2-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0efc2-123">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0efc2-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0efc2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0efc2-124">Remarks</span></span>

<span data-ttu-id="0efc2-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="0efc2-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0efc2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0efc2-126">Requirements</span></span>



| <span data-ttu-id="0efc2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0efc2-127">Requirement</span></span> | <span data-ttu-id="0efc2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0efc2-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0efc2-129">Header</span><span class="sxs-lookup"><span data-stu-id="0efc2-129">Header</span></span><br/> | <dl> <span data-ttu-id="0efc2-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0efc2-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0efc2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0efc2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efc2-132">**Verschlüsselungs Punkt**</span><span class="sxs-lookup"><span data-stu-id="0efc2-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="0efc2-133">**Iwmdrmencryptscatter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0efc2-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





