---
description: Berechnet den Hash, der in der abgeschlossenen Nachricht des SSL-Handshakes (Secure Sockets Layer Protocol) gesendet wurde.
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Sslcomputefinishedhash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959433"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="2f70e-103">Sslcomputefinishedhash-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f70e-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="2f70e-104">Die **sslcomputefinishedhash** -Funktion berechnet den [*Hash*](/windows/desktop/SecGloss/h-gly) , der in der fertigen Nachricht des SSL-Handshakes ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2f70e-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="2f70e-105">Weitere Informationen zur SSL-Handshake-Sequenz finden Sie unter [Beschreibung des Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="2f70e-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f70e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f70e-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2f70e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f70e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f70e-108">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f70e-109">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="2f70e-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="2f70e-110">*hmasterkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f70e-111">Das Handle des [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekts.</span><span class="sxs-lookup"><span data-stu-id="2f70e-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="2f70e-112">*hhandshakehash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f70e-113">Das Handle des Hashs der Handshake-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="2f70e-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="2f70e-114">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f70e-115">Ein Zeiger auf einen Puffer, der den Hash für die Abschluss Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="2f70e-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="2f70e-116">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f70e-117">Die Länge des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2f70e-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2f70e-118">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f70e-119">Eine der folgenden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="2f70e-119">One of the following constants.</span></span>



| <span data-ttu-id="2f70e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2f70e-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="2f70e-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2f70e-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="2f70e-122"><dt>**NCrypt \_ SSL \_ - \_ clientflag**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2f70e-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2f70e-123">Gibt an, dass es sich um einen Client Befehl handelt.</span><span class="sxs-lookup"><span data-stu-id="2f70e-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="2f70e-124"><dt>**NCrypt \_ SSL \_ - \_ Serverflag**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2f70e-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="2f70e-125">Gibt an, dass es sich um einen Server-Rückruf handelt</span><span class="sxs-lookup"><span data-stu-id="2f70e-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f70e-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f70e-126">Return value</span></span>

<span data-ttu-id="2f70e-127">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="2f70e-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="2f70e-128">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f70e-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="2f70e-129">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2f70e-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="2f70e-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f70e-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2f70e-131"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>2148073510 (0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="2f70e-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="2f70e-132">Eines der angegebenen Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2f70e-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f70e-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f70e-133">Remarks</span></span>

<span data-ttu-id="2f70e-134">Die **sslcomputefinishedhash** -Funktion ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshake verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f70e-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="2f70e-135">Die [**sslkreatehandshakehash**](sslcreatehandshakehash.md) -Funktion wird aufgerufen, um ein Hashhandle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2f70e-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="2f70e-136">Die [**sslhashhandshake**](sslhashhandshake.md) -Funktion wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2f70e-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="2f70e-137">Die **sslcomputefinishedhash** -Funktion wird mit dem Hashhandle aufgerufen, um den Digest der Hash Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f70e-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="2f70e-138">Der Hashwert wird berechnet, indem ein Hashwert für den geheimen Hauptschlüssel mit einem Hash aller vorherigen gesendeten oder empfangenen Hand Shake Nachrichten vorliegt.</span><span class="sxs-lookup"><span data-stu-id="2f70e-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="2f70e-139">Der Wert von *cboutput* bestimmt die Länge der Hashdaten.</span><span class="sxs-lookup"><span data-stu-id="2f70e-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="2f70e-140">Wenn das Protokoll " [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,0" verwendet wird, sollte dies immer "12 (Bytes)" lauten.</span><span class="sxs-lookup"><span data-stu-id="2f70e-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="2f70e-141">Weitere Informationen finden Sie in [der TLS-Protokoll Version 1,0](https://www.ietf.org/rfc/rfc2246.txt).</span><span class="sxs-lookup"><span data-stu-id="2f70e-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f70e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f70e-142">Requirements</span></span>



| <span data-ttu-id="2f70e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f70e-143">Requirement</span></span> | <span data-ttu-id="2f70e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="2f70e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f70e-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f70e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2f70e-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f70e-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f70e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2f70e-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f70e-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f70e-149">Header</span><span class="sxs-lookup"><span data-stu-id="2f70e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f70e-150"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f70e-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="2f70e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2f70e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f70e-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f70e-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

