---
description: Öffnet ein Handle für einen privaten Schlüssel.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Sslopenprivatekey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128804"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="5b182-103">Sslopenprivatekey-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b182-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="5b182-104">Die **sslopenprivatekey** -Funktion öffnet ein Handle für einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="5b182-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b182-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b182-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5b182-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b182-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b182-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b182-108">Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5b182-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5b182-109">*phprivatekey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5b182-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b182-110">Die Adresse eines Puffers, in den das Handle in den privaten Schlüssel geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b182-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="5b182-111">Wenn Sie die Verwendung des Schlüssels abgeschlossen haben, sollten Sie " *phprivatekey* " freigeben, indem Sie die [**sslfreeobject**](sslfreeobject.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5b182-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5b182-112">*pcertcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b182-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b182-113">Die Adresse des Zertifikats, aus dem der private Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b182-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="5b182-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b182-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b182-115">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5b182-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b182-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b182-116">Return value</span></span>

<span data-ttu-id="5b182-117">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5b182-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5b182-118">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5b182-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5b182-119">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5b182-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5b182-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5b182-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5b182-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b182-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b182-122"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="5b182-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="5b182-123">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5b182-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="5b182-124"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="5b182-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="5b182-125">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5b182-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="5b182-126"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="5b182-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5b182-127">Der Parameter " *phprivatekey* " oder " *pcertcontext* " ist **null**.</span><span class="sxs-lookup"><span data-stu-id="5b182-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="5b182-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b182-128">Remarks</span></span>

<span data-ttu-id="5b182-129">Der erhaltene private Schlüssel ist Teil eines [*öffentlichen/privaten Schlüssel Paars*](/windows/desktop/SecGloss/p-gly) innerhalb eines [*Zertifikats*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="5b182-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="5b182-130">Diese Funktion extrahiert lediglich den privaten Schlüssel aus dem Zertifikat, das durch den *pcertcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b182-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b182-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b182-131">Requirements</span></span>



| <span data-ttu-id="5b182-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b182-132">Requirement</span></span> | <span data-ttu-id="5b182-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5b182-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b182-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b182-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5b182-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b182-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b182-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b182-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5b182-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b182-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b182-138">Header</span><span class="sxs-lookup"><span data-stu-id="5b182-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b182-139"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b182-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5b182-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5b182-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b182-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b182-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

