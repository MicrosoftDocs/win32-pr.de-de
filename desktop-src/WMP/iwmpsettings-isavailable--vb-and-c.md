---
title: IWMPSettings.isAvailable (VB und C )
description: Die isAvailable-Eigenschaft (die get \_ isAvailable-Methode in C\) ruft einen Wert ab, der angibt, ob eine angegebene Aktion ausgeführt werden kann.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings.isAvailable (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590979677e79073466f7511b3f382a4bfcebc8bf0fd8ad4cb10f6dcd957db28a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135373"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings.isAvailable (VB und C#)

Die **isAvailable-Eigenschaft** (die **get \_ isAvailable-Methode** in C#) ruft einen Wert ab, der angibt, ob eine angegebene Aktion ausgeführt werden kann.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parameter

*bstrItem*

Eine **System.String,die** einer der folgenden Werte ist.



| Wert              | Beschreibung                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| AutoStart          | Ermittelt, ob die autoStart-Eigenschaft festgelegt werden kann, um anzugeben, dass Windows Media Player die Wiedergabe automatisch startet. |
| Balance            | Ermittelt, ob die Balance-Eigenschaft verwendet werden kann, um den Stereosaldo festzulegen.                                           |
| BaseURL            | Ermittelt, ob die baseURL-Eigenschaft festgelegt werden kann, um eine Basis-URL anzugeben.                                                |
| DefaultFrame       | Ermittelt, ob die defaultFrame-Eigenschaft festgelegt werden kann, um den Standardframe anzugeben.                                    |
| EnableErrorDialogs | Ermittelt, ob die enableErrorDialogs-Eigenschaft zum Aktivieren oder Deaktivieren der Anzeige von Fehlerdialogfeldern festgelegt werden kann.        |
| GetMode            | Ermittelt, ob die getMode-Methode zum Abrufen der aktuellen Schleife oder des Shufflemodus verwendet werden kann.                          |
| InvokeURLs         | Ermittelt, ob die invokeURLs-Eigenschaft festgelegt werden kann, um anzugeben, ob URL-Ereignisse einen Webbrowser starten sollen.         |
| Mute               | Ermittelt, ob die Stummschaltungseigenschaft festgelegt werden kann, um anzugeben, ob die Audioausgabe ein- oder ausgeschaltet ist.                        |
| PlayCount          | Ermittelt, ob die playCount-Eigenschaft festgelegt werden kann, um anzugeben, wie oft ein Medienelement wiedergegeben wird.                 |
| Rate               | Ermittelt, ob die Rate-Eigenschaft festgelegt werden kann, um die Wiedergaberate zu steuern.                                            |
| SetMode            | Ermittelt, ob die setMode-Methode verwendet werden kann, um die aktuelle Schleife oder den Shufflemodus anzugeben.                           |
| Volume             | Ermittelt, ob die Volumeeigenschaft festgelegt werden kann, um das Audiovolume anzugeben.                                           |



 

## <a name="property-value"></a>Eigenschaftswert

Ein **System.Boolean-Wert,** der angibt, ob die angegebene Aktion ausgeführt werden kann.

## <a name="remarks"></a>Hinweise

**IWMPSettings.isIdentical** ist eine Eigenschaft in Visual Basic, die einen Parameter annimmt. In C# wird dies als **IWMPSettings.get \_ isIdentical-Methode** bezeichnet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird jede der **IWMPSettings-Eigenschaften** mithilfe der **isAvailable-Eigenschaft** getestet (die **get \_ isAvailable-Methode** in C#). Der Eigenschaftenname und das Ergebnis jedes Tests werden in einem mehrzeiligen Textfeld angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB und C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.balance (VB und C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.baseURL (VB und C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.defaultFrame (VB und C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB und C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.getMode (VB und C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.invokeURLs (VB und C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.mute (VB und C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.playCount (VB und C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB und C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB und C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.volume (VB und C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





