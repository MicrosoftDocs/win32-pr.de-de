---
title: Iwmdrmencryptscatter-Verschlüsselungsmethode (wmdrmsdk. h)
description: Die verschlüsselungsscatter-Methode entkratzt und verschlüsselt Daten.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Verschlüsseltscatter-Methode Windows Media-Format
- Verschlüsseltscatter-Methode Windows Media-Format, iwmdrmencryptscatter-Schnittstelle
- Iwmdrmencryptscatter-Schnittstelle Windows Media-Format, verschlüsseltscatter-Methode
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369526"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="b2651-106">Iwmdrmencryptscatter:: verschlüsseltscatter-Methode</span><span class="sxs-lookup"><span data-stu-id="b2651-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="b2651-107">Die **verschlüsselungsscatter** -Methode entkratzt und verschlüsselt Daten.</span><span class="sxs-lookup"><span data-stu-id="b2651-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2651-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2651-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="b2651-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2651-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2651-110">*cblocks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2651-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2651-111">Anzahl der Elemente im *rgblocks* -Array.</span><span class="sxs-lookup"><span data-stu-id="b2651-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="b2651-112">*rgblocks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2651-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2651-113">Array von mindestens einer [**WMDRM- \_ Verschlüsselungs \_ Punkt \_ Block**](wmdrm-encrypt-scatter-block.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2651-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="b2651-114">Jedes Element beschreibt einen Datenblock, der entfernt und verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2651-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="b2651-115">*pwmcryptodata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2651-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2651-116">Zeiger auf eine [**wmdrmcryptodata**](wmdrmcryptodata.md) -Struktur, die Verschlüsselungs Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="b2651-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="b2651-117">Legen Sie auf **null** fest, um die Standardparameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2651-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="b2651-118">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2651-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2651-119">Die Größe des Ausgabedaten Puffers, der als *pboutput* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b2651-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="b2651-120">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b2651-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2651-121">Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="b2651-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2651-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2651-122">Return value</span></span>

<span data-ttu-id="b2651-123">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2651-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b2651-124">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b2651-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b2651-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b2651-125">Return code</span></span>                                                                          | <span data-ttu-id="b2651-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2651-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b2651-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2651-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b2651-128">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2651-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2651-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2651-129">Remarks</span></span>

<span data-ttu-id="b2651-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2651-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2651-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2651-131">Requirements</span></span>



| <span data-ttu-id="b2651-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2651-132">Requirement</span></span> | <span data-ttu-id="b2651-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b2651-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2651-134">Header</span><span class="sxs-lookup"><span data-stu-id="b2651-134">Header</span></span><br/> | <dl> <span data-ttu-id="b2651-135"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2651-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2651-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2651-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2651-137">**Initencryptscatter**</span><span class="sxs-lookup"><span data-stu-id="b2651-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="b2651-138">**Iwmdrmencryptscatter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b2651-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





