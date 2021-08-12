---
title: Player.ScriptCommand-Ereignis
description: Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird. | Player.ScriptCommand-Ereignis
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- ScriptCommand-Ereignis Windows Media Player
- ScriptCommand-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , ScriptCommand-Ereignis
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
ms.openlocfilehash: 27f54aac54cf56e65b71dbd604d57d5ae9404a0148db139779ced3aa9e0da0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572428"
---
# <a name="playerscriptcommand-event"></a>Player.ScriptCommand-Ereignis

Das **ScriptCommand-Ereignis** tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.

## <a name="syntax"></a>Syntax


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*scType* 
</dt> <dd>

Zeichenfolge, die den Typ des Skriptbefehls angibt.

</dd> <dt>

*Param* 
</dt> <dd>

**Zeichenfolge,** die den Skriptbefehl angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Befehle können zwischen den Sounds und Bildern einer Windows Mediendatei oder eines Medienstreams eingebettet werden. Die Befehle sind ein Paar von Unicode-Zeichenfolgen, die einer bestimmten Zeit im Stream zugeordnet sind. Wenn der Stream die dem Befehl zugeordnete Zeit erreicht, sendet das Windows Media Player-Steuerelement ein **ScriptCommand-Ereignis** mit zwei Parametern. Ein Parameter gibt den Typ des zu sendenden Befehls an, und der andere Parameter gibt den Befehl an. Der Typ des Parameters wird verwendet, um zu bestimmen, wie der Befehlsparameter verarbeitet wird. Jeder Befehlstyp kann in eine Datei oder einen Stream eingebettet werden, die vom **ScriptCommand-Ereignis** verarbeitet werden soll.

In der folgenden Tabelle sind Skriptbefehlstypen aufgeführt, die automatisch von Windows Media Player verarbeitet werden.



| type                   | Beschreibung                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Das -Steuerelement zeigt den zugeordneten Text im DIV an, der von *ClosedCaption* angegeben wird. **captioningID**.                                                                  |
| EREIGNIS                  | Weist das Steuerelement an, anweisungen auszuführen, die für das angegebene Ereignis definiert sind.                                                                                          |
| Dateiname               | Das Steuerelement setzt seine **URL-Eigenschaft** zurück, versucht, die angegebene Datei zu öffnen, und beginnt sofort mit der Wiedergabe des neuen Streams.                                        |
| OPENEVENT              | Puffert den zugeordneten EVENT-Typbefehl für die rechtzeitige Ausführung des EVENT-Skripts.                                                                                 |
| SYNCHRONIZEDLYRICRIC | Der *Parameter Param* enthält den synchronisierten Text . Windows Media Player zeigt den Text im Untertitelbereich des Features **Jetzt wiedergeben an.** |
| TEXT                   | Das -Steuerelement zeigt den zugeordneten Text im DIV an, der von *ClosedCaption* angegeben wird. **captioningID**.                                                                  |
| URL                    | Das -Steuerelement öffnet automatisch die url, die im Standardinternetbrowser angegeben wird, wenn die *Einstellungen.* **die invokeURLs-Eigenschaft** ist auf TRUE festgelegt.                      |



 

Sie können einen beliebigen anderen Befehlstyp einbetten, solange Sie reziproken Code für die Verarbeitung des Befehls bereitstellen. Obwohl unbekannte Befehle vom Windows Media Player-Steuerelement ignoriert werden, werden sie weiterhin an das **ScriptCommand-Ereignis** übergeben.

URL-Befehle, die vom Windows Media Player-Steuerelement empfangen werden, werden automatisch in Ihrem Standardwebbrowser aufgerufen, wenn die *Einstellungen.* **die invokeURLs-Eigenschaft** ist auf TRUE festgelegt. Sie können die *Einstellungen* verwenden. **defaultFrame-Eigenschaft,** um den Zielframe anzugeben, in dem die Webseite angezeigt wird.

Die an Windows Media Player gesendete URL wird relativ zur Basis-URL verarbeitet, die vom *Einstellungen* angegeben wird. **baseURL-Eigenschaft.** Die Basis-URL wird mit der relativ angegebenen URL verkettet, was zu einer vollständig angegebenen URL führt, die vom **ScriptCommand-Ereignis** als Befehlsparameter übergeben wird.

Das Windows Media Player-Steuerelement verarbeitet eingehende BEFEHLE vom Typ "URL" immer wie folgt:

1.  Ein URL-Typbefehl wird empfangen.
2.  *Einstellungen*. **baseURL** wird verwendet, um eine vollständige URL aus der im Skriptbefehl angegebenen relative URL zu erstellen.
3.  *ScriptCommand* wird aufgerufen.
4.  Nachdem *ScriptCommand* zurückgegeben wurde, *Einstellungen*. **invokeURLs** ist aktiviert.
5.  Wenn *Einstellungen*. **invokeURLs** ist true, und der Befehl ist ein URL-Typ. Die angegebene URL wird aufgerufen. Wenn *Einstellungen*. **invokeURLs** ist false, oder wenn der Befehl kein URL-Typ ist, wird der Befehl ignoriert.

Beim Erstellen einer Windows Media-Datei können Sie angeben, in welchem Frame die neue URL angezeigt wird, indem Sie zwei Amperands und den Namen des Frames im Parameterfeld verketten. Das folgende Beispiel veranschaulicht typische *ScriptCommand-Parameter.* Sie gibt an, dass die URL *mypage* im *Rahmen des Myframes* gestartet werden muss.


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei gescannt wird (schnell weitergeleitet oder schnell umgekehrt).

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> <dt>

[**Einstellungen.baseURL**](settings-baseurl.md)
</dt> <dt>

[**Einstellungen.defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**Einstellungen.invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





