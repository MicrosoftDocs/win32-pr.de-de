---
description: Ruft eine angegebene Eigenschaft eines Zertifikats ab.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Certstoreprovgetcertproperty-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362420"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="58a10-103">Certstoreprovgetcertproperty-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="58a10-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="58a10-104">Die **certstoreprovgetcertproperty** -Rückruffunktion Ruft eine angegebene Eigenschaft eines Zertifikats ab.</span><span class="sxs-lookup"><span data-stu-id="58a10-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58a10-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="58a10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58a10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a10-107">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58a10-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a10-108">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="58a10-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="58a10-109">*pcertcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58a10-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a10-110">Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="58a10-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="58a10-111">*dwpropid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58a10-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a10-112">Gibt einen Eigenschafts Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="58a10-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="58a10-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58a10-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a10-114">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="58a10-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="58a10-115">*pvData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58a10-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58a10-116">Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur enthalten soll, die von der Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="58a10-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="58a10-117">Kann bei einem ersten Aufrufe der-Funktion auf **null** festgelegt werden, um den Wert von *pcbData* abzurufen, bevor für den Pufferspeicher zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="58a10-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="58a10-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="58a10-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58a10-119">Ein Zeiger auf ein **DWORD** , das die Länge des *pvData* -Puffers angibt.</span><span class="sxs-lookup"><span data-stu-id="58a10-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a10-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58a10-120">Return value</span></span>

<span data-ttu-id="58a10-121">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="58a10-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a10-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58a10-122">Requirements</span></span>



| <span data-ttu-id="58a10-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58a10-123">Requirement</span></span> | <span data-ttu-id="58a10-124">Wert</span><span class="sxs-lookup"><span data-stu-id="58a10-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58a10-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58a10-125">Minimum supported client</span></span><br/> | <span data-ttu-id="58a10-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58a10-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="58a10-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58a10-127">Minimum supported server</span></span><br/> | <span data-ttu-id="58a10-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58a10-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58a10-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58a10-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a10-130">**CERT- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="58a10-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
