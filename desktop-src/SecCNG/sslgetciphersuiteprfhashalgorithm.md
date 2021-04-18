---
description: 'Gibt den CNG-Algorithmusbezeichner (Cryptography API: Next Generation) des Hash Algorithmus zurück, der für das Eingabe Protokoll, die Verschlüsselungs Sammlung und den Schlüsseltyp für die Pseudo Zufallsfunktion (Transport Layer Security Protocol) verwendet wird.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Sslgetciphersuiteprf HashAlgorithm-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354869"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="c49b3-103">Sslgetciphersuiteprf HashAlgorithm-Funktion</span><span class="sxs-lookup"><span data-stu-id="c49b3-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="c49b3-104">Die **sslgetciphersuiteprf HashAlgorithm** -Funktion gibt den CNG-Algorithmus (Cryptography API: Next Generation) des [*Hash Algorithmus*](/windows/desktop/SecGloss/h-gly) zurück, der für das Eingabe Protokoll, die Verschlüsselungs Sammlung und den Schlüsseltyp für die " [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*Pseudo Random Function*](/windows/desktop/SecGloss/p-gly) (PRF)" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c49b3-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c49b3-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c49b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c49b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c49b3-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49b3-108">Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="c49b3-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c49b3-109">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49b3-110">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c49b3-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c49b3-111">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49b3-112">Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c49b3-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c49b3-113">*dwkeytype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49b3-114">Einer der [**Schlüsseltyp-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c49b3-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="c49b3-115">Legen Sie für Schlüsseltypen, bei denen es sich nicht um eine [*Kryptographie*](/windows/desktop/SecGloss/e-gly) (ECC) handelt, diesen Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="c49b3-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c49b3-116">*szprf Hash* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c49b3-117">Einer der [**CNG-Algorithmusbezeichner**](cng-algorithm-identifiers.md) für den Hash, der für die TLS-PRF verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c49b3-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="c49b3-118">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49b3-119">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c49b3-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c49b3-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c49b3-120">Return value</span></span>

<span data-ttu-id="c49b3-121">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c49b3-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c49b3-122">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c49b3-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c49b3-123">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="c49b3-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c49b3-124">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c49b3-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c49b3-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c49b3-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c49b3-126"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="c49b3-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="c49b3-127">Der *hsslprovider* -Parameter enthält einen ungültigen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c49b3-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="c49b3-128"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="c49b3-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="c49b3-129">Der *szprfhash* -Parameter ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c49b3-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="c49b3-130"><dt>**Ernte \_ Nicht \_ unterstützt**</dt> <dt>0x80090029l</dt></span><span class="sxs-lookup"><span data-stu-id="c49b3-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="c49b3-131">Die ausgewählte Funktion wird in der angegebenen Version der Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c49b3-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="c49b3-132"><dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt></span><span class="sxs-lookup"><span data-stu-id="c49b3-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="c49b3-133">Der *dwFlags* -Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c49b3-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="c49b3-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c49b3-134">Remarks</span></span>

<span data-ttu-id="c49b3-135">Diese **sslgetciphersuiteprfhashalgorithm** -Funktion wird für die Konversationen von TLS 1,2 oder höher aufgerufen, um den Hash Algorithmus abzufragen, der in der TLS-PRF verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c49b3-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49b3-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c49b3-136">Requirements</span></span>



| <span data-ttu-id="c49b3-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c49b3-137">Requirement</span></span> | <span data-ttu-id="c49b3-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c49b3-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49b3-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c49b3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c49b3-140">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c49b3-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c49b3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c49b3-142">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c49b3-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c49b3-143">Header</span><span class="sxs-lookup"><span data-stu-id="c49b3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c49b3-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c49b3-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c49b3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c49b3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c49b3-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c49b3-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

