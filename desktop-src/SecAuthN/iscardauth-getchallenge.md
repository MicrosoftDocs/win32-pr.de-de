---
description: Die getchallenge-Methode gibt eine Herausforderung von der Smartcard zurück.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'Iscardauth:: getchallenge-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215109"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="624e4-103">Iscardauth:: getchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="624e4-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="624e4-104">\[Die **getchallenge** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="624e4-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="624e4-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="624e4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="624e4-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="624e4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="624e4-107">Die **getchallenge** -Methode gibt eine Herausforderung von der [*Smartcard*](../secgloss/s-gly.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="624e4-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="624e4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="624e4-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="624e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="624e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624e4-110">*lalgoid* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="624e4-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="624e4-111">Der Algorithmus, der beim Authentifizierungsprozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="624e4-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="624e4-112">*llengthof Challenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="624e4-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="624e4-113">Maximale Länge der erwarteten Antwort.</span><span class="sxs-lookup"><span data-stu-id="624e4-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="624e4-114">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="624e4-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="624e4-115">Ein [**ibytebuffer**](ibytebuffer.md) -Objekt, das herstellerspezifische Parameter des Authentifizierungsprozesses enthält.</span><span class="sxs-lookup"><span data-stu-id="624e4-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="624e4-116">*pbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="624e4-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="624e4-117">Bei der Eingabe verweist auf den Puffer.</span><span class="sxs-lookup"><span data-stu-id="624e4-117">On input, points to the buffer.</span></span>

<span data-ttu-id="624e4-118">Bei der Ausgabe enthält die Abfrage Daten von der Karte.</span><span class="sxs-lookup"><span data-stu-id="624e4-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="624e4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="624e4-119">Return value</span></span>

<span data-ttu-id="624e4-120">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="624e4-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="624e4-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="624e4-121">Return code</span></span>                                                                                   | <span data-ttu-id="624e4-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="624e4-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="624e4-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="624e4-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="624e4-124">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="624e4-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="624e4-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="624e4-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="624e4-126">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="624e4-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="624e4-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="624e4-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="624e4-128">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="624e4-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="624e4-129"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="624e4-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="624e4-130">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="624e4-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="624e4-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="624e4-131">Remarks</span></span>

<span data-ttu-id="624e4-132">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardauth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="624e4-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="624e4-133">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="624e4-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="624e4-134">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="624e4-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="624e4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="624e4-135">Requirements</span></span>



| <span data-ttu-id="624e4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="624e4-136">Requirement</span></span> | <span data-ttu-id="624e4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="624e4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="624e4-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="624e4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="624e4-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="624e4-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="624e4-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="624e4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="624e4-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="624e4-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="624e4-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="624e4-142">End of client support</span></span><br/>    | <span data-ttu-id="624e4-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="624e4-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="624e4-144">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="624e4-144">End of server support</span></span><br/>    | <span data-ttu-id="624e4-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="624e4-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="624e4-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="624e4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624e4-147">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="624e4-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
