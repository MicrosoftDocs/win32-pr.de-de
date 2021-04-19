---
title: Methode "iwmpnetwork getproxyname"
description: Die getproxyname-Methode gibt den Namen des verwendeten Proxy Servers zurück.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- getproxyname-Methode, Windows Media Player
- getproxyname-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, getproxyname-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360287"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="22df9-106">Iwmpnetwork:: getproxyname-Methode</span><span class="sxs-lookup"><span data-stu-id="22df9-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="22df9-107">Die **getproxyname** -Methode gibt den Namen des verwendeten Proxy Servers zurück.</span><span class="sxs-lookup"><span data-stu-id="22df9-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="22df9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="22df9-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="22df9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="22df9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22df9-110">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22df9-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22df9-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="22df9-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="22df9-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="22df9-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22df9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22df9-113">Return value</span></span>

<span data-ttu-id="22df9-114">Ein **System. String** -Wert, der der Name des verwendeten Proxy Servers ist.</span><span class="sxs-lookup"><span data-stu-id="22df9-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="22df9-115">Der Wert ist nur dann von Bedeutung, wenn **iwmpnetwork. getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="22df9-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="22df9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22df9-116">Remarks</span></span>

<span data-ttu-id="22df9-117">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22df9-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="22df9-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22df9-118">Examples</span></span>

<span data-ttu-id="22df9-119">Im folgenden Codebeispiel wird **getproxyname** verwendet, um die Namen der Windows Media Player-Proxy Server für die Protokolle http und MMS anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22df9-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="22df9-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="22df9-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="22df9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22df9-121">Requirements</span></span>



| <span data-ttu-id="22df9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22df9-122">Requirement</span></span> | <span data-ttu-id="22df9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="22df9-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22df9-124">Version</span><span class="sxs-lookup"><span data-stu-id="22df9-124">Version</span></span><br/>   | <span data-ttu-id="22df9-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="22df9-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="22df9-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="22df9-126">Namespace</span></span><br/> | <span data-ttu-id="22df9-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="22df9-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="22df9-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="22df9-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="22df9-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="22df9-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22df9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22df9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22df9-131">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="22df9-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="22df9-132">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="22df9-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="22df9-133">**Iwmpnetwork. setproxyname (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="22df9-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





