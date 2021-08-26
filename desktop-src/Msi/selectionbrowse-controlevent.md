---
description: Das SelectionTree-Steuerelement verwendet das SelectionBrowse-Ereignis, um ein Dialogfeld Durchsuchen zu erstellen, sodass der Pfad des hervorgehobenen Elements geändert werden kann.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70d7c50e69921a5fefe7cff3c88c2351cacdecda42a164e8334c9afb3977bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040610"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent

Das [SelectionTree-Steuerelement](selectiontree-control.md) verwendet das SelectionBrowse-Ereignis, um ein Dialogfeld **Durchsuchen** zu erstellen, sodass der Pfad des hervorgehobenen Elements geändert werden kann.

Dieses Ereignis sollte von einem [PushButton-Steuerelement](pushbutton-control.md) veröffentlicht werden, das sich im selben Dialogfeld wie das Steuerelement befindet, das dieses Ereignis abonniert. Das Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

Alle Steuerelemente, die ein SelectionBrowse-Ereignis veröffentlichen, werden deaktiviert, wenn ein Feature ausgewählt wurde, das bereits installiert, nicht konfigurierbar oder nicht für die lokale Installation ausgewählt wurde. Um konfigurierbar zu sein, muss das Feature über eine [öffentliche Eigenschaft](public-properties.md) verfügen, die in das \_ Verzeichnisfeld der [Featuretabelle](feature-table.md)eingegeben wird.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Der Name des zu erstellenden Dialogfelds.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) im gleichen modalen Dialogfeld wie SelectionTree verwendet dieses Ereignis, um das Dialogfeld **Durchsuchen** auszulösen.

 

 



