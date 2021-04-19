---
description: Legt den pccert-Kontext eines Zertifikats fest oder ruft ihn ab \_ .
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Icertcontext:: certcontext-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361979"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="65fa0-103">Icertcontext:: certcontext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="65fa0-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="65fa0-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="65fa0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="65fa0-105">Die **certcontext** -Eigenschaft legt den pccert- \_ Kontext eines Zertifikats fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="65fa0-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="65fa0-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="65fa0-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fa0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="65fa0-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="65fa0-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="65fa0-108">Property value</span></span>

<span data-ttu-id="65fa0-109">Der pccert- \_ Kontext des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="65fa0-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65fa0-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="65fa0-110">Error codes</span></span>

<span data-ttu-id="65fa0-111">Wenn die Eigenschaften Zugriffsmethoden **\_ certcontext platzieren** und **\_ certcontext** erfolgreich abrufen, geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="65fa0-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="65fa0-112">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="65fa0-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="65fa0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65fa0-113">Remarks</span></span>

<span data-ttu-id="65fa0-114">Sie müssen entweder die [**freecontext**](icertcontext-freecontext.md) -Methode oder die [**certfreecertifitorecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion abrufen, um den kontextfrei zugeben.</span><span class="sxs-lookup"><span data-stu-id="65fa0-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="65fa0-115">Wenn Sie die **certcontext** -Eigenschaft festlegen, wird der Status des gesamten [**Zertifikat**](certificate.md) Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="65fa0-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="65fa0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65fa0-116">Requirements</span></span>



| <span data-ttu-id="65fa0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65fa0-117">Requirement</span></span> | <span data-ttu-id="65fa0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="65fa0-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65fa0-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="65fa0-119">Redistributable</span></span><br/> | <span data-ttu-id="65fa0-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="65fa0-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="65fa0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="65fa0-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="65fa0-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65fa0-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65fa0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65fa0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fa0-124">**Icertcontext**</span><span class="sxs-lookup"><span data-stu-id="65fa0-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




