---
description: Ruft die XML-Daten (über das Netzwerk gesendet) ab, die das Token darstellen.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Iupdateendpointauthtoken:: tokendata-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350463"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="31ff5-103">Iupdateendpointauthtoken:: tokendata-Methode</span><span class="sxs-lookup"><span data-stu-id="31ff5-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="31ff5-104">Ruft die XML-Daten (über das Netzwerk gesendet) ab, die das Token darstellen.</span><span class="sxs-lookup"><span data-stu-id="31ff5-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ff5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31ff5-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="31ff5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ff5-107">*pszumkendata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="31ff5-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ff5-108">Die über das Netzwerk gesendeten XML-Daten, die das Token darstellen.</span><span class="sxs-lookup"><span data-stu-id="31ff5-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="31ff5-109">Beispielsweise ist die Daten für ein WS-Security SAML-Token (Security Assertion Markup Language) 1,1 der SAML-Code, der der Anforderung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="31ff5-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ff5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31ff5-110">Return value</span></span>

<span data-ttu-id="31ff5-111">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="31ff5-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="31ff5-112">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31ff5-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ff5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31ff5-113">Requirements</span></span>



| <span data-ttu-id="31ff5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31ff5-114">Requirement</span></span> | <span data-ttu-id="31ff5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="31ff5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ff5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31ff5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="31ff5-117">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31ff5-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="31ff5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31ff5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="31ff5-119">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31ff5-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="31ff5-120">Header</span><span class="sxs-lookup"><span data-stu-id="31ff5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ff5-121"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ff5-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="31ff5-122">IDL</span><span class="sxs-lookup"><span data-stu-id="31ff5-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31ff5-123"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31ff5-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="31ff5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31ff5-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="31ff5-125"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ff5-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="31ff5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="31ff5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ff5-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ff5-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31ff5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31ff5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ff5-129">**Iupdateendpointauthtoken**</span><span class="sxs-lookup"><span data-stu-id="31ff5-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




