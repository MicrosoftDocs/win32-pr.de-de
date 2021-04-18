---
title: Insert-Methode
description: Insert-Methode
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338058"
---
# <a name="insert-method"></a>Insert-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Fügt ein **Befehls** Objekt in die **Commands** -Auflistung ein.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Commands. Insert* *  *Name*, *ref Name*, *before*\_

*Beschriftung*, *Stimme, aktiviert, sichtbar*



| Teil      | BESCHREIBUNG                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Name*    | Erforderlich. Ein Zeichen folgen Wert, der der ID entspricht, die Sie dem [**Befehl**](/windows/desktop/lwef/the-command-object)zuweisen.                                                                                                                                                                                               |
| *RefName* | Erforderlich. Ein Zeichen folgen Wert, der dem Namen (ID) des Befehls direkt oberhalb oder unterhalb des Befehls entspricht, an dem der neue Befehl eingefügt werden soll.                                                                                                                                                                 |
| *Vorher*  | Dies ist optional. Ein boolescher Wert, der angibt, ob der neue Befehl vor dem Befehl eingefügt werden soll, der von *refname* angegeben wird. **True** (Standard). Der neue Befehl wird vor dem Befehl eingefügt, auf den verwiesen wird.<br/> **False** Der neue Befehl wird nach dem Befehl eingefügt, auf den verwiesen wird.<br/> |
| *Caption* | Dies ist optional. Ein Zeichen folgen Wert, der dem Namen entspricht, der im Popupmenü des Zeichens und im Befehlsfenster angezeigt wird, wenn die Client Anwendung aktiv ist. Weitere Informationen finden Sie in der [**Beschriftung**](caption-property.md)-Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.    |
| *Voice*   | Dies ist optional. Ein Zeichen folgen Wert, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum erkennen dieses Befehls verwendet werden sollen. Weitere Informationen zum Formatieren von Alternativen für die Zeichenfolge finden Sie in der **Voice** -Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.                                  |
| *Aktiviert* | Dies ist optional. Ein boolescher Wert, der angibt, ob der Befehl aktiviert ist. Der Standardwert ist **True**. Weitere Informationen finden Sie unter der **aktivierten** Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.                                                                                                  |
| *Visible* | Dies ist optional. Ein boolescher Wert, der angibt, ob der Befehl im Befehlsfenster sichtbar ist, wenn die Client Anwendung aktiv ist. Der Standardwert ist **True**. Weitere Informationen finden Sie in der [**Visible**](visible-property.md) -Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.       |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Wert der Eigenschaft " [**Name**](name-property.md) " eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts muss [**innerhalb der Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung eindeutig sein. Sie müssen einen **Befehl** entfernen, bevor Sie einen neuen **Befehl** mit der gleichen **namens** Eigenschafts Einstellung erstellen können. Wenn Sie versuchen, einen **Befehl** mit einer bereits vorhandenen **Name** -Eigenschaft zu erstellen, wird ein Fehler ausgelöst.

Diese Methode gibt auch ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt zurück. Dies ermöglicht es Ihnen, ein Objekt zu deklarieren und ihm einen **Befehl** zuzuweisen, wenn Sie die **Insert** -Methode aufzurufen.


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Weitere Informationen

[**Add-Methode**](add-method.md), [**Remove**](remove-method.md)-Methode, [**RemoveAll-Methode**](removeall-method.md)


 

