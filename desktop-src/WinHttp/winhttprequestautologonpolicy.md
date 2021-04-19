---
description: Enthält mögliche Einstellungen für die Richtlinie für die automatische Anmeldung.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Winhttprequestautologonpolicy-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345726"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="14bab-103">Winhttprequestautologonpolicy-Enumeration</span><span class="sxs-lookup"><span data-stu-id="14bab-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="14bab-104">Die **winhttprequestautologonpolicy** -Enumeration enthält mögliche Einstellungen für die [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="14bab-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="14bab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14bab-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="14bab-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="14bab-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="14bab-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**Autologonpolicy \_ immer**</span><span class="sxs-lookup"><span data-stu-id="14bab-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="14bab-108">Eine authentifizierte Anmeldung, bei der die Standard Anmelde Informationen verwendet werden, wird für alle Anforderungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14bab-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="14bab-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**Autologonpolicy \_ onlyifbypassproxy**</span><span class="sxs-lookup"><span data-stu-id="14bab-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="14bab-110">Eine authentifizierte Anmeldung, bei der die Standard Anmelde Informationen verwendet werden, wird nur für Anforderungen im lokalen Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14bab-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="14bab-111">Das lokale Intranet gilt als beliebiger Server in der Proxy Umgehungs Liste in der aktuellen Proxykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="14bab-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="14bab-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**Autologonpolicy \_ nie**</span><span class="sxs-lookup"><span data-stu-id="14bab-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="14bab-113">Die Authentifizierung wird nicht automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="14bab-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14bab-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14bab-114">Remarks</span></span>

<span data-ttu-id="14bab-115">Um die Richtlinie für die automatische Anmeldung festzulegen, nennen Sie die [**setautologonpolicy**](iwinhttprequest-setautologonpolicy.md) -Methode, und geben Sie eine der vorangehenden Konstanten an.</span><span class="sxs-lookup"><span data-stu-id="14bab-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="14bab-116">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="14bab-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14bab-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14bab-117">Requirements</span></span>



| <span data-ttu-id="14bab-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14bab-118">Requirement</span></span> | <span data-ttu-id="14bab-119">Wert</span><span class="sxs-lookup"><span data-stu-id="14bab-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bab-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14bab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14bab-121">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14bab-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="14bab-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14bab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14bab-123">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14bab-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="14bab-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="14bab-124">Redistributable</span></span><br/>          | <span data-ttu-id="14bab-125">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="14bab-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="14bab-126">IDL</span><span class="sxs-lookup"><span data-stu-id="14bab-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14bab-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14bab-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14bab-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14bab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bab-129">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="14bab-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




