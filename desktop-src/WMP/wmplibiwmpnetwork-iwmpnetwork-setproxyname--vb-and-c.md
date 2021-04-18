---
title: Iwmpnetwork setproxyname-Methode
description: Die setproxyname-Methode gibt den Namen des zu verwendenden Proxy Servers an. | Iwmpnetwork setproxyname-Methode
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- setproxyname-Methode, Windows Media Player
- setproxyname-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxyname-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355054"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="6a45f-107">Iwmpnetwork:: setproxyname-Methode</span><span class="sxs-lookup"><span data-stu-id="6a45f-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="6a45f-108">Die **setproxyname** -Methode gibt den Namen des zu verwendenden Proxy Servers an.</span><span class="sxs-lookup"><span data-stu-id="6a45f-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a45f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a45f-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="6a45f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a45f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a45f-111">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a45f-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a45f-112">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="6a45f-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="6a45f-113">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="6a45f-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a45f-114">*bstrinproxyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a45f-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a45f-115">Ein **System. String** -Wert, der den Namen des zu verwendenden Proxy Servers ist.</span><span class="sxs-lookup"><span data-stu-id="6a45f-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a45f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a45f-116">Return value</span></span>

<span data-ttu-id="6a45f-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6a45f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a45f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a45f-118">Remarks</span></span>

<span data-ttu-id="6a45f-119">Diese Methode hat keine Auswirkung, es sei denn, der Wert, der von **iwmpnetwork. getproxysettings** abgerufen wird, ist 2 (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="6a45f-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="6a45f-120">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a45f-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="6a45f-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a45f-121">Examples</span></span>

<span data-ttu-id="6a45f-122">Im folgenden Codebeispiel wird **setproxyname** verwendet, um den Namen des Windows Media Player-Proxy Servers für das MMS-Protokoll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6a45f-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="6a45f-123">Der neue Name wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="6a45f-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="6a45f-124">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6a45f-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6a45f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a45f-125">Requirements</span></span>



| <span data-ttu-id="6a45f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a45f-126">Requirement</span></span> | <span data-ttu-id="6a45f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6a45f-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a45f-128">Version</span><span class="sxs-lookup"><span data-stu-id="6a45f-128">Version</span></span><br/>   | <span data-ttu-id="6a45f-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="6a45f-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6a45f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a45f-130">Namespace</span></span><br/> | <span data-ttu-id="6a45f-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6a45f-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6a45f-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="6a45f-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6a45f-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6a45f-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a45f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a45f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a45f-135">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6a45f-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a45f-136">**Iwmpnetwork. getproxyname (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6a45f-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a45f-137">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6a45f-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





