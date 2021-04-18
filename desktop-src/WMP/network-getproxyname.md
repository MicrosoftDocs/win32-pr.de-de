---
title: Network. getproxyname-Methode
description: Die getproxyname-Methode ruft den Namen des verwendeten Proxy Servers ab.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- getproxyname-Methode, Windows Media Player
- getproxyname-Methode, Windows Media Player, Network-Klasse
- Network Class Windows Media Player, getproxyname-Methode
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372061"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="a380b-106">Network. getproxyname-Methode</span><span class="sxs-lookup"><span data-stu-id="a380b-106">Network.getProxyName method</span></span>

<span data-ttu-id="a380b-107">Die **getproxyname** -Methode ruft den Namen des verwendeten Proxy Servers ab.</span><span class="sxs-lookup"><span data-stu-id="a380b-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="a380b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a380b-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="a380b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a380b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a380b-110">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a380b-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a380b-111">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="a380b-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="a380b-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a380b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a380b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a380b-113">Return value</span></span>

<span data-ttu-id="a380b-114">Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen des verwendeten Proxy Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="a380b-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="a380b-115">Der zurückgegebene Wert ist nur dann von Bedeutung, wenn **getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="a380b-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="a380b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a380b-116">Remarks</span></span>

<span data-ttu-id="a380b-117">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a380b-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="a380b-118">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a380b-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a380b-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a380b-119">Examples</span></span>

<span data-ttu-id="a380b-120">Im folgenden JScript-Beispiel wird *Network* verwendet. **getproxyname** zum Anzeigen der Namen der Windows Media Player-Proxy Server für die HTTP-und MMS-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="a380b-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="a380b-121">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a380b-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="a380b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a380b-122">Requirements</span></span>



| <span data-ttu-id="a380b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a380b-123">Requirement</span></span> | <span data-ttu-id="a380b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a380b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a380b-125">Version</span><span class="sxs-lookup"><span data-stu-id="a380b-125">Version</span></span><br/> | <span data-ttu-id="a380b-126">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a380b-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a380b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a380b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="a380b-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a380b-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a380b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a380b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a380b-130">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="a380b-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a380b-131">**Network. getproxysettings**</span><span class="sxs-lookup"><span data-stu-id="a380b-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





