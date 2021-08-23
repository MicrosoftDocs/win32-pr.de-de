---
title: Methode hinzufügen
description: Methode hinzufügen
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ae6cc3cd0a39be8b293a6ae64a96859e5d4fcf6d23ff410439422676b3527e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976830"
---
# <a name="add-method"></a>Methode hinzufügen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Fügt der [Commands-Auflistung](the-command-object.md) ein [Command-Objekt](the-commands-collection-object.md) hinzu.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands.Add_ *  *Name*, *Caption*, *Voice*, *Enabled*, *Visible*



| Teil      | Beschreibung                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Name*    | Erforderlich. Ein Zeichenfolgenwert, der der ID entspricht, die Sie für den Befehl zuweisen.                                                                                                                                                                                                                                        |
| *Caption* | Optional. Ein Zeichenfolgenwert, der dem Namen entspricht, der im Popupmenü des Zeichens und im Befehlsfenster angezeigt wird, wenn die Clientanwendung eingabeaktiv ist. Weitere Informationen finden Sie unter der [Caption-Eigenschaft](the-command-object.md) des [Command-Objekts.](caption-property.md)                       |
| *Voice*   | Optional. Ein Zeichenfolgenwert, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine für die Erkennung dieses Befehls verwendet werden sollen. Weitere Informationen zu Formatierungsalternativen für die Zeichenfolge finden Sie in der [Voice-Eigenschaft](the-command-object.md) des [Command-Objekts.](voice-property.md)                                |
| *Aktiviert* | Optional. Ein boolescher Wert, der angibt, ob der Befehl aktiviert ist. Der Standardwert ist **True**. Weitere Informationen finden Sie unter der [Enabled-Eigenschaft](the-command-object.md) des [Command-Objekts.](enabled-property.md)                                                                                              |
| *Visible* | Optional. Ein boolescher Wert, der angibt, ob der Befehl im Popupmenü des Zeichens für das Zeichen sichtbar ist, wenn die Clientanwendung eingabeaktiv ist. Der Standardwert ist **True**. Weitere Informationen finden Sie unter der [Visible-Eigenschaft](the-command-object.md) des [Command-Objekts.](visible-property.md) |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Wert der [Name-Eigenschaft](the-command-object.md) eines [Command-Objekts](name-property.md) muss innerhalb der Commands-Auflistung [eindeutig](the-commands-collection-object.md) sein. Sie müssen einen Befehl entfernen, bevor Sie einen neuen Befehl mit der gleichen Name-Eigenschafteneinstellung erstellen können. Der Versuch, einen Befehl mit einer bereits vorhanden Eigenschaft Name zu erstellen, löst einen Fehler aus.

Diese Methode gibt auch ein [Command-Objekt](the-command-object.md) zurück. Dadurch können Sie ein Objekt deklarieren und ihm einen Befehl zuweisen, wenn Sie die Addmethod aufrufen.


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

 

 




