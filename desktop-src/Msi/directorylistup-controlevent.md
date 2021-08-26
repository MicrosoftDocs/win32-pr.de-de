---
description: Dieses Ereignis benachrichtigt das DirectoryList-Steuerelement, dass der Benutzer das übergeordnete Element des aktuellen Verzeichnisses auswählen möchte. Weitere Informationen finden Sie unter Dialogfeld "Durchsuchen".
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99fb0731a06f30cf788e3565e0988bf5b20ebce7abec8be351f4d1fe9d2aab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086180"
---
# <a name="directorylistup-controlevent"></a>DirectoryListUp ControlEvent

Dieses Ereignis benachrichtigt das [DirectoryList-Steuerelement,](directorylist-control.md) dass der Benutzer das übergeordnete Element des aktuellen Verzeichnisses auswählen möchte. Weitere Informationen finden Sie unter [Dialogfeld "Durchsuchen".](browse-dialog.md)

Dieses Ereignis sollte von einem [PushButton-Steuerelement](pushbutton-control.md) veröffentlicht werden, das sich im gleichen Dialogfeld wie das Steuerelement befindet, das dieses Ereignis akribiert. Das Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

Wenn das aktuelle Verzeichnis das Stammverzeichnis des Laufwerks ist, deaktiviert ein DirectoryListUp-Ereignis alle anderen Steuerelemente, die ein DirectoryListUp-Ereignis veröffentlichen.

## <a name="published-by"></a>Veröffentlicht von

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in demselben modalen Dialogfeld wie directoryList wird verwendet, um das Hochsens im Pfad auszulösen.

 

 



