---
description: Führt einen SSL-Schlüsselaustausch Vorgang (Server Side Secure Sockets Layer Protocol) aus.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Sslimportmasterkey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362462"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="c5325-103">Sslimportmasterkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5325-103">SslImportMasterKey function</span></span>

<span data-ttu-id="c5325-104">Die **sslimportmasterkey** -Funktion führt einen serverseitigen [*Secure Sockets Layer Protokoll*](/windows/desktop/SecGloss/s-gly) (SSL)-Schlüsselaustausch Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="c5325-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5325-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5325-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c5325-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5325-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-108">Das Handle für die SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="c5325-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-109">*hprivatekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-110">Das Handle für den [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) , der im Austausch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5325-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-111">*phmasterkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5325-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-112">Ein Zeiger auf das Handle, um den [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly)zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c5325-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="c5325-113">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-114">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5325-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-115">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-116">Einer der [**Cipher Suite-Bezeichner Werte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5325-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-117">*pparameterlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-118">Ein Zeiger auf ein Array von [**ncryptbuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) -Puffern, die Informationen enthalten, die als Teil des Schlüsselaustausch Vorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5325-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="c5325-119">Der genaue Satz Puffer ist abhängig vom verwendeten Protokoll und der Verschlüsselungs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="c5325-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="c5325-120">Die Liste enthält mindestens Puffer, die den vom Client und vom Server bereitgestellten Zufallswert enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5325-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-121">*pbencryptedkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-122">Ein Zeiger auf einen Puffer, der den verschlüsselten Schlüssel für den geheimen Hauptschlüssel enthält, der mit dem [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) des Servers verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="c5325-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-123">*cbencryptedkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-124">Die Größe des *pbencryptedkey* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c5325-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c5325-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5325-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5325-126">Legen Sie diesen Parameter auf das **NCrypt- \_ SSL- \_ \_ Serverflag** fest, um anzugeben, dass es sich um einen Server</span><span class="sxs-lookup"><span data-stu-id="c5325-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5325-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5325-127">Return value</span></span>

<span data-ttu-id="c5325-128">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c5325-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c5325-129">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5325-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c5325-130">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="c5325-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c5325-131">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c5325-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c5325-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5325-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5325-133"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="c5325-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="c5325-134">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c5325-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="c5325-135"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="c5325-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="c5325-136">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5325-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="c5325-137"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="c5325-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="c5325-138">Der *phmasterkey* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c5325-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="c5325-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5325-139">Remarks</span></span>

<span data-ttu-id="c5325-140">Diese Funktion entschlüsselt den geheimen Hauptschlüssel, berechnet den SSL-Hauptschlüssel und gibt ein Handle für dieses Objekt an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="c5325-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="c5325-141">Dieser Hauptschlüssel kann dann verwendet werden, um den SSL-Sitzungsschlüssel abzuleiten und den SSL-Handshake abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c5325-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="c5325-142">Diese Funktion wird verwendet, wenn der [*RSA*](/windows/desktop/SecGloss/r-gly) -Schlüsselaustausch Algorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5325-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="c5325-143">Wenn [*dh*](/windows/desktop/SecGloss/d-gly) verwendet wird, ruft der Servercode stattdessen [**sslgeneratemasterkey**](sslgeneratemasterkey.md) auf.</span><span class="sxs-lookup"><span data-stu-id="c5325-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5325-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5325-144">Requirements</span></span>



| <span data-ttu-id="c5325-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5325-145">Requirement</span></span> | <span data-ttu-id="c5325-146">Wert</span><span class="sxs-lookup"><span data-stu-id="c5325-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5325-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5325-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c5325-148">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5325-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5325-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5325-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c5325-150">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5325-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5325-151">Header</span><span class="sxs-lookup"><span data-stu-id="c5325-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5325-152"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5325-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c5325-153">DLL</span><span class="sxs-lookup"><span data-stu-id="c5325-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5325-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5325-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

