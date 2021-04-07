---
description: Die Anwendung wird von der APP- \_ Authentifizierungsmethode authentifiziert. Sie ermöglicht es einer Anwendung, sich selbst zu authentifizieren (mithilfe eines Challenge/Signature-Protokolls), wenn die Authentifizierung von einer Smartcard angefordert wird.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'Iscardauth:: APP_Auth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863532"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="6256d-104">Iscardauth:: App-Authentifizierungs \_ Methode</span><span class="sxs-lookup"><span data-stu-id="6256d-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="6256d-105">\[Die **App \_** -Authentifizierungsmethode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6256d-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6256d-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6256d-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6256d-107">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6256d-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6256d-108">Die Anwendung wird von der APP-Authentifizierungsmethode authentifiziert. **\_**</span><span class="sxs-lookup"><span data-stu-id="6256d-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="6256d-109">Sie ermöglicht es einer Anwendung, sich selbst zu authentifizieren (mithilfe eines Challenge/Signature-Protokolls), wenn die Authentifizierung von einer [*Smartcard*](../secgloss/s-gly.md)angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="6256d-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6256d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6256d-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="6256d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6256d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6256d-112">*lalgoid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6256d-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6256d-113">Der Algorithmus, der beim Authentifizierungsprozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6256d-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="6256d-114">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6256d-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6256d-115">Ein [**ibytebuffer**](ibytebuffer.md) mit anbieterspezifischen Parametern des Authentifizierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="6256d-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="6256d-116">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6256d-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6256d-117">Erforderliche Daten für die Berechnung.</span><span class="sxs-lookup"><span data-stu-id="6256d-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6256d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6256d-118">Return value</span></span>

<span data-ttu-id="6256d-119">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6256d-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6256d-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6256d-120">Return code</span></span>                                                                                   | <span data-ttu-id="6256d-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6256d-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6256d-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6256d-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6256d-123">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6256d-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6256d-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6256d-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6256d-125">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="6256d-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6256d-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="6256d-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6256d-127">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6256d-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6256d-128"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6256d-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6256d-129">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6256d-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6256d-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6256d-130">Remarks</span></span>

<span data-ttu-id="6256d-131">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardauth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="6256d-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="6256d-132">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6256d-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6256d-133">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6256d-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6256d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6256d-134">Requirements</span></span>



| <span data-ttu-id="6256d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6256d-135">Requirement</span></span> | <span data-ttu-id="6256d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6256d-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6256d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6256d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6256d-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6256d-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6256d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6256d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6256d-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6256d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6256d-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6256d-141">End of client support</span></span><br/>    | <span data-ttu-id="6256d-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6256d-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6256d-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6256d-143">End of server support</span></span><br/>    | <span data-ttu-id="6256d-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6256d-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6256d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6256d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6256d-146">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="6256d-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="6256d-147">**Ibytebuffer**</span><span class="sxs-lookup"><span data-stu-id="6256d-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
