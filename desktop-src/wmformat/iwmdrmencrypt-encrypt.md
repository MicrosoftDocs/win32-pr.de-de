---
title: Iwmdrmencrypt-Verschlüsselungsmethode (wmdrmsdk. h)
description: Die Methode "verschlüsseln" verschlüsselt einen Datenpuffer an Ort und Stelle.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Verschlüsselungsmethode (Windows Media-Format)
- Verschlüsseln der Methode Windows Media-Format, iwmdrmencrypt-Schnittstelle
- Iwmdrmencrypt-Schnittstelle Windows Media-Format, Methode verschlüsseln
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365385"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="43cae-106">Iwmdrmencrypt:: Verschlüsseln-Methode</span><span class="sxs-lookup"><span data-stu-id="43cae-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="43cae-107">Die Methode " **verschlüsseln** " verschlüsselt einen Datenpuffer an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="43cae-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="43cae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="43cae-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="43cae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="43cae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43cae-110">*pbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="43cae-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43cae-111">Die zu verschlüsselnden Daten.</span><span class="sxs-lookup"><span data-stu-id="43cae-111">Data to encrypt.</span></span> <span data-ttu-id="43cae-112">Wenn die Methode erfolgreich ausgeführt wird, werden die Daten bei der Rückgabe verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="43cae-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="43cae-113">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cae-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cae-114">Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="43cae-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="43cae-115">*pwmcryptodata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cae-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cae-116">Zeiger auf eine [**wmdrmcryptodata**](wmdrmcryptodata.md) -Struktur mit zusätzlichen Parametern.</span><span class="sxs-lookup"><span data-stu-id="43cae-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="43cae-117">Legen Sie auf **null** fest, um die Standard Verschlüsselungs Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="43cae-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43cae-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43cae-118">Return value</span></span>

<span data-ttu-id="43cae-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="43cae-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="43cae-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="43cae-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="43cae-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="43cae-121">Return code</span></span>                                                                          | <span data-ttu-id="43cae-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43cae-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="43cae-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43cae-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="43cae-124">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43cae-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43cae-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43cae-125">Remarks</span></span>

<span data-ttu-id="43cae-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="43cae-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="43cae-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43cae-127">Requirements</span></span>



| <span data-ttu-id="43cae-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43cae-128">Requirement</span></span> | <span data-ttu-id="43cae-129">Wert</span><span class="sxs-lookup"><span data-stu-id="43cae-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43cae-130">Header</span><span class="sxs-lookup"><span data-stu-id="43cae-130">Header</span></span><br/> | <dl> <span data-ttu-id="43cae-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="43cae-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43cae-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43cae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cae-133">**Iwmdrmencrypt-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="43cae-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="43cae-134">**Wmdrmcryptodata**</span><span class="sxs-lookup"><span data-stu-id="43cae-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





