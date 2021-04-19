---
description: Listet die erste oder nächste CTL in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder sucht Sie.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Certstoreprovfindctl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362385"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="9f08c-103">Certstoreprovfindctl-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="9f08c-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="9f08c-104">Die **certstoreprovfindctl** -Rückruffunktion listet die erste oder nächste [*CTL*](../secgloss/c-gly.md) in einem [*externen Speicher*](../secgloss/e-gly.md) auf, der den angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="9f08c-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f08c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f08c-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="9f08c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f08c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f08c-107">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f08c-108">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9f08c-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f08c-109">*pfindinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f08c-110">Ein Zeiger auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) Struktur, die alle Parameter enthält, die an den [**certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f08c-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="9f08c-111">Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f08c-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="9f08c-112">*pprevctlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f08c-113">Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur der letzten gefundenen CTL.</span><span class="sxs-lookup"><span data-stu-id="9f08c-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="9f08c-114">Beim ersten Aufrufen der-Funktion sollte dieser Parameter auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f08c-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="9f08c-115">Bei nachfolgenden Aufrufen sollte Sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppprovctlcontext* -Parameter zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9f08c-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="9f08c-116">Ein nicht-**null** -Zeiger, der in diesem Parameter übergeben wird, wird von der Rückruffunktion freigegeben.</span><span class="sxs-lookup"><span data-stu-id="9f08c-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="9f08c-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f08c-118">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="9f08c-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="9f08c-119">*ppvstoreprovfindinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f08c-120">Ein Zeiger auf einen Zeiger auf einen Puffer, um die Informationen zum Speicher Anbieter zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9f08c-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="9f08c-121">Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9f08c-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="9f08c-122">Nach dem ersten-Befehl wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufrufen der-Funktion zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9f08c-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="9f08c-123">*ppprovctlcontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f08c-124">Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf die gefundene CTL-Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f08c-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f08c-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f08c-125">Return value</span></span>

<span data-ttu-id="9f08c-126">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9f08c-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f08c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f08c-127">Requirements</span></span>



| <span data-ttu-id="9f08c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f08c-128">Requirement</span></span> | <span data-ttu-id="9f08c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9f08c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f08c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f08c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9f08c-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9f08c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f08c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9f08c-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f08c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f08c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f08c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f08c-135">**CERT \_ Store \_ Prov \_ Find \_ Info**</span><span class="sxs-lookup"><span data-stu-id="9f08c-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="9f08c-136">**Certfindctlinstore**</span><span class="sxs-lookup"><span data-stu-id="9f08c-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="9f08c-137">**CTL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="9f08c-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
