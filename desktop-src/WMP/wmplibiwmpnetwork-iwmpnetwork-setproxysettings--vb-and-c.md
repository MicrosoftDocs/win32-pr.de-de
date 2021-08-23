---
title: IWMPNetwork setProxySettings-Methode
description: Die setProxySettings-Methode gibt die Proxyeinstellungen für ein Protokoll an.
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- setProxySettings-Methode Windows Media Player
- setProxySettings-Methode Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , setProxySettings-Methode
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258c25fb962acdac2f682ba20b3280b8baa489496046c79d7edd03b519a67b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053468"
---
# <a name="iwmpnetworksetproxysettings-method"></a>IWMPNetwork::setProxySettings-Methode

Die **setProxySettings-Methode** gibt die Proxyeinstellungen für ein Protokoll an.

## <a name="syntax"></a>Syntax


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrProtocol* \[ In\]
</dt> <dd>

Eine **System.String,die** der Protokollname ist. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> <dt>

*lProxySetting* \[ In\]
</dt> <dd>

Eine **System.Int32-Datei,** die einer der folgenden Werte ist.



| Wert | Beschreibung                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Verwenden Sie keinen Proxyserver.                                           |
| 1     | Verwenden Sie die Proxyeinstellungen des aktuellen Browsers (nur für HTTP gültig). |
| 2     | Verwenden Sie die manuell angegebenen Proxyeinstellungen.                           |
| 3     | Automatische Erkennung der Proxyeinstellungen.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird ein Listenfeld verwendet, damit der Benutzer die Windows Media Player Proxyeinstellung für das HTTP-Protokoll festlegen kann. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





