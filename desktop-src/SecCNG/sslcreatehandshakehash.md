---
description: Ruft ein Hashhandle ab, das zum Hashen von Hand Shake Nachrichten verwendet wird.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Sslkreatehandshakehash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356663"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="5d98e-103">Sslkreatehandshakehash-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d98e-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="5d98e-104">Die **sslkreatehandshakehash** -Funktion Ruft ein Hashhandle ab, das zum Hashen von Hand Shake Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d98e-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d98e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d98e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5d98e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d98e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d98e-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d98e-108">Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5d98e-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5d98e-109">*phhandshakehash* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d98e-110">Ein Hash handle, das an andere SSL-Anbieter Funktionen übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5d98e-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="5d98e-111">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d98e-112">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5d98e-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="5d98e-113">Diese Funktion wird nicht mit dem SSL 2,0-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d98e-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="5d98e-114">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d98e-115">Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5d98e-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5d98e-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d98e-117">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5d98e-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d98e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d98e-118">Return value</span></span>

<span data-ttu-id="5d98e-119">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5d98e-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5d98e-120">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d98e-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5d98e-121">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5d98e-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5d98e-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5d98e-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5d98e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d98e-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d98e-124"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="5d98e-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="5d98e-125">Zum Zuordnen des Hash Puffers ist nicht genügend Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d98e-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="5d98e-126"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="5d98e-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="5d98e-127">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5d98e-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="5d98e-128"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="5d98e-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5d98e-129">Der *phhandshakehash* ist NULL.</span><span class="sxs-lookup"><span data-stu-id="5d98e-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="5d98e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d98e-130">Remarks</span></span>

<span data-ttu-id="5d98e-131">Die **sslkreatehandshakehash** -Funktion ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshakes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d98e-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="5d98e-132">Die **sslkreatehandshakehash** -Funktion wird aufgerufen, um ein Hashhandle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d98e-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="5d98e-133">Die [**sslhashhandshake**](sslhashhandshake.md) -Funktion wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5d98e-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="5d98e-134">Die [**sslcomputefinishedhash**](sslcomputefinishedhash.md) -Funktion wird mit dem Hashhandle aufgerufen, um den Digest der Hash Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5d98e-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d98e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d98e-135">Requirements</span></span>



| <span data-ttu-id="5d98e-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d98e-136">Requirement</span></span> | <span data-ttu-id="5d98e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5d98e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d98e-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d98e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5d98e-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d98e-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d98e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5d98e-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d98e-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d98e-142">Header</span><span class="sxs-lookup"><span data-stu-id="5d98e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d98e-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d98e-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5d98e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5d98e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d98e-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d98e-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

