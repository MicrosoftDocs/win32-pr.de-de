---
title: Iwmpnetwork setproxyexceptionlist-Methode
description: Die setproxyexceptionlist-Methode gibt die Proxy Ausnahmeliste an. | Iwmpnetwork setproxyexceptionlist-Methode
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- setproxyexceptionlist-Methode, Windows Media Player
- setproxyexceptionlist-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxyexceptionlist-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372780"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="4b998-107">Iwmpnetwork:: setproxyexceptionlist-Methode</span><span class="sxs-lookup"><span data-stu-id="4b998-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="4b998-108">Die **setproxyexceptionlist** -Methode gibt die Proxy Ausnahmeliste an.</span><span class="sxs-lookup"><span data-stu-id="4b998-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b998-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b998-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="4b998-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b998-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b998-111">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b998-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b998-112">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="4b998-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="4b998-113">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4b998-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b998-114">*pbstrexceptionlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b998-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b998-115">Eine **System. String** , bei der es sich um eine durch Semikolons getrennte Liste von Hosts handelt, für die der Proxy Server umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="4b998-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="4b998-116">Führende und nachfolgende Leerzeichen sollten nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4b998-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b998-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b998-117">Return value</span></span>

<span data-ttu-id="4b998-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b998-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b998-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b998-119">Remarks</span></span>

<span data-ttu-id="4b998-120">Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxy Server umgehen, wenn der Hostteil der Ziel-URL mit einem Eintrag in der Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4b998-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="4b998-121">Das \* Zeichen kann als Platzhalter Zeichen zum Auflisten von Einträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b998-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="4b998-122">Beispielsweise \* entspricht ". com" allen Hosts in der com-Domäne, und 67. \* entspricht allen Hosts in der 67-Klasse einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="4b998-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="4b998-123">Diese Methode hat keine Auswirkung, es sei denn, der Wert, der von **iwmpnetwork. getproxysettings** abgerufen wird, ist 2 (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="4b998-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="4b998-124">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b998-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="4b998-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b998-125">Examples</span></span>

<span data-ttu-id="4b998-126">Im folgenden Codebeispiel wird **setproxyexceptionlist** verwendet, um eine Liste von Hosts anzugeben, für die der Proxy Server bei Verwendung des MMS-Protokolls umgangen wird.</span><span class="sxs-lookup"><span data-stu-id="4b998-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="4b998-127">Die neue Liste wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="4b998-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="4b998-128">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4b998-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4b998-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b998-129">Requirements</span></span>



| <span data-ttu-id="4b998-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b998-130">Requirement</span></span> | <span data-ttu-id="4b998-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4b998-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b998-132">Version</span><span class="sxs-lookup"><span data-stu-id="4b998-132">Version</span></span><br/>   | <span data-ttu-id="4b998-133">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="4b998-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4b998-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b998-134">Namespace</span></span><br/> | <span data-ttu-id="4b998-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4b998-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4b998-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="4b998-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4b998-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4b998-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b998-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b998-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b998-139">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4b998-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4b998-140">**Iwmpnetwork. getproxyexceptionlist (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4b998-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4b998-141">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4b998-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





