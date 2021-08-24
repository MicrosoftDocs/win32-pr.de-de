---
title: Insert-Methode
description: Insert-Methode
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94b63da0477ee048239afa34ff57475dcce8f0d1129f4574d6b7b6543d75e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114630"
---
# <a name="insert-method"></a>Insert-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Fügt ein **Command-Objekt** in die **Commands-Auflistung** ein.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands.Insert_ *  *Name*, *RefName*, *Before*\_

*Caption,* *Voice, Enabled, Visible*



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Name*    | Erforderlich. Ein Zeichenfolgenwert, der der ID entspricht, die Sie dem [**Befehl**](/windows/desktop/lwef/the-command-object)zuweisen.                                                                                                                                                                                               |
| *Refname* | Erforderlich. Ein Zeichenfolgenwert, der dem Namen (ID) des Befehls direkt oberhalb oder unterhalb des Befehls entspricht, in den Sie den neuen Befehl einfügen möchten.                                                                                                                                                                 |
| *Vorher*  | Optional. Ein boolescher Wert, der angibt, ob der neue Befehl vor dem von RefName angegebenen Befehl eingefügt werden *soll.* **True** (Standard). Der neue Befehl wird vor dem Befehl eingefügt, auf den verwiesen wird.<br/> **False** Der neue Befehl wird nach dem Befehl eingefügt, auf den verwiesen wird.<br/> |
| *Caption* | Optional. Ein Zeichenfolgenwert, der dem Namen entspricht, der im Popupmenü des Zeichens und im Befehlsfenster angezeigt wird, wenn die Clientanwendung eingabeaktiv ist. Weitere Informationen finden Sie in der [**Caption-Eigenschaft**](caption-property.md)des [**Command-Objekts.**](/windows/desktop/lwef/the-command-object)    |
| *Voice*   | Optional. Ein Zeichenfolgenwert, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum Erkennen dieses Befehls verwendet werden sollen. Weitere Informationen zum Formatieren von Alternativen für die Zeichenfolge finden Sie in der **Voice-Eigenschaft** des [**Command-Objekts.**](/windows/desktop/lwef/the-command-object)                                  |
| *Aktiviert* | Optional. Ein boolescher Wert, der angibt, ob der Befehl aktiviert ist. Der Standardwert ist **True**. Weitere Informationen finden Sie in der **Enabled-Eigenschaft** des [**Command-Objekts.**](/windows/desktop/lwef/the-command-object)                                                                                                  |
| *Visible* | Optional. Ein boolescher Wert, der angibt, ob der Befehl im Befehlsfenster sichtbar ist, wenn die Clientanwendung eingabeaktiv ist. Der Standardwert ist **True**. Weitere Informationen finden Sie in der [**Visible-Eigenschaft**](visible-property.md) des [**Command-Objekts.**](/windows/desktop/lwef/the-command-object)       |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Wert der [**Name-Eigenschaft**](name-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) muss innerhalb seiner [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) eindeutig sein. Sie müssen einen **Befehl** entfernen, bevor Sie einen neuen **Befehl** mit der gleichen Einstellung für die **Name-Eigenschaft** erstellen können. Der Versuch, einen **Befehl** mit einer bereits vorhandenen **Name-Eigenschaft** zu erstellen, löst einen Fehler aus.

Diese Methode gibt auch ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) zurück. Dadurch können Sie ein Objekt deklarieren und ihm einen **Befehl** zuweisen, wenn Sie die **Insert-Methode** aufrufen.


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Weitere Informationen

[**Methode hinzufügen,**](add-method.md) [**Methode entfernen,**](remove-method.md) [**RemoveAll-Methode**](removeall-method.md)


 

