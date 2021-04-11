---
description: Die Configure-Methode übermittelt Informationen zur Aufzeichnungs Konfiguration.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'IStats:: Configure-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217799"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="04c95-103">IStats:: Configure-Methode</span><span class="sxs-lookup"><span data-stu-id="04c95-103">IStats::Configure method</span></span>

<span data-ttu-id="04c95-104">Die **configure** -Methode übermittelt Informationen zur Aufzeichnungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="04c95-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c95-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04c95-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="04c95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04c95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c95-107">*hconfigurationblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04c95-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04c95-108">Handle für das BLOB, das vom Aufrufer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="04c95-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="04c95-109">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="04c95-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04c95-110">Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="04c95-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04c95-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04c95-111">Return value</span></span>

<span data-ttu-id="04c95-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="04c95-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="04c95-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="04c95-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="04c95-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="04c95-114">Return code</span></span>                                                                                                         | <span data-ttu-id="04c95-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04c95-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04c95-116"><dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="04c95-117">Die Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="04c95-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="04c95-118"><dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="04c95-119">Die Methode " **kreateblob** " wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="04c95-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="04c95-120"><dt>**Ungültiges nmerr- \_ \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="04c95-121">Das Objekt, auf das verwiesen wird, ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="04c95-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="04c95-122"><dt>**nmerr- \_ Uplevel- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="04c95-123">Die BLOB-Versionsnummer ist falsch.</span><span class="sxs-lookup"><span data-stu-id="04c95-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="04c95-124"><dt>**der nmerr- \_ \_ blobeintrag ist \_ bereits \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="04c95-125">Ein BLOB-Eintrag ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="04c95-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="04c95-126"><dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="04c95-127">Für das vom *hconfigurationblob* -Parameter angegebene konfigurationsblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="04c95-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="04c95-128">Sehen Sie sich den vom " *herrorblob* "-Parameter zurückgegebenen fehlerblob an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="04c95-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="04c95-129"><dt>**mehrdeutiger nmerr- \_ \_ Spezifizierer**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="04c95-130">Im BLOB fehlen Besitzer-oder Kategorieinformationen.</span><span class="sxs-lookup"><span data-stu-id="04c95-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="04c95-131"><dt>**nmerr- \_ BLOB- \_ Besitzer \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="04c95-132">Der Besitzer Abschnitt des BLOBs wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="04c95-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="04c95-133"><dt>**nmerr- \_ BLOB- \_ Kategorie \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="04c95-134">Der Kategorieabschnitt des BLOBs wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="04c95-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="04c95-135"><dt>**Unbekannte nmerr- \_ \_ Kategorie**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="04c95-136">Die Kategorieinformationen wurden gefunden, aber nicht verstanden.</span><span class="sxs-lookup"><span data-stu-id="04c95-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="04c95-137"><dt>**Unbekanntes nmerr- \_ \_ Tag**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="04c95-138">Taginformationen wurden gefunden, aber nicht verstanden.</span><span class="sxs-lookup"><span data-stu-id="04c95-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="04c95-139"><dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="04c95-140">Das BLOB ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="04c95-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="04c95-141"><dt>**nmerr-Fehler (unzulässig) \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="04c95-142">Der Auslöse Teil des BLOBs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="04c95-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="04c95-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04c95-143">Remarks</span></span>

<span data-ttu-id="04c95-144">Sie müssen diese Methode anwenden, um eine NPP, die gestartet, beendet, aber nicht getrennt wurde, neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="04c95-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="04c95-145">Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor im Konfigurations-BLOB, das im *hconfigurationblob* -Parameter angegeben ist, nicht verstehen oder finden konnte.</span><span class="sxs-lookup"><span data-stu-id="04c95-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="04c95-146">Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="04c95-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="04c95-147">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="04c95-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="04c95-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04c95-148">Requirements</span></span>



| <span data-ttu-id="04c95-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04c95-149">Requirement</span></span> | <span data-ttu-id="04c95-150">Wert</span><span class="sxs-lookup"><span data-stu-id="04c95-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c95-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04c95-151">Minimum supported client</span></span><br/> | <span data-ttu-id="04c95-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04c95-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="04c95-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04c95-153">Minimum supported server</span></span><br/> | <span data-ttu-id="04c95-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04c95-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="04c95-155">Header</span><span class="sxs-lookup"><span data-stu-id="04c95-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="04c95-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="04c95-157">DLL</span><span class="sxs-lookup"><span data-stu-id="04c95-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04c95-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04c95-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04c95-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04c95-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04c95-160">IStats</span><span class="sxs-lookup"><span data-stu-id="04c95-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="04c95-161">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="04c95-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="04c95-162">BlobNetzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="04c95-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




