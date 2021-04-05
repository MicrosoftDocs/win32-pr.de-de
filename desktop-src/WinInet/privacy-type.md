---
title: Daten Schutztyp (WinInet. h)
description: Gibt an, dass die Datenschutzeinstellungen entweder für Drittanbieter-oder Drittanbieter Cookies gelten.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859295"
---
# <a name="privacy-type"></a><span data-ttu-id="10fc9-103">Daten Schutztyp</span><span class="sxs-lookup"><span data-stu-id="10fc9-103">Privacy Type</span></span>

<span data-ttu-id="10fc9-104">Gibt an, dass die Datenschutzeinstellungen entweder für Drittanbieter-oder Drittanbieter Cookies gelten.</span><span class="sxs-lookup"><span data-stu-id="10fc9-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="10fc9-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**Daten \_ Schutztyp \_ erste \_ Partei**</span><span class="sxs-lookup"><span data-stu-id="10fc9-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10fc9-106">0</span><span class="sxs-lookup"><span data-stu-id="10fc9-106">0</span></span>
</dt> <dt>



<span data-ttu-id="10fc9-107">Bezieht sich auf die Datenschutzeinstellungen für Cookies von ersten Anbietern.</span><span class="sxs-lookup"><span data-stu-id="10fc9-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="10fc9-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**Datenschutz von \_ \_ Dritt \_ Anbietern**</span><span class="sxs-lookup"><span data-stu-id="10fc9-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10fc9-109">1</span><span class="sxs-lookup"><span data-stu-id="10fc9-109">1</span></span>
</dt> <dt>



<span data-ttu-id="10fc9-110">Bezieht sich auf Datenschutzeinstellungen für Cookies von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="10fc9-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10fc9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10fc9-111">Remarks</span></span>

<span data-ttu-id="10fc9-112">Cookies werden als erste Partei und als Drittanbieter kategorisiert.</span><span class="sxs-lookup"><span data-stu-id="10fc9-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="10fc9-113">Ein erst Anbieter Cookie stammt aus der Host Domäne.</span><span class="sxs-lookup"><span data-stu-id="10fc9-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="10fc9-114">Wenn " https://www.blueyonderairlines.com " in der Adressleiste von Microsoft Internet Explorer gefunden wird, ist "www.blueyonderairlines.com" die Host Domäne.</span><span class="sxs-lookup"><span data-stu-id="10fc9-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="10fc9-115">Wenn Sie diese Seite aufrufen und ein Cookie aus einer anderen Domäne als "www.blueyonderairlines.com" (z. b. "www.fourthcoffee.com") festgelegt ist, wird dieses Cookie als Drittanbieter-Cookie angesehen.</span><span class="sxs-lookup"><span data-stu-id="10fc9-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="10fc9-116">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="10fc9-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="10fc9-117">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10fc9-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="10fc9-118">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="10fc9-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10fc9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10fc9-119">Requirements</span></span>



| <span data-ttu-id="10fc9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10fc9-120">Requirement</span></span> | <span data-ttu-id="10fc9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="10fc9-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10fc9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10fc9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10fc9-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10fc9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="10fc9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10fc9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10fc9-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10fc9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10fc9-126">Header</span><span class="sxs-lookup"><span data-stu-id="10fc9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fc9-127"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fc9-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fc9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10fc9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fc9-129">**Privacygetzonepreferencew**</span><span class="sxs-lookup"><span data-stu-id="10fc9-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="10fc9-130">**Privacysetzonepreferencew**</span><span class="sxs-lookup"><span data-stu-id="10fc9-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

