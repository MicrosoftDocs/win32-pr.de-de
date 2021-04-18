---
title: Iwmsecurebuffer-Entschlüsselungsmethode (wmdrmsdk. h)
description: Die Entschlüsselungsmethode entschlüsselt einen Datenzeiger, der durch Aufrufen der Verschlüsselungsmethode verschlüsselt wurde.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Entschlüsselungsmethode Windows Media-Format
- Entschlüsselungsmethode Windows Media-Format, iwmsecurebuffer-Schnittstelle
- Iwmsecurebuffer-Schnittstelle Windows Media-Format, Entschlüsselungsmethode
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371366"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="8cdf5-106">Iwmsecurebuffer::D ecrypt-Methode</span><span class="sxs-lookup"><span data-stu-id="8cdf5-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="8cdf5-107">Die **Entschlüsselungsmethode** entschlüsselt einen Datenzeiger, der durch Aufrufen der [**Verschlüsselungs**](iwmsecurebuffer-encrypt.md) Methode verschlüsselt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cdf5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cdf5-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="8cdf5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cdf5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cdf5-110">*psecurechannel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cdf5-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cdf5-111">Zeiger auf eine sichere Kanal Schnittstelle, die den verschlüsselten Datenzeiger enthält.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cdf5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cdf5-112">Return value</span></span>

<span data-ttu-id="8cdf5-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8cdf5-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8cdf5-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8cdf5-115">Return code</span></span>                                                                          | <span data-ttu-id="8cdf5-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cdf5-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8cdf5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8cdf5-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8cdf5-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8cdf5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cdf5-119">Remarks</span></span>

<span data-ttu-id="8cdf5-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cdf5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cdf5-121">Requirements</span></span>



| <span data-ttu-id="8cdf5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cdf5-122">Requirement</span></span> | <span data-ttu-id="8cdf5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8cdf5-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cdf5-124">Header</span><span class="sxs-lookup"><span data-stu-id="8cdf5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8cdf5-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cdf5-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8cdf5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cdf5-126">Library</span></span><br/> | <dl> <span data-ttu-id="8cdf5-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cdf5-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cdf5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cdf5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cdf5-129">**Verschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="8cdf5-130">**Iwmsecurebuffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





