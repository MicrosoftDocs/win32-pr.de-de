---
description: Definiert die Medien Schlüssel-Fehlercodes für die Medien-Engine.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: MF_MEDIA_ENGINE_KEYERR-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351348"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="902ec-103">MF- \_ Medien- \_ Engine \_ keyerr-Enumeration</span><span class="sxs-lookup"><span data-stu-id="902ec-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="902ec-104">Definiert die Medien Schlüssel-Fehlercodes für die Medien-Engine.</span><span class="sxs-lookup"><span data-stu-id="902ec-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="902ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="902ec-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="902ec-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="902ec-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="902ec-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ mediaengine \_ keyerr \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="902ec-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="902ec-108">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="902ec-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="902ec-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF \_ mediaengine \_ keyerr- \_ Client**</span><span class="sxs-lookup"><span data-stu-id="902ec-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="902ec-110">Fehler beim Client.</span><span class="sxs-lookup"><span data-stu-id="902ec-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="902ec-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF \_ mediaengine \_ keyerr- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="902ec-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="902ec-112">Fehler beim Dienst.</span><span class="sxs-lookup"><span data-stu-id="902ec-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="902ec-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF \_ mediaengine \_ keyerr- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="902ec-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="902ec-114">Es ist ein Fehler mit der Ausgabe aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="902ec-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="902ec-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ mediaengine \_ keyerr \_ hardwarechange**</span><span class="sxs-lookup"><span data-stu-id="902ec-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="902ec-116">Fehler im Zusammenhang mit einer Hardware Änderung.</span><span class="sxs-lookup"><span data-stu-id="902ec-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="902ec-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF \_ mediaengine \_ keyerr- \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="902ec-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="902ec-118">Fehler bei der Domäne.</span><span class="sxs-lookup"><span data-stu-id="902ec-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="902ec-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="902ec-119">Remarks</span></span>

<span data-ttu-id="902ec-120">**MF \_ Die Medien- \_ Engine \_ keyerr** wird mit dem *Code* -Parameter von [**IMF mediakeysessionnotify:: keyerror**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) und dem von [**IMF mediakeysession:: getError**](imfmediakeysession-geterror.md)zurückgegebenen *Codewert* verwendet.</span><span class="sxs-lookup"><span data-stu-id="902ec-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="902ec-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="902ec-121">Requirements</span></span>



| <span data-ttu-id="902ec-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="902ec-122">Requirement</span></span> | <span data-ttu-id="902ec-123">Wert</span><span class="sxs-lookup"><span data-stu-id="902ec-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="902ec-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="902ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="902ec-125">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="902ec-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="902ec-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="902ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="902ec-127">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="902ec-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="902ec-128">IDL</span><span class="sxs-lookup"><span data-stu-id="902ec-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="902ec-129"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="902ec-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="902ec-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="902ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="902ec-131">Media Foundation Enumerationen</span><span class="sxs-lookup"><span data-stu-id="902ec-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




