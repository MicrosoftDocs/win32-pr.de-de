---
description: Listet das erste oder nächste Zertifikat in einem externen Speicher auf, das den angegebenen Kriterien entspricht, oder ermittelt es.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Certstoreprovfindcert-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347078"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="2f5a2-103">Certstoreprovfindcert-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="2f5a2-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="2f5a2-104">Die **certstoreprovfindcert** -Rückruffunktion listet das erste oder nächste Zertifikat in einem [*externen Speicher*](../secgloss/e-gly.md) auf, das den angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f5a2-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="2f5a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f5a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f5a2-107">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5a2-108">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f5a2-109">*pfindinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5a2-110">Ein Zeiger auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) Struktur, die alle Parameter enthält, die an die [**certfindcertifikateinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a2-111">*pprevcertcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5a2-112">Ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) des gefundenen Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="2f5a2-113">Beim ersten Aufrufen der-Funktion sollte dieser Parameter auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="2f5a2-114">Bei nachfolgenden Aufrufen sollte Sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppprovcertcontext* -Parameter zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="2f5a2-115">Ein nicht-**null** -Zeiger, der in diesem Parameter übergeben wird, wird von der Rückruffunktion freigegeben.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a2-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5a2-117">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a2-118">*ppvstoreprovfindinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5a2-119">Ein Zeiger auf einen Zeiger auf einen Puffer, um die Informationen zum Speicher Anbieter zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="2f5a2-120">Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="2f5a2-121">Nach dem ersten-Befehl wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufrufen der-Funktion zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a2-122">*ppprovcertcontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5a2-123">Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf das gefundene Zertifikat zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f5a2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f5a2-124">Return value</span></span>

<span data-ttu-id="2f5a2-125">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f5a2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f5a2-126">Requirements</span></span>



| <span data-ttu-id="2f5a2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f5a2-127">Requirement</span></span> | <span data-ttu-id="2f5a2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2f5a2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f5a2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f5a2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f5a2-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2f5a2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f5a2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f5a2-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f5a2-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f5a2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f5a2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f5a2-134">**CERT- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="2f5a2-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="2f5a2-135">**CERT \_ Store \_ Prov \_ Find \_ Info**</span><span class="sxs-lookup"><span data-stu-id="2f5a2-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="2f5a2-136">**Certfindcertifi. Store**</span><span class="sxs-lookup"><span data-stu-id="2f5a2-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
