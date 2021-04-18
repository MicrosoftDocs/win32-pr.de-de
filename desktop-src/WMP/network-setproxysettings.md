---
title: Network. setproxysettings-Methode
description: Die setproxysettings-Methode gibt die Proxy Einstellung für ein bestimmtes Protokoll an.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setproxysettings-Methode, Windows-Media Player
- setproxysettings-Methode, Windows Media Player, Network-Klasse
- Netzwerk Klassen-Windows-Media Player, setproxysettings-Methode
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352871"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="6b542-106">Network. setproxysettings-Methode</span><span class="sxs-lookup"><span data-stu-id="6b542-106">Network.setProxySettings method</span></span>

<span data-ttu-id="6b542-107">Die **setproxysettings** -Methode gibt die Proxy Einstellung für ein bestimmtes Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="6b542-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b542-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b542-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="6b542-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b542-110">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b542-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b542-111">**Zeichenfolge** , die den Namen des Protokolls angibt.</span><span class="sxs-lookup"><span data-stu-id="6b542-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="6b542-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="6b542-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b542-113">*Einstellung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b542-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b542-114">**Number** (**Long**), der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="6b542-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="6b542-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6b542-115">Value</span></span> | <span data-ttu-id="6b542-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b542-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="6b542-117">0</span><span class="sxs-lookup"><span data-stu-id="6b542-117">0</span></span>     | <span data-ttu-id="6b542-118">Verwenden Sie keinen Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="6b542-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="6b542-119">1</span><span class="sxs-lookup"><span data-stu-id="6b542-119">1</span></span>     | <span data-ttu-id="6b542-120">Verwenden Sie die Proxy Einstellungen des aktuellen Browsers (nur gültig für http).</span><span class="sxs-lookup"><span data-stu-id="6b542-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="6b542-121">2</span><span class="sxs-lookup"><span data-stu-id="6b542-121">2</span></span>     | <span data-ttu-id="6b542-122">Verwenden Sie die manuell angegebenen Proxy Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="6b542-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="6b542-123">3</span><span class="sxs-lookup"><span data-stu-id="6b542-123">3</span></span>     | <span data-ttu-id="6b542-124">Erkennen Sie die Proxy Einstellungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="6b542-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b542-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b542-125">Return value</span></span>

<span data-ttu-id="6b542-126">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6b542-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b542-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b542-127">Remarks</span></span>

<span data-ttu-id="6b542-128">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b542-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="6b542-129">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b542-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6b542-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b542-130">Examples</span></span>

<span data-ttu-id="6b542-131">Im folgenden Beispiel wird JScript mit einem HTML SELECT- **Element verwendet, um dem Benutzer die Angabe der Windows Media Player-Proxy Einstellung für das HTTP-Protokoll zu ermöglichen. Das Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b542-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6b542-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b542-132">Requirements</span></span>



| <span data-ttu-id="6b542-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b542-133">Requirement</span></span> | <span data-ttu-id="6b542-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6b542-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b542-135">Version</span><span class="sxs-lookup"><span data-stu-id="6b542-135">Version</span></span><br/> | <span data-ttu-id="6b542-136">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6b542-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6b542-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6b542-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b542-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b542-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b542-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b542-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b542-140">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="6b542-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





