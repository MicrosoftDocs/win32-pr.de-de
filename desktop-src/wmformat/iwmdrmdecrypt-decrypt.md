---
title: Iwmdrmentschlüsseln-Entschlüsselungsmethode (wmdrmsdk. h)
description: Die Entschlüsselungsmethode entschlüsselt einen Datenpuffer an Ort und Stelle.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Entschlüsselungsmethode Windows Media-Format
- Entschlüsselungsmethode Windows Media-Format, iwmdrmentschlüsselungsschnittstelle
- Iwmdrmentschlüsselungsschnittstelle Windows Media-Format, Entschlüsselungsmethode
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365894"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="2f59c-106">Iwmdrmentschlüsselungsmethode::D ecrypt-Methode</span><span class="sxs-lookup"><span data-stu-id="2f59c-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="2f59c-107">Die **Entschlüsselungsmethode** entschlüsselt einen Datenpuffer an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="2f59c-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f59c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f59c-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="2f59c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f59c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f59c-110">*pbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f59c-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f59c-111">Die zu entschlüsselnden Daten.</span><span class="sxs-lookup"><span data-stu-id="2f59c-111">Data to be decrypted.</span></span> <span data-ttu-id="2f59c-112">Wenn die Methode erfolgreich ausgeführt wird, werden diese Daten bei Rückgabe entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="2f59c-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="2f59c-113">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f59c-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f59c-114">Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2f59c-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2f59c-115">*pwmcryptodata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f59c-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f59c-116">Zeiger auf eine [**wmdrmcryptodata**](wmdrmcryptodata.md) -Struktur mit zusätzlichen Parametern.</span><span class="sxs-lookup"><span data-stu-id="2f59c-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="2f59c-117">Kann **null** sein, wenn der Inhalt mit den Standardparametern verschlüsselt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f59c-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f59c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f59c-118">Return value</span></span>

<span data-ttu-id="2f59c-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="2f59c-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2f59c-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2f59c-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2f59c-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2f59c-121">Return code</span></span>                                                                          | <span data-ttu-id="2f59c-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f59c-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2f59c-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f59c-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2f59c-124">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f59c-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f59c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f59c-125">Remarks</span></span>

<span data-ttu-id="2f59c-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f59c-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f59c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f59c-127">Requirements</span></span>



| <span data-ttu-id="2f59c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f59c-128">Requirement</span></span> | <span data-ttu-id="2f59c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2f59c-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f59c-130">Header</span><span class="sxs-lookup"><span data-stu-id="2f59c-130">Header</span></span><br/> | <dl> <span data-ttu-id="2f59c-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f59c-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f59c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f59c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f59c-133">**Iwmdrmentschlüsseln-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2f59c-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="2f59c-134">**Wmdrmcryptodata**</span><span class="sxs-lookup"><span data-stu-id="2f59c-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





