---
description: Ruft den Schlüssel ab, der zum Verschlüsseln der ausgehenden Nachrichten verwendet wird, die vom Token geschützt werden.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Iupdateendpointauthtoken:: SigningKey-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041785"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="baf65-103">Iupdateendpointauthtoken:: SigningKey-Methode</span><span class="sxs-lookup"><span data-stu-id="baf65-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="baf65-104">Ruft den Schlüssel ab, der zum Verschlüsseln der ausgehenden Nachrichten verwendet wird, die vom Token geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="baf65-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="baf65-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="baf65-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="baf65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf65-107">*pbkey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="baf65-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="baf65-108">Schlüssel, der zum Verschlüsseln der ausgehenden Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="baf65-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="baf65-109">*pcbkeysize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="baf65-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="baf65-110">Größe des Schlüssels, auf den durch den *pbkey* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="baf65-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf65-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baf65-111">Return value</span></span>

<span data-ttu-id="baf65-112">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="baf65-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="baf65-113">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="baf65-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="baf65-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baf65-114">Requirements</span></span>



| <span data-ttu-id="baf65-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baf65-115">Requirement</span></span> | <span data-ttu-id="baf65-116">Wert</span><span class="sxs-lookup"><span data-stu-id="baf65-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf65-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="baf65-117">Minimum supported client</span></span><br/> | <span data-ttu-id="baf65-118">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baf65-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="baf65-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="baf65-119">Minimum supported server</span></span><br/> | <span data-ttu-id="baf65-120">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baf65-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="baf65-121">Header</span><span class="sxs-lookup"><span data-stu-id="baf65-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="baf65-122"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="baf65-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="baf65-123">IDL</span><span class="sxs-lookup"><span data-stu-id="baf65-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="baf65-124"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="baf65-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="baf65-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="baf65-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="baf65-126"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="baf65-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="baf65-127">DLL</span><span class="sxs-lookup"><span data-stu-id="baf65-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baf65-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baf65-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baf65-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baf65-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf65-130">**Iupdateendpointauthtoken**</span><span class="sxs-lookup"><span data-stu-id="baf65-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




