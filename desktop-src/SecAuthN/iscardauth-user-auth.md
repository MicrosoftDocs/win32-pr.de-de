---
description: Die Benutzer \_ Authentifizierungsmethode ermöglicht den Zugriff auf Benutzer Authentifizierungsdienste.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'Iscardauth:: User_Auth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862407"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="901a7-103">Iscardauth:: User \_ auth-Methode</span><span class="sxs-lookup"><span data-stu-id="901a7-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="901a7-104">\[Die **Benutzer \_** Authentifizierungsmethode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="901a7-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="901a7-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="901a7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="901a7-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="901a7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="901a7-107">Die **Benutzer \_** Authentifizierungsmethode ermöglicht den Zugriff auf Benutzer Authentifizierungsdienste.</span><span class="sxs-lookup"><span data-stu-id="901a7-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="901a7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="901a7-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="901a7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="901a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="901a7-110">*lAlgorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="901a7-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901a7-111">Der Algorithmus, der beim Authentifizierungsprozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="901a7-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="901a7-112">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="901a7-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901a7-113">Ein [**ibytebuffer**](ibytebuffer.md) -Objekt, das herstellerspezifische Parameter des Authentifizierungsprozesses enthält.</span><span class="sxs-lookup"><span data-stu-id="901a7-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="901a7-114">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="901a7-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901a7-115">Die im Authentifizierungsprozess zu verwendenden Daten.</span><span class="sxs-lookup"><span data-stu-id="901a7-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="901a7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="901a7-116">Return value</span></span>

<span data-ttu-id="901a7-117">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="901a7-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="901a7-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="901a7-118">Return code</span></span>                                                                                   | <span data-ttu-id="901a7-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="901a7-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="901a7-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="901a7-121">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="901a7-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="901a7-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="901a7-123">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="901a7-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="901a7-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="901a7-125">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="901a7-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="901a7-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="901a7-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="901a7-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="901a7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="901a7-128">Remarks</span></span>

<span data-ttu-id="901a7-129">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardauth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="901a7-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="901a7-130">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="901a7-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="901a7-131">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="901a7-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="901a7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="901a7-132">Requirements</span></span>



| <span data-ttu-id="901a7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="901a7-133">Requirement</span></span> | <span data-ttu-id="901a7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="901a7-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="901a7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="901a7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="901a7-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="901a7-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="901a7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="901a7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="901a7-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="901a7-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="901a7-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="901a7-139">End of client support</span></span><br/>    | <span data-ttu-id="901a7-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="901a7-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="901a7-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="901a7-141">End of server support</span></span><br/>    | <span data-ttu-id="901a7-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="901a7-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="901a7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="901a7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="901a7-144">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="901a7-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="901a7-145">**Ibytebuffer**</span><span class="sxs-lookup"><span data-stu-id="901a7-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
