---
title: Iwmpnetwork getproxysettings-Methode
description: Die getproxysettings-Methode gibt Informationen zu den Proxy Einstellungen für ein Protokoll zurück.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- getproxysettings-Methode, Windows-Media Player
- getproxysettings-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, getproxysettings-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372143"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="fe636-106">Iwmpnetwork:: getproxysettings-Methode</span><span class="sxs-lookup"><span data-stu-id="fe636-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="fe636-107">Die **getproxysettings** -Methode gibt Informationen zu den Proxy Einstellungen für ein Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="fe636-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe636-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe636-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="fe636-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe636-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe636-110">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe636-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe636-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="fe636-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="fe636-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="fe636-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe636-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe636-113">Return value</span></span>

<span data-ttu-id="fe636-114">Ein **System. Int32** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="fe636-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="fe636-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fe636-115">Value</span></span> | <span data-ttu-id="fe636-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe636-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe636-117">0</span><span class="sxs-lookup"><span data-stu-id="fe636-117">0</span></span>     | <span data-ttu-id="fe636-118">Ein Proxy Server wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe636-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="fe636-119">1</span><span class="sxs-lookup"><span data-stu-id="fe636-119">1</span></span>     | <span data-ttu-id="fe636-120">Die Proxy Einstellungen für den aktuellen Browser werden verwendet (nur für http gültig).</span><span class="sxs-lookup"><span data-stu-id="fe636-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="fe636-121">2</span><span class="sxs-lookup"><span data-stu-id="fe636-121">2</span></span>     | <span data-ttu-id="fe636-122">Die manuell angegebenen Proxy Einstellungen werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe636-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="fe636-123">3</span><span class="sxs-lookup"><span data-stu-id="fe636-123">3</span></span>     | <span data-ttu-id="fe636-124">Die Proxy Einstellungen werden automatisch erkannt.</span><span class="sxs-lookup"><span data-stu-id="fe636-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="fe636-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe636-125">Remarks</span></span>

<span data-ttu-id="fe636-126">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe636-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="fe636-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe636-127">Examples</span></span>

<span data-ttu-id="fe636-128">Im folgenden Codebeispiel wird **getproxysettings** verwendet, um eine Meldung anzuzeigen, die Informationen über die aktuellen Proxy Einstellungen des Players in einer Bezeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="fe636-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="fe636-129">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fe636-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="fe636-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe636-130">Requirements</span></span>



| <span data-ttu-id="fe636-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe636-131">Requirement</span></span> | <span data-ttu-id="fe636-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fe636-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe636-133">Version</span><span class="sxs-lookup"><span data-stu-id="fe636-133">Version</span></span><br/>   | <span data-ttu-id="fe636-134">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="fe636-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fe636-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe636-135">Namespace</span></span><br/> | <span data-ttu-id="fe636-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fe636-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fe636-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="fe636-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fe636-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fe636-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe636-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe636-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe636-140">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fe636-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fe636-141">**Iwmpnetwork. setproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fe636-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





