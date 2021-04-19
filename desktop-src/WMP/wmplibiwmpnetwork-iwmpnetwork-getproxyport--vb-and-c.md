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
# <a name="iwmpnetworkgetproxyport-method"></a>Iwmpnetwork:: getproxyport-Methode

Die **getproxyport** -Methode gibt den verwendeten ProxyPort zurück.

## <a name="syntax"></a>Syntax


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





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauprotocol* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Protokoll Name ist. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Int32** , das den verwendeten ProxyPort ist. Der Wert ist nur dann von Bedeutung, wenn **iwmpnetwork. getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).

## <a name="remarks"></a>Bemerkungen

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getproxyport** verwendet, um die aktuellen Windows Media Player Proxy Portnummern für die MMS-und HTTP-Protokolle anzuzeigen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. getproxysettings (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. setproxyport (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





