---
description: Die scesvasetachmentupdate-Funktion wird von den Snap-Ins für die Sicherheitskonfiguration aufgerufen, um Konfigurationsänderungen an die Sicherheitsdatenbank zu übergeben.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Scesvcalltachmentupdate-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750865"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="7ff61-103">Scesvcalltachmentupdate-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="7ff61-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="7ff61-104">Die **scesvasetachmentupdate** -Funktion wird von den Snap-Ins für die Sicherheitskonfiguration aufgerufen, um Konfigurationsänderungen an die Sicherheitsdatenbank zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="7ff61-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ff61-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7ff61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ff61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff61-107">*pscecbinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff61-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff61-108">Zeiger auf eine [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur, die das Rückruf Handle und Funktionszeiger auf SCE enthält.</span><span class="sxs-lookup"><span data-stu-id="7ff61-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="7ff61-109">*Serviceingefo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff61-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff61-110">Aktualisierte Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-110">Updated configuration information.</span></span> <span data-ttu-id="7ff61-111">Die Datenstruktur, die für diese Informationen verwendet wird, sind [**scesvc- \_ Konfigurations \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span><span class="sxs-lookup"><span data-stu-id="7ff61-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff61-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ff61-112">Return value</span></span>

<span data-ttu-id="7ff61-113">Wenn diese Funktion erfolgreich ausgeführt wird, wird "scestatus Success" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="7ff61-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="7ff61-114">Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ff61-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="7ff61-115">Weitere Informationen zu den Sicherheits Konfigurations-Fehlercodes finden Sie unter [Anhang Return Values](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7ff61-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff61-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ff61-116">Remarks</span></span>

<span data-ttu-id="7ff61-117">Die **scesvtortachmentupdate** -Funktion muss folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="7ff61-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="7ff61-118">Rufen Sie die Rückruffunktion auf, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfqueryinfo) verwiesen wird, um die aktuellen Basis Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="7ff61-119">Rufen Sie die Rückruffunktion auf, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfqueryinfo) verwiesen wird, um den letzten Satz von unterschieden (Analyse Informationen) aus der Sicherheitsdatenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="7ff61-120">Verwenden Sie die bereitgestellten Dienst Informationen (siehe *serviceInfo*), um die neue Basiskonfiguration zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="7ff61-121">Verwenden Sie die bereitgestellten Dienst Informationen (siehe *serviceInfo*) und die Analyse, um die neuen Differenz Informationen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="7ff61-122">Rufen Sie die Rückruffunktion auf, auf die vom **pfsetinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfsetinfo) verwiesen wird, um die neue Basiskonfiguration in der Sicherheitsdatenbank festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="7ff61-123">Rufen Sie die Rückruffunktion auf, auf die vom **pfsetinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfsetinfo) verwiesen wird, um die neuen Analyse Informationen in der Sicherheitsdatenbank festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7ff61-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="7ff61-124">Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentupdate](implementing-scesvcattachmentupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff61-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff61-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ff61-125">Requirements</span></span>



| <span data-ttu-id="7ff61-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ff61-126">Requirement</span></span> | <span data-ttu-id="7ff61-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7ff61-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ff61-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ff61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff61-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ff61-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7ff61-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ff61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff61-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ff61-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ff61-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ff61-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff61-133">**scesvc- \_ Rückruf \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="7ff61-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="7ff61-134">**scesvc- \_ Konfigurations \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="7ff61-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




