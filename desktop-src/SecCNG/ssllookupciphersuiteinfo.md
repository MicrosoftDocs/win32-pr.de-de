---
description: Ruft die Chiffre Sammlungs Informationen für ein angegebenes Protokoll, eine Verschlüsselungs Sammlung und einen Schlüsseltyp Satz ab.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Ssllookupciphersuiteinfo-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869016"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="47e93-103">Ssllookupciphersuiteinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="47e93-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="47e93-104">Die **ssllookupciphersuiteinfo** -Funktion Ruft die Chiffre Sammlungs Informationen für ein angegebenes Protokoll, eine Verschlüsselungs Sammlung und einen Schlüsseltyp Satz ab.</span><span class="sxs-lookup"><span data-stu-id="47e93-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47e93-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="47e93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e93-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e93-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e93-108">Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="47e93-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="47e93-109">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e93-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e93-110">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="47e93-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="47e93-111">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e93-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e93-112">Einer der [**Cipher Suite-Bezeichner Werte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="47e93-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="47e93-113">*dwkeytype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e93-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e93-114">Eine der [**Schlüsseltyp**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) -ID-Werte des CNG-SSL-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="47e93-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="47e93-115">*pciphersuite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47e93-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47e93-116">Die Adresse eines Puffers, der eine [**NCrypt- \_ SSL \_ \_**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) -Verschlüsselungs Sammlungs Struktur enthält, in der die Chiffre Sammlungs Informationen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="47e93-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="47e93-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e93-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e93-118">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="47e93-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e93-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47e93-119">Return value</span></span>

<span data-ttu-id="47e93-120">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="47e93-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="47e93-121">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47e93-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="47e93-122">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="47e93-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="47e93-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="47e93-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="47e93-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47e93-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="47e93-125"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="47e93-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="47e93-126">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="47e93-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="47e93-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47e93-127">Requirements</span></span>



| <span data-ttu-id="47e93-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47e93-128">Requirement</span></span> | <span data-ttu-id="47e93-129">Wert</span><span class="sxs-lookup"><span data-stu-id="47e93-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e93-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47e93-130">Minimum supported client</span></span><br/> | <span data-ttu-id="47e93-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47e93-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47e93-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47e93-132">Minimum supported server</span></span><br/> | <span data-ttu-id="47e93-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47e93-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47e93-134">Header</span><span class="sxs-lookup"><span data-stu-id="47e93-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e93-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e93-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="47e93-136">DLL</span><span class="sxs-lookup"><span data-stu-id="47e93-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47e93-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47e93-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

