---
title: Player. ScriptCommand-Ereignis
description: Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird. | Player. ScriptCommand-Ereignis
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- ScriptCommand-Ereignisfenster Media Player
- ScriptCommand-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, ScriptCommand-Ereignis
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365856"
---
# <a name="playerscriptcommand-event"></a>Player. ScriptCommand-Ereignis

Das **ScriptCommand** -Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.

## <a name="syntax"></a>Syntax


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sctype* 
</dt> <dd>

Zeichenfolge, die den Typ des Skript Befehls angibt.

</dd> <dt>

*Parameter* 
</dt> <dd>

**Zeichenfolge** , die den Skript Befehl angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Befehle können zwischen den Sounds und Bildern einer Windows Media-Datei oder eines Windows-Streams eingebettet werden. Die Befehle sind ein paar von Unicode-Zeichen folgen, die mit einer bestimmten Zeit im Stream verknüpft sind. Wenn der Stream den dem Befehl zugeordneten Zeitpunkt erreicht, sendet das Windows Media Player-Steuerelement ein **ScriptCommand** -Ereignis mit zwei Parametern. Ein Parameter gibt den Typ des gesendeten Befehls an, und der andere Parameter gibt den Befehl an. Der Parametertyp wird verwendet, um zu bestimmen, wie der Befehlsparameter verarbeitet wird. Alle Befehls Typen können in eine Datei oder einen Stream eingebettet werden, damit Sie vom **ScriptCommand** -Ereignis verarbeitet wird.

In der folgenden Tabelle sind Skript Befehls Typen aufgeführt, die automatisch von Windows Media Player verarbeitet werden.



| type                   | BESCHREIBUNG                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Das-Steuerelement zeigt den zugeordneten Text in dem durch *closedcaption* angegebenen div-Element an. **captioningid**.                                                                  |
| EREIGNIS                  | Weist das Steuerelement an, Anweisungen auszuführen, die für das angegebene Ereignis definiert sind.                                                                                          |
| Einfügen               | Das-Steuerelement setzt seine **URL** -Eigenschaft zurück, versucht, die angegebene Datei zu öffnen, und beginnt sofort mit der Wiedergabe des neuen Streams.                                        |
| OpenEvent              | Puffert den zugeordneten Ereignistyp Befehl für die rechtzeitige Ausführung des Ereignis Skripts.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Der Parameter *param* enthält den synchronisierten Text. In Windows Media Player wird der Text im Bereich geschlossene Überschrift der Funktion **jetzt abgespielt** angezeigt. |
| TEXT                   | Das-Steuerelement zeigt den zugeordneten Text in dem durch *closedcaption* angegebenen div-Element an. **captioningid**.                                                                  |
| URL                    | Das-Steuerelement öffnet automatisch die URL, die mit dem Standard Internet Browser angegeben wird, wenn die *Einstellungen*. die **invokeurls** -Eigenschaft ist auf true festgelegt.                      |



 

Sie können beliebige andere Befehls Typen einbetten, solange Sie gegenseitigen Code zur Behandlung des Befehls bereitstellen. Obwohl unbekannte Befehle vom Windows Media Player-Steuerelement ignoriert werden, werden Sie weiterhin an das **ScriptCommand** -Ereignis übergeben.

URL-Befehle, die vom Windows Media Player-Steuerelement empfangen werden, werden automatisch in Ihrem Standard Webbrowser aufgerufen, wenn die *Einstellungen*. die **invokeurls** -Eigenschaft ist auf true festgelegt. Sie können die *Einstellungen* verwenden. **defaultframe** -Eigenschaft, um den Zielframe anzugeben, in dem die Webseite angezeigt wird.

Die an Windows Media Player gesendete URL wird relativ zur Basis-URL verarbeitet, die in den *Einstellungen* angegeben ist. **baseurl** -Eigenschaft. Die Basis-URL wird mit der relativ angegebenen URL verkettet, was zu einer vollständig angegebenen URL führt, die vom **ScriptCommand** -Ereignis als Befehlsparameter übergeben wird.

Das Windows Media Player-Steuerelement verarbeitet eingehende URL-Typbefehle immer wie folgt:

1.  Ein URL-Type-Befehl wird empfangen.
2.  *Einstellungen*. **baseurl** wird verwendet, um eine vollständige URL aus der relative URL zu erstellen, die im Skript Befehl angegeben ist.
3.  *ScriptCommand* wird aufgerufen.
4.  Nachdem *ScriptCommand* zurückgegeben wurde, werden die *Einstellungen*. **invokeurls** wird geprüft.
5.  Wenn *Einstellungen*. **invokeurls** ist true, und der Befehl ist ein URL-Typ, die angegebene URL wird aufgerufen. Wenn *Einstellungen*. **invokeurls** ist false, oder wenn der Befehl kein URL-Typ ist, wird der Befehl ignoriert.

Wenn Sie eine Windows Media-Datei erstellen, können Sie angeben, in welchem Frame die neue URL angezeigt werden soll, indem Sie zwei kaufmännische und den Namen des Frames im Parameterfeld verketten. Im folgenden Beispiel werden typische *ScriptCommand* -Parameter veranschaulicht. Er gibt an, dass die URL *MyPage* im Frame " *MyFrame* " gestartet werden muss.


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei gescannt wird (schnell weitergeleitet oder schnell-umgekehrt).

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Settings. baseurl**](settings-baseurl.md)
</dt> <dt>

[**Settings. defaultframe**](settings-defaultframe.md)
</dt> <dt>

[**Settings. invokeurls**](settings-invokeurls.md)
</dt> </dl>

 

 





