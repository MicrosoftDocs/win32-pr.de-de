---
title: Hinzufügen des schließenden ButtonElement
description: Hinzufügen des schließenden ButtonElement
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Erstellen von Skins, ButtonElement-Element
- Windows Media Player Skins, ButtonElement-Element
- Skins, ButtonElement-Element
- Skin-Definitions Dateien, ButtonElement-Element
- ButtonElement-Element
- Elemente, ButtonElement
- Erstellen von Skins, schließen von Schaltflächen
- Windows Media Player Skins, schließen von Schaltflächen
- Skins, Schaltflächen Schließen
- Skin-Definitions Dateien, schließen-Schaltflächen
- Schließen von Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206854"
---
# <a name="adding-the-close-buttonelement"></a>Hinzufügen des schließenden ButtonElement

Die Schaltfläche Schließen ähnelt dem Konzept der Wiedergabe Schaltfläche, verfügt aber über unterschiedliche Codes und Farben.

Fügen Sie den schließenden **ButtonElement** -Code nach der schließenden Spitze Klammer des Wiedergabe- **buttonelements** ein.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Die folgenden Attribute werden verwendet, um das **ButtonElement** für die Schaltfläche "Schließen" zu definieren:

**mappingColor**

Dies ist der Farbwert des Bereichs in der Mappings-Grafikdatei, den Sie zuvor erstellt haben. In diesem Fall ist es die rote Farbe. Dieses Attribut ist für ein beliebiges **ButtonElement** erforderlich. Wenn Sie diese Farbe definieren, sagen Sie Windows Media Player, diesen Farbbereich dem XML-Code dieser Schaltfläche zuzuordnen.

**uptooltip**

Dadurch wird der Text definiert, der angezeigt wird, wenn der Benutzer mit dem Mauszeiger auf die Schaltfläche bewegt wird. Dies ist identisch mit der Wiedergabe Schaltfläche, mit der Ausnahme, dass Sie mit "Close" gekennzeichnet ist.

**OnClick**

Definiert das Ereignis, das auftritt, wenn mit der Maus auf die Schaltfläche geklickt wird. Der Wert dieses Ereignis Attributs wird als Ereignishandler bezeichnet und ist entweder eine Zeile von Microsoft JScript-Code oder eine JScript-Funktion in einer externen Textdatei, die vom **loadscript** -Attribut einer **Ansicht** geladen wird. In diesem Fall ruft der JScript-Code die **Close** -Methode des **Ansichts** Elements mithilfe der globalen Attribut **Ansicht** auf, die die Ansicht schließt und Windows-Media Player herunterfährt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skin-Definitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




