---
title: IWMPNetwork setProxyName-Methode
description: Die setProxyName-Methode gibt den Namen des zu verwendenden Proxyservers an. | IWMPNetwork setProxyName-Methode
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- setProxyName-Methode Windows Media Player
- setProxyName-Methode Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , setProxyName-Methode
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
ms.openlocfilehash: fe4525b3933f0929413a2719e1338083b00b9995a4ba39085f5787c6feca9931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568715"
---
# <a name="iwmpnetworksetproxyname-method"></a>IWMPNetwork::setProxyName-Methode

Die **setProxyName-Methode** gibt den Namen des zu verwendenden Proxyservers an.

## <a name="syntax"></a>Syntax


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





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrProtocol* \[ In\]
</dt> <dd>

Eine **System.String,die** der Protokollname ist. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> <dt>

*bstrProxyName* \[ In\]
</dt> <dd>

Eine **System.String,** die dem Namen des zu verwendende Proxyservers entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode hat keine Auswirkung, es sei denn, der aus **IWMPNetwork.getProxySettings** abgerufene Wert ist 2 (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **setProxyName** verwendet, um den Namen des Windows Media Player Proxyservers für das MMS-Protokoll anzugeben. Der neue Name wird aus einem Textfeld abgerufen, wenn auf eine Schaltfläche geklickt wird. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Serie 9 oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxyName (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





