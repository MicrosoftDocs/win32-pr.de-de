---
description: Dieses Ereignis benachrichtigt das DirectoryList-Steuerelement, dass ein neuer Ordner erstellt werden muss. er erstellt den neuen Ordner und wählt das Namensfeld des Ordners zur Bearbeitung aus.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281835954c947e4bcaaf6e4e2019cbd422151e6cca39b83fa84a0abe0db010cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378900"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent

Dieses Ereignis benachrichtigt das [DirectoryList-Steuerelement,](directorylist-control.md) dass ein neuer Ordner erstellt werden muss. er erstellt den neuen Ordner und wählt das Namensfeld des Ordners zur Bearbeitung aus. Der Standardname des neuen Ordners kann in der [UIText-Tabelle](uitext-table.md)erstellt werden. Geben Sie "NewFolder" in die Spalte Schlüssel ein. Geben Sie den Wert für den Standardnamen des neuen Ordners in die Spalte Text ein. Dieser Wert muss in Form eines [Filename-Spaltendatentyps](filename.md) sein und die \| SFN-LFN-Syntax verwenden. Wenn dieser Wert in der UIText-Tabelle nicht vorhanden ist oder ein ungültiger Wert ist, verwendet das Installationsprogramm den Standardwert "Fldr \| New Folder". Weitere Informationen finden Sie unter [Dialogfeld "Durchsuchen".](browse-dialog.md)

Dieses Ereignis sollte von einem [PushButton-Steuerelement](pushbutton-control.md) veröffentlicht werden, das sich im selben Dialogfeld wie das Steuerelement befindet, das dieses Ereignis abonniert. Das Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

Beachten Sie, dass kein zweiter neuer Ordner erstellt wird, wenn dieses ControlEvent erneut aufgerufen wird, wenn bereits ein neuer Ordner vorhanden ist. In diesem Fall wählt der Aufruf von DirectoryListNew den Namen des vorhandenen neuen Ordners zur Bearbeitung aus.

## <a name="published-by"></a>Veröffentlicht von

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) im gleichen modalen Dialogfeld wie DirectoryList wird verwendet, um die Erstellung eines neuen Ordners auszulösen.

 

 



