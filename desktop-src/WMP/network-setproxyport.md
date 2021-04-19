---
title: Network. setproxyport-Methode
description: Die setproxyport-Methode gibt den zu verwendenden ProxyPort an. | Network. setproxyport-Methode
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- setproxyport-Methode, Windows Media Player
- setproxyport-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klassen-Windows-Media Player, setproxyport-Methode
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370496"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="9e6c6-107">Network. setproxyport-Methode</span><span class="sxs-lookup"><span data-stu-id="9e6c6-107">Network.setProxyPort method</span></span>

<span data-ttu-id="9e6c6-108">Die **setproxyport** -Methode gibt den zu verwendenden ProxyPort an.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6c6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e6c6-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="9e6c6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e6c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6c6-111">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e6c6-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e6c6-112">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="9e6c6-113">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="9e6c6-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e6c6-114">*Port* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e6c6-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e6c6-115">**Zahl** (**Long**), die den zu verwendenden ProxyPort angibt.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e6c6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e6c6-116">Return value</span></span>

<span data-ttu-id="9e6c6-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6c6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e6c6-118">Remarks</span></span>

<span data-ttu-id="9e6c6-119">Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="9e6c6-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="9e6c6-120">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="9e6c6-121">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="9e6c6-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e6c6-122">Examples</span></span>

<span data-ttu-id="9e6c6-123">Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxyport** , um die Portnummer des Windows-Media Player Proxys für das MMS-Protokoll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="9e6c6-124">Die Portnummer wird von einem HTML-Eingabe Element mit ID = "Port" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="9e6c6-125">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="9e6c6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e6c6-126">Requirements</span></span>



| <span data-ttu-id="9e6c6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e6c6-127">Requirement</span></span> | <span data-ttu-id="9e6c6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9e6c6-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6c6-129">Version</span><span class="sxs-lookup"><span data-stu-id="9e6c6-129">Version</span></span><br/> | <span data-ttu-id="9e6c6-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9e6c6-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9e6c6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9e6c6-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e6c6-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e6c6-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e6c6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e6c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6c6-134">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="9e6c6-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





