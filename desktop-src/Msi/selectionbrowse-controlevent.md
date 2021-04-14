---
description: Das SelectionTree-Steuerelement verwendet das selectionbrowse-Ereignis, um ein Dialogfeld zum Durchsuchen zu erzeugen, sodass es möglich ist, den Pfad des hervorgehobenen Elements zu ändern.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: Selectionbrowse-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350228"
---
# <a name="selectionbrowse-controlevent"></a>Selectionbrowse-ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionbrowse-Ereignis, um ein Dialogfeld zum **Durchsuchen** zu erzeugen, sodass es möglich ist, den Pfad des hervorgehobenen Elements zu ändern.

Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert. Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Alle Steuerelemente, die ein selectionbrowse-Ereignis veröffentlichen, werden deaktiviert, wenn eine Funktion ausgewählt wurde, die bereits installiert, nicht konfigurierbar oder nicht für die lokale Installation ausgewählt ist. Damit die Funktion konfiguriert werden kann, muss Sie über eine [öffentliche Eigenschaft](public-properties.md) verfügen, die in das Feld "Verzeichnis" \_ der [Funktions Tabelle](feature-table.md)eingegeben wird.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Der Name des Dialog Felds, das erzeugt werden soll.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie die SelectionTree verwendet dieses Ereignis, um das Dialogfeld **Durchsuchen** zu initiieren.

 

 



