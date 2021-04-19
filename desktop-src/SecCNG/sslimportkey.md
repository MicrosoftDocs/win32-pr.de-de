---
description: Importiert einen Schlüssel in den SSL-Protokoll Anbieter (Secure Sockets Layer Protocol).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Sslimportkey-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349154"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="836b9-103">Sslimportkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="836b9-103">SslImportKey function</span></span>

<span data-ttu-id="836b9-104">Die **sslimportkey** -Funktion importiert einen Schlüssel in den SSL-Protokoll Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="836b9-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="836b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="836b9-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="836b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="836b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836b9-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836b9-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b9-108">Das Handle für die SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="836b9-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="836b9-109">*phkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="836b9-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="836b9-110">Ein Zeiger auf das Handle des [*Kryptografieschlüssels*](/windows/desktop/SecGloss/c-gly) , der den importierten Schlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="836b9-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="836b9-111">*pszblobtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836b9-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b9-112">Eine NULL-terminierte Unicode-Zeichenfolge, die einen Bezeichner enthält, der den Typ des [*BLOBs*](/windows/desktop/SecGloss/b-gly) angibt, der im *pbinput* -Puffer enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="836b9-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="836b9-113">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="836b9-113">This can be one of the following values.</span></span>



| <span data-ttu-id="836b9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="836b9-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="836b9-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="836b9-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="836b9-116"><dt>**bcrypt \_ dh \_ Public \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="836b9-117">Exportieren Sie einen Diffie-Hellman [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="836b9-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="836b9-118">Der *pboutput* -Puffer empfängt eine [**bcrypt \_ DH-Schlüssel- \_ \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.</span><span class="sxs-lookup"><span data-stu-id="836b9-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="836b9-119"><dt>**bcrypt \_ eccpublic- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="836b9-120">Exportieren eines [*öffentlichen Schlüssels*](/windows/desktop/SecGloss/p-gly)der [*elliptischen Kurve Kryptografie*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="836b9-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="836b9-121">Der *pboutput* -Puffer empfängt eine [**bcrypt \_ ecckey- \_ blobstruktur**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) , die direkt auf die Schlüsseldaten folgt.</span><span class="sxs-lookup"><span data-stu-id="836b9-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="836b9-122"><dt>**bcrypt \_ - \_ Schlüssel- \_ BLOB nicht transparent**</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="836b9-123">Exportieren Sie einen [*symmetrischen Schlüssel*](/windows/desktop/SecGloss/s-gly) in einem Format, das für einen einzelnen [*Kryptografiedienstanbieter*](/windows/desktop/SecGloss/c-gly) (CSP) spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="836b9-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="836b9-124">Nicht transparente BLOBs sind nicht übertragbar und müssen mit demselben CSP importiert werden, der das BLOB generiert hat.</span><span class="sxs-lookup"><span data-stu-id="836b9-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="836b9-125"><dt>**bcrypt \_ rsapublic- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="836b9-126">Exportieren Sie einen öffentlichen [*RSA*](/windows/desktop/SecGloss/r-gly) -Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="836b9-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="836b9-127">Der *pboutput* -Puffer empfängt eine [**bcrypt \_ rsaKey- \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) -Struktur, auf die die Schlüsseldaten unmittelbar folgen.</span><span class="sxs-lookup"><span data-stu-id="836b9-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="836b9-128">*pbKeyBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836b9-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b9-129">Ein Zeiger auf den Puffer, der das [*Schlüsselblob*](/windows/desktop/SecGloss/k-gly)enthält.</span><span class="sxs-lookup"><span data-stu-id="836b9-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="836b9-130">*cbKeyBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836b9-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b9-131">Die Größe des *pbKeyBlob* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="836b9-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="836b9-132">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836b9-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b9-133">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="836b9-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836b9-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="836b9-134">Return value</span></span>

<span data-ttu-id="836b9-135">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="836b9-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="836b9-136">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="836b9-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="836b9-137">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="836b9-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="836b9-138">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="836b9-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="836b9-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="836b9-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="836b9-140"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="836b9-141">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="836b9-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="836b9-142"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="836b9-143">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="836b9-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="836b9-144"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="836b9-145">Der *phkey* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="836b9-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="836b9-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="836b9-146">Remarks</span></span>

<span data-ttu-id="836b9-147">Sie können die **sslimportkey** -Funktion verwenden, um Sitzungsschlüssel im Rahmen der Übertragung von Sitzungs Schlüsseln von einem Prozess in einen anderen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="836b9-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="836b9-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="836b9-148">Requirements</span></span>



| <span data-ttu-id="836b9-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="836b9-149">Requirement</span></span> | <span data-ttu-id="836b9-150">Wert</span><span class="sxs-lookup"><span data-stu-id="836b9-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="836b9-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="836b9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="836b9-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="836b9-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="836b9-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="836b9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="836b9-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="836b9-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="836b9-155">Header</span><span class="sxs-lookup"><span data-stu-id="836b9-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="836b9-156"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="836b9-157">DLL</span><span class="sxs-lookup"><span data-stu-id="836b9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="836b9-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="836b9-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

