---
description: Führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende CAB-Datei heruntergeladen wurde.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Ieaxiservicecallback:: verifyfile-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529879"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="b47a0-103">Ieaxiservicecallback:: verifyfile-Methode</span><span class="sxs-lookup"><span data-stu-id="b47a0-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="b47a0-104">Die **verifyfile** -Methode führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende CAB-Datei heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b47a0-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b47a0-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="b47a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b47a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b47a0-107">*bstraufileurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b47a0-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b47a0-108">Die URL des zu überprüfen ActiveX-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b47a0-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="b47a0-109">*bstrapprovedfilename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b47a0-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b47a0-110">Der Name der Datei, in der die CAB-Datei, die dem ActiveX-Objekt zugeordnet ist, heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b47a0-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b47a0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b47a0-111">Return value</span></span>

<span data-ttu-id="b47a0-112">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b47a0-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="b47a0-113">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="b47a0-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b47a0-114">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="b47a0-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="b47a0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b47a0-115">Requirements</span></span>



| <span data-ttu-id="b47a0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b47a0-116">Requirement</span></span> | <span data-ttu-id="b47a0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b47a0-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47a0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b47a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b47a0-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b47a0-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b47a0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b47a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b47a0-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b47a0-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="b47a0-122">IID</span><span class="sxs-lookup"><span data-stu-id="b47a0-122">IID</span></span><br/>                      | <span data-ttu-id="b47a0-123">IID \_ ieaxiservicecallback ist als 1823e7ba-ec36-447a-9b2e-b4912e15afe7 definiert.</span><span class="sxs-lookup"><span data-stu-id="b47a0-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b47a0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b47a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47a0-125">**Ieaxiservicecallback**</span><span class="sxs-lookup"><span data-stu-id="b47a0-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

