---
description: Berechnet den geheimen Hauptschlüssel des Secure Sockets Layer Protokolls (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Sslgeneratemasterkey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393806"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="0b24a-103">Sslgeneratemasterkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="0b24a-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="0b24a-104">Die **sslgeneratemasterkey** -Funktion berechnet den geheimen Hauptschlüssel des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="0b24a-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b24a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b24a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0b24a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b24a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b24a-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-108">Das Handle für die SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="0b24a-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-109">*hprivatekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-110">Das Handle für den [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) , der im Austausch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b24a-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-111">*hpublickey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-112">Das Handle für den [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) , der im Austausch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b24a-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-113">*phmasterkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-114">Ein Zeiger auf das Handle des generierten [*Haupt Schlüssels*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="0b24a-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-115">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-116">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="0b24a-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-117">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-118">Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="0b24a-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-119">*pparameterlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-120">Ein Zeiger auf ein Array von [**ncryptbuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) -Puffern, die Informationen enthalten, die als Teil des Schlüsselaustausch Vorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b24a-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="0b24a-121">Der genaue Satz Puffer ist abhängig vom verwendeten Protokoll und der Verschlüsselungs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0b24a-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="0b24a-122">Die Liste enthält mindestens Puffer, die den vom Client und vom Server bereitgestellten Zufallswert enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b24a-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-123">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-124">Die Adresse eines Puffers, der den geheimen Hauptschlüssel empfängt, der mit dem öffentlichen Schlüssel des Servers verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="0b24a-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="0b24a-125">Der *cboutput* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="0b24a-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="0b24a-126">Wenn dieser Parameter **null** ist, gibt diese Funktion die erforderliche Größe in Byte in dem **DWORD** -Element zurück, auf das durch den *pcbresult* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0b24a-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="0b24a-127">Dieser Puffer wird verwendet, wenn ein RSA-Schlüsselaustausch durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b24a-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="0b24a-128">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-129">Die Größe des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0b24a-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-130">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-131">Ein Zeiger auf einen **DWORD** -Wert, in den die Anzahl der in den *pboutput* -Puffer geschriebenen Bytes aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b24a-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0b24a-132">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b24a-133">Gibt an, ob diese Funktion für den Client seitigen oder serverseitigen Schlüsselaustausch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b24a-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="0b24a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0b24a-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="0b24a-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b24a-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="0b24a-136"><dt>**NCrypt \_ SSL \_ - \_ clientflag**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0b24a-137">Gibt einen Client seitigen Schlüsselaustausch an.</span><span class="sxs-lookup"><span data-stu-id="0b24a-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="0b24a-138"><dt>**NCrypt \_ SSL \_ - \_ Serverflag**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="0b24a-139">Gibt einen serverseitigen Schlüsselaustausch an.</span><span class="sxs-lookup"><span data-stu-id="0b24a-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b24a-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b24a-140">Return value</span></span>

<span data-ttu-id="0b24a-141">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="0b24a-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="0b24a-142">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b24a-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="0b24a-143">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="0b24a-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0b24a-144">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0b24a-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="0b24a-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b24a-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b24a-146"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="0b24a-147">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0b24a-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="0b24a-148"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="0b24a-149">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0b24a-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="0b24a-150"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="0b24a-151">Der Parameter " *phmasterkey* " oder " *hpublickey* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0b24a-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="0b24a-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b24a-152">Requirements</span></span>



| <span data-ttu-id="0b24a-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b24a-153">Requirement</span></span> | <span data-ttu-id="0b24a-154">Wert</span><span class="sxs-lookup"><span data-stu-id="0b24a-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b24a-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b24a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0b24a-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0b24a-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b24a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0b24a-158">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b24a-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0b24a-159">Header</span><span class="sxs-lookup"><span data-stu-id="0b24a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b24a-160"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="0b24a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="0b24a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b24a-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b24a-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

