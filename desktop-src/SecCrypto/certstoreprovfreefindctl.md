---
description: Wird aufgerufen, wenn das vom certstoreprovfindctl-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von certstoreprovfindctl nicht verwendet und daher freigegeben wurde.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Certstoreprovfrefindctl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362421"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="27e98-103">Certstoreprovfrefindctl-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="27e98-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="27e98-104">Die **certstoreprovfrefindctl** -Rückruffunktion wird aufgerufen, wenn das vom [**certstoreprovfindctl**](certstoreprovfindctl.md) -Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von " **certstoreprovfindctl**" freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="27e98-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="27e98-105">Bevor der Close-Rückruf aufgerufen wird, müssen alle vom [**certstoreprovfindctl**](certstoreprovfindctl.md) -Rückruf zurückgegebenen Zertifikate vom Anbieter mithilfe von **certstoreprovfindctl** oder **certstoreprovfreifindctl** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="27e98-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e98-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="27e98-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="27e98-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="27e98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27e98-108">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27e98-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27e98-109">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="27e98-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e98-110">*pctlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27e98-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27e98-111">Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="27e98-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="27e98-112">*pvstoreprovfindinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27e98-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27e98-113">Ein Zeiger auf einen Puffer, der Informationen zu suchen enthält.</span><span class="sxs-lookup"><span data-stu-id="27e98-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="27e98-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27e98-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27e98-115">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="27e98-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27e98-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27e98-116">Return value</span></span>

<span data-ttu-id="27e98-117">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="27e98-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="27e98-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27e98-118">Requirements</span></span>



| <span data-ttu-id="27e98-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27e98-119">Requirement</span></span> | <span data-ttu-id="27e98-120">Wert</span><span class="sxs-lookup"><span data-stu-id="27e98-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27e98-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27e98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27e98-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27e98-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="27e98-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27e98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27e98-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27e98-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27e98-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27e98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e98-126">**Certstoreprovfindctl**</span><span class="sxs-lookup"><span data-stu-id="27e98-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="27e98-127">**CTL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="27e98-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
