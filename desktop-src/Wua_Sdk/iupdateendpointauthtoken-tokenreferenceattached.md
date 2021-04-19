---
description: Ruft das XML-Format eines angefügten Verweises auf das Token ab.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Iupdateendpointauthtoken:: tokenreferenceattached-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350462"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a><span data-ttu-id="d597f-103">Iupdateendpointauthtoken:: tokenreferenceattached-Methode</span><span class="sxs-lookup"><span data-stu-id="d597f-103">IUpdateEndpointAuthToken::TokenReferenceAttached method</span></span>

<span data-ttu-id="d597f-104">Ruft das XML-Format eines angefügten Verweises auf das Token ab.</span><span class="sxs-lookup"><span data-stu-id="d597f-104">Gets the XML format of an attached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="d597f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d597f-105">Syntax</span></span>


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="d597f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d597f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d597f-107">*psztokenreference* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d597f-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d597f-108">Zeiger auf den Verweis auf ein angefügtes Token.</span><span class="sxs-lookup"><span data-stu-id="d597f-108">Pointer to the attached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d597f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d597f-109">Return value</span></span>

<span data-ttu-id="d597f-110">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d597f-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="d597f-111">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d597f-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d597f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d597f-112">Remarks</span></span>

<span data-ttu-id="d597f-113">Ein angefügter Verweis verweist auf eine referenece (z. b. das Zeichen, das das Token verwendet), das sich in derselben Nachricht befindet, in der sich das Token befindet.</span><span class="sxs-lookup"><span data-stu-id="d597f-113">An attached reference refers a referece (such as the signiture that is using the token) that is in the same message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="d597f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d597f-114">Requirements</span></span>



| <span data-ttu-id="d597f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d597f-115">Requirement</span></span> | <span data-ttu-id="d597f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d597f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d597f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d597f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d597f-118">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d597f-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="d597f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d597f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d597f-120">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d597f-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d597f-121">Header</span><span class="sxs-lookup"><span data-stu-id="d597f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d597f-122"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="d597f-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="d597f-123">IDL</span><span class="sxs-lookup"><span data-stu-id="d597f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d597f-124"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d597f-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="d597f-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d597f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d597f-126"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d597f-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="d597f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d597f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d597f-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d597f-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d597f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d597f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d597f-130">**Iupdateendpointauthtoken**</span><span class="sxs-lookup"><span data-stu-id="d597f-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




