---
description: Legt den pccert- \_ Ketten Kontext eines Zertifikats fest oder ruft ihn ab \_ .
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Ichaincontext:: ChainContext-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355281"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="7da45-103">Ichaincontext:: ChainContext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da45-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="7da45-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="7da45-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="7da45-105">Die **chainContext** -Eigenschaft legt den pccert- \_ Ketten \_ Kontext eines Zertifikats fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="7da45-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="7da45-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7da45-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da45-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da45-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="7da45-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7da45-108">Property value</span></span>

<span data-ttu-id="7da45-109">Der pccert- \_ Ketten \_ Kontext des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="7da45-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7da45-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7da45-110">Error codes</span></span>

<span data-ttu-id="7da45-111">Wenn die Eigenschaften Zugriffsmethoden **\_ chainContext platzieren** und **\_ chainContext** erfolgreich abrufen, geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7da45-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="7da45-112">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7da45-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7da45-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7da45-113">Remarks</span></span>

<span data-ttu-id="7da45-114">Zum Freigeben des Kontexts muss entweder die [**freecontext**](ichaincontext-freecontext.md) -Methode oder die [**certfreecertificatechain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) -Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7da45-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="7da45-115">Wenn Sie die **chainContext** -Eigenschaft festlegen, wird der Status des gesamten [**Kette**](chain.md) -Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7da45-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da45-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7da45-116">Requirements</span></span>



| <span data-ttu-id="7da45-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7da45-117">Requirement</span></span> | <span data-ttu-id="7da45-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7da45-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7da45-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7da45-119">Redistributable</span></span><br/> | <span data-ttu-id="7da45-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7da45-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7da45-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7da45-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="7da45-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7da45-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da45-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7da45-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da45-124">**Ichaincontext**</span><span class="sxs-lookup"><span data-stu-id="7da45-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




