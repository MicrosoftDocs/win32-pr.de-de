---
title: Iwmpnetwork getproxyport-Methode
description: Die getproxyport-Methode gibt den verwendeten ProxyPort zurück.
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- getproxyport-Methode, Windows Media Player
- getproxyport-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, getproxyport-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358631"
---
# <a name="iwmpnetworkgetproxyport-method"></a><span data-ttu-id="9f4c3-106">Iwmpnetwork:: getproxyport-Methode</span><span class="sxs-lookup"><span data-stu-id="9f4c3-106">IWMPNetwork::getProxyPort method</span></span>

<span data-ttu-id="9f4c3-107">Die **getproxyport** -Methode gibt den verwendeten ProxyPort zurück.</span><span class="sxs-lookup"><span data-stu-id="9f4c3-107">The **getProxyPort** method returns the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f4c3-108">Syntax</span></span>


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a><span data-ttu-id="9f4c3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f4c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f4c3-110">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f4c3-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f4c3-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="9f4c3-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="9f4c3-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="9f4c3-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f4c3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f4c3-113">Return value</span></span>

<span data-ttu-id="9f4c3-114">Ein **System. Int32** , das den verwendeten ProxyPort ist.</span><span class="sxs-lookup"><span data-stu-id="9f4c3-114">A **System.Int32** that is the proxy port being used.</span></span> <span data-ttu-id="9f4c3-115">Der Wert ist nur dann von Bedeutung, wenn **iwmpnetwork. getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="9f4c3-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f4c3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f4c3-116">Remarks</span></span>

<span data-ttu-id="9f4c3-117">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f4c3-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="9f4c3-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f4c3-118">Examples</span></span>

<span data-ttu-id="9f4c3-119">Im folgenden Codebeispiel wird **getproxyport** verwendet, um die aktuellen Windows Media Player Proxy Portnummern für die MMS-und HTTP-Protokolle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f4c3-119">The following code example uses **getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="9f4c3-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9f4c3-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
```





## <a name="requirements"></a><span data-ttu-id="9f4c3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f4c3-121">Requirements</span></span>



| <span data-ttu-id="9f4c3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f4c3-122">Requirement</span></span> | <span data-ttu-id="9f4c3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9f4c3-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4c3-124">Version</span><span class="sxs-lookup"><span data-stu-id="9f4c3-124">Version</span></span><br/>   | <span data-ttu-id="9f4c3-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="9f4c3-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9f4c3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f4c3-126">Namespace</span></span><br/> | <span data-ttu-id="9f4c3-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9f4c3-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9f4c3-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="9f4c3-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9f4c3-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9f4c3-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f4c3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f4c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4c3-131">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9f4c3-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9f4c3-132">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9f4c3-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9f4c3-133">**Iwmpnetwork. setproxyport (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9f4c3-133">**IWMPNetwork.setProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





