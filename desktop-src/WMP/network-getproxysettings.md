---
title: Network. getproxysettings-Methode
description: Die getproxysettings-Methode ruft die Proxy Einstellung für ein bestimmtes Protokoll ab.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- getproxysettings-Methode, Windows-Media Player
- getproxysettings-Methode, Windows Media Player, Network-Klasse
- Netzwerk Klassen-Windows Media Player, getproxysettings-Methode
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361928"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="ccf20-106">Network. getproxysettings-Methode</span><span class="sxs-lookup"><span data-stu-id="ccf20-106">Network.getProxySettings method</span></span>

<span data-ttu-id="ccf20-107">Die **getproxysettings** -Methode ruft die Proxy Einstellung für ein bestimmtes Protokoll ab.</span><span class="sxs-lookup"><span data-stu-id="ccf20-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf20-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccf20-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="ccf20-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccf20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf20-110">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccf20-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf20-111">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="ccf20-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="ccf20-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ccf20-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf20-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccf20-113">Return value</span></span>

<span data-ttu-id="ccf20-114">Diese Methode gibt eine **Zahl** (**Long**) zurück, die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="ccf20-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="ccf20-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ccf20-115">Value</span></span> | <span data-ttu-id="ccf20-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccf20-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ccf20-117">0</span><span class="sxs-lookup"><span data-stu-id="ccf20-117">0</span></span>     | <span data-ttu-id="ccf20-118">Ein Proxy Server wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccf20-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="ccf20-119">1</span><span class="sxs-lookup"><span data-stu-id="ccf20-119">1</span></span>     | <span data-ttu-id="ccf20-120">Die Proxy Einstellungen für den aktuellen Browser werden verwendet (nur gültig für http).</span><span class="sxs-lookup"><span data-stu-id="ccf20-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="ccf20-121">2</span><span class="sxs-lookup"><span data-stu-id="ccf20-121">2</span></span>     | <span data-ttu-id="ccf20-122">Die manuell angegebenen Proxy Einstellungen werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccf20-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="ccf20-123">3</span><span class="sxs-lookup"><span data-stu-id="ccf20-123">3</span></span>     | <span data-ttu-id="ccf20-124">Die Proxy Einstellungen werden automatisch erkannt.</span><span class="sxs-lookup"><span data-stu-id="ccf20-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="ccf20-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccf20-125">Remarks</span></span>

<span data-ttu-id="ccf20-126">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf20-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="ccf20-127">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ccf20-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="ccf20-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccf20-128">Examples</span></span>

<span data-ttu-id="ccf20-129">Im folgenden JScript-Beispiel wird *Network* verwendet. **getproxysettings** zum Anzeigen einer Meldung, die Informationen zu den aktuellen Proxy Einstellungen des Players im Browserfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="ccf20-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="ccf20-130">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccf20-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="ccf20-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccf20-131">Requirements</span></span>



| <span data-ttu-id="ccf20-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccf20-132">Requirement</span></span> | <span data-ttu-id="ccf20-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ccf20-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf20-134">Version</span><span class="sxs-lookup"><span data-stu-id="ccf20-134">Version</span></span><br/> | <span data-ttu-id="ccf20-135">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ccf20-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ccf20-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf20-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="ccf20-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf20-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf20-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccf20-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf20-139">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="ccf20-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





