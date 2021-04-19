---
title: Iwmpnetwork (setproxyport-Methode)
description: Die setproxyport-Methode gibt den zu verwendenden ProxyPort an. | Iwmpnetwork (setproxyport-Methode)
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- setproxyport-Methode, Windows Media Player
- setproxyport-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, setproxyport-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365605"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="aa4f3-107">Iwmpnetwork:: setproxyport-Methode</span><span class="sxs-lookup"><span data-stu-id="aa4f3-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="aa4f3-108">Die **setproxyport** -Methode gibt den zu verwendenden ProxyPort an.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4f3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa4f3-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="aa4f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa4f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4f3-111">*bstrauprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa4f3-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4f3-112">Ein **System. String** -Wert, der der Protokoll Name ist.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="aa4f3-113">Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="aa4f3-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa4f3-114">*lproxyport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa4f3-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4f3-115">Ein **System. Int32** , der der zu verwendende ProxyPort ist.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4f3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa4f3-116">Return value</span></span>

<span data-ttu-id="aa4f3-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa4f3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa4f3-118">Remarks</span></span>

<span data-ttu-id="aa4f3-119">Diese Methode hat keine Auswirkung, es sei denn, der Wert, der von **iwmpnetwork. getproxysettings** abgerufen wird, ist 2 (manuelle Einstellungen verwenden).</span><span class="sxs-lookup"><span data-stu-id="aa4f3-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="aa4f3-120">Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="aa4f3-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa4f3-121">Examples</span></span>

<span data-ttu-id="aa4f3-122">Im folgenden Codebeispiel wird **setproxyport** verwendet, um die Portnummer des Windows-Media Player Proxys für das MMS-Protokoll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="aa4f3-123">Die Portnummer wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="aa4f3-124">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="aa4f3-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="aa4f3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa4f3-125">Requirements</span></span>



| <span data-ttu-id="aa4f3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa4f3-126">Requirement</span></span> | <span data-ttu-id="aa4f3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="aa4f3-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4f3-128">Version</span><span class="sxs-lookup"><span data-stu-id="aa4f3-128">Version</span></span><br/>   | <span data-ttu-id="aa4f3-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="aa4f3-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="aa4f3-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa4f3-130">Namespace</span></span><br/> | <span data-ttu-id="aa4f3-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="aa4f3-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="aa4f3-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="aa4f3-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aa4f3-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="aa4f3-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4f3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa4f3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4f3-135">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="aa4f3-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aa4f3-136">**Iwmpnetwork. getproxyport (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="aa4f3-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aa4f3-137">**Iwmpnetwork. getproxysettings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="aa4f3-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





