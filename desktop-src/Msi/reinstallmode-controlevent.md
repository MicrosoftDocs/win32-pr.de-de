---
description: Ermöglicht es dem Autor, den Validierungs Modus oder die Modi während einer erneuten Installation anzugeben, während das aktuelle Dialogfeld ausgeführt wird.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: REINSTALLMODE-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349843"
---
# <a name="reinstallmode-controlevent"></a>REINSTALLMODE-ControlEvent

Der REINSTALLMODE-controleventermöglicht es dem Autor, den Validierungs Modus oder die Modi während einer erneuten Installation anzugeben, während das aktuelle Dialogfeld ausgeführt wird.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden und erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge. Eine Liste möglicher Werte finden Sie unter [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Dieses Ereignis ist an ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld gebunden. Das gleiche [PUSHBUTTON](pushbutton-control.md) -Steuerelement sollte auch an eine [neuinstallationscontrolevent](reinstall-controlevent.md) gebunden werden.

 

 



