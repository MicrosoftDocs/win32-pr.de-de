---
description: Gibt einen SSL-Sitzungsschlüssel (Secure Sockets Layer Protocol) oder einen öffentlichen kurzlebigen Schlüssel in einem serialisierten BLOB zurück.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Sslexportkey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959428"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="4b767-103">Sslexportkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="4b767-103">SslExportKey function</span></span>

<span data-ttu-id="4b767-104">Die **sslexportkey** -Funktion gibt einen SSL- [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) oder einen öffentlichen kurzlebigen Schlüssel in einem serialisierten [*BLOB*](/windows/desktop/SecGloss/b-gly)zurück.</span><span class="sxs-lookup"><span data-stu-id="4b767-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b767-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b767-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4b767-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b767-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b767-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b767-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-108">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="4b767-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="4b767-109">*HKEY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b767-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-110">Das Handle des zu exportierenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="4b767-110">The handle of the key to export.</span></span>

<span data-ttu-id="4b767-111">Wenn Sie keinen Schlüssel angeben, legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="4b767-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="4b767-112">Ein *HKEY* -Handle wird durch Aufrufen der [**sslopenprivatekey**](sslopenprivatekey.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4b767-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="4b767-113">Handles, die von der [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Funktion abgerufen werden, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b767-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b767-114">*pszblobtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b767-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-115">Eine mit NULL endenden Unicode-Zeichenfolge, die einen Bezeichner enthält, der den Typ des zu exportierenden BLOBs angibt.</span><span class="sxs-lookup"><span data-stu-id="4b767-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="4b767-116">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="4b767-116">This can be one of the following values.</span></span>



| <span data-ttu-id="4b767-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4b767-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="4b767-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4b767-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="4b767-119"><dt>**bcrypt \_ dh \_ Public \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="4b767-120">Exportieren Sie einen Diffie-Hellman [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="4b767-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="4b767-121">Der *pboutput* -Puffer empfängt eine [**bcrypt \_ DH-Schlüssel- \_ \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.</span><span class="sxs-lookup"><span data-stu-id="4b767-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="4b767-122"><dt>**bcrypt \_ eccpublic- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="4b767-123">Exportieren eines öffentlichen Schlüssels der [*elliptischen Kurve Kryptografie*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="4b767-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="4b767-124">Der *pboutput* -Puffer empfängt eine [**bcrypt \_ ecckey- \_ blobstruktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) , die direkt auf die Schlüsseldaten folgt.</span><span class="sxs-lookup"><span data-stu-id="4b767-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="4b767-125"><dt>**bcrypt \_ - \_ Schlüssel- \_ BLOB nicht transparent**</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="4b767-126">Exportieren Sie einen symmetrischen Schlüssel in einem Format, das für einen einzelnen [*Kryptografiedienstanbieter*](/windows/desktop/SecGloss/c-gly) (CSP) spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="4b767-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="4b767-127">Nicht transparente BLOBs sind nicht übertragbar und müssen mit demselben *Kryptografiedienstanbieter* (CSP) importiert werden, der das BLOB generiert hat.</span><span class="sxs-lookup"><span data-stu-id="4b767-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="4b767-128"><dt>**bcrypt \_ rsapublic- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="4b767-129">Exportieren Sie einen öffentlichen RSA-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="4b767-129">Export an RSA public key.</span></span> <span data-ttu-id="4b767-130">Der *pboutput* -Puffer empfängt eine [**bcrypt \_ rsaKey- \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.</span><span class="sxs-lookup"><span data-stu-id="4b767-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="4b767-131">*pboutput* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="4b767-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-132">Die Adresse eines Puffers, der das [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly)empfängt.</span><span class="sxs-lookup"><span data-stu-id="4b767-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="4b767-133">Der *cboutput* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="4b767-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="4b767-134">Wenn dieser Parameter **null** ist, fügt diese Funktion die erforderliche Größe (in Bytes) in das **DWORD** ein, auf das durch den *pcbresult* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4b767-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4b767-135">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b767-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-136">Die Größe des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4b767-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4b767-137">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4b767-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-138">Die Adresse einer **DWORD** -Variablen, die die Anzahl von Bytes empfängt, die in den *pboutput* -Puffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b767-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="4b767-139">Wenn der *pboutput* -Parameter beim Aufrufen der-Funktion auf **null** festgelegt ist, wird die erforderliche Größe für den *pboutput* -Puffer in Bytes in dem **DWORD** zurückgegeben, auf das von diesem Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4b767-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4b767-140">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b767-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b767-141">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4b767-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b767-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b767-142">Return value</span></span>

<span data-ttu-id="4b767-143">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4b767-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="4b767-144">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4b767-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="4b767-145">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="4b767-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="4b767-146">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4b767-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="4b767-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b767-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4b767-148"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="4b767-149">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4b767-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b767-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b767-150">Remarks</span></span>

<span data-ttu-id="4b767-151">Die **sslexportkey** -Funktion ermöglicht das Transportieren von Sitzungs Schlüsseln von einem Prozess zu einem anderen und das Exportieren des öffentlichen Teils eines kurzlebigen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="4b767-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="4b767-152">Beim Exportieren von Sitzungs Schlüsseln ist der BLOB-Typ nicht transparent, was bedeutet, dass das BLOB-Format irrelevant ist, solange die Funktionen **sslexportkey** und [**sslimportkey**](sslimportkey.md) Sie interpretieren können.</span><span class="sxs-lookup"><span data-stu-id="4b767-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="4b767-153">Beim Exportieren des öffentlichen Teils eines kurzlebigen Schlüssels muss der BLOB-Typ der geeignete Typ sein, z. b. " **NCrypt \_ dh \_ Public \_ BLOB** " oder " **NCrypt \_ eccpublic \_ BLOB**".</span><span class="sxs-lookup"><span data-stu-id="4b767-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b767-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b767-154">Requirements</span></span>



| <span data-ttu-id="4b767-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b767-155">Requirement</span></span> | <span data-ttu-id="4b767-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4b767-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b767-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b767-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4b767-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b767-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4b767-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b767-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4b767-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b767-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4b767-161">Header</span><span class="sxs-lookup"><span data-stu-id="4b767-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b767-162"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="4b767-163">DLL</span><span class="sxs-lookup"><span data-stu-id="4b767-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b767-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b767-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

