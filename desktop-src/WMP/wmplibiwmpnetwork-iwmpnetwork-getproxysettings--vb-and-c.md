---
title: Iwmpnetwork getproxysettings-Methode
description: Die getproxysettings-Methode gibt Informationen zu den Proxy Einstellungen für ein Protokoll zurück.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- getproxysettings-Methode, Windows-Media Player
- getproxysettings-Methode, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, getproxysettings-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372143"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>Iwmpnetwork:: getproxysettings-Methode

Die **getproxysettings** -Methode gibt Informationen zu den Proxy Einstellungen für ein Protokoll zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauprotocol* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Protokoll Name ist. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Int32** -Wert, der einem der folgenden Werte entspricht.



| Wert | BESCHREIBUNG                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Ein Proxy Server wird nicht verwendet.                                                |
| 1     | Die Proxy Einstellungen für den aktuellen Browser werden verwendet (nur für http gültig). |
| 2     | Die manuell angegebenen Proxy Einstellungen werden verwendet.                            |
| 3     | Die Proxy Einstellungen werden automatisch erkannt.                                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getproxysettings** verwendet, um eine Meldung anzuzeigen, die Informationen über die aktuellen Proxy Einstellungen des Players in einer Bezeichnung enthält. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
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

[**Iwmpnetwork. setproxysettings (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





