---
description: Ermöglicht dem Autor das Initiieren einer Neuinstallation einiger oder aller Features, während das aktuelle Dialogfeld ausgeführt wird.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: ControlEvent neu installieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350207"
---
# <a name="reinstall-controlevent"></a>ControlEvent neu installieren

Mit der installieren Sie controleventkann der Autor eine Neuinstallation einiger oder aller Features initiieren, während das aktuelle Dialogfeld ausgeführt wird.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden und erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, die entweder der Name der Funktion oder "All" ist.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Dieses Ereignis ist an ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld gebunden. Das gleiche [PUSHBUTTON](pushbutton-control.md) -Steuerelement sollte auch an eine [REINSTALLMODE](reinstallmode-controlevent.md) -ControlEvent gebunden werden.

 

 



