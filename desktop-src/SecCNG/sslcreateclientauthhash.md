---
description: Ruft ein Handle für den Handshake-Hash ab, der für die Client Authentifizierung verwendet wird.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Sslkreateclientauthhash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345894"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="6da13-103">Sslkreateclientauthhash-Funktion</span><span class="sxs-lookup"><span data-stu-id="6da13-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="6da13-104">Die **sslkreateclientauthhash** -Funktion Ruft ein Handle für den Handshake- [*Hash*](/windows/desktop/SecGloss/h-gly) ab, der für die Client Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6da13-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da13-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6da13-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6da13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6da13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da13-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da13-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da13-108">Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="6da13-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="6da13-109">*phhandshakehash* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6da13-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6da13-110">Ein Zeiger auf eine **NCrypt- \_ Hash \_ handle** -Variable, um das Hashhandle zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="6da13-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="6da13-111">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da13-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da13-112">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6da13-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="6da13-113">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da13-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da13-114">Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6da13-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="6da13-115">*pszhashalgid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da13-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da13-116">Einer der [**CNG-Algorithmus-Bezeichner**](cng-algorithm-identifiers.md) Werte.</span><span class="sxs-lookup"><span data-stu-id="6da13-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="6da13-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da13-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da13-118">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6da13-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da13-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6da13-119">Return value</span></span>

<span data-ttu-id="6da13-120">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="6da13-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6da13-121">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6da13-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6da13-122">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="6da13-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6da13-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6da13-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="6da13-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6da13-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6da13-125"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="6da13-126">Der *hsslprovider* -Parameter enthält einen ungültigen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6da13-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="6da13-127"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="6da13-128">Der Parameter " *phhandshakehash* " ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6da13-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="6da13-129"><dt>**Ernte \_ Nicht \_ unterstützt**</dt> <dt>0x80090029l</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="6da13-130">Die ausgewählte Funktion wird in der angegebenen Version der Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6da13-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="6da13-131"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="6da13-132">Nicht genügend Arbeitsspeicher zum Zuordnen von Puffern.</span><span class="sxs-lookup"><span data-stu-id="6da13-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="6da13-133"><dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="6da13-134">Der *dwFlags* -Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6da13-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="6da13-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6da13-135">Remarks</span></span>

<span data-ttu-id="6da13-136">Die **sslkreateclientauthhash** -Funktion wird für die Konversationen von [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,2 oder höher aufgerufen, um Hash Objekte zu erstellen, die zum Hashen von Hand Shake Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6da13-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="6da13-137">Sie wird einmal für jeden möglichen [*Hash Algorithmus*](/windows/desktop/SecGloss/h-gly) aufgerufen, der in der Client Authentifizierungs Signatur verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6da13-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="6da13-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6da13-138">Requirements</span></span>



| <span data-ttu-id="6da13-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6da13-139">Requirement</span></span> | <span data-ttu-id="6da13-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6da13-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da13-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6da13-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6da13-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6da13-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6da13-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6da13-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6da13-144">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6da13-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6da13-145">Header</span><span class="sxs-lookup"><span data-stu-id="6da13-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6da13-146"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6da13-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6da13-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da13-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da13-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

