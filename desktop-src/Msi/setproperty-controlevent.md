---
description: 'Die Syntax für das SetProperty-Ereignis unterscheidet sich von anderen ControlEvents anstelle des Namens des Ereignisses, wobei die Eigenschaft in eckige Klammern gesetzt wird: \[ Eigenschafts \_ Name \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373159"
---
# <a name="setproperty-controlevent"></a>SetProperty-ControlEvent

Die Syntax für das SetProperty-Ereignis unterscheidet sich von anderen ControlEvents anstelle des Namens des Ereignisses, wobei die Eigenschaft in eckige Klammern gesetzt wird: \[ Eigenschafts \_ Name \] . Das-Argument ist der neue Wert der-Eigenschaft. Zum Deaktivieren der-Eigenschaft muss das-Argument lauten {} . Dies ist erforderlich, da das-Argument ein Primärschlüssel in der Tabelle ist und daher nicht NULL sein kann. Das-Argument wird mit der formattext-Methode formatiert, daher kann das-Argument jeden beliebigen Ausdruck enthalten, der von der formattext-Methode behandelt werden kann. Die Eigenschaftswerte werden zum Zeitpunkt des ControlEvent ausgewertet.

Dieses Ereignis kann durch ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element, ein [CheckBox-Steuer](checkbox-control.md)Element oder ein [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der neue Wert der Eigenschaft. {} für NULL.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld, das mit diesem Ereignis verknüpft ist, sodass eine Eigenschaft geändert wird, wenn die Schaltfläche gedrückt wird.

 

 



