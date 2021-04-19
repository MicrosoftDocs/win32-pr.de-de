---
description: Wird aufgerufen, wenn das vom certstoreprovfindcert-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von certstoreprovfindcert nicht verwendet und daher freigegeben wurde.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Certstoreprovfrefindcert-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353846"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="7055a-103">Certstoreprovfrefindcert-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="7055a-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="7055a-104">Die **certstoreprovfrefindcert** -Rückruffunktion wird aufgerufen, wenn das vom [**certstoreprovfindcert**](certstoreprovfindcert.md) -Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **certstoreprovfindcert** freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7055a-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="7055a-105">Bevor der Close-Rückruf aufgerufen wird, müssen alle vom [**certstoreprovfindcert**](certstoreprovfindcert.md) -Rückruf zurückgegebenen Zertifikate vom Anbieter mithilfe von **certstoreprovfindcert** oder **certstoreprovfreifindcert** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7055a-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7055a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7055a-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7055a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7055a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7055a-108">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7055a-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7055a-109">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7055a-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7055a-110">*pcertcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7055a-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7055a-111">Ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="7055a-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="7055a-112">*pvstoreprovfindinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7055a-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7055a-113">Ein Zeiger auf einen Puffer, der Informationen zu suchen enthält.</span><span class="sxs-lookup"><span data-stu-id="7055a-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="7055a-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7055a-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7055a-115">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="7055a-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7055a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7055a-116">Return value</span></span>

<span data-ttu-id="7055a-117">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="7055a-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7055a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7055a-118">Requirements</span></span>



| <span data-ttu-id="7055a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7055a-119">Requirement</span></span> | <span data-ttu-id="7055a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7055a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7055a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7055a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7055a-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7055a-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7055a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7055a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7055a-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7055a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7055a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7055a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7055a-126">**CERT- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="7055a-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="7055a-127">**Certstoreprovfindcert**</span><span class="sxs-lookup"><span data-stu-id="7055a-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
