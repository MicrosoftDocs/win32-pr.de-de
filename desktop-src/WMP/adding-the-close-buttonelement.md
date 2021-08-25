---
title: Hinzufügen des Schaltflächenelements "Schließen"
description: Hinzufügen des Schaltflächenelements "Schließen"
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Erstellen von Skins, BUTTONELEMENT-Element
- Windows Media Player Skins, BUTTONELEMENT-Element
- skins,BUTTONELEMENT-Element
- Skindefinitionsdateien, BUTTONELEMENT-Element
- BUTTONELEMENT-Element
- elements,BUTTONELEMENT
- Erstellen von Skins, Schaltflächen schließen
- Windows Media Player Skins, Schaltflächen schließen
- Skins, Schaltflächen schließen
- Skindefinitionsdateien, Schaltflächen schließen
- Schaltflächen schließen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5d2a85e43ae4a664504c213d182b396707ff9cfa663187e7f153fa4cc154e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765475"
---
# <a name="adding-the-close-buttonelement"></a>Hinzufügen des Schaltflächenelements "Schließen"

Die Schaltfläche Schließen ähnelt dem Konzept der Wiedergabeschaltfläche, weist jedoch unterschiedliche Codes und Farben auf.

Setzen Sie den Code **Buttonelement** schließen nach der schließenden spitzen Klammer von **Play BUTTONELEMENT**.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Die folgenden Attribute werden verwendet, um **buttonelement** für die Schaltfläche Schließen zu definieren:

**mappingColor**

Dies ist der Farbwert des Bereichs in der Zuordnungsartdatei, die Sie zuvor erstellt haben. In diesem Fall handelt es sich um die rote Volltonfarbe. Dieses Attribut ist für jedes **BUTTONELEMENT** erforderlich. Indem Sie diese Farbe definieren, teilen Sie Windows Media Player mit, diesen Farbbereich dem XML-Code dieser Schaltfläche zuzuordnen.

**upToolTip**

Dadurch wird der Text definiert, der angezeigt wird, wenn der Benutzer mit der Maus auf die Schaltfläche zeigt. Dies entspricht der Wiedergabeschaltfläche, mit der Ausnahme, dass sie mit "Schließen" bezeichnet wird.

**Onclick**

Dadurch wird das Ereignis definiert, das auftritt, wenn mit der Maustaste auf die Schaltfläche geklickt wird. Der Wert dieses Ereignisattributs wird als Ereignishandler bezeichnet und ist entweder eine Zeile von Microsoft JScript Code oder eine JScript Funktion in einer externen Textdatei, die vom **loadScript-Attribut** einer **VIEW** geladen wird. In diesem Fall ruft der JScript Code die **close-Methode** des **VIEW-Elements** mithilfe der globalen **Attributansicht** auf, die die Ansicht schließt und Windows Media Player herunterfährt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skindefinitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




