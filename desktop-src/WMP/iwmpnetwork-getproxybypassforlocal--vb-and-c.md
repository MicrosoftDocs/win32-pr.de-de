---
title: IWMPNetwork getProxyBypassForLocal-Methode
description: Die getProxyBypassForLocal-Methode gibt einen Wert zurück, der angibt, ob der Proxyserver umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- getProxyBypassForLocal-Methode Windows Media Player
- getProxyBypassForLocal-Methode Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , getProxyBypassForLocal-Methode
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
ms.openlocfilehash: 50d23307ab8872fb49b2b4797d54b78a71a04adba350287fa23cb8e5ab90541c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996480"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a>IWMPNetwork::getProxyBypassForLocal-Methode

Die **getProxyBypassForLocal-Methode** gibt einen Wert zurück, der angibt, ob der Proxyserver umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.

## <a name="syntax"></a>Syntax


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





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrProtocol* 
</dt> <dd>

Eine **System.String,die** der Protokollname ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Boolean-Wert,** der angibt, ob der Proxyserver umgangen wird. Der Wert ist nur sinnvoll, wenn **IWMPNetwork.getProxySettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).

## <a name="remarks"></a>Hinweise

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getProxyBypassForLocal** verwendet, um anzuzeigen, ob Windows Media Player so festgelegt ist, dass der Proxyserver für lokale Adressen umgangen wird. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|-----------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                             |
| Namespace<br/> | **WMPLib**<br/>                                                                         |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxyBypassForLocal (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





