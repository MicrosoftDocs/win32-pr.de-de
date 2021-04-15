---
description: Listet die erste oder nächste Zertifikat Sperr Liste in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder ermittelt Sie.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Certstoreprovfindcrl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529711"
---
# <a name="certstoreprovfindcrl-callback-function"></a><span data-ttu-id="54899-103">Certstoreprovfindcrl-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="54899-103">CertStoreProvFindCRL callback function</span></span>

<span data-ttu-id="54899-104">Die **certstoreprovfindcrl** -Rückruffunktion listet die erste oder die nächste [*CRL*](../secgloss/c-gly.md) in einem externen [*Speicher*](../secgloss/e-gly.md) auf, die den angegebenen Kriterien entspricht, oder sucht Sie.</span><span class="sxs-lookup"><span data-stu-id="54899-104">The **CertStoreProvFindCRL** callback function enumerates or finds the first or next [*CRL*](../secgloss/c-gly.md) in an external [*store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="54899-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54899-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
);
```



## <a name="parameters"></a><span data-ttu-id="54899-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54899-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54899-107">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54899-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54899-108">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="54899-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="54899-109">*pfindinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54899-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54899-110">Ein Zeiger auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) Struktur, die alle Parameter enthält, die an die [**certfindcrlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="54899-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="54899-111">*pprevcrlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54899-111">*pPrevCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54899-112">Ein Zeiger auf eine [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) Struktur der letzten gefundenen CRL.</span><span class="sxs-lookup"><span data-stu-id="54899-112">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure of the last CRL found.</span></span> <span data-ttu-id="54899-113">Beim ersten Aufrufen der-Funktion sollte dieser Parameter auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="54899-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="54899-114">Bei nachfolgenden Aufrufen sollte Sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppprovcrlcontext* -Parameter zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="54899-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCRLContext* parameter on the last call.</span></span> <span data-ttu-id="54899-115">Ein nicht-**null** -Zeiger, der in diesem Parameter übergeben wird, wird von der Rückruffunktion freigegeben.</span><span class="sxs-lookup"><span data-stu-id="54899-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="54899-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54899-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54899-117">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="54899-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="54899-118">*ppvstoreprovfindinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54899-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54899-119">Ein Zeiger auf einen Zeiger auf einen Puffer, um die Informationen zum Speicher Anbieter zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="54899-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="54899-120">Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="54899-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="54899-121">Nach dem ersten-Befehl wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufrufen der-Funktion zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="54899-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="54899-122">*ppprovcrlcontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54899-122">*ppProvCrlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54899-123">Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf die gefundene CRL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54899-123">On a successful find, a pointer to the CRL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54899-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54899-124">Return value</span></span>

<span data-ttu-id="54899-125">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="54899-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="54899-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54899-126">Requirements</span></span>



| <span data-ttu-id="54899-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54899-127">Requirement</span></span> | <span data-ttu-id="54899-128">Wert</span><span class="sxs-lookup"><span data-stu-id="54899-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54899-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54899-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54899-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54899-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="54899-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54899-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54899-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54899-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54899-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54899-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54899-134">**CERT \_ Store \_ Prov \_ Find \_ Info**</span><span class="sxs-lookup"><span data-stu-id="54899-134">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="54899-135">**Certfindcrlinstore**</span><span class="sxs-lookup"><span data-stu-id="54899-135">**CertFindCRLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[<span data-ttu-id="54899-136">**CRL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="54899-136">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
