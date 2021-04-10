---
description: Wird aufgerufen, wenn das vom certstoreprovfindcrl-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von certstoreprovfindcrl nicht verwendet und daher freigegeben wurde.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Certstoreprovfrefindcrl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867168"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="904bb-103">Certstoreprovfrefindcrl-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="904bb-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="904bb-104">Die **certstoreprovfrefindcrl** -Rückruffunktion wird aufgerufen, wenn das vom [**certstoreprovfindcrl**](certstoreprovfindcrl.md) -Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **certstoreprovfindcrl** freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="904bb-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="904bb-105">Bevor der schließende Rückruf aufgerufen wird, müssen alle vom [**certstoreprovfindcrl**](certstoreprovfindcrl.md) -Rückruf zurückgegebenen Zertifikate vom Anbieter mithilfe von **certstoreprovfindcrl** oder **certstoreprovfreifindcrl** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="904bb-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="904bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="904bb-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="904bb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="904bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904bb-108">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="904bb-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904bb-109">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="904bb-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="904bb-110">*pcrlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="904bb-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904bb-111">Ein Zeiger auf einen [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="904bb-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="904bb-112">*pvstoreprovfindinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="904bb-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904bb-113">Ein Zeiger auf einen Puffer, der Informationen zu suchen enthält.</span><span class="sxs-lookup"><span data-stu-id="904bb-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="904bb-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="904bb-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904bb-115">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="904bb-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904bb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="904bb-116">Return value</span></span>

<span data-ttu-id="904bb-117">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="904bb-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="904bb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="904bb-118">Requirements</span></span>



| <span data-ttu-id="904bb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="904bb-119">Requirement</span></span> | <span data-ttu-id="904bb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="904bb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="904bb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="904bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="904bb-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="904bb-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="904bb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="904bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="904bb-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="904bb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="904bb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="904bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904bb-126">**Certstoreprovfindcrl**</span><span class="sxs-lookup"><span data-stu-id="904bb-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="904bb-127">**CRL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="904bb-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
