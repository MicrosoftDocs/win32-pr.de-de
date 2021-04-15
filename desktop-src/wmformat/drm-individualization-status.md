---
title: DRM_INDIVIDUALIZATION_STATUS-Enumeration (drmexternals. h)
description: Der DRM- \_ Individualisierungs \_ Status-Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung. | DRM_INDIVIDUALIZATION_STATUS-Enumeration (drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394025"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="90a8a-106">DRM_INDIVIDUALIZATION_STATUS-Enumeration (drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="90a8a-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="90a8a-107">Der **DRM- \_ Individualisierungs \_ Status** -Enumerationstyp definiert die gültigen Zustände für die DRM- [*Individualisierung*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="90a8a-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="90a8a-108">Wenn eine Anwendung mit einem Aufruf von [**iwmdrmreader:: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize)eine Individualisierung initiiert, wird der Fortschritt der Individualisierungs Anforderung durch Aufrufe der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="90a8a-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="90a8a-109">In den Individualisierungs Statusmeldungen wird das WMT-Element \_ Individual des Enumerationstyps [**WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) als *Status* Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="90a8a-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="90a8a-110">Der Status der Individualisierung wird im *pValue* -Parameter an **OnStatus** übergeben.</span><span class="sxs-lookup"><span data-stu-id="90a8a-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a8a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="90a8a-111">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="90a8a-112">Konstanten</span><span class="sxs-lookup"><span data-stu-id="90a8a-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90a8a-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**Indi nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="90a8a-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-114">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="90a8a-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="90a8a-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**Indi \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="90a8a-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-116">Gibt den Beginn des Individualisierungs Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="90a8a-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="90a8a-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**Indi \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="90a8a-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-118">Gibt an, dass der Individualisierungsprozess abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="90a8a-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="90a8a-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**Indi \_ Fail**</span><span class="sxs-lookup"><span data-stu-id="90a8a-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-120">Gibt an, dass der Individualisierungsprozess fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="90a8a-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="90a8a-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**Indi \_ Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="90a8a-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-122">Gibt an, dass der Individualisierungsprozess aufgrund eines Aufrufes von [**iwmdrmreader:: cancelindividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization)abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="90a8a-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="90a8a-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Indi \_ herunterladen**</span><span class="sxs-lookup"><span data-stu-id="90a8a-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-124">Gibt an, dass das Sicherheits Upgrade heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="90a8a-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="90a8a-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**Indi- \_ Installation**</span><span class="sxs-lookup"><span data-stu-id="90a8a-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="90a8a-126">Gibt an, dass das Sicherheits Upgrade installiert wird.</span><span class="sxs-lookup"><span data-stu-id="90a8a-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90a8a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90a8a-127">Remarks</span></span>

<span data-ttu-id="90a8a-128">Diese Enumeration wird von der [**WM \_ Individual \_ Status**](wm-individualize-status.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="90a8a-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a8a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90a8a-129">Requirements</span></span>



| <span data-ttu-id="90a8a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90a8a-130">Requirement</span></span> | <span data-ttu-id="90a8a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="90a8a-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a8a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90a8a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="90a8a-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90a8a-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="90a8a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90a8a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="90a8a-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90a8a-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="90a8a-136">Version</span><span class="sxs-lookup"><span data-stu-id="90a8a-136">Version</span></span><br/>                  | <span data-ttu-id="90a8a-137">SDK für Windows Media-Format 7 oder höhere Versionen des SDKs</span><span class="sxs-lookup"><span data-stu-id="90a8a-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="90a8a-138">Header</span><span class="sxs-lookup"><span data-stu-id="90a8a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="90a8a-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="90a8a-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90a8a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90a8a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a8a-141">**DRM- \_ http- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="90a8a-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="90a8a-142">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="90a8a-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





