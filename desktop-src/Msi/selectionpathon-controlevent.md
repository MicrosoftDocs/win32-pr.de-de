---
description: Das SelectionTree-Steuerelement verwendet das SelectionPathOn-Ereignis, um einen booleschen Wert zu veröffentlichen, der angibt, ob dem aktuell ausgewählten Feature ein Auswahlpfad zugeordnet ist. Dieses Ereignis sollte in der EventMapping-Tabelle verfasst werden.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea32926117c200f466bd2c40ac611e7ccbc47fb6a231a5dcf93ffa2ee0446b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040430"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent

Das [SelectionTree-Steuerelement](selectiontree-control.md) verwendet das SelectionPathOn-Ereignis, um einen booleschen Wert zu veröffentlichen, der angibt, ob dem aktuell ausgewählten Feature ein Auswahlpfad zugeordnet ist. Dieses Ereignis sollte in der [EventMapping-Tabelle verfasst werden.](eventmapping-table.md)

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

Das SelectionPathOn ControlEvent wird nie während einer [Wartungsinstallation veröffentlicht.](maintenance-installation.md)

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text-Steuerelement](text-control.md) im gleichen modalen Dialogfeld wie selectionTree sollte das Ereignis über die [EventMapping-Tabelle abonnieren.](eventmapping-table.md) Das Textsteuerfeld zeigt die Beschriftung des Auswahlpfads an. Dieses Textsteuerfeld ist je nach Ereignis sichtbar oder ausgeblendet.

 

 



