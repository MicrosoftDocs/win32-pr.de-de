---
title: Das Befehlsobjekt
description: Das Befehlsobjekt
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242a90022431b826cf877edd862cd89a39d193865ed31afc1e4ff911f4189756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245616"
---
# <a name="the-command-object"></a>Das Befehlsobjekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) ist ein Element in einer [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object) Der Server bietet dem  Benutzer Zugriff auf Ihre Command-Objekte, wenn ihre Clientanwendung eingabeaktiv wird.

-   [Befehlsobjekteigenschaften](command-object-properties.md)

Um auf die Eigenschaft eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zuzugreifen, verweisen Sie in seiner Auflistung mithilfe der [**Name-Eigenschaft**](name-property.md) darauf. In VBScript und Visual Basic können Sie die **Name-Eigenschaft** direkt verwenden:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Verwenden Sie für Programmiersprachen, die keine Sammlungen unterstützen, die [**Command-Methode:**](command-method.md)


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Sie können auch auf ein Command-Objekt verweisen, indem Sie einen Verweis darauf erstellen. Deklarieren Sie in Visual Basic eine Objektvariable, und verwenden Sie die Set-Anweisung, um den Verweis zu erstellen:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In Visual Basic 5.0 können Sie das Objekt auch als Typ [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) deklarieren und den Verweis erstellen. Diese Konvention ermöglicht eine frühe Bindung, was zu einer besseren Leistung führt:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In VBScript können Sie einen Verweis als bestimmten Typ deklarieren, aber Sie können die Variable trotzdem deklarieren und auf den [**Befehl**](/windows/desktop/lwef/the-command-object) in der Auflistung festlegen:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Ein Befehl kann entweder im Popupmenü des Zeichens und im Befehlsfenster oder in beiden angezeigt werden. Um im Popupmenü angezeigt zu werden, muss eine Beschriftung vorhanden sein, und die [**Visible-Eigenschaft**](visible-property.md) muss auf **True** festgelegt sein. Darüber hinaus muss die **Visible-Eigenschaft** des Commands-Auflistungsobjekts auch auf **True** festgelegt werden. Um im Befehlsfenster angezeigt zu werden, muss für einen [**Befehl**](/windows/desktop/lwef/the-command-object) die Eigenschaften [**Caption**](caption-property.md) und [**Voice**](voice-property.md) festgelegt sein. Beachten Sie, dass sich die Popupmenüeinträge eines Zeichens nicht ändern, während das Menü angezeigt wird. Wenn Sie Befehle hinzufügen oder entfernen oder deren Eigenschaften ändern, während das Popupmenü des Zeichens angezeigt wird, werden diese Änderungen im Menü immer dann angezeigt, wenn sie vom Benutzer als Nächstes angezeigt werden. Das Befehlsfenster spiegelt jedoch alle Änderungen, die Sie vornehmen, dynamisch wider.

In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften eines [**Befehls**](/windows/desktop/lwef/the-command-object) auf seine Darstellung auswirken:



Caption-Eigenschaft

Voice-Caption-Eigenschaft

Voice-Eigenschaft

Visible-Eigenschaft

Enabled-Eigenschaft

Wird im Popupmenü des Zeichens angezeigt.

Wird im Befehlsfenster angezeigt.

Ja

Ja

Ja

True

True

Normal, [ **beschriftungsbeschriftung**](caption-property.md)

Ja, mit [ **VoiceCaption**](voicecaption-property.md)

Ja

Ja

Ja

True

Falsch

Deaktiviert, mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Ja

Ja

False

True

Wird nicht angezeigt

Ja, mit [ **VoiceCaption**](voicecaption-property.md)

Ja

Ja

Ja

False

False

Wird nicht angezeigt

Nein

Ja

Ja

Nein 

True

True

Normal, [ **beschriftungsbeschriftung**](caption-property.md)

Nein

Ja

Ja

Nein 

True

Falsch

Deaktiviert, mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Ja

Nein 

False

True

Wird nicht angezeigt

Nein

Ja

Ja

Nein 

Falsch

False

Wird nicht angezeigt

Nein

Nein 

Ja

Ja

True

True

Wird nicht angezeigt

Ja, mit [ **VoiceCaption**](voicecaption-property.md)

Nein 

Ja

Ja

True

Falsch

Wird nicht angezeigt

Nein

Nein 

Ja

Ja

False

True

Wird nicht angezeigt

Ja, mit [ **VoiceCaption**](voicecaption-property.md)

Nein 

Ja

Ja

False

False

Wird nicht angezeigt

Nein

Nein 

Ja

Nein 

True

True

Wird nicht angezeigt

Nein

Nein 

Ja

Nein 

True

Falsch

Wird nicht angezeigt

Nein

Nein 

Ja

Nein 

False

True

Wird nicht angezeigt

Nein

Nein 

Ja

Nein 

Falsch

False

Wird nicht angezeigt

Nein

Ja

Nein 

Ja

True

True

Normal, verwenden von [ **Caption**](caption-property.md)

Ja, verwenden von [ **Caption**](caption-property.md)

Ja

Nein 

Ja

True

Falsch

Deaktiviert mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Nein 

Ja

False

True

Wird nicht angezeigt

Ja, verwenden von [ **Caption**](caption-property.md)

Ja

Nein 

Ja

False

False

Wird nicht angezeigt

Nein

Ja

Nein 

Nein 

True

True

Normal, verwenden von [ **Caption**](caption-property.md)

Nein

Ja

Nein 

Nein 

True

Falsch

Deaktiviert mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Nein 

Nein 

False

True

Wird nicht angezeigt

Nein

Ja

Nein 

Nein 

Falsch

False

Wird nicht angezeigt

Nein

Nein 

Nein 

Ja

True

True

Wird nicht angezeigt

Nein 

Nein 

Nein 

Ja

True

Falsch

Wird nicht angezeigt

Nein

Nein 

Nein 

Ja

False

True

Wird nicht angezeigt

Nein 

Nein 

Nein 

Ja

False

False

Wird nicht angezeigt

Nein

Nein 

Nein 

Nein 

True

True

Wird nicht angezeigt

Nein

Nein 

Nein 

Nein 

True

Falsch

Wird nicht angezeigt

Nein

Nein 

Nein 

Nein 

False

True

Wird nicht angezeigt

Nein

Nein 

Nein 

Nein 

Falsch

False

Wird nicht angezeigt

Nein

 Wenn die Eigenschafteneinstellung NULL ist. In einigen Programmiersprachen wird eine leere Zeichenfolge möglicherweise nicht als NULL-Zeichenfolge interpretiert.  Auf den Befehl kann weiterhin über die Stimme zugegriffen werden.<br/>



 

Wenn der Server Eingaben für einen Ihrer Befehle empfängt, sendet er ein [**Command-Ereignis**](/windows/desktop/lwef/the-command-object) und übergibt den Namen des **Befehls** als Attribut des [**UserInput-Objekts**](/windows/desktop/lwef/iagentuserinput) zurück. Sie können dann bedingte Anweisungen verwenden, um den **Befehl** abzugleichen und zu verarbeiten.

 

