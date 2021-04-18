---
title: Iwmpsettings. IsAvailable (VB und C)
description: Die IsAvailable-Eigenschaft (die get \_ IsAvailable-Methode in C \) Ruft einen Wert ab, der angibt, ob eine angegebene Aktion ausgeführt werden kann.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- Iwmpsettings. IsAvailable (VB und C) Windows Media Player
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
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351208"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>Iwmpsettings. IsAvailable (VB und c#)

Mit der **IsAvailable** -Eigenschaft (der **get \_ IsAvailable** -Methode in c#) wird ein Wert abgerufen, der angibt, ob eine bestimmte Aktion ausgeführt werden kann.


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

*bstritem*

Ein **System. String** -Wert, der einem der folgenden Werte entspricht.



| Wert              | BESCHREIBUNG                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| AutoStart          | Ermittelt, ob die Autostart-Eigenschaft festgelegt werden kann, um anzugeben, dass Windows Media Player die Wiedergabe automatisch startet. |
| Balance            | Ermittelt, ob die Balance-Eigenschaft verwendet werden kann, um den Stereo Saldo festzulegen.                                           |
| Basis            | Ermittelt, ob die baseurl-Eigenschaft festgelegt werden kann, um eine Basis-URL anzugeben.                                                |
| Defaultframe       | Ermittelt, ob die defaultframe-Eigenschaft festgelegt werden kann, um den Standard Frame anzugeben.                                    |
| Enableerrordialogfelder | Ermittelt, ob die enableerrordialogs-Eigenschaft festgelegt werden kann, um das Anzeigen von Fehler Dialogfeldern zu aktivieren oder deaktivieren.        |
| GetMode            | Ermittelt, ob die getMode-Methode verwendet werden kann, um die aktuelle Schleife oder den Streamingmodus abzurufen.                          |
| Invokeurls         | Ermittelt, ob die invokeurls-Eigenschaft festgelegt werden kann, um anzugeben, ob URL-Ereignisse einen Webbrowser starten sollen.         |
| Mute               | Ermittelt, ob die stumm Eigenschaft festgelegt werden kann, um anzugeben, ob die Audioausgabe ein-oder ausgeschaltet ist.                        |
| Playcount          | Ermittelt, ob die playcount-Eigenschaft festgelegt werden kann, um anzugeben, wie oft ein Medien Element abgespielt werden soll.                 |
| Rate               | Ermittelt, ob die Raten Eigenschaft festgelegt werden kann, um die Wiedergabe Rate zu steuern.                                            |
| SetMode            | Ermittelt, ob die setmode-Methode verwendet werden kann, um die aktuelle Schleife oder den Shuffle-Modus anzugeben.                           |
| Lautstärke             | Ermittelt, ob die Volumeeigenschaft festgelegt werden kann, um das audiovolume anzugeben.                                           |



 

## <a name="property-value"></a>Eigenschaftswert

Ein **System. Boolean** -Wert, der angibt, ob die angegebene Aktion ausgeführt werden kann.

## <a name="remarks"></a>Bemerkungen

**Iwmpsettings. isidentical** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt. In c# wird dies als **iwmpsettings. get \_ isidentical** -Methode bezeichnet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird jede der **iwmpsettings** -Eigenschaften mithilfe der **IsAvailable** -Eigenschaft getestet (die **get \_ IsAvailable** -Methode in c#). Der Eigenschaftsname und das Ergebnis jedes Tests werden in einem mehrzeiligen Textfeld angezeigt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Autostart (VB und c#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Balance (VB und c#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. baseurl (VB und c#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. defaultframe (VB und c#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. enableerrordialogs (VB und c#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. getMode (VB und c#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. invokeurls (VB und c#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. stumm (VB und c#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. playcount (VB und c#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Rate (VB und c#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. SetMode (VB und c#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Volume (VB und c#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





