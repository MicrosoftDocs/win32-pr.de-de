---
description: Mit der \_ Methode "ICC auth" kann eine Anwendung die Smartcard authentifizieren.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'Iscardauth:: ICC_Auth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958876"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="0023b-103">Iscardauth:: ICC \_ auth-Methode</span><span class="sxs-lookup"><span data-stu-id="0023b-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="0023b-104">\[Die Methode " **ICC \_ auth** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0023b-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0023b-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0023b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0023b-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0023b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0023b-107">Mit der Methode " **ICC \_ auth** " kann eine Anwendung die Smartcard authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="0023b-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="0023b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0023b-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0023b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0023b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0023b-110">*lalgoid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0023b-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0023b-111">Der Algorithmus, der beim Authentifizierungsprozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0023b-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="0023b-112">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0023b-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0023b-113">Ein [**ibytebuffer**](ibytebuffer.md) -Objekt, das herstellerspezifische Parameter des Authentifizierungsprozesses enthält.</span><span class="sxs-lookup"><span data-stu-id="0023b-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="0023b-114">*pbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0023b-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0023b-115">Enthält bei der Eingabedaten, die im Authentifizierungsprozess verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0023b-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="0023b-116">Bei Ausgabe enthält das Ergebnis des Authentifizierungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0023b-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0023b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0023b-117">Return value</span></span>

<span data-ttu-id="0023b-118">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0023b-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0023b-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0023b-119">Return code</span></span>                                                                                   | <span data-ttu-id="0023b-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0023b-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0023b-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0023b-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0023b-122">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0023b-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0023b-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0023b-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0023b-124">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="0023b-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0023b-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0023b-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0023b-126">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0023b-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0023b-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0023b-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0023b-128">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0023b-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0023b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0023b-129">Remarks</span></span>

<span data-ttu-id="0023b-130">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardauth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="0023b-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="0023b-131">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0023b-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0023b-132">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0023b-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0023b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0023b-133">Requirements</span></span>



| <span data-ttu-id="0023b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0023b-134">Requirement</span></span> | <span data-ttu-id="0023b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0023b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0023b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0023b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0023b-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0023b-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0023b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0023b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0023b-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0023b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0023b-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0023b-140">End of client support</span></span><br/>    | <span data-ttu-id="0023b-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0023b-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0023b-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0023b-142">End of server support</span></span><br/>    | <span data-ttu-id="0023b-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0023b-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0023b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0023b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0023b-145">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="0023b-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
