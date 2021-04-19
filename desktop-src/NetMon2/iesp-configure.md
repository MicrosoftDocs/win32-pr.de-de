---
description: Die Configure-Methode übermittelt Konfigurationsinformationen für eine Erfassung.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP:: Configure-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353017"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="0c477-103">IESP:: Configure-Methode</span><span class="sxs-lookup"><span data-stu-id="0c477-103">IESP::Configure method</span></span>

<span data-ttu-id="0c477-104">Die **configure** -Methode übermittelt Konfigurationsinformationen für eine Erfassung.</span><span class="sxs-lookup"><span data-stu-id="0c477-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c477-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c477-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="0c477-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c477-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c477-107">*hconfigurationblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c477-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c477-108">Handle für das BLOB, das vom Aufrufer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="0c477-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="0c477-109">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c477-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c477-110">Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="0c477-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="0c477-111">Informationen zum Inhalt eines Fehler-BLOB finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="0c477-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c477-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c477-112">Return value</span></span>

<span data-ttu-id="0c477-113">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0c477-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0c477-114">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="0c477-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0c477-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0c477-115">Return code</span></span>                                                                                                         | <span data-ttu-id="0c477-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c477-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c477-117"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="0c477-118">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="0c477-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="0c477-119"><dt>**nmerr \_ nicht \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="0c477-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0c477-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="0c477-121"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="0c477-122">Der NPP meldet, dass die Erfassungs Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="0c477-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="0c477-123"><dt>**nmerr-Fehler (unzulässig) \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="0c477-124">Der Auslöse Teil des konfigurationsblobs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="0c477-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="0c477-125"><dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="0c477-126">Für das von *hconfigurationblob* angegebene konfigurationsblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0c477-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="0c477-127">Sehen Sie sich den von *herrorblob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="0c477-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="0c477-128"><dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="0c477-129">Das BLOB ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="0c477-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="0c477-130"><dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="0c477-131">Die Methode " **kreateblob** " wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c477-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="0c477-132"><dt>**Ungültiges nmerr- \_ \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="0c477-133">Das Objekt, auf das verwiesen wird, ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c477-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="0c477-134"><dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="0c477-135">Die Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="0c477-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="0c477-136"><dt>**nmerr- \_ Uplevel- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="0c477-137">Die BLOB-Versionsnummer ist falsch.</span><span class="sxs-lookup"><span data-stu-id="0c477-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="0c477-138"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="0c477-139">Es war kein Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c477-139">No memory was available.</span></span> <span data-ttu-id="0c477-140">Fahren Sie Windows herunter, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0c477-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="0c477-141"><dt>**nmerr- \_ Timeout**</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="0c477-142">Timeout für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0c477-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="0c477-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c477-143">Remarks</span></span>

<span data-ttu-id="0c477-144">Sie müssen diese Methode anwenden, um eine NPP neu zu starten, die gestartet und beendet wurde, jedoch nicht getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="0c477-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="0c477-145">Das vom " *herrorblob* "-Parameter zurückgegebene Fehler-BLOB enthält Einträge, die Netzwerkmonitor in dem in *hconfigurationblob* angegebenen Konfigurations-BLOB nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="0c477-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="0c477-146">Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0c477-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="0c477-147">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0c477-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c477-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c477-148">Requirements</span></span>



| <span data-ttu-id="0c477-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c477-149">Requirement</span></span> | <span data-ttu-id="0c477-150">Wert</span><span class="sxs-lookup"><span data-stu-id="0c477-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c477-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c477-151">Minimum supported client</span></span><br/> | <span data-ttu-id="0c477-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c477-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0c477-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c477-153">Minimum supported server</span></span><br/> | <span data-ttu-id="0c477-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c477-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0c477-155">Header</span><span class="sxs-lookup"><span data-stu-id="0c477-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c477-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0c477-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0c477-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c477-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c477-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




