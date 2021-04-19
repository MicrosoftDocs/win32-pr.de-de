---
title: Network. getproxybypassforlocal-Methode
description: Die getproxybypassforlocal-Methode ruft einen Wert ab, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- getproxybypassforlocal-Methode, Windows Media Player
- getproxybypassforlocal-Methode, Windows Media Player, Network-Klasse
- Netzwerk Klasse, Windows Media Player, getproxybypassforlocal-Methode
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370062"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="a6a71-106">Network. getproxybypassforlocal-Methode</span><span class="sxs-lookup"><span data-stu-id="a6a71-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="a6a71-107">Die **getproxybypassforlocal** -Methode ruft einen Wert ab, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="a6a71-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a71-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6a71-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="a6a71-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6a71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a71-110">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6a71-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a71-111">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="a6a71-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="a6a71-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a6a71-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a71-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6a71-113">Return value</span></span>

<span data-ttu-id="a6a71-114">Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="a6a71-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="a6a71-115">Der zurückgegebene Wert ist nur dann von Bedeutung, wenn **getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="a6a71-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a71-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6a71-116">Remarks</span></span>

<span data-ttu-id="a6a71-117">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6a71-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="a6a71-118">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6a71-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a6a71-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6a71-119">Examples</span></span>

<span data-ttu-id="a6a71-120">Im folgenden JScript-Beispiel wird *Network* verwendet. **getproxybypassforlocal** , um anzuzeigen, ob die Windows-Media Player so festgelegt ist, dass der Proxy Server für lokale Adressen umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="a6a71-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="a6a71-121">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a6a71-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="a6a71-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6a71-122">Requirements</span></span>



| <span data-ttu-id="a6a71-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6a71-123">Requirement</span></span> | <span data-ttu-id="a6a71-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a6a71-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a71-125">Version</span><span class="sxs-lookup"><span data-stu-id="a6a71-125">Version</span></span><br/> | <span data-ttu-id="a6a71-126">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a6a71-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a6a71-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a6a71-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="a6a71-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6a71-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a71-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6a71-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a71-130">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="a6a71-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a6a71-131">**Network. getproxysettings**</span><span class="sxs-lookup"><span data-stu-id="a6a71-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





