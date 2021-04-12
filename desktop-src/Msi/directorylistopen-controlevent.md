---
description: Mit diesem Ereignis wird ein Verzeichnis im directerylist-Steuerelement ausgewählt und hervorgehoben, das vom Benutzer geöffnet werden soll. Weitere Informationen finden Sie unter Dialog Feld "Durchsuchen".
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: Director-listopen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218850"
---
# <a name="directorylistopen-controlevent"></a>Director-listopen ControlEvent

Mit diesem Ereignis wird ein Verzeichnis im [directerylist-Steuer](directorylist-control.md) Element ausgewählt und hervorgehoben, das vom Benutzer geöffnet werden soll. Weitere Informationen finden Sie unter [Dialog Feld "Durchsuchen](browse-dialog.md)".

Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert. Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Wenn kein Verzeichnis im [Director List-Steuer](directorylist-control.md)Element ausgewählt wurde, deaktiviert ein Ereignis vom Datentyp directoriylistopen alle anderen Steuerelemente, die ein directoriylistopen-Ereignis veröffentlichen.

## <a name="published-by"></a>Veröffentlicht von

[Directoren auflisten](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie Director List wird verwendet, um die Schritt Ausführung im Pfad zu initiieren.

 

 



