---
description: Dieses Ereignis wählt ein Verzeichnis im DirectoryList-Steuerelement aus, das der Benutzer geöffnet hat, und hebt dieses hervor. Weitere Informationen finden Sie unter Dialogfeld "Durchsuchen".
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1453ffd42e0763ec747f02f7030818eaba3d533e5dfcca4570c13596efdcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947324"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent

Dieses Ereignis wählt ein Verzeichnis im [DirectoryList-Steuerelement](directorylist-control.md) aus, das der Benutzer geöffnet hat, und hebt dieses hervor. Weitere Informationen finden Sie unter [Dialogfeld "Durchsuchen".](browse-dialog.md)

Dieses Ereignis sollte von einem [PushButton-Steuerelement](pushbutton-control.md) veröffentlicht werden, das sich im selben Dialogfeld wie das Steuerelement befindet, das dieses Ereignis abonniert. Das Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

Wenn im [DirectoryList-Steuerelement](directorylist-control.md)kein Verzeichnis ausgewählt wurde, deaktiviert ein DirectoryListOpen-Ereignis alle anderen Steuerelemente, die ein DirectoryListOpen-Ereignis veröffentlichen.

## <a name="published-by"></a>Veröffentlicht von

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) im gleichen modalen Dialogfeld wie directoryList wird verwendet, um das schrittweise Herunterfahren im Pfad auszulösen.

 

 



