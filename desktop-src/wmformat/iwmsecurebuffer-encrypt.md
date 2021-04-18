---
title: Iwmsecurebuffer-Verschlüsselungsmethode (wmdrmsdk. h)
description: Die Methode "verschlüsseln" verschlüsselt einen Datenzeiger.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Verschlüsselungsmethode (Windows Media-Format)
- Verschlüsselungsmethode Windows Media-Format, iwmsecurebuffer-Schnittstelle
- Iwmsecurebuffer-Schnittstelle Windows Media-Format, Methode verschlüsseln
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371566"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="e7f90-106">Iwmsecurebuffer:: Verschlüsseln-Methode</span><span class="sxs-lookup"><span data-stu-id="e7f90-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="e7f90-107">Die Methode " **verschlüsseln** " verschlüsselt einen Datenzeiger.</span><span class="sxs-lookup"><span data-stu-id="e7f90-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f90-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7f90-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="e7f90-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7f90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f90-110">*psecurechannel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7f90-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f90-111">Zeiger auf eine sichere Kanal Schnittstelle mit dem Datenzeiger, der verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7f90-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f90-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7f90-112">Return value</span></span>

<span data-ttu-id="e7f90-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="e7f90-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7f90-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e7f90-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7f90-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e7f90-115">Return code</span></span>                                                                          | <span data-ttu-id="e7f90-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7f90-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7f90-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7f90-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7f90-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7f90-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7f90-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7f90-119">Remarks</span></span>

<span data-ttu-id="e7f90-120">Verwenden Sie diese Methode, um Datenzeiger zu verschlüsseln, damit Sie über dll-Grenzen hinweg gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e7f90-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f90-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7f90-121">Requirements</span></span>



| <span data-ttu-id="e7f90-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7f90-122">Requirement</span></span> | <span data-ttu-id="e7f90-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e7f90-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f90-124">Header</span><span class="sxs-lookup"><span data-stu-id="e7f90-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e7f90-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f90-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7f90-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7f90-126">Library</span></span><br/> | <dl> <span data-ttu-id="e7f90-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f90-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f90-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7f90-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f90-129">**Entschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="e7f90-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="e7f90-130">**Iwmsecurebuffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e7f90-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





