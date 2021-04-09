---
title: Inapsystemhealthagentcallback processsohresponse-Methode (napsystemhealthagent. h)
description: Wird aufgerufen, wenn der NAPAgent eine sohresponse empfängt, die für diesen Integritäts-Agent bestimmt ist.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Processsohresponse-Methode NAP
- Processsohresponse-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, processsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956608"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="7a5f0-106">Inapsystemhealthagentcallback::P rocesssohresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="7a5f0-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="7a5f0-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7a5f0-108">Die **inapsystemhealthagentcallback::P rocesssohresponse** -Methode wird aufgerufen, wenn der NAPAgent eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) empfängt, die für diesen Integritäts-Agent bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5f0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a5f0-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="7a5f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a5f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5f0-111">*Anforderung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a5f0-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5f0-112">Ein com-Zeiger auf ein [**inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md) -Objekt, das das Anforderungs Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5f0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a5f0-113">Return value</span></span>

<span data-ttu-id="7a5f0-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7a5f0-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7a5f0-115">Return code</span></span>                                                                                            | <span data-ttu-id="7a5f0-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a5f0-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a5f0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f0-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="7a5f0-118">Gibt die erfolgreiche Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="7a5f0-119"><dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f0-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="7a5f0-120">Wird von dieser Implementierung zurückgegeben, wenn die Antwort nicht das richtige Format hat.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a5f0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a5f0-121">Remarks</span></span>

<span data-ttu-id="7a5f0-122">Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="7a5f0-123">Wenn der NAPAgent eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) empfängt, die für diesen Integritäts-Agent bestimmt ist, ruft er diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="7a5f0-124">Der Integritäts-Agent muss die sohresponse vom Anforderungs Objekt Abfragen.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="7a5f0-125">Er darf keine Verweise auf das Anforderungs Objekt enthalten, nachdem dieser-Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="7a5f0-126">Die **inapsystemhealthagentcallback::P rocesssohresponse** -Methode darf nicht blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="7a5f0-127">Wenn eine Korrektur Verarbeitung erforderlich ist, muss jede Implementierung von **processsohresponse** einen neuen Thread starten, um die Verarbeitungs Verarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="7a5f0-128">Der NAPAgent muss [**inapsystemhealthagentcallback:: getfixupinfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) aufrufen, um den Korrektur Status des SHA zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="7a5f0-129">Diese Methode muss ein **\_ \_ Ungültiges NAP \_ E-Paket** zurückgeben, wenn die Antwort nicht das richtige Format hat.</span><span class="sxs-lookup"><span data-stu-id="7a5f0-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5f0-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a5f0-130">Requirements</span></span>



| <span data-ttu-id="7a5f0-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a5f0-131">Requirement</span></span> | <span data-ttu-id="7a5f0-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7a5f0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5f0-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a5f0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5f0-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a5f0-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7a5f0-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a5f0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5f0-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a5f0-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7a5f0-137">Header</span><span class="sxs-lookup"><span data-stu-id="7a5f0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5f0-138"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f0-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a5f0-139">IDL</span><span class="sxs-lookup"><span data-stu-id="7a5f0-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a5f0-140"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f0-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5f0-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a5f0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5f0-142">**Inapsystemhealthagentcallback**</span><span class="sxs-lookup"><span data-stu-id="7a5f0-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





