---
title: Network. setproxybypassforlocal-Methode
description: Die setproxybypassforlocal-Methode gibt einen Wert an, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- setproxybypassforlocal-Methode, Windows Media Player
- setproxybypassforlocal-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klasse Windows Media Player, setproxybypassforlocal-Methode
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361945"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="2c844-106">Network. setproxybypassforlocal-Methode</span><span class="sxs-lookup"><span data-stu-id="2c844-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="2c844-107">Die **setproxybypassforlocal** -Methode gibt einen Wert an, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="2c844-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c844-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c844-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="2c844-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c844-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c844-110">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c844-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c844-111">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="2c844-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="2c844-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="2c844-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c844-113">*Umgehung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c844-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c844-114">**Boolescher** Wert, der angibt, ob der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="2c844-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c844-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c844-115">Return value</span></span>

<span data-ttu-id="2c844-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2c844-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c844-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c844-117">Remarks</span></span>

<span data-ttu-id="2c844-118">Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="2c844-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="2c844-119">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c844-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="2c844-120">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c844-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="2c844-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c844-121">Examples</span></span>

<span data-ttu-id="2c844-122">Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxybypassforlocal** , um anzugeben, ob der Windows-Media Player Proxyserver bei Verwendung des MMS-Protokolls umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="2c844-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="2c844-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c844-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="2c844-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c844-124">Requirements</span></span>



| <span data-ttu-id="2c844-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c844-125">Requirement</span></span> | <span data-ttu-id="2c844-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2c844-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c844-127">Version</span><span class="sxs-lookup"><span data-stu-id="2c844-127">Version</span></span><br/> | <span data-ttu-id="2c844-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2c844-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2c844-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2c844-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c844-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c844-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c844-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c844-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c844-132">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="2c844-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





