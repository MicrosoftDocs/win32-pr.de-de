---
description: Die scesvasetachmentconfig-Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System konfiguriert ist.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Scesvcalltachmentconfig-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750872"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="896be-103">Scesvcalltachmentconfig-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="896be-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="896be-104">Die **scesvasetachmentconfig** -Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="896be-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="896be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="896be-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="896be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="896be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896be-107">*pscecbinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="896be-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896be-108">Zeiger auf eine [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur, die das Daten Bank Handle und die Rückruf Funktionen enthält, um Informationen abzufragen, festzulegen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="896be-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896be-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="896be-109">Return value</span></span>

<span data-ttu-id="896be-110">Wenn diese Funktion erfolgreich ausgeführt wird, wird "scestatus Success" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="896be-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="896be-111">Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="896be-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="896be-112">Weitere Informationen zu den Sicherheits Konfigurations-Fehlercodes finden Sie unter [Anhang Return Values](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="896be-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="896be-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="896be-113">Remarks</span></span>

<span data-ttu-id="896be-114">Verwenden Sie bei der Implementierung dieser Funktion die Rückruffunktion, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfqueryinfo) verwiesen wird, um Konfigurationsinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="896be-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="896be-115">Konfigurieren Sie dann den Dienst mithilfe der zurückgegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="896be-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="896be-116">Diese Funktion muss folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="896be-116">This function must do the following:</span></span>

-   <span data-ttu-id="896be-117">Abfragen von Konfigurationsinformationen aus dem Sicherheitskonfigurations Tool, die mithilfe der Rückruffunktion festgelegt werden, auf die das **pfqueryinfo** -Element der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur verweist (pscecbinfo->pfqueryinfo).</span><span class="sxs-lookup"><span data-stu-id="896be-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="896be-118">Konfigurieren Sie den Dienst mithilfe der Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="896be-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="896be-119">Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentconfig](implementing-scesvcattachmentconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="896be-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="896be-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="896be-120">Requirements</span></span>



| <span data-ttu-id="896be-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="896be-121">Requirement</span></span> | <span data-ttu-id="896be-122">Wert</span><span class="sxs-lookup"><span data-stu-id="896be-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="896be-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="896be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="896be-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="896be-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="896be-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="896be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="896be-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="896be-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="896be-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="896be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896be-128">**scesvc- \_ Rückruf \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="896be-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="896be-129">**Scesvpetachmentanalysis**</span><span class="sxs-lookup"><span data-stu-id="896be-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




