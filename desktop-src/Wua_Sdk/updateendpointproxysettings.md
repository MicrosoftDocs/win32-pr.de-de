---
description: Die updateendpointproxysettings-Struktur definiert die Proxy Einstellungen, die beim Anfordern eines Tokens verwendet werden.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Updateendpointproxysettings-Struktur (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041781"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="b7c87-103">Updateendpointproxysettings-Struktur</span><span class="sxs-lookup"><span data-stu-id="b7c87-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="b7c87-104">Die **updateendpointproxysettings** -Struktur definiert die Proxy Einstellungen, die beim Anfordern eines Tokens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7c87-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c87-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c87-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="b7c87-106">Member</span><span class="sxs-lookup"><span data-stu-id="b7c87-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7c87-107">**szproxyaddr**</span><span class="sxs-lookup"><span data-stu-id="b7c87-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="b7c87-108">Der DNS-Name oder die IP-Adresse des zu verwendenden Proxy Servers (z. b. "Proxy.somecorp.com" oder "192.168.0.4") oder eine leere Zeichenfolge, wenn kein Proxy verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7c87-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="b7c87-109">**szbypasslist**</span><span class="sxs-lookup"><span data-stu-id="b7c87-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="b7c87-110">Eine Liste von Host Adressen, die den Proxy Server umgehen sollen, oder eine leere Zeichenfolge, wenn alle Host Adressen den Proxy Server verwenden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7c87-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="b7c87-111">WUA verwendet diese Daten nicht, wenn **szproxyaddr** leer ist.</span><span class="sxs-lookup"><span data-stu-id="b7c87-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="b7c87-112">**szusername**</span><span class="sxs-lookup"><span data-stu-id="b7c87-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="b7c87-113">Der Benutzername, der zur Authentifizierung beim Proxy Server verwendet wird, oder die leere Zeichenfolge, wenn keine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b7c87-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="b7c87-114">WUA verwendet diese Daten nicht, wenn **szproxyaddr** leer ist.</span><span class="sxs-lookup"><span data-stu-id="b7c87-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="b7c87-115">**szPassword**</span><span class="sxs-lookup"><span data-stu-id="b7c87-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="b7c87-116">Das Kennwort, das für die Authentifizierung beim Proxy Server verwendet wird, oder die leere Zeichenfolge, wenn keine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b7c87-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="b7c87-117">WUA verwendet diese Daten nicht, wenn **szproxyaddr** leer ist.</span><span class="sxs-lookup"><span data-stu-id="b7c87-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7c87-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7c87-118">Requirements</span></span>



| <span data-ttu-id="b7c87-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7c87-119">Requirement</span></span> | <span data-ttu-id="b7c87-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c87-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c87-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7c87-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c87-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7c87-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b7c87-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7c87-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c87-124">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7c87-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b7c87-125">Header</span><span class="sxs-lookup"><span data-stu-id="b7c87-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7c87-126"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c87-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7c87-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b7c87-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7c87-128"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7c87-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c87-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7c87-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c87-130">**Getendpointtoken**</span><span class="sxs-lookup"><span data-stu-id="b7c87-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




