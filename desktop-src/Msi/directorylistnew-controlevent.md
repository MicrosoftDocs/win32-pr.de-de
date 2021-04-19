---
description: Dieses Ereignis benachrichtigt das directorylist-Steuerelement, dass ein neuer Ordner erstellt werden muss. Er erstellt den neuen Ordner und wählt das Namensfeld des Ordners für die Bearbeitung aus.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: Director-listnew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366338"
---
# <a name="directorylistnew-controlevent"></a>Director-listnew ControlEvent

Dieses Ereignis benachrichtigt das [directorylist-Steuer](directorylist-control.md) Element, dass ein neuer Ordner erstellt werden muss. Er erstellt den neuen Ordner und wählt das Namensfeld des Ordners für die Bearbeitung aus. Der Standardname des neuen Ordners kann in der [UIText-Tabelle](uitext-table.md)erstellt werden. Geben Sie "NewFolder" in die Schlüssel Spalte ein. Geben Sie den Wert für den Standardnamen des neuen Ordners in die Text Spalte ein. Dieser Wert muss in Form eines Datentyps der [Dateiname](filename.md) -Spalte vorliegen und die SFN- \| LFN-Syntax verwenden. Wenn dieser Wert in der UIText-Tabelle nicht vorhanden ist oder ein ungültiger Wert ist, verwendet das Installationsprogramm den Standardwert "fldr \| New Folder". Weitere Informationen finden Sie unter [Dialog Feld "Durchsuchen](browse-dialog.md)".

Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert. Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Beachten Sie Folgendes: Wenn dieses ControlEvent erneut aufgerufen wird, wenn ein neuer Ordner bereits vorhanden ist, wird kein zweiter neuer Ordner erstellt. In diesem Fall wählt der Aufruf von directorylistnew den Namen des vorhandenen neuen Ordners für die Bearbeitung aus.

## <a name="published-by"></a>Veröffentlicht von

[Directoren auflisten](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie das directorylist-Objekt wird verwendet, um die Erstellung eines neuen Ordners zu initiieren.

 

 



