---
description: Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Iupdateendpointauthtoken:: tokenreferenceunattached-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343325"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="6bbee-103">Iupdateendpointauthtoken:: tokenreferenceunattached-Methode</span><span class="sxs-lookup"><span data-stu-id="6bbee-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="6bbee-104">Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.</span><span class="sxs-lookup"><span data-stu-id="6bbee-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bbee-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="6bbee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bbee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bbee-107">*psztokenreference* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6bbee-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbee-108">Zeiger auf den nicht angefügten Tokenverweis.</span><span class="sxs-lookup"><span data-stu-id="6bbee-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bbee-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bbee-109">Return value</span></span>

<span data-ttu-id="6bbee-110">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6bbee-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="6bbee-111">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6bbee-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bbee-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bbee-112">Remarks</span></span>

<span data-ttu-id="6bbee-113">Ein nicht angefügter Verweis verweist auf eine referenece (z. b. das Zeichen, das das Token verwendet), das nicht in der Nachricht, in der sich das Token befindet, befindet.</span><span class="sxs-lookup"><span data-stu-id="6bbee-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bbee-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bbee-114">Requirements</span></span>



| <span data-ttu-id="6bbee-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bbee-115">Requirement</span></span> | <span data-ttu-id="6bbee-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6bbee-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbee-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bbee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6bbee-118">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bbee-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="6bbee-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bbee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6bbee-120">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bbee-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6bbee-121">Header</span><span class="sxs-lookup"><span data-stu-id="6bbee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bbee-122"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bbee-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6bbee-123">IDL</span><span class="sxs-lookup"><span data-stu-id="6bbee-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6bbee-124"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6bbee-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="6bbee-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6bbee-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bbee-126"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bbee-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="6bbee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6bbee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bbee-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bbee-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bbee-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bbee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbee-130">**Iupdateendpointauthtoken**</span><span class="sxs-lookup"><span data-stu-id="6bbee-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




