---
description: Ruft den Typ des Endpunkt Tokens ab, z. b. ein WS-Security SAML-Token (Security Assertion Markup Language) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'Iupdateendpointauthtoken:: TokenType-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526678"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="7c729-103">Iupdateendpointauthtoken:: TokenType-Methode</span><span class="sxs-lookup"><span data-stu-id="7c729-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="7c729-104">Ruft den Typ des Endpunkt Tokens ab, z. b. ein WS-Security SAML-Token (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="7c729-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c729-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c729-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="7c729-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c729-107">" *ptokentype* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c729-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c729-108">Der Typ des Endpunkt Tokens.</span><span class="sxs-lookup"><span data-stu-id="7c729-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c729-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c729-109">Return value</span></span>

<span data-ttu-id="7c729-110">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7c729-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="7c729-111">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c729-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c729-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c729-112">Requirements</span></span>



| <span data-ttu-id="7c729-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c729-113">Requirement</span></span> | <span data-ttu-id="7c729-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7c729-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c729-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c729-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7c729-116">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c729-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="7c729-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c729-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7c729-118">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c729-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="7c729-119">Header</span><span class="sxs-lookup"><span data-stu-id="7c729-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c729-120"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c729-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c729-121">IDL</span><span class="sxs-lookup"><span data-stu-id="7c729-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c729-122"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c729-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c729-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c729-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c729-124"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c729-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c729-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7c729-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c729-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c729-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c729-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c729-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c729-128">**Iupdateendpointauthtoken**</span><span class="sxs-lookup"><span data-stu-id="7c729-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




