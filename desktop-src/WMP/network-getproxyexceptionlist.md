---
title: Network. getproxyexceptionlist-Methode
description: Die getproxyexceptionlist-Methode ruft die Proxy Ausnahmeliste ab.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- getproxyexceptionlist-Methode, Windows Media Player
- getproxyexceptionlist-Methode, Windows Media Player, Network-Klasse
- Network-Klasse, Windows Media Player, getproxyexceptionlist-Methode
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359745"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="e1576-106">Network. getproxyexceptionlist-Methode</span><span class="sxs-lookup"><span data-stu-id="e1576-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="e1576-107">Die **getproxyexceptionlist** -Methode ruft die Proxy Ausnahmeliste ab.</span><span class="sxs-lookup"><span data-stu-id="e1576-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1576-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1576-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="e1576-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1576-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1576-110">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1576-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1576-111">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="e1576-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="e1576-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e1576-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1576-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1576-113">Return value</span></span>

<span data-ttu-id="e1576-114">Diese Methode gibt eine **Zeichen** Folge zurück, die eine durch Semikolons getrennte Liste von Hosts angibt, für die der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="e1576-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="e1576-115">Der zurückgegebene Wert ist nur dann von Bedeutung, wenn **getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="e1576-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1576-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1576-116">Remarks</span></span>

<span data-ttu-id="e1576-117">Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxy Server umgehen, wenn der Hostteil der Ziel-URL mit einem Eintrag in der Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e1576-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="e1576-118">Das \* Zeichen kann als Platzhalter für das Auflisten von Einträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1576-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="e1576-119">Beispielsweise \* entspricht. com allen Hosts in der com-Domäne, während 67. \* entspricht allen Hosts in der 67-Klasse als Subnetz.</span><span class="sxs-lookup"><span data-stu-id="e1576-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="e1576-120">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1576-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="e1576-121">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1576-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="e1576-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1576-122">Examples</span></span>

<span data-ttu-id="e1576-123">Im folgenden JScript-Beispiel wird *Network* verwendet. **getproxyexceptionlist** zum Anzeigen der Listen der umgangen Proxys für die MMS-und HTTP-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="e1576-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="e1576-124">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1576-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="e1576-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1576-125">Requirements</span></span>



| <span data-ttu-id="e1576-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1576-126">Requirement</span></span> | <span data-ttu-id="e1576-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e1576-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1576-128">Version</span><span class="sxs-lookup"><span data-stu-id="e1576-128">Version</span></span><br/> | <span data-ttu-id="e1576-129">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e1576-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e1576-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e1576-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1576-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1576-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1576-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1576-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1576-133">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="e1576-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="e1576-134">**Network. getproxysettings**</span><span class="sxs-lookup"><span data-stu-id="e1576-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





