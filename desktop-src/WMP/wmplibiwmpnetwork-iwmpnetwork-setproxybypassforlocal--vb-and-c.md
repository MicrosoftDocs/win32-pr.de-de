---
title: Iwmpnetwork-setproxybypassforlocal-Methode
description: Die setproxybypassforlocal-Methode gibt an, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- setproxybypassforlocal-Methode, Windows Media Player
- setproxybypassforlocal-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxybypassforlocal-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370135"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="668cf-106">Iwmpnetwork:: setproxybypassforlocal-Methode</span><span class="sxs-lookup"><span data-stu-id="668cf-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="668cf-107">Die **setproxybypassforlocal** -Methode gibt an, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="668cf-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="668cf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="668cf-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="668cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="668cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="668cf-110">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="668cf-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="668cf-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="668cf-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="668cf-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="668cf-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="668cf-113">" *f bypassforlocal* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="668cf-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="668cf-114">Ein **System. Boolean** -Wert, der angibt, ob der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="668cf-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="668cf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="668cf-115">Return value</span></span>

<span data-ttu-id="668cf-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="668cf-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="668cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="668cf-117">Remarks</span></span>

<span data-ttu-id="668cf-118">Diese Methode hat keine Auswirkung, es sei denn, der Wert, der von **iwmpnetwork. getproxysettings** abgerufen wird, ist 2 (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="668cf-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="668cf-119">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="668cf-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="668cf-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="668cf-120">Examples</span></span>

<span data-ttu-id="668cf-121">Im folgenden Codebeispiel wird **setproxybypassforlocal** verwendet, um anzugeben, ob der Windows-Media Player Proxyserver bei Verwendung des MMS-Protokolls umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="668cf-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="668cf-122">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="668cf-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="668cf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="668cf-123">Requirements</span></span>



| <span data-ttu-id="668cf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="668cf-124">Requirement</span></span> | <span data-ttu-id="668cf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="668cf-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668cf-126">Version</span><span class="sxs-lookup"><span data-stu-id="668cf-126">Version</span></span><br/>   | <span data-ttu-id="668cf-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="668cf-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="668cf-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="668cf-128">Namespace</span></span><br/> | <span data-ttu-id="668cf-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="668cf-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="668cf-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="668cf-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="668cf-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="668cf-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="668cf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="668cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="668cf-133">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="668cf-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="668cf-134">**Iwmpnetwork. getproxybypassforlocal (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="668cf-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="668cf-135">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="668cf-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





