---
title: Network. setproxyname-Methode
description: Die setproxyname-Methode gibt den Namen des zu verwendenden Proxy Servers an. | Network. setproxyname-Methode
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- setproxyname-Methode, Windows Media Player
- setproxyname-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klasse, Windows Media Player, setproxyname-Methode
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371169"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="46977-107">Network. setproxyname-Methode</span><span class="sxs-lookup"><span data-stu-id="46977-107">Network.setProxyName method</span></span>

<span data-ttu-id="46977-108">Die **setproxyname** -Methode gibt den Namen des zu verwendenden Proxy Servers an.</span><span class="sxs-lookup"><span data-stu-id="46977-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="46977-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46977-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="46977-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46977-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46977-111">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46977-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46977-112">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="46977-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="46977-113">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="46977-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="46977-114">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46977-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46977-115">Eine **Zeichenfolge** , die den Namen des zu verwendenden Proxy Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="46977-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46977-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46977-116">Return value</span></span>

<span data-ttu-id="46977-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="46977-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46977-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46977-118">Remarks</span></span>

<span data-ttu-id="46977-119">Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="46977-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="46977-120">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46977-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="46977-121">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46977-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="46977-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46977-122">Examples</span></span>

<span data-ttu-id="46977-123">Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxyname** , um den Namen des Windows Media Player-Proxy Servers für das MMS-Protokoll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="46977-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="46977-124">Der neue Name wird von einem HTML-Text Element mit der ID "Name" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="46977-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="46977-125">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="46977-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="46977-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46977-126">Requirements</span></span>



| <span data-ttu-id="46977-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46977-127">Requirement</span></span> | <span data-ttu-id="46977-128">Wert</span><span class="sxs-lookup"><span data-stu-id="46977-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46977-129">Version</span><span class="sxs-lookup"><span data-stu-id="46977-129">Version</span></span><br/> | <span data-ttu-id="46977-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="46977-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="46977-131">DLL</span><span class="sxs-lookup"><span data-stu-id="46977-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="46977-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46977-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46977-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46977-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46977-134">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="46977-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





