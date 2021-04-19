---
title: Iwmpnetwork getproxyexceptionlist-Methode
description: Die getproxyexceptionlist-Methode gibt die Proxy Ausnahmeliste zurück.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- getproxyexceptionlist-Methode, Windows Media Player
- getproxyexceptionlist-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, getproxyexceptionlist-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369553"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="19deb-106">Iwmpnetwork:: getproxyexceptionlist-Methode</span><span class="sxs-lookup"><span data-stu-id="19deb-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="19deb-107">Die **getproxyexceptionlist** -Methode gibt die Proxy Ausnahmeliste zurück.</span><span class="sxs-lookup"><span data-stu-id="19deb-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="19deb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19deb-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="19deb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19deb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19deb-110">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19deb-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19deb-111">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="19deb-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="19deb-112">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="19deb-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19deb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19deb-113">Return value</span></span>

<span data-ttu-id="19deb-114">Eine **System. String** , bei der es sich um eine durch Semikolons getrennte Liste von Hosts handelt, für die der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="19deb-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="19deb-115">Der Wert ist nur dann von Bedeutung, wenn **iwmpnetwork. getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="19deb-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="19deb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19deb-116">Remarks</span></span>

<span data-ttu-id="19deb-117">Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxy Server umgehen, wenn der Hostteil der Ziel-URL mit einem Eintrag in der Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="19deb-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="19deb-118">Das \* Zeichen kann als Platzhalter Zeichen zum Auflisten von Einträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19deb-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="19deb-119">Beispielsweise \* entspricht ". com" allen Hosts in der com-Domäne, und 67. \* entspricht allen Hosts in der 67-Klasse einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="19deb-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="19deb-120">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19deb-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="19deb-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19deb-121">Examples</span></span>

<span data-ttu-id="19deb-122">Im folgenden Codebeispiel wird **getproxyexceptionlist** verwendet, um anzuzeigen, ob Windows Media Player so festgelegt ist, dass der Proxy Server für lokale Adressen umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="19deb-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="19deb-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="19deb-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="19deb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19deb-124">Requirements</span></span>



| <span data-ttu-id="19deb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19deb-125">Requirement</span></span> | <span data-ttu-id="19deb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19deb-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19deb-127">Version</span><span class="sxs-lookup"><span data-stu-id="19deb-127">Version</span></span><br/>   | <span data-ttu-id="19deb-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="19deb-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="19deb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="19deb-129">Namespace</span></span><br/> | <span data-ttu-id="19deb-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="19deb-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="19deb-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="19deb-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="19deb-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="19deb-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19deb-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19deb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19deb-134">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="19deb-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19deb-135">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="19deb-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19deb-136">**Iwmpnetwork. setproxyexceptionlist (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="19deb-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





