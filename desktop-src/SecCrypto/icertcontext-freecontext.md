---
description: Gibt einen pccert-kontextfrei, \_ der über die certcontext-Eigenschaft abgerufen wurde.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Icertcontext:: freecontext-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367655"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="17e84-103">Icertcontext:: freecontext-Methode</span><span class="sxs-lookup"><span data-stu-id="17e84-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="17e84-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="17e84-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="17e84-105">Die **freecontext** -Methode gibt einen pccert-kontextfrei, \_ der über die [**certcontext**](icertcontext-certcontext.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="17e84-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e84-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e84-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="17e84-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="17e84-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e84-108">*pcertcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17e84-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e84-109">Der pccert- \_ Kontext, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="17e84-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e84-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17e84-110">Return value</span></span>

<span data-ttu-id="17e84-111">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="17e84-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="17e84-112">Der Wert S \_ OK weist auf Erfolg hin.</span><span class="sxs-lookup"><span data-stu-id="17e84-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="17e84-113">Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="17e84-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e84-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17e84-114">Remarks</span></span>

<span data-ttu-id="17e84-115">Diese Methode gibt nicht den pccert-kontextfrei, der \_ in einem [**Zertifikat**](certificate.md) Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="17e84-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="17e84-116">Es sollte nur verwendet werden, um einen pccert-kontextfrei zugeben, \_ der über die [**certcontext**](icertcontext-certcontext.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="17e84-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e84-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17e84-117">Requirements</span></span>



| <span data-ttu-id="17e84-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17e84-118">Requirement</span></span> | <span data-ttu-id="17e84-119">Wert</span><span class="sxs-lookup"><span data-stu-id="17e84-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17e84-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="17e84-120">Redistributable</span></span><br/> | <span data-ttu-id="17e84-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="17e84-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="17e84-122">DLL</span><span class="sxs-lookup"><span data-stu-id="17e84-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="17e84-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17e84-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e84-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17e84-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e84-125">**Icertcontext**</span><span class="sxs-lookup"><span data-stu-id="17e84-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




