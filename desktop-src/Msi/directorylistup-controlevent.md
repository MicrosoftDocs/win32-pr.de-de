---
description: Dieses Ereignis benachrichtigt das Director List-Steuerelement, dass der Benutzer das übergeordnete Element des aktuellen Verzeichnisses auswählen möchte. Weitere Informationen finden Sie unter Dialog Feld "Durchsuchen".
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: Director-listup-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961005"
---
# <a name="directorylistup-controlevent"></a>Director-listup-ControlEvent

Dieses Ereignis benachrichtigt das [Director List-Steuer](directorylist-control.md) Element, dass der Benutzer das übergeordnete Element des aktuellen Verzeichnisses auswählen möchte. Weitere Informationen finden Sie unter [Dialog Feld "Durchsuchen](browse-dialog.md)".

Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert. Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Handelt es sich bei dem aktuellen Verzeichnis um das Stammverzeichnis des Laufwerks, werden alle anderen Steuerelemente, die ein Director-listup-Ereignis veröffentlichen, von einem directoriylistup-Ereignis deaktiviert.

## <a name="published-by"></a>Veröffentlicht von

[Directoren auflisten](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie Director List wird verwendet, um eine Schritt-für-Schritt-Ausführung des Pfads zu aktivieren.

 

 



