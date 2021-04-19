---
title: Network. setproxyexceptionlist-Methode
description: Die setproxyexceptionlist-Methode gibt die Proxy Ausnahmeliste an. | Network. setproxyexceptionlist-Methode
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- setproxyexceptionlist-Methode, Windows Media Player
- setproxyexceptionlist-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klassen-Windows-Media Player, setproxyexceptionlist-Methode
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369932"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="c4e34-107">Network. setproxyexceptionlist-Methode</span><span class="sxs-lookup"><span data-stu-id="c4e34-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="c4e34-108">Die **setproxyexceptionlist** -Methode gibt die Proxy Ausnahmeliste an.</span><span class="sxs-lookup"><span data-stu-id="c4e34-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4e34-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4e34-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="c4e34-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4e34-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e34-111">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4e34-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e34-112">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="c4e34-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="c4e34-113">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c4e34-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4e34-114">*Liste* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4e34-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e34-115">Eine **Zeichenfolge** , die eine durch Semikolons getrennte Liste von Hosts angibt, für die der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="c4e34-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e34-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4e34-116">Return value</span></span>

<span data-ttu-id="c4e34-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c4e34-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e34-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4e34-118">Remarks</span></span>

<span data-ttu-id="c4e34-119">Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxy Server umgehen, wenn der Hostteil der Ziel-URL mit einem Eintrag in der Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c4e34-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="c4e34-120">Das \* Zeichen kann als Platzhalter für das Auflisten von Einträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4e34-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="c4e34-121">Beispielsweise \* entspricht ". com" allen Hosts in der com-Domäne, und 67. \* entspricht allen Hosts in der 67-Klasse einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="c4e34-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="c4e34-122">Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="c4e34-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="c4e34-123">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4e34-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="c4e34-124">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4e34-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c4e34-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4e34-125">Examples</span></span>

<span data-ttu-id="c4e34-126">Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxyexceptionlist** zum Angeben einer Liste von Hosts, für die der Proxy Server bei Verwendung des MMS-Protokolls umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="c4e34-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="c4e34-127">Die neue Liste wird aus einem HTML-Text Element mit ID = "xList" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c4e34-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="c4e34-128">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4e34-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="c4e34-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4e34-129">Requirements</span></span>



| <span data-ttu-id="c4e34-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4e34-130">Requirement</span></span> | <span data-ttu-id="c4e34-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c4e34-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e34-132">Version</span><span class="sxs-lookup"><span data-stu-id="c4e34-132">Version</span></span><br/> | <span data-ttu-id="c4e34-133">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c4e34-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c4e34-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c4e34-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="c4e34-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4e34-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e34-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4e34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e34-137">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="c4e34-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





