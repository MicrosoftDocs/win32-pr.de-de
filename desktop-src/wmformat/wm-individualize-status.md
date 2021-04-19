---
title: WM_INDIVIDUALIZE_STATUS Struktur (drmexternals. h)
description: Die WM \_ Individual- \_ Status Struktur zeichnet den Status des Individualisierungs Vorgangs auf.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS Struktur-Windows Media-Format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346313"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="a36fc-104">WM_INDIVIDUALIZE_STATUS Struktur (drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="a36fc-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="a36fc-105">Die **WM \_ Individual- \_ Status** Struktur zeichnet den Status des [*Individualisierungs*](wmformat-glossary.md) Vorgangs auf.</span><span class="sxs-lookup"><span data-stu-id="a36fc-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36fc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a36fc-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="a36fc-107">Member</span><span class="sxs-lookup"><span data-stu-id="a36fc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a36fc-108">**Std.**</span><span class="sxs-lookup"><span data-stu-id="a36fc-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-109">**HRESULT** -Rückgabecode.</span><span class="sxs-lookup"><span data-stu-id="a36fc-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="a36fc-110">**"Endstatus"**</span><span class="sxs-lookup"><span data-stu-id="a36fc-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-111">Der Wert des DRM-Enumerationstyps für den [**\_ Individualisierungs \_ Status**](drm-individualization-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a36fc-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="a36fc-112">**pszindirespurl**</span><span class="sxs-lookup"><span data-stu-id="a36fc-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Antwort-URL der Individualisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="a36fc-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="a36fc-114">**dwhttprequest**</span><span class="sxs-lookup"><span data-stu-id="a36fc-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-115">**DWORD** , das die Anzahl von HTTP-Roundtrips zum Individualisierungs Dienst angibt, die abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="a36fc-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="a36fc-116">**umhttpstatus**</span><span class="sxs-lookup"><span data-stu-id="a36fc-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-117">Der Wert des [**DRM- \_ http-statusenumerationstyps \_**](drm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a36fc-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="a36fc-118">**dwhttpreadprogress**</span><span class="sxs-lookup"><span data-stu-id="a36fc-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-119">**DWORD** , das die Anzahl der bis jetzt heruntergeladenen Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="a36fc-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="a36fc-120">**dwhttpreadtotal**</span><span class="sxs-lookup"><span data-stu-id="a36fc-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="a36fc-121">**DWORD** , das die Gesamtzahl der herunter zuladenden Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="a36fc-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="a36fc-122">Verwenden Sie diesen Wert und **dwhttpreadprogress** , um eine Benutzeroberfläche anzuzeigen, die angibt, wie viel der Download abgeschlossen ist und wie viel verbleiben muss.</span><span class="sxs-lookup"><span data-stu-id="a36fc-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a36fc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a36fc-123">Remarks</span></span>

<span data-ttu-id="a36fc-124">Diese Struktur wird von den DRM-Laufzeitkomponenten ausgefüllt und an Anwendungen im *pValue* -Parameter der Anwendung [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode gesendet, wenn das Ereignis gleich WMT \_ Individual ist.</span><span class="sxs-lookup"><span data-stu-id="a36fc-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="a36fc-125">Die Anwendung empfängt dieses Ereignis mehrmals während des Downloadvorgangs.</span><span class="sxs-lookup"><span data-stu-id="a36fc-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="a36fc-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a36fc-126">Requirements</span></span>



| <span data-ttu-id="a36fc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a36fc-127">Requirement</span></span> | <span data-ttu-id="a36fc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a36fc-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a36fc-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a36fc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a36fc-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36fc-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a36fc-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a36fc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a36fc-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36fc-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a36fc-133">Version</span><span class="sxs-lookup"><span data-stu-id="a36fc-133">Version</span></span><br/>                  | <span data-ttu-id="a36fc-134">SDK für Windows Media-Format 7 oder höhere Versionen des SDKs</span><span class="sxs-lookup"><span data-stu-id="a36fc-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="a36fc-135">Header</span><span class="sxs-lookup"><span data-stu-id="a36fc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a36fc-136"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="a36fc-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a36fc-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a36fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36fc-138">**DRM- \_ http- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a36fc-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="a36fc-139">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="a36fc-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





