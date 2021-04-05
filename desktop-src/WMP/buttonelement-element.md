---
title: ButtonElement-Element
description: ButtonElement-Element
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- Windows Media Player Skins, ButtonElement-Element
- Skins, ButtonElement-Element
- ButtonElement-Element
- Verweis für Skins, ButtonElement-Element
- Elemente, ButtonElement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711927"
---
# <a name="buttonelement-element"></a>ButtonElement-Element

Das **ButtonElement** -Element definiert eine einzelne Schaltfläche innerhalb eines übergeordneten **ButtonGroup** -Elements. Es unterstützt die folgenden Attribute. Vordefinierte **ButtonElement** -Elemente werden zur einfacheren Bereitstellung bereitgestellt.

Das **ButtonElement** -Element unterstützt die folgenden Attribute.



| Attribut                                      | BESCHREIBUNG                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](buttonelement-cursor.md)             | Gibt den Wert des **ButtonElement** -Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über dem **Button-Element** befindet.                                                                                      |
| [auf](buttonelement-down.md)                 | Gibt den up-oder Down-Wert des **buttonelements** an oder ruft ihn ab.                                                                                                                                            |
| [downtooltip](buttonelement-downtooltip.md)   | Gibt den QuickInfo-Text an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über dem **Button-Element** befindet und sich das **Button Element** im Zustand "gedrückt" befindet.                                                                |
| [Index](buttonelement-index.md)               | Ruft den Index des **ButtonElement** innerhalb der **ButtonGroup** ab.                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | Gibt den Farbschlüssel an, der dieses **ButtonElement** in der **ButtonElement** -Gruppe identifiziert, oder ruft ihn ab.                                                                                                      |
| [Klebe](buttonelement-sticky.md)             | Gibt einen Wert an, der angibt, ob das **ButtonElement** kurz ist, oder ruft diesen Wert ab. Wenn die Kurznotiz festgehalten wird, ändert sich der Status eines **ButtonElement** , nachdem es geklickt wurde |
| [uptooltip](buttonelement-uptooltip.md)       | Gibt den QuickInfo-Text an, der angezeigt wird, wenn sich der Mauszeiger über dem **Button-Element** befindet und sich das **ButtonElement** im Zustand "aktiv" oder "aktiv" befindet.                                                        |



 

Das **ButtonElement** -Element unterstützt die folgende Methode.



| Methode                           | BESCHREIBUNG                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [Sie](buttonelement-click.md) | Ruft den **OnClick** -Ereignishandler auf, der für das **ButtonElement** definiert ist. |



 

Das **ButtonElement** -Element kann die Umgebungs Ereignishandler implementieren. Weitere Informationen finden Sie unter [Ambient-Ereignishandler](ambient-event-handlers.md).

Das **ButtonElement** -Element unterstützt die folgenden Ambient-Attribute: " [aktiviert](ambientattributes-enabled.md) " und " [Tabstopps](ambientattributes-tabstop.md)".

Vordefinierte Effekte sind normale **Effekte** Elemente mit verschiedenen allgemeinen Attribut Einstellungen, die standardmäßig angegeben werden. Die folgenden vordefinierten **ButtonElement** -Elemente sind verfügbar.



| Vordefiniertes ButtonElement         | BESCHREIBUNG                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Ffwdelta-Element](ffwdelement.md)   | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. FastForward** aufruft. |
| [Nextelements](nextelement.md)   | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. Next** aufruft.        |
| [Pauenelement](pauseelement.md) | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. Pause** aufruft.       |
| [Playelement](playerelement.md) | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. Play** aufruft.        |
| [Prevelements](prevelement.md)   | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. Previous** aufruft.    |
| [Rewelements](rewelement.md)     | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. Rewind** aufruft.      |
| [Stop Element](stopelement.md)   | Ein **ButtonElement** mit einem integrierten **OnClick** -Ereignishandler, der **Player. Controls. Pause** aufruft.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




