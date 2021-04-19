---
description: Übermittelt Konfigurationsdaten für eine Datenerfassung.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Untc:: Configure-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353045"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="756a3-103">Untc:: Configure-Methode</span><span class="sxs-lookup"><span data-stu-id="756a3-103">IRTC::Configure method</span></span>

<span data-ttu-id="756a3-104">Die [**configure**](configure.md) -Methode übermittelt Konfigurationsdaten für eine Datenerfassung.</span><span class="sxs-lookup"><span data-stu-id="756a3-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="756a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="756a3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="756a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="756a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="756a3-107">*hconfigurationblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="756a3-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="756a3-108">Ein Handle für das BLOB, das vom Aufrufer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="756a3-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="756a3-109">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="756a3-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="756a3-110">Ein Handle für ein fehlerblob, das zusätzliche Fehler Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="756a3-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="756a3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="756a3-111">Return value</span></span>

<span data-ttu-id="756a3-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="756a3-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="756a3-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="756a3-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="756a3-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="756a3-114">Return code</span></span>                                                                                                         | <span data-ttu-id="756a3-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="756a3-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="756a3-116"><dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="756a3-117">Die Methode " **kreateblob** " wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="756a3-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="756a3-118"><dt>**Ungültiges nmerr- \_ \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="756a3-119">Das Objekt, auf das verwiesen wird, ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="756a3-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="756a3-120"><dt>**nmerr- \_ Uplevel- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="756a3-121">Die BLOB-Versionsnummer ist falsch.</span><span class="sxs-lookup"><span data-stu-id="756a3-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="756a3-122"><dt>**der nmerr- \_ \_ blobeintrag ist \_ bereits \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="756a3-123">Dupliziertes BLOB.</span><span class="sxs-lookup"><span data-stu-id="756a3-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="756a3-124"><dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="756a3-125">Für das von *hconfigurationblob* angegebene Konfigurations-BLOB fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="756a3-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="756a3-126">Zeigen Sie das von *herrorblob* zurückgegebene fehlerblob an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="756a3-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="756a3-127"><dt>**mehrdeutiger nmerr- \_ \_ Spezifizierer**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="756a3-128">Die BLOB-Besitzer-oder Kategoriedaten fehlen.</span><span class="sxs-lookup"><span data-stu-id="756a3-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="756a3-129"><dt>**nmerr- \_ BLOB- \_ Besitzer \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="756a3-130">Der Abschnitt "BLOB-Besitzer" wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="756a3-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="756a3-131"><dt>**nmerr- \_ BLOB- \_ Kategorie \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="756a3-132">Der Abschnitt "BLOB-Kategorie" wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="756a3-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="756a3-133"><dt>**Unbekannte nmerr- \_ \_ Kategorie**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="756a3-134">Der Abschnitt BLOB Category wurde gefunden, aber nicht verstanden.</span><span class="sxs-lookup"><span data-stu-id="756a3-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="756a3-135"><dt>**Unbekanntes nmerr- \_ \_ Tag**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="756a3-136">Der BLOB-Tagabschnitt wurde gefunden, aber nicht verstanden.</span><span class="sxs-lookup"><span data-stu-id="756a3-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="756a3-137"><dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="756a3-138">Das BLOB ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="756a3-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="756a3-139"><dt>**nmerr-Fehler (unzulässig) \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="756a3-140">Der Auslöse Teil des BLOBs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="756a3-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="756a3-141"><dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="756a3-142">Die Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="756a3-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="756a3-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="756a3-143">Remarks</span></span>

<span data-ttu-id="756a3-144">Sie müssen diese Methode anwenden, um eine NPP neu zu starten, die gestartet, beendet, aber nicht getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="756a3-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="756a3-145">Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hconfigurationblob* angegebenen Konfigurations-BLOB nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="756a3-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="756a3-146">Das zurückgegebene fehlerblob enthält Fehler Daten, die von der Anwendung für die Problembehandlung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="756a3-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="756a3-147">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag, Netzwerkmonitor nicht finden kann, im zurückgegebenen fehlerblob enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="756a3-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="756a3-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="756a3-148">Requirements</span></span>



| <span data-ttu-id="756a3-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="756a3-149">Requirement</span></span> | <span data-ttu-id="756a3-150">Wert</span><span class="sxs-lookup"><span data-stu-id="756a3-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756a3-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="756a3-151">Minimum supported client</span></span><br/> | <span data-ttu-id="756a3-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="756a3-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="756a3-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="756a3-153">Minimum supported server</span></span><br/> | <span data-ttu-id="756a3-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="756a3-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="756a3-155">Header</span><span class="sxs-lookup"><span data-stu-id="756a3-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="756a3-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="756a3-157">DLL</span><span class="sxs-lookup"><span data-stu-id="756a3-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="756a3-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="756a3-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756a3-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="756a3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756a3-160">"Iran"</span><span class="sxs-lookup"><span data-stu-id="756a3-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="756a3-161">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="756a3-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="756a3-162">BlobNetzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="756a3-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




