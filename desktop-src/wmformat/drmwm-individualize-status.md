---
title: WM_INDIVIDUALIZE_STATUS Struktur (wmdrmsdk. h)
description: Die WM \_ Individual \_ Status-Struktur enthält Informationen zu einem ausstehenden Individualisierungsprozess.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS Struktur-Windows Media-Format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369703"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="dbad3-104">WM_INDIVIDUALIZE_STATUS Struktur (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="dbad3-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="dbad3-105">Die **WM \_ Individual \_ Status** -Struktur enthält Informationen zu einem ausstehenden Individualisierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="dbad3-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbad3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbad3-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="dbad3-107">Member</span><span class="sxs-lookup"><span data-stu-id="dbad3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dbad3-108">**Std.**</span><span class="sxs-lookup"><span data-stu-id="dbad3-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-109">**HRESULT** -Rückgabecode.</span><span class="sxs-lookup"><span data-stu-id="dbad3-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="dbad3-110">**"Endstatus"**</span><span class="sxs-lookup"><span data-stu-id="dbad3-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-111">Wert aus dem [**DRM- \_ \_ Status**](drmdrm-individualization-status.md) -Enumerationstyp, der den aktuellen Status des Individualisierungs Prozesses angibt.</span><span class="sxs-lookup"><span data-stu-id="dbad3-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="dbad3-112">**pszindirespurl**</span><span class="sxs-lookup"><span data-stu-id="dbad3-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Antwort-URL der Individualisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="dbad3-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="dbad3-114">**dwhttprequest**</span><span class="sxs-lookup"><span data-stu-id="dbad3-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-115">Die Anzahl der HTTP-Roundtrips zum Individualisierungs Dienst, die abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="dbad3-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="dbad3-116">**umhttpstatus**</span><span class="sxs-lookup"><span data-stu-id="dbad3-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-117">Der Wert des [**DRM- \_ http-statusenumerationstyps \_**](drmdrm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="dbad3-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="dbad3-118">**dwhttpreadprogress**</span><span class="sxs-lookup"><span data-stu-id="dbad3-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-119">Die Anzahl der heruntergeladenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="dbad3-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="dbad3-120">**dwhttpreadtotal**</span><span class="sxs-lookup"><span data-stu-id="dbad3-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="dbad3-121">Die Gesamtzahl der herunter zuladenden bytes.</span><span class="sxs-lookup"><span data-stu-id="dbad3-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="dbad3-122">Sie können diesen Wert und **dwhttpreadprogress** verwenden, um eine Benutzeroberfläche anzuzeigen, die angibt, wie viel der Download abgeschlossen ist und wie viel verbleiben muss.</span><span class="sxs-lookup"><span data-stu-id="dbad3-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbad3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbad3-123">Remarks</span></span>

<span data-ttu-id="dbad3-124">Diese Struktur wird empfangen, wenn Sie die [**iwmdrmindividualizationstatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dbad3-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="dbad3-125">Sie enthält den Status des ausstehenden Individualisierungs Prozesses zum Zeitpunkt des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="dbad3-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbad3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbad3-126">Requirements</span></span>



| <span data-ttu-id="dbad3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbad3-127">Requirement</span></span> | <span data-ttu-id="dbad3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="dbad3-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbad3-129">Header</span><span class="sxs-lookup"><span data-stu-id="dbad3-129">Header</span></span><br/> | <dl> <span data-ttu-id="dbad3-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbad3-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbad3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbad3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbad3-132">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="dbad3-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





