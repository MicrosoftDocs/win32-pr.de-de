---
description: Listet die Verschlüsselungs Sammlungen auf, die von einem Protokoll Anbieter für Secure Sockets Layer Protokoll (SSL) unterstützt werden.
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Sslenenciphersuites-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345039"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="dc14a-103">Sslenenciphersuites-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc14a-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="dc14a-104">Die Funktion **sslenumciphersuites** listet die Verschlüsselungs Sammlungen auf, die von einem Protokoll Anbieter für [*Secure Sockets Layer Protokoll*](/windows/desktop/SecGloss/s-gly) (SSL) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dc14a-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc14a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc14a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dc14a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc14a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc14a-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc14a-108">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="dc14a-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="dc14a-109">*hprivatekey* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc14a-110">Das Handle eines [*privaten Schlüssels*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="dc14a-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="dc14a-111">Wenn ein privater Schlüssel angegeben wird, listet **sslenumciphersuites** die Verschlüsselungs Sammlungen auf, die mit dem privaten Schlüssel kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="dc14a-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="dc14a-112">Wenn der private Schlüssel z. b. ein DSS-Schlüssel ist, werden nur die DSS dit-Verschlüsselungs Sammlungen \_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc14a-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="dc14a-113">Wenn der private Schlüssel ein RSA-Schlüssel ist, aber keine unformatierten Entschlüsselungs Vorgänge unterstützt, werden die SSL2 verwendet-Verschlüsselungs Sammlungen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc14a-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="dc14a-114">Legen Sie diesen Parameter auf **null** fest, wenn Sie keinen privaten Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="dc14a-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="dc14a-115">Ein *hprivatekey* -Handle wird durch Aufrufen der [**sslopenprivatekey**](sslopenprivatekey.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dc14a-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="dc14a-116">Handles, die von der [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Funktion abgerufen werden, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc14a-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc14a-117">*ppciphersuite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc14a-118">Ein Zeiger auf eine [**NCrypt- \_ SSL- \_ Chiffre \_**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) Sammlungs Struktur, die die Adresse der nächsten Verschlüsselungs Sammlung in der Liste empfängt.</span><span class="sxs-lookup"><span data-stu-id="dc14a-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="dc14a-119">" *ppumschlag State* \[ " in, out\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc14a-120">Ein Zeiger auf einen Puffer, der die aktuelle Position in der Liste der Verschlüsselungs Sammlungen angibt.</span><span class="sxs-lookup"><span data-stu-id="dc14a-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="dc14a-121">Legen Sie den Zeiger beim ersten **sslenumciphersuites**-aufrufswert auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="dc14a-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="dc14a-122">Übergeben Sie bei jedem nachfolgenden-Rückruf den nicht geänderten Wert zurück an **sslenenciphersuites**.</span><span class="sxs-lookup"><span data-stu-id="dc14a-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="dc14a-123">Wenn keine weiteren Verschlüsselungs Sammlungen verfügbar sind, sollten Sie " *pprestate* " durch Aufrufen der Funktion " [**sslfreebuffer**](sslfreebuffer.md) " freigeben.</span><span class="sxs-lookup"><span data-stu-id="dc14a-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dc14a-124">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc14a-125">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="dc14a-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc14a-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc14a-126">Return value</span></span>

<span data-ttu-id="dc14a-127">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="dc14a-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="dc14a-128">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc14a-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="dc14a-129">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="dc14a-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dc14a-130">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="dc14a-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="dc14a-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc14a-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc14a-132"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="dc14a-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="dc14a-133">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dc14a-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="dc14a-134"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="dc14a-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="dc14a-135">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dc14a-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="dc14a-136"><dt>**Ernte \_ Keine \_ weiteren \_ Elemente**</dt> <dt>0x8009002al</dt></span><span class="sxs-lookup"><span data-stu-id="dc14a-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="dc14a-137">Es werden keine zusätzlichen Verschlüsselungs Sammlungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc14a-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dc14a-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc14a-138">Remarks</span></span>

<span data-ttu-id="dc14a-139">Um alle Verschlüsselungs Sammlungen aufzulisten, die vom SSL-Anbieter unterstützt werden, müssen Sie die **sslenumciphersuites** -Funktion in einer Schleife aufzurufen, bis die **\_ \_ \_ Elemente nicht mehr** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc14a-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc14a-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc14a-140">Requirements</span></span>



| <span data-ttu-id="dc14a-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc14a-141">Requirement</span></span> | <span data-ttu-id="dc14a-142">Wert</span><span class="sxs-lookup"><span data-stu-id="dc14a-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc14a-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc14a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="dc14a-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc14a-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc14a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="dc14a-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc14a-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dc14a-147">Header</span><span class="sxs-lookup"><span data-stu-id="dc14a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc14a-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc14a-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="dc14a-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc14a-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc14a-150"><dt>Ncrypt. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc14a-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="dc14a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="dc14a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc14a-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc14a-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dc14a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc14a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc14a-154">**ncrypt-SSL-Verschlüsselungs \_ \_ \_ Sammlung**</span><span class="sxs-lookup"><span data-stu-id="dc14a-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

