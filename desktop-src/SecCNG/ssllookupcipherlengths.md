---
description: Gibt eine NCrypt \_ \_ -SSL-Chiffre \_ Längen Struktur zurück, die die Header-und nach Spann Längen des Eingabe Protokolls, der Verschlüsselungs Sammlung und des Schlüssel Typs enthält.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Ssllookupcipherlängen-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959381"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="7e371-103">Ssllookupcipherlängen-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e371-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="7e371-104">Die **ssllookupcipherlängen** -Funktion gibt eine [**NCrypt- \_ SSL- \_ Chiffre \_ Längen**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) Struktur zurück, die die Header-und nach Spann Längen des Eingabe Protokolls, der Verschlüsselungs Sammlung und des Schlüssel Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="7e371-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e371-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e371-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7e371-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e371-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e371-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e371-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-108">Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="7e371-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="7e371-109">*dwprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e371-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-110">Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7e371-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="7e371-111">*dwciphersuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e371-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-112">Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7e371-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="7e371-113">*dwkeytype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e371-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-114">Einer der [**Schlüsseltyp-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="7e371-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="7e371-115">Legen Sie für Schlüsseltypen, bei denen es sich nicht um eine [*Kryptographie*](/windows/desktop/SecGloss/e-gly) (ECC) handelt, diesen Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="7e371-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7e371-116">*pcipherlängen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e371-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-117">Ein Zeiger auf einen Puffer, der die [**NCrypt- \_ SSL- \_ Chiffre \_ Längen**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) Struktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="7e371-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e371-118">*cbcipherlängen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e371-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-119">Die Länge des Puffers in Byte, auf den durch den *pcipherlength* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7e371-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7e371-120">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e371-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e371-121">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7e371-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e371-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e371-122">Return value</span></span>

<span data-ttu-id="7e371-123">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7e371-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7e371-124">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e371-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7e371-125">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="7e371-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7e371-126">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7e371-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7e371-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e371-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e371-128"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="7e371-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="7e371-129">Der *hsslprovider* -Parameter enthält einen ungültigen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="7e371-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="7e371-130"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="7e371-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="7e371-131">Der *pcipherlength* -Parameter ist auf **null** festgelegt, oder die von *cbcipherlength* angegebene Pufferlänge ist zu kurz.</span><span class="sxs-lookup"><span data-stu-id="7e371-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="7e371-132"><dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt></span><span class="sxs-lookup"><span data-stu-id="7e371-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="7e371-133">Der *dwFlags* -Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7e371-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="7e371-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e371-134">Remarks</span></span>

<span data-ttu-id="7e371-135">Die **ssllookupcipherlängen** -Funktion wird für die Konversationen von [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,1 oder höher aufgerufen, um die Header-und nach Spann Längen für das angeforderte Protokoll, die Verschlüsselungs Sammlung und den Schlüsseltyp abzufragen.</span><span class="sxs-lookup"><span data-stu-id="7e371-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e371-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e371-136">Requirements</span></span>



| <span data-ttu-id="7e371-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e371-137">Requirement</span></span> | <span data-ttu-id="7e371-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7e371-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e371-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e371-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7e371-140">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e371-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e371-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e371-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7e371-142">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e371-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e371-143">Header</span><span class="sxs-lookup"><span data-stu-id="7e371-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e371-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e371-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7e371-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7e371-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e371-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e371-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

