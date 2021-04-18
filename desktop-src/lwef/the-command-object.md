---
title: Das Command-Objekt
description: Das Command-Objekt
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340263"
---
# <a name="the-command-object"></a>Das Command-Objekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt ist ein Element in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung. Der Server stellt dem Benutzer Zugriff auf die **Befehls** Objekte zur Verfügung, wenn die Client Anwendung aktiv wird.

-   [Befehls Objekteigenschaften](command-object-properties.md)

Wenn Sie auf die-Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zugreifen möchten, verweisen Sie in der zugehörigen Auflistung mit der Eigenschaft " [**Name**](name-property.md) " darauf. In VBScript und Visual Basic können Sie die **Name** -Eigenschaft direkt verwenden:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Verwenden Sie für Programmiersprachen, die keine Auflistungen unterstützen, die [**Befehls**](command-method.md) Methode:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Sie können auch auf ein Befehls Objekt verweisen, indem Sie einen Verweis darauf erstellen. Deklarieren Sie in Visual Basic eine Objekt Variable, und verwenden Sie die Set-Anweisung, um den Verweis zu erstellen:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In Visual Basic 5,0 können Sie das Objekt auch als Typ [**iagentctlcommandex**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) deklarieren und den Verweis erstellen. Diese Konvention ermöglicht eine frühe Bindung, was zu einer besseren Leistung führt:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In VBScript können Sie einen Verweis als einen bestimmten Typ deklarieren, aber Sie können die Variable trotzdem deklarieren und Sie auf den [**Befehl**](/windows/desktop/lwef/the-command-object) in der Sammlung festlegen:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Ein Befehl kann entweder im Popup-Menü des Zeichens und im Fenster "Befehle" oder in beiden angezeigt werden. Um im Popup Menü angezeigt zu werden, muss Sie über eine Beschriftung verfügen, und die [**Visible**](visible-property.md) -Eigenschaft muss auf **true** festgelegt sein. Außerdem muss die **sichtbare** Eigenschaft des Commands-Auflistungs Objekts auch auf **true** festgelegt werden. Um im Fenster Befehle angezeigt zu werden, muss für einen [**Befehl**](/windows/desktop/lwef/the-command-object) die [**Beschriftung**](caption-property.md) und die [**sprach**](voice-property.md) Eigenschaften festgelegt sein. Beachten Sie, dass sich die Popup Menüeinträge eines Zeichens nicht ändern, während das Menü angezeigt wird. Wenn Sie Befehle hinzufügen oder entfernen oder deren Eigenschaften ändern, während das Popup Menü des Zeichens angezeigt wird, werden diese Änderungen im Menü angezeigt, sobald der Benutzer das nächste Mal anzeigt. Das Fenster "Befehle" reflektiert jedoch dynamisch alle Änderungen, die Sie vornehmen.

In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften eines [**Befehls**](/windows/desktop/lwef/the-command-object) auf seine Darstellung auswirken:



Caption-Eigenschaft

Voice-Caption-Eigenschaft

Voice-Eigenschaft

Visible-Eigenschaft

Enabled-Eigenschaft

Wird im Popupmenü des Zeichens angezeigt.

Wird im Fenster "Befehle" angezeigt

Ja

Ja

Ja

True

True

Normal, mit [ **Beschriftung**](caption-property.md)

Ja, mit [ **voicecaption**](voicecaption-property.md)

Ja

Ja

Ja

Richtig

False

Deaktiviert mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Ja

Ja

False

True

Wird nicht angezeigt

Ja, mit [ **voicecaption**](voicecaption-property.md)

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

Normal, mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Ja

Nein 

Richtig

False

Deaktiviert mit [ **Beschriftung**](caption-property.md)

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

False

False

Wird nicht angezeigt

Nein

Nein 

Ja

Ja

True

True

Wird nicht angezeigt

Ja, mit [ **voicecaption**](voicecaption-property.md)

Nein 

Ja

Ja

Richtig

False

Wird nicht angezeigt

Nein

Nein 

Ja

Ja

False

True

Wird nicht angezeigt

Ja, mit [ **voicecaption**](voicecaption-property.md)

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

Richtig

False

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

False

False

Wird nicht angezeigt

Nein

Ja

Nein 

Ja

True

True

Normal, mit [ **Beschriftung**](caption-property.md)

Ja, mit [ **Beschriftung**](caption-property.md)

Ja

Nein 

Ja

Richtig

False

Deaktiviert mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Nein 

Ja

False

True

Wird nicht angezeigt

Ja, mit [ **Beschriftung**](caption-property.md)

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

Normal, mit [ **Beschriftung**](caption-property.md)

Nein

Ja

Nein 

Nein 

Richtig

False

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

False

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

Richtig

False

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

Richtig

False

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

False

False

Wird nicht angezeigt

Nein

 , Wenn die Eigenschafts Einstellung NULL ist. In manchen Programmiersprachen kann eine leere Zeichenfolge nicht wie eine NULL-Zeichenfolge interpretiert werden.  Der Befehl ist weiterhin sprach zugänglich.<br/>



 

Wenn der Server Eingaben für einen ihrer Befehle empfängt, sendet er ein [**Befehls**](/windows/desktop/lwef/the-command-object) Ereignis und übergibt den Namen des **Befehls** als Attribut des [**UserInput**](/windows/desktop/lwef/iagentuserinput) -Objekts zurück. Anschließend können Sie bedingte Anweisungen verwenden, um den **Befehl** abzugleichen und zu verarbeiten.

 

