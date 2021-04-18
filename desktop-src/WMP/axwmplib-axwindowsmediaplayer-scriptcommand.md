---
title: ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird. | ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- ScriptCommand-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358093"
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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ scriptcommandeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ scriptcommandevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft | BESCHREIBUNG                                                   |
|----------|---------------------------------------------------------------|
| sctype   | System. StringGibt den Typ des Skript Befehls an.<br/> |
| Parameter    | System. StringGibt den Skript Befehl an.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

Befehle können zwischen den Sounds und Bildern einer Windows Media-Datei oder eines Windows-Streams eingebettet werden. Die Befehle sind ein paar von Unicode-Zeichen folgen, die mit einer bestimmten Zeit im Stream verknüpft sind. Wenn der Stream den dem Befehl zugeordneten Zeitpunkt erreicht, sendet das Windows Media Player-Steuerelement ein **ScriptCommand** -Ereignis mit zwei Parametern. Ein Parameter gibt den Typ des gesendeten Befehls an, und der andere Parameter gibt den Befehl an. Der Parametertyp wird verwendet, um zu bestimmen, wie der Befehlsparameter verarbeitet wird. Alle Befehls Typen können in eine Datei oder einen Stream eingebettet werden, damit Sie vom **ScriptCommand** -Ereignis verarbeitet wird.

In der folgenden Tabelle sind Skript Befehls Typen aufgeführt, die automatisch von Windows Media Player verarbeitet werden.



| type                   | BESCHREIBUNG                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Das-Steuerelement zeigt den zugeordneten Text im von iwmpclosedcaption angegebenen HTML-Element an. **captioningid**.                                                       |
| EREIGNIS                  | Das Steuerelement führt Anweisungen aus, die für das angegebene Ereignis definiert sind.                                                                                                  |
| Einfügen               | Das-Steuerelement setzt seine **URL** -Eigenschaft zurück, versucht, die angegebene Datei zu öffnen, und beginnt sofort mit der Wiedergabe des neuen Streams.                                        |
| OpenEvent              | Puffert den zugeordneten Ereignistyp Befehl für die rechtzeitige Ausführung des Ereignis Skripts.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Der Parameter *param* enthält den synchronisierten Text. In Windows Media Player wird der Text im Bereich geschlossene Überschrift der Funktion **jetzt abgespielt** angezeigt. |
| TEXT                   | Das-Steuerelement zeigt den zugeordneten Text im von iwmpclosedcaption angegebenen HTML-Element an. **captioningid**.                                                       |
| URL                    | Das-Steuerelement öffnet automatisch die URL, die mit dem Standard Internet Browser angegeben wird, wenn iwmpsettings. die **invokeurls** -Eigenschaft ist auf true festgelegt.                    |



 

Sie können beliebige andere Befehls Typen einbetten, solange Sie Code zum Verarbeiten des Befehls bereitstellen. Obwohl unbekannte Befehle vom Windows Media Player-Steuerelement ignoriert werden, werden Sie weiterhin an das **ScriptCommand** -Ereignis übergeben.

Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei im schnell Forward-oder Rewind-Modus gescannt wird.

URL-Befehle, die vom Windows-Media Player-Steuerelement empfangen werden, werden automatisch in Ihrem Standard Webbrowser aufgerufen, wenn iwmpsettings. die **invokeurls** -Eigenschaft ist auf true festgelegt. Sie können die iwmpsettings verwenden. **defaultframe** -Eigenschaft, um den Zielframe anzugeben, in dem die Webseite angezeigt wird.

Die an Windows Media Player gesendete URL wird relativ zur Basis-URL verarbeitet, die von iwmpsettings angegeben wird. **baseurl** -Eigenschaft. Die Basis-URL wird mit dem relative URL verkettet, was zu einer vollständig angegebenen URL führt, die vom **ScriptCommand** -Ereignis als Befehlsparameter übergeben wird.

Das Windows Media Player-Steuerelement verarbeitet eingehende URL-Befehle immer wie folgt:

1.  Ein URL-Type-Befehl wird empfangen.
2.  Iwmpsettings. **baseurl** wird verwendet, um eine vollständige URL aus der relative URL zu erstellen, die im Skript Befehl angegeben ist.
3.  **ScriptCommand** wird aufgerufen.
4.  Nachdem **ScriptCommand** zurückgegeben wurde, iwmpsettings. **invokeurls** wird geprüft.
5.  Wenn iwmpsettings. **invokeurls** ist true, und der Befehl ist ein URL-Befehl, die angegebene URL wird aufgerufen. Wenn iwmpsettings. **invokeurls** ist false, oder wenn der Befehl kein URL-Befehl ist, wird der Befehl ignoriert.

Wenn Sie eine Windows Media-Datei erstellen, können Sie angeben, in welchem Frame die neue URL angezeigt werden soll, indem Sie zwei kaufmännische und den Namen des Frames im Parameterfeld verketten. Im folgenden Beispiel werden typische **ScriptCommand** -Parameter veranschaulicht. Er gibt an, dass die URL *MyPage* im Frame " *MyFrame* " gestartet werden muss.


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei gescannt wird (schnell weitergeleitet oder reaktiviert).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Iwmpclosedcaption. captioningid (VB und c#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. baseurl (VB und c#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. defaultframe (VB und c#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. invokeurls (VB und c#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





