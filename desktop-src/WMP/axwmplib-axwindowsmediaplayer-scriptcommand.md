---
title: ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird. | ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- ScriptCommand-Ereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26724d8d2d86bd14be9aa5360678dd9caf54620e48d4b361ab120bc2b8927fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509330"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts

Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                   |
|----------|---------------------------------------------------------------|
| scType   | System.String Gibt den Typ des Skriptbefehls an.<br/> |
| Parameter    | System.String Gibt den Skriptbefehl an.<br/>         |



 

## <a name="remarks"></a>Hinweise

Befehle können in die Sounds und Bilder einer Mediendatei oder eines Windows Stream eingebettet werden. Die Befehle sind ein Paar von Unicode-Zeichenfolgen, die einer festgelegten Zeit im Stream zugeordnet sind. Wenn der Stream die Zeit erreicht, die dem Befehl zugeordnet ist, sendet das **Windows Media Player-Steuerelement ein ScriptCommand-Ereignis** mit zwei Parametern. Ein Parameter gibt den Typ des gesendeten Befehls an, während der andere Parameter den Befehl angibt. Der Typ des Parameters wird verwendet, um zu bestimmen, wie der Befehlsparameter verarbeitet wird. Jeder Befehlstyp kann in eine Datei oder einen Stream eingebettet werden, um vom **ScriptCommand-Ereignis behandelt zu** werden.

In der folgenden Tabelle werden Skriptbefehlstypen aufgeführt, die automatisch von der Windows Media Player.



| Typ                   | Beschreibung                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Das -Steuerelement zeigt den zugeordneten Text in dem durch IWMPClosedCaption angegebenen HTML-Element an. **captioningId**.                                                       |
| EREIGNIS                  | Das -Steuerelement führt anweisungen aus, die für das angegebene Ereignis definiert sind.                                                                                                  |
| Dateiname               | Das Steuerelement setzt seine **URL-Eigenschaft** zurück, versucht, die angegebene Datei zu öffnen, und beginnt sofort mit der Wiedergabe des neuen Streams.                                        |
| OPENEVENT              | Puffert den zugeordneten EVENT-Typbefehl für die rechtzeitige Ausführung des EVENT-Skripts.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Der *Parameter param* enthält den synchronisierten Text . Windows Media Player wird der Text im Untertitelbereich des Features **Jetzt wieder verwendet** angezeigt. |
| TEXT                   | Das -Steuerelement zeigt den zugeordneten Text in dem durch IWMPClosedCaption angegebenen HTML-Element an. **captioningId**.                                                       |
| URL                    | Das Steuerelement öffnet automatisch die URL, die mithilfe des Standard-Internetbrowsers angegeben wird, wenn IWMPSettings verwendet wird. **Die invokeURLs-Eigenschaft** ist auf TRUE festgelegt.                    |



 

Sie können jeden anderen Befehlstyp einbetten, solange Sie Code zur Handhabung des Befehls bereitstellen. Obwohl unbekannte Befehle vom Steuerelement ignoriert Windows Media Player werden, werden sie weiterhin an das **ScriptCommand-Ereignis** übergeben.

Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei im Modus für schnelles Vorwärts- oder Zurücksenden gescannt wird.

URL-Befehle, die vom Windows Media Player-Steuerelement empfangen werden, werden automatisch in Ihrem Standardwebbrowser aufgerufen, wenn IWMPSettings verwendet wird. **Die invokeURLs-Eigenschaft** ist auf TRUE festgelegt. Sie können die IWMPSettings verwenden. **defaultFrame-Eigenschaft,** um den Zielframe anzugeben, in dem die Webseite angezeigt wird.

Die an Windows Media Player url wird relativ zur Basis-URL verarbeitet, die von IWMPSettings angegeben wird. **baseURL-Eigenschaft.** Die Basis-URL wird mit dem relative URL verkettet, was zu einer vollständig angegebenen URL führt, die vom **ScriptCommand-Ereignis** als Befehlsparameter übergeben wird.

Das Windows Media Player verarbeitet eingehende URL-Befehle immer wie folgt:

1.  Ein URL-Typbefehl wird empfangen.
2.  IWMPSettings. **baseURL wird** verwendet, um eine vollständige URL aus dem im Skriptbefehl angegebenen relative URL zu erstellen.
3.  **ScriptCommand** wird aufgerufen.
4.  Nachdem **ScriptCommand zurückgegeben** wurde, wird IWMPSettings zurückgegeben. **invokeURLs** ist überprüft.
5.  Wenn IWMPSettings. **invokeURLs** ist true, und der Befehl ist ein URL-Befehl. Die angegebene URL wird aufgerufen. Wenn IWMPSettings. **invokeURLs** ist false, oder wenn der Befehl kein URL-Befehl ist, wird der Befehl ignoriert.

Beim Erstellen einer Windows Media-Datei können Sie angeben, in welchem Frame die neue URL angezeigt wird, indem Sie zwei ampersands und den Namen des Frames im Parameterfeld verketten. Das folgende Beispiel veranschaulicht typische **ScriptCommand-Parameter.** Sie gibt an, dass die URL *mypage* im *myframe-Frame gestartet werden* muss.


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei gescannt wird (schnelles Weitergeleitetes oder erneutes Durchwaschen).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.captioningId (VB und C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.baseURL (VB und C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.defaultFrame (VB und C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.invokeURLs (VB und C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





