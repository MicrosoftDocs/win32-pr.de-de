---
description: Gibt ein Zertifikat an, das zum Signieren eines Dokuments verwendet wird. Das Zertifikat kann in einer SPC-Datei (Software Publisher Certificate) oder in einem Zertifikat Speicher gespeichert werden.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217619"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="85ec1-104">Signatur Geber- \_ Zertifikat Struktur</span><span class="sxs-lookup"><span data-stu-id="85ec1-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="85ec1-105">Die **Signatur Geber \_** -Zertifikat Struktur gibt ein [*Zertifikat*](../secgloss/c-gly.md) an, das zum Signieren eines Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85ec1-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="85ec1-106">Das Zertifikat kann in einer SPC-Datei ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) oder in einem [*Zertifikat Speicher*](../secgloss/c-gly.md)gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="85ec1-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="85ec1-107">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="85ec1-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="85ec1-108">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="85ec1-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85ec1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="85ec1-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="85ec1-110">Member</span><span class="sxs-lookup"><span data-stu-id="85ec1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="85ec1-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="85ec1-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="85ec1-112">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="85ec1-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="85ec1-113">**dwcertchoice**</span><span class="sxs-lookup"><span data-stu-id="85ec1-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="85ec1-114">Gibt an, wie das Zertifikat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="85ec1-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="85ec1-115">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="85ec1-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="85ec1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="85ec1-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="85ec1-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="85ec1-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="85ec1-118"><dt>**Signatur \_ Geber CERT \_ SPC- \_ Datei**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="85ec1-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="85ec1-119">Das Zertifikat wird in einer SPC-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="85ec1-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="85ec1-120">Der Member " **pwszspcfile** " enthält den Pfad und den Dateinamen der SPC-Datei.</span><span class="sxs-lookup"><span data-stu-id="85ec1-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="85ec1-121"><dt>**Signatur \_ Geber Zertifikat \_ Speicher**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="85ec1-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="85ec1-122">Das Zertifikat wird in einem Zertifikat Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="85ec1-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="85ec1-123">Das **pcertstoreinfo** -Element enthält einen Zeiger auf eine Signatur Geber-Zertifikat [**\_ Speicher- \_ \_ Informations**](signer-cert-store-info.md) Struktur, die den Zertifikat Speicher angibt, in dem das Zertifikat gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="85ec1-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="85ec1-124"><dt>**Signatur \_ Geber Zertifikat- \_ SPC- \_ Kette**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="85ec1-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="85ec1-125">Das Zertifikat wird in einer SPC-Datei gespeichert und mit einer Zertifikat Kette verknüpft.</span><span class="sxs-lookup"><span data-stu-id="85ec1-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="85ec1-126">Das **pspcchaininfo** -Element enthält einen Zeiger auf eine Signatur Geber- [**\_ SPC- \_ Ketten \_ Info**](signer-spc-chain-info.md) -Struktur, die die Ketten Informationen für das Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="85ec1-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85ec1-127">**pwszspcfile**</span><span class="sxs-lookup"><span data-stu-id="85ec1-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="85ec1-128">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Pfad und den Dateinamen der SPC-Datei enthält, in der das Zertifikat gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="85ec1-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="85ec1-129">Dieser Member wird nur verwendet, wenn das **dwcertchoice** -Element eine Signatur Geber- **Zertifikat-SPC- \_ \_ \_ Datei** enthält.</span><span class="sxs-lookup"><span data-stu-id="85ec1-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="85ec1-130">**pcertstoreingefo**</span><span class="sxs-lookup"><span data-stu-id="85ec1-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="85ec1-131">Ein Zeiger auf eine Signatur Geber-Zertifikat [**\_ \_ Speicher \_ Info**](signer-cert-store-info.md) -Struktur, die den Zertifikat Speicher angibt, in dem das Zertifikat gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="85ec1-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="85ec1-132">Dieser Member wird nur verwendet, wenn das **dwcertchoice** -Element den Signatur Geber- **\_ Zertifikat \_ Speicher** enthält.</span><span class="sxs-lookup"><span data-stu-id="85ec1-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="85ec1-133">**pspcchaininfo**</span><span class="sxs-lookup"><span data-stu-id="85ec1-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="85ec1-134">Ein Zeiger auf die Informationsstruktur der Signatur Geber- [**\_ SPC- \_ Kette \_**](signer-spc-chain-info.md) , die die Ketten Informationen für das Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="85ec1-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="85ec1-135">Dieser Member wird nur verwendet, wenn der **dwcertchoice** -Member eine Signatur Geber- **Zertifikat-SPC- \_ \_ \_ Kette** enthält.</span><span class="sxs-lookup"><span data-stu-id="85ec1-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="85ec1-136">**HWND**</span><span class="sxs-lookup"><span data-stu-id="85ec1-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="85ec1-137">Das Handle des Fensters, das als Besitzer beliebiger Dialogfelder verwendet werden soll, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="85ec1-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="85ec1-138">Dieser Member wird derzeit nicht verwendet und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="85ec1-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85ec1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85ec1-139">Requirements</span></span>



| <span data-ttu-id="85ec1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85ec1-140">Requirement</span></span> | <span data-ttu-id="85ec1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="85ec1-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85ec1-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85ec1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="85ec1-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85ec1-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="85ec1-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85ec1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="85ec1-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85ec1-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85ec1-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85ec1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ec1-147">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="85ec1-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="85ec1-148">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="85ec1-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
