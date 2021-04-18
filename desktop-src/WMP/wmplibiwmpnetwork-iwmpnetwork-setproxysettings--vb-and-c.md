---
title: Iwmpnetwork (setproxysettings-Methode)
description: Mit der setproxysettings-Methode werden die Proxy Einstellungen für ein Protokoll angegeben.
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- setproxysettings-Methode, Windows-Media Player
- setproxysettings-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxysettings-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fc36c12335cf97ad7bff34924850155f2fd747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358159"
---
# <a name="iwmpnetworksetproxysettings-method"></a><span data-ttu-id="4556d-106">Iwmpnetwork:: setproxysettings-Methode</span><span class="sxs-lookup"><span data-stu-id="4556d-106">IWMPNetwork::setProxySettings method</span></span>

<span data-ttu-id="4556d-107">Mit der **setproxysettings** -Methode werden die Proxy Einstellungen für ein Protokoll angegeben.</span><span class="sxs-lookup"><span data-stu-id="4556d-107">The **setProxySettings** method specifies the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="4556d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4556d-108">Syntax</span></span>


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a><span data-ttu-id="4556d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4556d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4556d-110">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4556d-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4556d-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="4556d-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="4556d-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4556d-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="4556d-113">*lproxysetting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4556d-113">*lProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4556d-114">Ein **System. Int32** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="4556d-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="4556d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4556d-115">Value</span></span> | <span data-ttu-id="4556d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4556d-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="4556d-117">0</span><span class="sxs-lookup"><span data-stu-id="4556d-117">0</span></span>     | <span data-ttu-id="4556d-118">Verwenden Sie keinen Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="4556d-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="4556d-119">1</span><span class="sxs-lookup"><span data-stu-id="4556d-119">1</span></span>     | <span data-ttu-id="4556d-120">Verwenden Sie die Proxy Einstellungen des aktuellen Browsers (nur für http gültig).</span><span class="sxs-lookup"><span data-stu-id="4556d-120">Use the proxy settings of the current browser (valid only for HTTP).</span></span> |
| <span data-ttu-id="4556d-121">2</span><span class="sxs-lookup"><span data-stu-id="4556d-121">2</span></span>     | <span data-ttu-id="4556d-122">Verwenden Sie die manuell angegebenen Proxy Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4556d-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="4556d-123">3</span><span class="sxs-lookup"><span data-stu-id="4556d-123">3</span></span>     | <span data-ttu-id="4556d-124">Erkennen Sie die Proxy Einstellungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="4556d-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4556d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4556d-125">Return value</span></span>

<span data-ttu-id="4556d-126">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4556d-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4556d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4556d-127">Remarks</span></span>

<span data-ttu-id="4556d-128">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4556d-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="4556d-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4556d-129">Examples</span></span>

<span data-ttu-id="4556d-130">Im folgenden Codebeispiel wird ein Listenfeld verwendet, um dem Benutzer das Festlegen der Windows Media Player-Proxy Einstellung für das HTTP-Protokoll zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4556d-130">The following code example uses a list box to allow the user to set the Windows Media Player proxy setting for the HTTP protocol.</span></span> <span data-ttu-id="4556d-131">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4556d-131">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a><span data-ttu-id="4556d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4556d-132">Requirements</span></span>



| <span data-ttu-id="4556d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4556d-133">Requirement</span></span> | <span data-ttu-id="4556d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4556d-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4556d-135">Version</span><span class="sxs-lookup"><span data-stu-id="4556d-135">Version</span></span><br/>   | <span data-ttu-id="4556d-136">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="4556d-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4556d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="4556d-137">Namespace</span></span><br/> | <span data-ttu-id="4556d-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4556d-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4556d-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="4556d-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4556d-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4556d-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4556d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4556d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4556d-142">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4556d-142">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4556d-143">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4556d-143">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





