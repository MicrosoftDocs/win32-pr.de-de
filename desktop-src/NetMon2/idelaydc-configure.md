---
description: Die Configure-Methode übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Idelta aydcconfigure-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484315"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="3d64d-103">Idelta aydc:: Configure-Methode</span><span class="sxs-lookup"><span data-stu-id="3d64d-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="3d64d-104">Die **configure** -Methode übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d64d-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d64d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d64d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3d64d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d64d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d64d-107">*hconfigurationblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d64d-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d64d-108">Handle für das BLOB, das die Konfigurationsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="3d64d-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="3d64d-109">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d64d-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d64d-110">Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="3d64d-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="3d64d-111">Informationen zum Inhalt eines Fehler-BLOB finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="3d64d-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d64d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d64d-112">Return value</span></span>

<span data-ttu-id="3d64d-113">Wenn diese Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3d64d-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3d64d-114">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="3d64d-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3d64d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3d64d-115">Return code</span></span>                                                                                                      | <span data-ttu-id="3d64d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d64d-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d64d-117"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="3d64d-118">Der NPP meldet, dass die Erfassungs Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="3d64d-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="3d64d-119"><dt>**nmerr-Datenträger \_ \_ nicht \_ lokal \_ korrigiert**</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="3d64d-120"><dt>**nmerr \_ konnte \_ keinen \_ Arbeits \_ Speicher erstellen.**</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="3d64d-121"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="3d64d-122">Es war kein Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3d64d-122">No memory was available.</span></span> <span data-ttu-id="3d64d-123">Fahren Sie Windows herunter, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3d64d-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="3d64d-124"><dt>**Ungültiger nmerr- \_ \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="3d64d-125">Das vom hconfiguration-Parameter angegebene konfigurationsblob ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3d64d-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d64d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d64d-126">Remarks</span></span>

<span data-ttu-id="3d64d-127">Sie müssen diese Methode anwenden, um eine NPP neu zu starten, die gestartet, beendet, aber nicht getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d64d-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="3d64d-128">Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hconfigurationblob* angegebenen Konfigurations-BLOB nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="3d64d-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="3d64d-129">Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3d64d-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="3d64d-130">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3d64d-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d64d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d64d-131">Requirements</span></span>



| <span data-ttu-id="3d64d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d64d-132">Requirement</span></span> | <span data-ttu-id="3d64d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3d64d-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d64d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d64d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3d64d-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d64d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3d64d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d64d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3d64d-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d64d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3d64d-138">Header</span><span class="sxs-lookup"><span data-stu-id="3d64d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d64d-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3d64d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3d64d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d64d-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d64d-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d64d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d64d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d64d-143">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="3d64d-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="3d64d-144">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="3d64d-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="3d64d-145">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="3d64d-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="3d64d-146">Idelta aydc:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="3d64d-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




