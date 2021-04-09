---
title: Methode hinzufügen
description: Methode hinzufügen
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036850"
---
# <a name="add-method"></a>Methode hinzufügen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Fügt [der Befehls](the-commands-collection-object.md) Auflistung ein [Befehls](the-command-object.md) Objekt hinzu.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Befehle. Add* *  *Name*, *Caption*, *Voice*, *aktiviert*, *Visible*



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Name*    | Erforderlich. Ein Zeichen folgen Wert, der der ID entspricht, die Sie für den Befehl zuweisen.                                                                                                                                                                                                                                        |
| *Caption* | Dies ist optional. Ein Zeichen folgen Wert, der dem Namen entspricht, der im Popupmenü des Zeichens und im Befehlsfenster angezeigt wird, wenn die Client Anwendung aktiv ist. Weitere Informationen finden Sie in der [Beschriftung](caption-property.md) -Eigenschaft des [Befehls](the-command-object.md) Objekts.                       |
| *Voice*   | Dies ist optional. Ein Zeichen folgen Wert, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum erkennen dieses Befehls verwendet werden sollen. Weitere Informationen zum Formatieren von Alternativen für die Zeichenfolge finden Sie in der [Voice](voice-property.md) -Eigenschaft des [Befehls](the-command-object.md) Objekts.                                |
| *Aktiviert* | Dies ist optional. Ein boolescher Wert, der angibt, ob der Befehl aktiviert ist. Der Standardwert ist **True**. Weitere Informationen finden Sie unter der [aktivierten](enabled-property.md) Eigenschaft des [Befehls](the-command-object.md) Objekts.                                                                                              |
| *Visible* | Dies ist optional. Ein boolescher Wert, der angibt, ob der Befehl im Popup Menü des Zeichens für das Zeichen sichtbar ist, wenn die Client Anwendung aktiv ist. Der Standardwert ist **True**. Weitere Informationen finden Sie in der [Visible](visible-property.md) -Eigenschaft des [Befehls](the-command-object.md) Objekts. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Wert der Eigenschaft " [Name](name-property.md) " eines [Befehls](the-command-object.md) Objekts muss [innerhalb der Befehls](the-commands-collection-object.md) Auflistung eindeutig sein. Sie müssen einen Befehl entfernen, bevor Sie einen neuen Befehl mit der gleichen Namens Eigenschafts Einstellung erstellen können. Wenn Sie versuchen, einen Befehl mit einer bereits vorhandenen Name-Eigenschaft zu erstellen, wird ein Fehler ausgelöst.

Diese Methode gibt auch ein [Command](the-command-object.md) -Objekt zurück. Dies ermöglicht es Ihnen, ein Objekt zu deklarieren und ihm einen Befehl zuzuweisen, wenn Sie die AddMethod-Methode aufgerufen haben.


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Insert-Methode**](insert-method.md)
</dt> <dt>

[**RemoveAll-Methode**](removeall-method.md)
</dt> <dt>

[**Remove-Methode**](remove-method.md)
</dt> </dl>

 

 




