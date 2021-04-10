---
description: Überprüft die angegebene Signatur mit dem angegebenen Hash und dem öffentlichen Schlüssel.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Sslverifysignature-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862323"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="97873-103">Sslverifysignature-Funktion</span><span class="sxs-lookup"><span data-stu-id="97873-103">SslVerifySignature function</span></span>

<span data-ttu-id="97873-104">Die **sslverifysignature** -Funktion überprüft die angegebene Signatur mit dem angegebenen [*Hash*](/windows/desktop/SecGloss/h-gly) und dem [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="97873-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="97873-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97873-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="97873-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97873-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-108">Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="97873-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="97873-109">*hpublickey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-110">Das Handle für den öffentlichen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="97873-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="97873-111">*pbHashValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-112">Ein Zeiger auf einen Puffer, der den Hash enthält, der zum Überprüfen der Signatur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97873-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="97873-113">*cbhashwert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-114">Die Größe des *pbHashValue* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="97873-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="97873-115">*pbSignature* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-116">Ein Zeiger auf einen Puffer, der die zu überprüfende Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="97873-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="97873-117">*cbsignature* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-118">Die Größe des *pbSignature* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="97873-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="97873-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97873-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97873-120">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="97873-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97873-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97873-121">Return value</span></span>

<span data-ttu-id="97873-122">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="97873-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="97873-123">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97873-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="97873-124">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="97873-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="97873-125">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="97873-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="97873-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97873-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="97873-127"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="97873-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="97873-128">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="97873-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97873-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97873-129">Remarks</span></span>

<span data-ttu-id="97873-130">Die **sslverifysignature** -Funktion wird derzeit nicht von Windows aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="97873-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="97873-131">Diese Funktion ist ein erforderlicher Bestandteil der SSL-Anbieter Schnittstelle und sollte vollständig implementiert werden, um die Vorwärtskompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="97873-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="97873-132">Die aktuellen Implementierungen der Serverseite der TLS-Verbindung ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) aufrufen die [**ncryptverifysignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) -Funktion während der Client Authentifizierung, um die Zertifikat Verifizierungs Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="97873-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="97873-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97873-133">Requirements</span></span>



| <span data-ttu-id="97873-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97873-134">Requirement</span></span> | <span data-ttu-id="97873-135">Wert</span><span class="sxs-lookup"><span data-stu-id="97873-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97873-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97873-136">Minimum supported client</span></span><br/> | <span data-ttu-id="97873-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97873-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97873-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97873-138">Minimum supported server</span></span><br/> | <span data-ttu-id="97873-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97873-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="97873-140">Header</span><span class="sxs-lookup"><span data-stu-id="97873-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="97873-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="97873-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="97873-142">DLL</span><span class="sxs-lookup"><span data-stu-id="97873-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97873-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97873-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

