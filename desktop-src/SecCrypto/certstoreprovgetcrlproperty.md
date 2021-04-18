---
description: Ruft eine angegebene Eigenschaft einer CRL ab.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Certstoreprovgetcrlproperty-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357511"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="f3efa-103">Certstoreprovgetcrlproperty-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="f3efa-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="f3efa-104">Die **certstoreprovgetcrlproperty** -Rückruffunktion Ruft eine angegebene Eigenschaft einer [*CRL*](../secgloss/c-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="f3efa-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3efa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3efa-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="f3efa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3efa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3efa-107">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3efa-108">**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f3efa-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3efa-109">*pcrlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3efa-110">Ein Zeiger auf eine [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f3efa-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3efa-111">*dwpropid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3efa-112">Gibt einen Eigenschafts Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="f3efa-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f3efa-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3efa-114">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="f3efa-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="f3efa-115">*pvData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3efa-116">Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) Struktur enthalten soll, die von der Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3efa-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="f3efa-117">Kann bei einem ersten Aufrufe der-Funktion auf **null** festgelegt werden, um den Wert von *pcbData* abzurufen, bevor für den Pufferspeicher zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f3efa-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f3efa-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3efa-119">Ein Zeiger auf ein **DWORD** , das die Länge des *pvData* -Puffers angibt.</span><span class="sxs-lookup"><span data-stu-id="f3efa-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3efa-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3efa-120">Return value</span></span>

<span data-ttu-id="f3efa-121">Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f3efa-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3efa-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3efa-122">Requirements</span></span>



| <span data-ttu-id="f3efa-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3efa-123">Requirement</span></span> | <span data-ttu-id="f3efa-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f3efa-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3efa-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3efa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3efa-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f3efa-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3efa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3efa-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3efa-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3efa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3efa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3efa-130">**CRL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="f3efa-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
