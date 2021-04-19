---
description: Ruft eine angegebene Eigenschaft einer Zertifikat Vertrauens Liste (Certificate Trust List, CTL) ab.
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Certstoreprovgetctlproperty-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368936"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="c7d22-103">Certstoreprovgetctlproperty-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="c7d22-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="c7d22-104">Die **certstoreprovgetctlproperty** -Rückruffunktion Ruft eine angegebene Eigenschaft einer [*Zertifikat Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) ab.</span><span class="sxs-lookup"><span data-stu-id="c7d22-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7d22-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="c7d22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d22-107">*hstoreprov* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d22-108">Ein **hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c7d22-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7d22-109">*pctlcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d22-110">Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="c7d22-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7d22-111">*dwpropid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d22-112">Gibt einen Eigenschafts Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="c7d22-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c7d22-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d22-114">Alle benötigten Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="c7d22-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="c7d22-115">*pvData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d22-116">Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur enthalten soll, die von der Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7d22-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="c7d22-117">Dieser Parameter kann bei einem ersten Aufrufen der-Funktion auf **null** festgelegt werden, um den Wert von *pcbData* vor der Zuweisung von Arbeitsspeicher für den Puffer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7d22-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="c7d22-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d22-119">Ein Zeiger auf ein **DWORD** , das die Länge des *pvData* -Puffers angibt.</span><span class="sxs-lookup"><span data-stu-id="c7d22-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d22-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7d22-120">Return value</span></span>

<span data-ttu-id="c7d22-121">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion einen Wert ungleich NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="c7d22-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="c7d22-122">Wenn die Funktion fehlschlägt, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c7d22-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d22-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7d22-123">Requirements</span></span>



| <span data-ttu-id="c7d22-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7d22-124">Requirement</span></span> | <span data-ttu-id="c7d22-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c7d22-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7d22-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7d22-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d22-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c7d22-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7d22-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d22-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7d22-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7d22-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7d22-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d22-131">**CTL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="c7d22-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
