---
description: Berechnet einen Hash, der während der Zertifikat Authentifizierung verwendet werden soll.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Sslcomputeclientauthhash-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215555"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="a2a6d-103">Sslcomputeclientauthhash-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2a6d-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="a2a6d-104">Die **sslcomputeclientauthhash** -Funktion berechnet einen [*Hash*](/windows/desktop/SecGloss/h-gly) , der während der [*Zertifikat*](/windows/desktop/SecGloss/c-gly) Authentifizierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2a6d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a2a6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2a6d-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-108">Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="a2a6d-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-109">*hmasterkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-110">Das Handle des [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekts.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-111">*hhandshakehash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-112">Das Handle des Hashwerts des bisher berechneten Handshakes.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-113">*pszalgid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-114">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den angeforderten [*Kryptografiealgorithmus*](/windows/desktop/SecGloss/c-gly)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="a2a6d-115">Hierbei kann es sich um einen der Standard- [**CNG-Algorithmus**](cng-algorithm-identifiers.md) -IDs oder den Bezeichner für einen anderen registrierten Algorithmus handeln.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-116">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-117">Die Adresse eines Puffers, der das [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly)empfängt.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="a2a6d-118">Der *cboutput* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="a2a6d-119">Wenn dieser Parameter **null** ist, fügt diese Funktion die erforderliche Größe (in Bytes) in das **DWORD** ein, auf das durch den *pcbresult* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-120">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-121">Die Länge des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-122">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-123">Ein Zeiger auf einen **DWORD** -Wert, der die Länge des in den *pboutput* -Puffer geschriebenen Hashs in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a2a6d-124">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a6d-125">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2a6d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2a6d-126">Return value</span></span>

<span data-ttu-id="a2a6d-127">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a2a6d-128">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a2a6d-129">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="a2a6d-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a2a6d-130">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a2a6d-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="a2a6d-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2a6d-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a2a6d-132"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="a2a6d-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="a2a6d-133">Eines der angegebenen Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2a6d-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2a6d-134">Remarks</span></span>

<span data-ttu-id="a2a6d-135">Die **sslcomputeclientauthhash** -Funktion berechnet den Hash, der in der Zertifikat Überprüfungs Nachricht des SSL-Handshakes gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="a2a6d-136">Der Hashwert wird berechnet, indem ein Hashwert erstellt wird, der den geheimen Hauptschlüssel mit einem Hash aller zuvor gesendeten oder empfangenen Hand Shake Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="a2a6d-137">Weitere Informationen zur SSL-Handshake-Sequenz finden Sie unter [Beschreibung des Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="a2a6d-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="a2a6d-138">Die Art und Weise, in der der Hashwert berechnet wird, hängt vom verwendeten Protokoll und der verwendeten Verschlüsselungs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="a2a6d-139">Außerdem hängt der Hash vom Typ des verwendeten Client Authentifizierungs Schlüssels ab. der *pszalgid* -Parameter gibt den Schlüsseltyp an, der für die Client Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2a6d-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a6d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2a6d-140">Requirements</span></span>



| <span data-ttu-id="a2a6d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2a6d-141">Requirement</span></span> | <span data-ttu-id="a2a6d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="a2a6d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a6d-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2a6d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a6d-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2a6d-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2a6d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a6d-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2a6d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a2a6d-147">Header</span><span class="sxs-lookup"><span data-stu-id="a2a6d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a6d-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a6d-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a2a6d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a2a6d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2a6d-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2a6d-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

