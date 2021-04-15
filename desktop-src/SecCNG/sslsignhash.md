---
description: Signiert einen Hash mit dem angegebenen privaten Schlüssel.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Sslsignhash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484627"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="21ace-103">Sslsignhash-Funktion</span><span class="sxs-lookup"><span data-stu-id="21ace-103">SslSignHash function</span></span>

<span data-ttu-id="21ace-104">Die **sslsignhash** -Funktion signiert einen [*Hash*](/windows/desktop/SecGloss/h-gly) mit dem angegebenen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="21ace-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="21ace-105">Der Signatur Prozess wird auf dem Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21ace-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ace-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="21ace-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="21ace-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="21ace-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ace-108">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ace-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-109">Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="21ace-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-110">*hprivatekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ace-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-111">Das Handle für den privaten Schlüssel, der zum Signieren des Hashwerts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21ace-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-112">*pbHashValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ace-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-113">Ein Zeiger auf einen Puffer, der den zu Signier nden Hash enthält.</span><span class="sxs-lookup"><span data-stu-id="21ace-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-114">*cbhashwert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ace-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-115">Die Größe des *pbHashValue* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="21ace-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-116">*pbSignature* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21ace-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-117">Die Adresse eines Puffers, der die Signatur des Hashwerts empfängt.</span><span class="sxs-lookup"><span data-stu-id="21ace-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="21ace-118">Der *cbsignature* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="21ace-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="21ace-119">Legen Sie den *pbSignature* -Parameter auf **null** fest, um die erforderliche Größe des Puffers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="21ace-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="21ace-120">Die erforderliche Größe des Puffers wird im *pcbresult* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21ace-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-121">*cbsignature* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ace-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-122">Die Größe des *pbSignature* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="21ace-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-123">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21ace-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-124">Ein Zeiger auf einen Wert, der nach Abschluss die tatsächliche Anzahl der in den *pbSignature* -Puffer geschriebenen Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="21ace-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="21ace-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ace-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ace-126">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="21ace-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ace-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21ace-127">Return value</span></span>

<span data-ttu-id="21ace-128">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="21ace-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="21ace-129">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21ace-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="21ace-130">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="21ace-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="21ace-131">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="21ace-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="21ace-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21ace-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="21ace-133"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="21ace-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="21ace-134">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="21ace-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21ace-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21ace-135">Requirements</span></span>



| <span data-ttu-id="21ace-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21ace-136">Requirement</span></span> | <span data-ttu-id="21ace-137">Wert</span><span class="sxs-lookup"><span data-stu-id="21ace-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21ace-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21ace-138">Minimum supported client</span></span><br/> | <span data-ttu-id="21ace-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21ace-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="21ace-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21ace-140">Minimum supported server</span></span><br/> | <span data-ttu-id="21ace-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21ace-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="21ace-142">Header</span><span class="sxs-lookup"><span data-stu-id="21ace-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="21ace-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="21ace-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="21ace-144">DLL</span><span class="sxs-lookup"><span data-stu-id="21ace-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21ace-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ace-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

