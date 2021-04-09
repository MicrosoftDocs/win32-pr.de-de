---
description: Die scesvasetachmentanalysis-Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System analysiert wird.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Scesvcalltachmentanalysis-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750873"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="e3f9d-103">Scesvcalltachmentanalysis-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="e3f9d-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="e3f9d-104">Die **scesvasetachmentanalysis** -Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f9d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3f9d-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e3f9d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3f9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f9d-107">*pscecbinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3f9d-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f9d-108">Zeiger auf eine [**scesvc \_ - \_ Rückruf**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Informationsstruktur, die ein undurchsichtiges Daten Bank Handle und Rückruf Funktionszeiger auf Abfrage-, festgelegte und kostenlose Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f9d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3f9d-109">Return value</span></span>

<span data-ttu-id="e3f9d-110">Wenn diese Funktion erfolgreich ausgeführt wird, wird "scestatus Success" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e3f9d-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="e3f9d-111">Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="e3f9d-112">Weitere Informationen zu den Sicherheits Konfigurations-Fehlercodes finden Sie unter [Anhang Return Values](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e3f9d-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f9d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3f9d-113">Remarks</span></span>

<span data-ttu-id="e3f9d-114">Die **scesvtortachmentanalysis** -Funktion muss folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="e3f9d-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="e3f9d-115">Direkte Abfrage von Konfigurationsinformationen aus dem Dienst.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="e3f9d-116">Rufen Sie die Rückruffunktion auf, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Informationsstruktur (pscecbinfo->pfqueryinfo) verwiesen wird, um Informationen aus der Sicherheitsdatenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="e3f9d-117">Berechnen Sie die Unterschiede zwischen den Informationen auf der Grundlage von Typ und Syntax.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="e3f9d-118">Rufen Sie die Rückruffunktion auf, auf die vom **pfset** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfabtinfo) verwiesen wird, um die Sicherheitsdatenbank mit den abgerufenen Dienst Informationen zu aktualisieren, die sich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e3f9d-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="e3f9d-119">Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentanalysis](implementing-scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="e3f9d-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f9d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3f9d-120">Requirements</span></span>



| <span data-ttu-id="e3f9d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3f9d-121">Requirement</span></span> | <span data-ttu-id="e3f9d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e3f9d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e3f9d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3f9d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f9d-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3f9d-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e3f9d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3f9d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f9d-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3f9d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3f9d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3f9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f9d-128">Implementieren von scesvpetachmentanalysis</span><span class="sxs-lookup"><span data-stu-id="e3f9d-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="e3f9d-129">**scesvc- \_ Rückruf \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="e3f9d-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="e3f9d-130">**Scesvalisitachmentconfig**</span><span class="sxs-lookup"><span data-stu-id="e3f9d-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




