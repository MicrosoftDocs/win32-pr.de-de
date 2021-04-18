---
title: Iwmpnetwork getproxybypassforlocal-Methode
description: Die getproxybypassforlocal-Methode gibt einen Wert zurück, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- getproxybypassforlocal-Methode, Windows Media Player
- getproxybypassforlocal-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, getproxybypassforlocal-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372035"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="025ac-106">Iwmpnetwork:: getproxybypassforlocal-Methode</span><span class="sxs-lookup"><span data-stu-id="025ac-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="025ac-107">Die **getproxybypassforlocal** -Methode gibt einen Wert zurück, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="025ac-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="025ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="025ac-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="025ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="025ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="025ac-110">*bstrauprotocol*</span><span class="sxs-lookup"><span data-stu-id="025ac-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="025ac-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="025ac-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="025ac-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="025ac-112">Return value</span></span>

<span data-ttu-id="025ac-113">Ein **System. Boolean** -Wert, der angibt, ob der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="025ac-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="025ac-114">Der Wert ist nur dann von Bedeutung, wenn **iwmpnetwork. getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="025ac-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="025ac-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="025ac-115">Remarks</span></span>

<span data-ttu-id="025ac-116">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="025ac-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="025ac-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="025ac-117">Examples</span></span>

<span data-ttu-id="025ac-118">Im folgenden Codebeispiel wird **getproxybypassforlocal** verwendet, um anzuzeigen, ob Windows Media Player so festgelegt ist, dass der Proxy Server für lokale Adressen umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="025ac-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="025ac-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="025ac-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="025ac-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="025ac-120">Requirements</span></span>



| <span data-ttu-id="025ac-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="025ac-121">Requirement</span></span> | <span data-ttu-id="025ac-122">Wert</span><span class="sxs-lookup"><span data-stu-id="025ac-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="025ac-123">Version</span><span class="sxs-lookup"><span data-stu-id="025ac-123">Version</span></span><br/>   | <span data-ttu-id="025ac-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="025ac-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="025ac-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="025ac-125">Namespace</span></span><br/> | <span data-ttu-id="025ac-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="025ac-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="025ac-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="025ac-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="025ac-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="025ac-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="025ac-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="025ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="025ac-130">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="025ac-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="025ac-131">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="025ac-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="025ac-132">**Iwmpnetwork. setproxybypassforlocal (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="025ac-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





